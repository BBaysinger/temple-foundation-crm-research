# CiviCRM + WordPress Setup Plan and Time Estimates

## Purpose

This document provides practical setup steps and estimated timelines for implementing CiviCRM with WordPress in two scopes:

1. Basic/initial feature launch (usable first production release)
2. Full required-feature rollout (all `✅` priority criteria from `evaluation-matrix.md`)

Optional-scope note:

- `Non-widget implementation path (API-first/headless)` is treated as a maybe add-on, not part of base required rollout.
- `Forkable source code for in-house feature development` is treated as a maybe add-on.

## Estimation Assumptions

- Team model: 1 technical implementer + 1 operations lead + part-time stakeholder reviewers
- Environment: WordPress hosting already available (or provisioned in Week 1)
- Data size: small-to-medium migration set (initial nonprofit stage)
- Integrations: Stripe/PayPal + email + accounting sync required
- Estimates include configuration, QA, training, and launch support
- Estimates are calendar-time ranges, not pure engineering hours

## AI/Codex-Assisted Adjustment

These baseline estimates are human-led delivery estimates. If the team uses AI/Codex heavily for implementation support, documentation generation, config drafting, and test/checklist creation, timelines can often improve.

Typical impact ranges:

- Configuration/documentation-heavy tasks: `20-35%` faster
- Repetitive mapping/report setup: `15-30%` faster
- Custom integration coding scaffolds: `10-25%` faster
- Stakeholder decisions, UAT, approvals, and training: usually unchanged

Practical adjusted ranges (same scope assumptions):

- Scope 1 (basic/initial features)
  - Baseline typical: `5-7 weeks`
  - AI/Codex-assisted typical: `4-6 weeks`
- Scope 2 (all required features)
  - Baseline additive: `+7 to +14 weeks` (excluding optional headless/forking add-ons)
  - AI/Codex-assisted additive: `+6 to +11 weeks` (excluding optional headless/forking add-ons)
- Total from scratch (Scope 1 + Scope 2)
  - Baseline typical: `12-21 weeks` (excluding optional headless/forking add-ons)
  - AI/Codex-assisted typical: `10-17 weeks` (excluding optional headless/forking add-ons)

Optional add-on impact (if selected):

- Headless/API-first path: `+3 to +6 weeks`
- Forking/extensibility approach: context-dependent (can reduce custom build time for some features)

Use caution with compressed timelines when business rules are still evolving. AI can accelerate execution, but it does not remove the need for stakeholder alignment and acceptance testing.

## Design Fidelity Add-On (Page Styling Depth)

The base estimates in this document assume practical, production-ready styling (brand alignment and usability), not full custom design-system implementation.

If your expectation includes stronger visual fidelity, add the following timeline ranges:

1. Basic brand alignment: `+3 to +6 days`

- Theme-level branding (colors, typography, logo treatment)
- Light form/page layout cleanup
- Basic responsive sanity checks

2. Medium fidelity implementation: `+2 to +4 weeks`

- Reusable template overrides for donation/event/member flows
- Structured style tokens and component-level consistency
- Expanded responsive QA and accessibility pass for key journeys

3. High fidelity implementation: `+4 to +8+ weeks`

- Design-system-level implementation across all public/portal surfaces
- Pixel-accurate parity to approved design comps
- Comprehensive cross-device/browser QA and accessibility remediation

Notes:

- These add-ons are cumulative relative to base scope assumptions.
- Timeline impact is usually highest when portal/constituent self-service UX is heavily customized.

## Scope 1: Basic/Initial Features Working

### Target outcome

A production-usable baseline that supports donor/contact management, online giving, events, and core communications with low operational friction.

### Recommended scope baseline

Aligned to `requirements.md` core items (`R-01` through `R-08` plus core access controls):

- Contact database and CSV import/export
- One-time + recurring donations
- Embeddable donation and event registration forms
- Event setup, RSVP/ticketing basics, confirmations/reminders
- Segmentation and basic email campaign sending
- Role-based access (admin/staff)
- Basic reports (donations, events, engagement)
- Website integration path (WordPress + CiviCRM forms/pages)

### Step-by-step plan (initial launch)

1. Foundation and architecture setup: 3-5 days

- Confirm WordPress hosting, backups, SSL, and domain strategy
- Install and harden WordPress + CiviCRM + required extensions
- Set environment conventions (config, staging, deployment workflow)

2. Data model and security baseline: 3-5 days

- Configure contact types, custom fields, tags, groups, relationships
- Define role permissions (admin vs staff)
- Configure dedupe rules and basic data hygiene policies

3. Donations and payment processing: 4-7 days

- Configure contribution pages/forms
- Set up Stripe/PayPal processors and test transactions
- Configure receipts and acknowledgment defaults
- Validate offline donation entry workflow

4. Event baseline workflows: 4-7 days

