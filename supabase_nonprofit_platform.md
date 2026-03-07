# Supabase-Based Nonprofit Platform Architecture

## Overview

This document describes a modern, low-cost architecture for building a
nonprofit platform using **Supabase** as the backend.\
The goal is to provide core nonprofit capabilities --- donations,
memberships, events, and volunteer management --- without relying on
expensive monolithic CRM systems.

This architecture works particularly well for organizations building a
**custom website frontend** using modern JavaScript frameworks.

It is most effective when the team explicitly owns data governance,
integration reliability, and ongoing operational support.

---

# Core Concept

Instead of using a traditional nonprofit CRM, the website becomes the
**primary platform**, and Supabase provides:

- Database (PostgreSQL)
- Authentication
- API layer
- Serverless functions
- Realtime capabilities

Payments and subscriptions are handled by **Stripe**, while the frontend
is built using **Next.js** and optionally **Payload CMS** for content
management.

---

# High-Level Architecture

    Frontend
    --------
    Next.js
    Payload CMS

    Backend Platform
    ----------------
    Supabase
    (Postgres + Auth + APIs)

    Payments
    --------
    Stripe

    Optional Services
    -----------------
    Email: Mailchimp / Resend
    Analytics: Plausible
    File Storage: Supabase Storage

---

# Source of Truth and Data Ownership

Define one authoritative system per record type before building
integrations.

| Domain                         | System of record                                             | Notes                                                                                    |
| ------------------------------ | ------------------------------------------------------------ | ---------------------------------------------------------------------------------------- |
| Donations and payment status   | Stripe + Supabase donations table                            | Stripe is canonical for payment outcomes; Supabase mirrors for reporting and operations. |
| Donor profile and segmentation | Supabase (donors)                                            | Keep one canonical donor ID across all tools.                                            |
| Membership status              | Stripe subscriptions + Supabase memberships                  | Stripe for billing state, Supabase for app access and member workflows.                  |
| Event registrations            | Supabase events/event_registrations (or external event tool) | If using an external event tool, sync back to Supabase daily.                            |
| Volunteer shifts/hours         | Supabase volunteers/volunteer_shifts                         | Required for reliable volunteer reporting and scheduling.                                |
| Email engagement               | Email platform                                               | Sync campaign outcomes to Supabase for aggregate analytics.                              |

Core governance rules:

- Use immutable external IDs (`stripe_customer_id`, `stripe_subscription_id`).
- Document field-level ownership (which system can write each field).
- Define dedupe and merge policy for duplicate contacts.
- Track lifecycle states for donor/member/volunteer consistently.

---

# Core Nonprofit Features

## Donations

Handled using **Stripe Checkout** and Stripe webhooks.

Flow:

    User submits donation
    → Stripe Checkout
    → Stripe webhook fires
    → Supabase function records donation
    → Donation saved in database

Key tables:

- donors
- donations
- campaigns

---

## Memberships

Memberships are implemented using **Stripe subscriptions**.

Flow:

    User purchases membership
    → Stripe subscription created
    → Webhook updates membership record
    → Member dashboard access enabled

Key tables:

- memberships
- donors
- membership_types

---

## Events

Events can be managed directly within Supabase.

Features:

- Event listings
- Registration forms
- Attendee tracking
- Optional ticket payments

Key tables:

- events
- event_registrations

---

## Volunteers

Volunteer management is handled through signup forms and assignment
tracking.

Features:

- Volunteer profiles
- Skills and availability
- Shift assignments
- Event volunteer tracking

Key tables:

- volunteers
- volunteer_shifts

---

# Integration Reliability (Required)

Minimum production patterns:

- Verify webhook signatures (Stripe and any third-party source).
- Use idempotency keys to prevent duplicate inserts.
- Add retry with exponential backoff for transient failures.
- Store failed events in a retry queue/dead-letter table.
- Run reconciliation jobs (daily) across Stripe and Supabase totals.

Suggested operational checks:

- Daily: donation and subscription reconciliation summary.
- Weekly: failed webhook/events review and retry sweep.
- Monthly: duplicate donor audit and mapping fixes.

---

# Example Database Schema

## donors

    id
    name
    email
    phone
    created_at
    lifetime_donations

## donations

    id
    donor_id
    amount
    stripe_payment_id
    campaign_id
    created_at

