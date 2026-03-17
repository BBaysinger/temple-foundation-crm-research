# Required Items by Difficulty and Time (Claude Estimate)

Date: March 13, 2026
Basis: `evaluation-matrix.md` rows marked `✅` only
Estimator: Claude (Opus 4.6) independent estimate
Implementation assumption: CiviCRM-oriented stack, 1 developer, production-ready config/testing, heavy AI assistance

## Estimation Instructions (Use Independent Judgment)

- Provide fresh estimates from scratch.
- Do not reference or reuse prior estimates from Codex, GPT, or any previous document.
- Treat this as a clean-room estimate based only on the scope listed below.
- Estimates should reflect implementation effort ranges, not elapsed calendar guarantees.
- Assume a 5-day work week unless otherwise stated.
- If assumptions are required, state them explicitly.

---

## Estimation Context

- Implementation target: CiviCRM-oriented stack
- Team size: 1 developer
- Delivery quality target: production-ready configuration and testing
- AI/tooling acceleration level: heavy AI assistance
- Notes:
  - Time estimates are implementation effort ranges.
  - Day-to-week conversions use a 5-day work week.
  - Two score-only rows in the matrix are excluded.

---

## Easy

These are mostly native setup, standard configuration, or straightforward admin workflows.

1. **Core contact model**
   `Contact records`, `Custom fields`, `Tagging`, `Segmentation`, `Notes on records`, `File attachments`, `Contact timelines`
   **Estimate:** `1.5–3 days`

2. **Basic data administration**
   `Data import/export (CSV)`, `Role-based access control`
   **Estimate:** `1–2 days`

3. **Basic communications setup**
   `Email templates`, `Email subgroups`, `Newsletter management`
   **Estimate:** `1–2 days`

4. **Basic event setup**
   `Event creation`, `RSVP tracking`, `Event capacity limits`, `Event feedback surveys`
   **Estimate:** `1.5–3 days`

5. **Usability baseline**
   `New-user onboarding usability`
   **Estimate:** `1–2 days`

6. **Budget validation**
   `Monthly platform cost fits target budget`
   **Estimate:** `0.5 day`

### Tier total

`6.5–12.5 days` (`~1.3–2.5 weeks`)

### Cumulative total

`6.5–12.5 days` (`~1.3–2.5 weeks`)

---

## Moderate

These involve cross-feature wiring, validation, and QA.

1. **Donation flow baseline**
   `One-time donations`, `Recurring donations`, `Donation forms (embeddable)`, `Offline donation entry`
   **Estimate:** `3–5 days`

2. **Campaign and fundraising operations**
   `Campaign tracking`, `Donation acknowledgement automation`, `Revenue reporting`, `Event revenue tracking`
   **Estimate:** `2–4 days`

3. **Event automation**
   `Event registration forms/workflows`, `Automated event confirmations`, `Event reminder automation`
   **Estimate:** `2–3 days`

4. **Volunteer and membership baseline**
   `Volunteer sign-up forms`, `Volunteer participation history`, `Volunteer categorization and tagging`, `Membership renewal reminders`, `Membership dues processing`
   **Estimate:** `3–6 days`

5. **Donor intelligence baseline**
   `Donor segmentation`, `Donor lifetime value calculation`
   **Estimate:** `2–3 days`

6. **Quality and reliability baseline**
   `Duplicate detection + merge quality`, `Backup/export resilience`
   **Estimate:** `1.5–3 days`

7. **Embedding path**
   `Embeddable forms/widgets flexibility`
   **Estimate:** `1–2 days`

### Tier total

`14.5–26 days` (`~2.9–5.2 weeks`)

### Cumulative total

`21–38.5 days` (`~4.2–7.7 weeks`)

---

## Hard

These typically require process design, integration logic, and deeper QA.

1. **Portal and self-service**
   `Constituent self-service portal (profile + preferences)`
   **Estimate:** `1–2 weeks`

2. **Fund accounting model**
   `Fund allocation tracking`, `Revenue categories`, `Pledge tracking`, `Planned giving / legacy gift tracking`
   **Estimate:** `1.5–3 weeks`

3. **Volunteer automation depth**
   `Volunteer coordination history`, `Automated volunteer communication (SMS + email)`, `Auto-populate volunteer past participation`
   **Estimate:** `1.5–3 weeks`

4. **Finance integrations**
   `QuickBooks integration`, `Accounting linkage (sync to accounting system)`, `Cashapp/Venmo capture flow`
   **Estimate:** `2–4 weeks`

5. **API integrations**
   `API/webhook depth for custom site workflows`
   **Estimate:** `1–2 weeks`

6. **Operations hardening**
   `Low ongoing admin overhead`, `Initial setup/config/deployment simplicity` workarounds
   **Estimate:** `1–2 weeks`

7. **Platform risk controls**
   `Scalability switch risk` mitigation, `Data migration complexity` planning and execution
   **Estimate:** `1.5–3 weeks`

### Tier total

`9.5–19 weeks`

### Cumulative total

`~13.7–26.7 weeks`

---

## Very Hard

These are usually highest-risk edge cases.

1. **Advanced accounting edge case**
   `QuickBooks class-tracking compatibility/workaround`
   **Estimate:** `2–4 weeks`

2. **SMS program at scale**
   `SMS marketing` with compliance workflows, segmentation, opt-in/out handling, and delivery process
   **Estimate:** `2–4 weeks`

### Tier total

`4–8 weeks`

### Cumulative total (all required tiers)

`~17.7–34.7 weeks` (`~4.4–8.7 months`)

---

## Maybe (Optional) - Very Hard Add-On

1. **Headless architecture**
   `Non-widget implementation path (API-first/headless)`
   **Estimate:** `3–8 weeks`

### Tier total (optional)

`3–8 weeks`

### Cumulative total (required + optional headless)

`~20.7–42.7 weeks` (`~5.2–10.7 months`)

---

## Roll-Up Totals

1. **MVP required subset (core CRM + donations + basic events + basic email):** `~2–3.5 weeks`
2. **Full required set (excluding optional headless paths):** `~17.7–34.7 weeks` (`~4.4–8.7 months`)
3. **If optional headless path is included from day one:** `~20.7–42.7 weeks` (`~5.2–10.7 months`)
4. **If optional extensibility is used strategically:** timeline impact is context-dependent; can reduce selected feature timelines by leveraging CiviCRM's open-source extensibility

---

## Practical Roll-Up Read

- A working MVP (contacts, donations, events, email) can ship in **2–3.5 weeks**.
- The full required feature set lands in roughly **4.4–8.7 months** of implementation effort.
- Adding the headless/API-first path extends the upper bound to **~10.7 months**.
- The Easy + Moderate tiers (~7.7 weeks worst case) deliver the bulk of day-to-day operational value; the Hard + Very Hard tiers are where schedule risk concentrates.

Biggest schedule risks:

- **QuickBooks integration + class-tracking compatibility** — CiviCRM rates 🛠️ for both; requires custom extension or middleware and depends on QB API cooperation.
- **Finance integrations broadly** — Cashapp/Venmo capture has no native CRM rail; requires external tooling and manual reconciliation design.
- **Volunteer automation depth** — CiviCRM's volunteer features (CiviVolunteer) are 🟡 at best; SMS + email automation for volunteers requires extension wiring.
- **Constituent self-service portal** — CiviCRM supports this natively, but production-quality UX requires theming and security hardening.
- **Data migration complexity** — rated 🟡; depends entirely on the state of existing data and source systems.
- **SMS at scale** — compliance (TCPA/10DLC registration), provider setup, and opt-in/out workflows add end-to-end process design effort beyond code.

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