- Configure event templates, registration forms, capacity, confirmations
- Set up RSVP and attendance/check-in basics
- Publish WordPress-facing event entry points

5. Email and segmentation baseline: 3-5 days

- Configure mailing sender/authentication requirements
- Build initial segments and starter templates
- Run test campaign and opt-out/unsubscribe checks

6. Reporting and operational readiness: 3-4 days

- Build core saved reports/dashboards for donations/events/engagement
- Document SOPs for daily/weekly admin actions
- Conduct role-based UAT and fix critical defects

7. Launch and hypercare: 2-3 days

- Cutover checklist execution
- Post-launch monitoring and rapid fixes

### Time estimate for Scope 1

- Fast track: 3-4 weeks
- Typical: 5-7 weeks
- Conservative (with rework/training overhead): 8-9 weeks

### Effort estimate (person-weeks)

- Technical implementer: 4-7 person-weeks
- Operations/admin lead: 1.5-3 person-weeks
- Stakeholder/UAT participation: 0.5-1 person-week

## Scope 2: All Required Features from the Matrix

### Target outcome

Deliver all `✅` priority criteria in `evaluation-matrix.md` for CiviCRM, including advanced donor, volunteer, membership, integration, governance, and implementation-control capabilities.

### Includes everything in Scope 1 plus

- Constituent portal/profile-preference path
- Pledge workflows and fund allocation/revenue-category rigor
- Donor LTV and donor tier logic where applicable
- Planned giving/legacy tracking
- Deeper event automations and post-event workflows
- Volunteer coordination history and auto-populated participation patterns
- SMS capabilities and multichannel communication controls
- Accounting linkage + QuickBooks integration path
- API/webhook implementation pathways
- Backup/export resilience, audit/compliance logging, and sandbox/testing process

Optional add-ons (if selected):

- non-widget/headless implementation pathway
- fork/extension program setup for in-house feature development

### Step-by-step plan (full required rollout)

1. Gap mapping against required matrix rows: 3-5 days

- Enumerate every `✅` priority row and map to current state
- Mark each as native/configuration/extension/custom
- Define acceptance criteria per row

2. Advanced fundraising and finance model: 1-2 weeks

- Configure pledges, fund allocations, revenue categories, acknowledgments
- Build accounting sync design and reconciliation process
- Validate tax receipt/reporting outputs

3. Constituent portal and preference management: 1-2 weeks

- Implement profile/preference update path via WordPress + CiviCRM
- Add authentication, profile UX, and preference sync rules
- UAT for profile edit and consent/communication preference changes

4. Volunteer and membership depth: 2-4 weeks

- Configure volunteer forms, participation history, categorization, automations
- Build membership renewal/dues lifecycle and reminders
- Add quality controls for data consistency across volunteer/member records

5. Advanced automation and integration layer: 2-4 weeks

- Implement triggered/welcome sequences and post-event flows
- Build API/webhook orchestration for website-first workflows
- Add monitoring and retry patterns for integration reliability

6. Reporting, governance, and resilience controls: 1-2 weeks

- Audit/compliance log review process
- Backup/export restoration testing
- Sandbox/staging release process and regression checklist

7. Full UAT, training, and phased go-live: 1-2 weeks

- Run requirement-by-requirement UAT
- Deliver role-based training and admin runbooks
- Phased rollout with stabilization window

### Time estimate for Scope 2

- If built after Scope 1: +7 to +14 weeks
- Total from scratch (Scope 1 + Scope 2): 12-21 weeks typical
- Conservative with complex integrations/change management: 22-28 weeks

### Effort estimate (person-weeks)

- Technical implementer: 10-18 person-weeks (total)
- Operations/admin lead: 4-7 person-weeks (total)
- Stakeholder/UAT participation: 1.5-3 person-weeks (total)

## Milestones and Decision Gates

1. Gate A: Initial Launch Ready

- Core donations, events, contacts, segmentation, and reporting pass UAT

2. Gate B: Required Feature Coverage Confirmed

- Every `✅` priority matrix criterion has passed acceptance checks

3. Gate C: Operational Sustainability

- Admin SOPs, training, and monitoring in place for ongoing low-risk operations

## Biggest Schedule Risks

- Unclear ownership for business rules (fund allocation, portal behavior, automations)
- Late data cleanup discoveries during migration
- Integration reliability issues without monitoring/retry design
- Under-scoped training and change-management time

## Ways to Shorten Timeline Safely

- Freeze MVP scope and defer non-required enhancements
- Use standard CiviCRM patterns before custom coding
- Build acceptance criteria before configuration work begins
- Run weekly UAT checkpoints instead of end-loaded testing

## Recommended Next Step

Create a row-by-row implementation tracker from `evaluation-matrix.md` (`✅` priority rows only) with these columns:

- owner
- implementation path (`✅` native / `🟡` config / `🛠️` custom)
- acceptance test
- due date
- status