## memberships

    id
    donor_id
    membership_type
    status
    stripe_subscription_id
    expires_at

## events

    id
    title
    date
    location
    capacity
    description

## event_registrations

    id
    event_id
    donor_id
    ticket_type
    created_at

## volunteers

    id
    name
    email
    skills
    availability

## volunteer_shifts

    id
    event_id
    volunteer_id
    role
    hours

---

# Authentication

Supabase provides built-in authentication for:

- donor accounts
- volunteer accounts
- member dashboards
- admin access

This allows the site to provide:

- donor history pages
- member portals
- volunteer schedules

without building a custom auth system.

---

# Authorization and RLS Policy Model

Supabase Row Level Security (RLS) should be enabled for all sensitive
tables.

Recommended roles:

- `admin`: full data and configuration access
- `staff`: operational CRUD for donor/event/volunteer workflows
- `member`: own membership and profile records
- `volunteer`: own profile, assigned shifts, and availability
- `donor`: own donation history and receipts

RLS examples to enforce:

- Donors can view only their own donations (`donor_id = auth.uid()` mapping).
- Volunteers can view/edit only their own profile and assigned shifts.
- Staff/admin roles can view organization-level operational data.
- Public role can only access explicitly published event/content views.

---

# Estimated Monthly Cost

| Service     | Estimated Cost        |
| ----------- | --------------------- |
| Supabase    | Free -- $25           |
| Stripe      | Transaction fees only |
| Email tools | $0 -- $20             |
| Hosting     | $10 -- $20            |

Typical total cost:

**\$20--50 per month**

---

# Security and Compliance Baseline

- Keep payment card collection in Stripe-hosted flows to reduce PCI
  scope.
- Enforce MFA for admin/staff accounts.
- Use least-privilege service keys and rotate secrets regularly.
- Encrypt backups and define retention/deletion policy for PII.
- Keep audit logs for donation changes, membership status updates, and
  volunteer-hour edits.

---

# Development Time Estimate

    Component                             Estimated Time
    ------------------------------------- ----------------
    Database schema + migrations          8--16 hours
    Stripe donation flow + webhooks       12--20 hours
    Membership subscriptions + gating      8--16 hours
    Event management + registrations      10--20 hours
    Volunteer system + shift workflows     8--16 hours
    Admin dashboards + exports            12--24 hours
    Reliability, reconciliation, QA       16--32 hours

Total development time:

**\~74--144 hours** (2--5 weeks depending scope and polish)

Note: the lower estimate is for MVP quality; production readiness with
auditing, error handling, and strong admin UX trends toward the upper
range.

---

# Reporting and Analytics Strategy

Use Supabase/Postgres views as the reporting backbone.

Recommended baseline reports:

- Donation totals by campaign, source, and month
- Active memberships, churn, and renewal forecast
- Event registrations vs attendance
- Volunteer hours by event and program
- Donor retention cohorts and repeat-giving rate

Implementation options:

- Internal admin dashboards (Next.js + SQL views)
- Scheduled exports to Google Sheets/BI tools
- Lightweight product analytics via Plausible/PostHog

---

# Phased Implementation Plan

## Phase 1: MVP (Launch)

- Donations, donor records, and basic receipts
- Event listings and registration
- Basic volunteer signup/profile capture

## Phase 2: Hardening

- Webhook reliability, retries, and reconciliation
- Role-based access and strict RLS rollout
- Data quality checks and dedupe workflows

## Phase 3: Scale and Automation

- Membership automation and portal enhancements
- Volunteer scheduling and hour verification workflows
- Advanced reporting and lifecycle automation

---

# Advantages

- Very low operating cost
- Full control over frontend design
- Modern developer stack
- Easily extensible
- Avoids vendor lock-in

---

# Limitations

- Requires a developer to maintain
- Less built-in reporting than traditional CRMs
- Some nonprofit workflows may need custom development
- Integration ownership replaces vendor-managed simplicity

---

# Summary

Using Supabase as a nonprofit backend enables a **modern, composable
nonprofit platform** with:

- Donations
- Membership management
- Event registration
- Volunteer tracking

Combined with Next.js and Stripe, this architecture delivers a powerful
system at a fraction of the cost of traditional nonprofit CRMs.
