# Required Items by Difficulty and Time (Optimistic Evaluation)

Date: March 12, 2026  
Basis: `evaluation-matrix.md` rows marked `✅` only  
Estimator: ChatGPT optimistic estimate  
Implementation assumption: CiviCRM-oriented stack, 1 developer who is also the only tester, production-ready configuration/testing, heavy AI assistance, disciplined scope control

## Estimation Rules

- Estimates are **implementation effort ranges**, not elapsed calendar guarantees.
- A **5-day work week** is assumed for week conversion.
- Estimates assume:
  - stakeholder access is reasonably prompt
  - payment/accounting vendors cooperate
  - data is not catastrophically messy
  - no major custom plugin is required beyond expected extension/config work
  - implementation stays close to CiviCRM’s intended workflows where possible
- Two score-only rows from the matrix remain excluded.
- These estimates are for a **real deliverable**, not a demo.
- Because the same person is both the **implementer and sole tester**, build speed can be high, but QA capacity is narrower and more fragile than in a multi-person team.

---

## Estimation Context

- Implementation target: CiviCRM-oriented stack
- Team: 1 developer
- QA model: same developer is the only tester
- Delivery quality: production-ready configuration and testing
- Acceleration: heavy AI assistance
- Estimate posture: optimistic but credible
- Notes:
  - Time estimates are implementation effort ranges.
  - Day-to-week conversions use a 5-day work week.
  - Two score rows in the matrix are excluded from this list.

---

## Easy (0.5-2 days each)

These are mostly native setup, standard configuration, or straightforward admin workflows.

1. **Core contact model**  
   `Contact records`, `Custom fields`, `Tagging`, `Segmentation`, `Notes on records`, `File attachments`, `Contact timelines`  
   **Estimate:** `1-3 days`

2. **Basic data administration**  
   `Data import/export (CSV)`, `Role-based access control`  
   **Estimate:** `1-2 days`

3. **Basic communications setup**  
   `Email templates`, `Email subgroups`, `Newsletter management`  
   **Estimate:** `1-2 days`

4. **Basic event setup**  
   `Event creation`, `RSVP tracking`, `Event capacity limits`, `Event feedback surveys`  
   **Estimate:** `1-2 days`

5. **Usability baseline**  
   `New-user onboarding usability`  
   **Estimate:** `1 day`

6. **Budget validation**  
   `Monthly platform cost fits target budget`  
   **Estimate:** `0.5 day`

### Tier total

`5.5-10.5 days` (`1.1-2.1 weeks`)

### Cumulative total

`5.5-10.5 days` (`1.1-2.1 weeks`)

---

## Moderate (2-5 days each)

These are workable in a normal implementation, but they involve more cross-feature wiring, QA, and edge handling.

1. **Donation flow baseline**  
   `One-time donations`, `Recurring donations`, `Donation forms (embeddable)`, `Offline donation entry`  
   **Estimate:** `2-4 days`

2. **Campaign and fundraising operations**  
   `Campaign tracking`, `Donation acknowledgement automation`, `Revenue reporting`, `Event revenue tracking`  
   **Estimate:** `2-4 days`

3. **Event automation**  
   `Event registration forms/workflows`, `Automated event confirmations`, `Event reminder automation`  
   **Estimate:** `2-3 days`

4. **Volunteer and membership baseline**  
   `Volunteer sign-up forms`, `Volunteer participation history`, `Volunteer categorization and tagging`, `Membership renewal reminders`, `Membership dues processing`  
   **Estimate:** `3-5 days`

5. **Donor intelligence baseline**  
   `Donor segmentation`, `Donor lifetime value calculation`  
   **Estimate:** `2-3 days`

6. **Quality and reliability baseline**  
   `Duplicate detection + merge quality`, `Backup/export resilience`  
   **Estimate:** `2-3 days`

7. **Embedding path**  
   `Embeddable forms/widgets flexibility`  
   **Estimate:** `1-2 days`

### Tier total

`14-24 days` (`2.8-4.8 weeks`)

