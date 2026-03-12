# Required Items by Difficulty and Time (From Evaluation Matrix)

Date: March 12, 2026  
Source: `evaluation-matrix.md` (rows marked `✅` in the criteria column only)

## Estimation Context

- Implementation target: CiviCRM-oriented stack
- Team: 1 developer
- Delivery quality: production-ready configuration and testing
- Acceleration: heavy AI assistance
- Notes:
  - Time estimates are implementation effort ranges.
  - Day-to-week conversions use a 5-day work week.
  - Two score rows in the matrix are excluded from this list.

## Easy (0.5-2 days each)

1. Core contact model: `Contact records`, `Custom fields`, `Tagging`, `Segmentation`, `Notes on records`, `File attachments`, `Contact timelines` (`2-4 days` bundle)
2. Basic data admin: `Data import/export (CSV)`, `Role-based access control` (`1-2 days`)
3. Basic communications setup: `Email templates`, `Email subgroups`, `Newsletter management` (`1-2 days`)
4. Basic event setup: `Event creation`, `RSVP tracking`, `Event capacity limits`, `Event feedback surveys` (`2-3 days`)
5. Usability baseline: `New-user onboarding usability` (`1-2 days`)
6. Budget validation: `Monthly platform cost fits target budget` (`0.5-1 day`)

Tier total: `7.5-14 days` (`~1.5-2.8 weeks`)  
Cumulative total: `7.5-14 days` (`~1.5-2.8 weeks`)

## Moderate (2-5 days each)

1. Donation flow baseline: `One-time donations`, `Recurring donations`, `Donation forms (embeddable)`, `Offline donation entry` (`4-7 days`)
2. Campaign and fundraising operations: `Campaign tracking`, `Donation acknowledgement automation`, `Revenue reporting`, `Event revenue tracking` (`3-5 days`)
3. Event automation: `Event registration forms/workflows`, `Automated event confirmations`, `Event reminder automation` (`3-5 days`)
4. Volunteer and membership baseline: `Volunteer sign-up forms`, `Volunteer participation history`, `Volunteer categorization and tagging`, `Membership renewal reminders`, `Membership dues processing` (`4-7 days`)
5. Donor intelligence baseline: `Donor segmentation`, `Donor lifetime value calculation` (`2-4 days`)
6. Quality and reliability baseline: `Duplicate detection + merge quality`, `Backup/export resilience` (`2-4 days`)
7. Embedding path: `Embeddable forms/widgets flexibility` (`2-3 days`)

Tier total: `20-35 days` (`~4-7 weeks`)  
Cumulative total: `27.5-49 days` (`~5.5-9.8 weeks`)

## Hard (1-3 weeks each)

1. Portal and self-service: `Constituent self-service portal (profile + preferences)` (`1-2 weeks`)
2. Fund accounting model: `Fund allocation tracking`, `Revenue categories`, `Pledge tracking`, `Planned giving / legacy gift tracking` (`2-4 weeks`)
3. Volunteer automation depth: `Volunteer coordination history`, `Automated volunteer communication (SMS + email)`, `Auto-populate volunteer past participation` (`2-4 weeks`)
4. Finance integrations: `QuickBooks integration`, `Accounting linkage (sync to accounting system)`, `Cashapp/Venmo` capture flow (`2-4 weeks`)
5. API integrations: `API/webhook depth for custom site workflows` (`1-2 weeks`)
6. Operations hardening: `Low ongoing admin overhead`, `Initial setup/config/deployment simplicity` workarounds (`1-3 weeks`)
7. Platform risk controls: `Scalability switch risk` mitigation, `Data migration complexity` planning and execution (`2-4 weeks`)

Tier total: `11-23 weeks`  
Cumulative total: `~16.5-32.8 weeks`

## Very Hard (3-8+ weeks each)

1. Advanced accounting edge case: `QuickBooks class-tracking compatibility/workaround` (`2-5 weeks`)
2. SMS program at scale: `SMS marketing` with compliant workflows and segmentation (`2-4 weeks`)

Tier total: `4-9 weeks`  
Cumulative total (all required tiers): `~20.5-41.8 weeks` (`~5-10 months`)

## Maybe (Optional) - Very Hard Add-On

1. Headless architecture: `Non-widget implementation path (API-first/headless)` (`3-6 weeks`)

Tier total (optional): `3-6 weeks`  
Cumulative total (required + optional headless): `~23.5-47.8 weeks` (`~5.5-11 months`)

## Roll-Up Totals

1. MVP required subset (core CRM + donations + basic events + basic email): `~3-5 weeks`
2. Full required set (excluding optional headless paths): `~20.5-41.8 weeks` (`~5-10 months`)
3. If optional headless path is included from day one: `~23.5-47.8 weeks` (`~5.5-11 months`)
4. If optional extensibility is used strategically: timeline impact is context-dependent and can reduce implementation time for selected features.

## Included Required Criteria Snapshot

Rows used from `evaluation-matrix.md` (criteria with `✅` priority marker):

- Contact records
- Custom fields
- Tagging
- Segmentation
- Notes on records
- File attachments
- Contact timelines
- Data import/export (CSV)
- Constituent self-service portal (profile + preferences)
- Role-based access control (admin vs staff)
- One-time donations
- Recurring donations
- Donation forms (embeddable)
- Campaign tracking
- Pledge tracking
- Offline donation entry
- Fund allocation tracking (annual, monthly, endowment, critical solicitations)
- Revenue categories (by program/fund/campaign)
- Donor lifetime value calculation
- Donor segmentation
- Planned giving / legacy gift tracking
- Donation acknowledgement automation (beyond receipts)
- Event creation
- RSVP tracking
- Event capacity limits
- Event reminder automation
- Event feedback surveys
- Event revenue tracking
- Event registration forms/workflows
- Automated event confirmations
- Volunteer sign-up forms
- Membership renewal reminders
- Membership dues processing
- Volunteer coordination history (assignments/shifts/tasks)
- Volunteer participation history
- Volunteer categorization and tagging
- Automated volunteer communication (SMS + email)
- Auto-populate volunteer past participation
- Email campaign builder
- Email templates
- Email subgroups
- SMS marketing
- Newsletter management
- Revenue reporting
- QuickBooks integration
- Accounting linkage (sync to accounting system)
- Cashapp/Venmo
- Embeddable forms/widgets flexibility
- API/webhook depth for custom site workflows
- QuickBooks class-tracking compatibility/workaround
- Initial setup/config/deployment simplicity
- Scalability switch risk
- Data migration complexity
- Duplicate detection + merge quality
- Backup/export resilience (full-fidelity exit path)
- Low ongoing admin overhead
- New-user onboarding usability
- Monthly platform cost fits target budget

Optional add-ons (maybe):
- Non-widget implementation path (API-first/headless)
- Forkable source code for in-house feature development
