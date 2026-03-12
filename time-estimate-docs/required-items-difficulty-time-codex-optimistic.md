# Required Items by Difficulty and Time (Optimistic Estimate)

Date: March 12, 2026  
Basis: `evaluation-matrix.md` rows marked `✅` only  
Estimator: Codex optimistic estimate  
Implementation assumption: CiviCRM-oriented stack, 1 developer, production-ready config/testing, heavy AI assistance

## Estimation Rules

- Estimates are **implementation effort ranges**, not elapsed calendar guarantees.
- A **5-day work week** is assumed for week conversion.
- Optimistic assumes:
  - fast stakeholder turnaround
  - clean-enough data and stable requirements
  - no major integration surprises
  - disciplined scope control
- Two score-only rows from the matrix remain excluded.
- These estimates still target a **real deliverable**, not a demo.

---

## Estimation Context

- Implementation target: CiviCRM-oriented stack
- Team: 1 developer
- Delivery quality: production-ready configuration and testing
- Acceleration: heavy AI assistance
- Notes:
  - Time estimates are implementation effort ranges.
  - Day-to-week conversions use a 5-day work week.
  - Two score rows in the matrix are excluded from this list.

---

## Easy (0.5-2 days each)

These are mostly native setup, standard configuration, or straightforward admin workflows.

1. **Core contact model**  
   `Contact records`, `Custom fields`, `Tagging`, `Segmentation`, `Notes on records`, `File attachments`, `Contact timelines`  
   **Estimate:** `1.5-3 days`

2. **Basic data administration**  
   `Data import/export (CSV)`, `Role-based access control`  
   **Estimate:** `0.5-1.5 days`

3. **Basic communications setup**  
   `Email templates`, `Email subgroups`, `Newsletter management`  
   **Estimate:** `0.5-1.5 days`

4. **Basic event setup**  
   `Event creation`, `RSVP tracking`, `Event capacity limits`, `Event feedback surveys`  
   **Estimate:** `1-2 days`

5. **Usability baseline**  
   `New-user onboarding usability`  
   **Estimate:** `0.5-1.5 days`

6. **Budget validation**  
   `Monthly platform cost fits target budget`  
   **Estimate:** `0.25-0.5 day`

### Tier total

`4.25-10 days` (`~0.9-2.0 weeks`)

### Cumulative total

`4.25-10 days` (`~0.9-2.0 weeks`)

---

## Moderate (2-5 days each)

These are workable in a normal implementation, but they involve cross-feature wiring and QA.

1. **Donation flow baseline**  
   `One-time donations`, `Recurring donations`, `Donation forms (embeddable)`, `Offline donation entry`  
   **Estimate:** `2-4 days`

2. **Campaign and fundraising operations**  
   `Campaign tracking`, `Donation acknowledgement automation`, `Revenue reporting`, `Event revenue tracking`  
   **Estimate:** `2-4 days`

3. **Event automation**  
   `Event registration forms/workflows`, `Automated event confirmations`, `Event reminder automation`  
   **Estimate:** `1.5-3 days`

4. **Volunteer and membership baseline**  
   `Volunteer sign-up forms`, `Volunteer participation history`, `Volunteer categorization and tagging`, `Membership renewal reminders`, `Membership dues processing`  
   **Estimate:** `3-5 days`

5. **Donor intelligence baseline**  
   `Donor segmentation`, `Donor lifetime value calculation`  
   **Estimate:** `1.5-3 days`

6. **Quality and reliability baseline**  
   `Duplicate detection + merge quality`, `Backup/export resilience`  
   **Estimate:** `1.5-3 days`

7. **Embedding path**  
   `Embeddable forms/widgets flexibility`  
   **Estimate:** `1-2 days`

### Tier total

`12.5-24 days` (`~2.5-4.8 weeks`)

### Cumulative total

`16.75-34 days` (`~3.35-6.8 weeks`)

---

## Hard (1-3 weeks each)

These usually require process design, integration logic, and higher QA depth.

1. **Portal and self-service**  
   `Constituent self-service portal (profile + preferences)`  
   **Estimate:** `1-1.5 weeks`

2. **Fund accounting model**  
   `Fund allocation tracking`, `Revenue categories`, `Pledge tracking`, `Planned giving / legacy gift tracking`  
   **Estimate:** `1.5-3 weeks`

3. **Volunteer automation depth**  
   `Volunteer coordination history`, `Automated volunteer communication (SMS + email)`, `Auto-populate volunteer past participation`  
   **Estimate:** `1.5-3 weeks`

4. **Finance integrations**  
   `QuickBooks integration`, `Accounting linkage (sync to accounting system)`, `Cashapp/Venmo capture flow`  
   **Estimate:** `1.5-3 weeks`

5. **API integrations**  
   `API/webhook depth for custom site workflows`  
   **Estimate:** `0.75-1.5 weeks`

6. **Operations hardening**  
   `Low ongoing admin overhead`, `Initial setup/config/deployment simplicity` workarounds  
   **Estimate:** `0.75-2 weeks`

7. **Platform risk controls**  
   `Scalability switch risk` mitigation, `Data migration complexity` planning and execution  
   **Estimate:** `1.5-3 weeks`

### Tier total

`8.5-17 weeks`

### Cumulative total

`~11.85-23.8 weeks`

---

## Very Hard (3-8+ weeks each)

These remain the highest-risk edge cases even in optimistic execution.

1. **Advanced accounting edge case**  
   `QuickBooks class-tracking compatibility/workaround`  
   **Estimate:** `1.5-3.5 weeks`

2. **SMS program at scale**  
   `SMS marketing` with compliant workflows, segmentation, opt-in/out handling, and delivery process  
   **Estimate:** `1.5-3 weeks`

### Tier total

`3-6.5 weeks`

### Cumulative total (all required tiers)

`~14.85-30.3 weeks` (`~3.7-7.6 months`)

---

## Maybe (Optional) - Very Hard Add-On

1. **Headless architecture**  
   `Non-widget implementation path (API-first/headless)`  
   **Estimate:** `2.5-5 weeks`

### Tier total (optional)

`2.5-5 weeks`

### Cumulative total (required + optional headless)

`~17.35-35.3 weeks` (`~4.3-8.8 months`)

---

## Roll-Up Totals

1. **MVP required subset (core CRM + donations + basic events + basic email):** `~1.5-3 weeks`
2. **Full required set (excluding optional headless paths):** `~14.85-30.3 weeks` (`~3.7-7.6 months`)
3. **If optional headless path is included from day one:** `~17.35-35.3 weeks` (`~4.3-8.8 months`)
4. **If optional extensibility is used strategically:** lower-middle range is realistically around `16-24 weeks` (`~4-6 months`) under tight scope and low rework.

---

## Practical Roll-Up Read

- **1.5-3 weeks** can produce a credible first release if decisions are fast and scope stays tight.
- **4-8 weeks** can produce a strong phase-1 operational release with fewer deferred items.
- **~4-8 months** remains realistic for full required coverage when hard edge cases are truly included.
- **Add ~2.5-5 weeks** if an API-first/headless path is required early.

Biggest schedule risks:

- accounting expectations expanding midstream
- SMS/compliance workflow depth
- constituent portal expectations
- dirty migration data
- trying to avoid widget-style embeds too early
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