### Cumulative total

`19.5-34.5 days` (`3.9-6.9 weeks`)

---

## Hard (1-3 weeks each)

These are the features that usually stop being "configuration only" and start demanding process design, extension strategy, integration logic, and operational tradeoffs.

1. **Portal and self-service**  
   `Constituent self-service portal (profile + preferences)`  
   **Estimate:** `1-2 weeks`

2. **Fund accounting model**  
   `Fund allocation tracking`, `Revenue categories`, `Pledge tracking`, `Planned giving / legacy gift tracking`  
   **Estimate:** `1-3 weeks`

3. **Volunteer automation depth**  
   `Volunteer coordination history`, `Automated volunteer communication (SMS + email)`, `Auto-populate volunteer past participation`  
   **Estimate:** `1-3 weeks`

4. **Finance integrations**  
   `QuickBooks integration`, `Accounting linkage (sync to accounting system)`, `Cashapp/Venmo capture flow`  
   **Estimate:** `1-3 weeks`

5. **API integrations**  
   `API/webhook depth for custom site workflows`  
   **Estimate:** `1-2 weeks`

6. **Operations hardening**  
   `Low ongoing admin overhead`, `Initial setup/config/deployment simplicity` workarounds  
   **Estimate:** `1-2 weeks`

7. **Platform risk controls**  
   `Scalability switch risk` mitigation, `Data migration complexity` planning and execution  
   **Estimate:** `1-3 weeks`

### Tier total

`7-18 weeks`

### Cumulative total

`10.9-24.9 weeks`  
Approx. `2.7-6.2 months`

---

## Very Hard (3-8+ weeks each)

These are the ugly edge cases and "looks simple on paper, gets painful in implementation" items.

1. **Advanced accounting edge case**  
   `QuickBooks class-tracking compatibility/workaround`  
   **Estimate:** `2-4 weeks`

2. **SMS program at scale**  
   `SMS marketing` with compliant workflows, segmentation, opt-in/out handling, and delivery process  
   **Estimate:** `2-4 weeks`

### Tier total

`4-8 weeks`

### Cumulative total (all required tiers)

`14.9-32.9 weeks`  
Approx. `3.7-8.2 months`

---

## Maybe (Optional) - Very Hard Add-On

1. **Headless architecture**  
   `Non-widget implementation path (API-first/headless)`  
   **Estimate:** `4-6 weeks`

### Tier total (optional)

`4-6 weeks`

### Cumulative total (required + optional headless)

`18.9-38.9 weeks`  
Approx. `4.7-9.7 months`

---

## Roll-Up Totals

1. **MVP required subset (core CRM + donations + basic events + basic email):** `10-15 days` (`2-3 weeks`)
2. **Full required set:** `14.9-32.9 weeks` (`3.7-8.2 months`)
3. **Full required set with moderate real-world friction:** `18-28 weeks`
4. **If optional headless path is included from day one:** add `4-6 weeks`

---

## Practical Roll-Up Read

- A **usable first release** centered on contacts, donations, basic email, and events is realistic in about **2-3 weeks of implementation effort**.
- A **full required implementation** is still a **multi-month system**, even under optimistic assumptions.
- Being the **only dev and only tester** reduces coordination overhead, but it also means the same person must validate payments, permissions, forms, automations, reporting, migration behavior, and integration flows.
- The biggest effort multipliers remain **constituent self-service**, **fund/accounting structure**, **QuickBooks linkage**, **SMS workflows/compliance**, and **volunteer automation depth**.
- A **headless/non-widget path** is possible, but it should be treated as a separate architectural premium, not a free styling choice.

Biggest schedule risks:

- accounting expectations expanding midstream
- SMS/compliance workflow depth
- constituent portal expectations
- dirty migration data
- trying to avoid widget-style embeds too early
- underestimating solo QA time
- underestimating admin/training/process design work

---

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

## Optional add-ons (maybe)

- Non-widget implementation path (API-first/headless)
- Forkable source code for in-house feature development
