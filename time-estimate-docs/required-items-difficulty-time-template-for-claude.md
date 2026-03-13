# Required Items by Difficulty and Time (Blank Estimation Template)

Date: ********\_\_\_\_********
Basis: `evaluation-matrix.md` rows marked `✅` only
Estimator: ********\_\_\_\_********
Implementation assumption: ********\_\_\_\_********

## Estimation Instructions (Use Independent Judgment)

- Provide fresh estimates from scratch.
- Do not reference or reuse prior estimates from Codex, GPT, or any previous document.
- Treat this as a clean-room estimate based only on the scope listed below.
- Estimates should reflect implementation effort ranges, not elapsed calendar guarantees.
- Assume a 5-day work week unless otherwise stated.
- If assumptions are required, state them explicitly.

---

## Estimation Context

- Implementation target: ********\_\_\_\_********
- Team size: ********\_\_\_\_********
- Delivery quality target: production-ready configuration and testing (or specify)
- AI/tooling acceleration level: ********\_\_\_\_********
- Notes:
  - Time estimates are implementation effort ranges.
  - Day-to-week conversions use a 5-day work week.
  - Two score-only rows in the matrix are excluded.

---

## Easy

These are mostly native setup, standard configuration, or straightforward admin workflows.

1. **Core contact model**
   `Contact records`, `Custom fields`, `Tagging`, `Segmentation`, `Notes on records`, `File attachments`, `Contact timelines`
   **Estimate:** `____________________`

2. **Basic data administration**
   `Data import/export (CSV)`, `Role-based access control`
   **Estimate:** `____________________`

3. **Basic communications setup**
   `Email templates`, `Email subgroups`, `Newsletter management`
   **Estimate:** `____________________`

4. **Basic event setup**
   `Event creation`, `RSVP tracking`, `Event capacity limits`, `Event feedback surveys`
   **Estimate:** `____________________`

5. **Usability baseline**
   `New-user onboarding usability`
   **Estimate:** `____________________`

6. **Budget validation**
   `Monthly platform cost fits target budget`
   **Estimate:** `____________________`

### Tier total

`____________________`

### Cumulative total

`____________________`

---

## Moderate

These involve cross-feature wiring, validation, and QA.

1. **Donation flow baseline**
   `One-time donations`, `Recurring donations`, `Donation forms (embeddable)`, `Offline donation entry`
   **Estimate:** `____________________`

2. **Campaign and fundraising operations**
   `Campaign tracking`, `Donation acknowledgement automation`, `Revenue reporting`, `Event revenue tracking`
   **Estimate:** `____________________`

3. **Event automation**
   `Event registration forms/workflows`, `Automated event confirmations`, `Event reminder automation`
   **Estimate:** `____________________`

4. **Volunteer and membership baseline**
   `Volunteer sign-up forms`, `Volunteer participation history`, `Volunteer categorization and tagging`, `Membership renewal reminders`, `Membership dues processing`
   **Estimate:** `____________________`

5. **Donor intelligence baseline**
   `Donor segmentation`, `Donor lifetime value calculation`
   **Estimate:** `____________________`

6. **Quality and reliability baseline**
   `Duplicate detection + merge quality`, `Backup/export resilience`
   **Estimate:** `____________________`

7. **Embedding path**
   `Embeddable forms/widgets flexibility`
   **Estimate:** `____________________`

### Tier total

`____________________`

### Cumulative total

`____________________`

---

## Hard

These typically require process design, integration logic, and deeper QA.

1. **Portal and self-service**
   `Constituent self-service portal (profile + preferences)`
   **Estimate:** `____________________`

2. **Fund accounting model**
   `Fund allocation tracking`, `Revenue categories`, `Pledge tracking`, `Planned giving / legacy gift tracking`
   **Estimate:** `____________________`

3. **Volunteer automation depth**
   `Volunteer coordination history`, `Automated volunteer communication (SMS + email)`, `Auto-populate volunteer past participation`
   **Estimate:** `____________________`

4. **Finance integrations**
   `QuickBooks integration`, `Accounting linkage (sync to accounting system)`, `Cashapp/Venmo capture flow`
   **Estimate:** `____________________`

5. **API integrations**
   `API/webhook depth for custom site workflows`
   **Estimate:** `____________________`

6. **Operations hardening**
   `Low ongoing admin overhead`, `Initial setup/config/deployment simplicity` workarounds
   **Estimate:** `____________________`

7. **Platform risk controls**
   `Scalability switch risk` mitigation, `Data migration complexity` planning and execution
   **Estimate:** `____________________`

### Tier total

`____________________`

### Cumulative total

`____________________`

---

## Very Hard

These are usually highest-risk edge cases.

1. **Advanced accounting edge case**
   `QuickBooks class-tracking compatibility/workaround`
   **Estimate:** `____________________`

2. **SMS program at scale**
   `SMS marketing` with compliance workflows, segmentation, opt-in/out handling, and delivery process
   **Estimate:** `____________________`

### Tier total

`____________________`

### Cumulative total (all required tiers)

`____________________`

---

## Maybe (Optional) - Very Hard Add-On

1. **Headless architecture**
   `Non-widget implementation path (API-first/headless)`
   **Estimate:** `____________________`

### Tier total (optional)

`____________________`

### Cumulative total (required + optional headless)

`____________________`

---

## Roll-Up Totals

1. **MVP required subset (core CRM + donations + basic events + basic email):** `____________________`
2. **Full required set (excluding optional headless paths):** `____________________`
3. **If optional headless path is included from day one:** `____________________`
4. **If optional extensibility is used strategically:** `____________________`

---

## Practical Roll-Up Read

- `____________________`
- `____________________`
- `____________________`
- `____________________`

Biggest schedule risks:

- `____________________`
- `____________________`
- `____________________`
- `____________________`
- `____________________`
- `____________________`

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
