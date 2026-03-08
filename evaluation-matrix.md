# CRM Evaluation Matrix

## Key: Priority

- `✅` Required
- `🟡` Possibly required
- `❓` Don't know

## Key: Feature Availability (per CRM)

- `✅` Feature present (native)
- `🟡` Feature present with extension/configuration/workaround
- `❌` Feature not present

## Key: Notes Marker

- `🟠` Click marker to jump to note/context

| Criteria                                                                      | Priority | CiviCRM                     | Pipedrive                    | Zeffy | DonorView | Givebutter | Bloomerang | Neon CRM |
| ----------------------------------------------------------------------------- | -------- | --------------------------- | ---------------------------- | ----- | --------- | ---------- | ---------- | -------- |
| Contact records                                                               | ✅       | ✅                          | ✅                           |       |           |            |            |          |
| Custom fields                                                                 | ✅       | ✅                          | ✅                           |       |           |            |            |          |
| Tagging                                                                       | ✅       | ✅                          | ✅                           |       |           |            |            |          |
| Segmentation                                                                  | ✅       | ✅                          | ✅                           |       |           |            |            |          |
| Notes on records                                                              | ✅       | ✅                          | ✅                           |       |           |            |            |          |
| File attachments                                                              | ✅       | ✅                          | ✅                           |       |           |            |            |          |
| Contact timelines                                                             | ✅       | ✅                          | ✅                           |       |           |            |            |          |
| Interaction history                                                           | ❓       | ✅                          | ✅                           |       |           |            |            |          |
| Activity tracking                                                             | ❓       | ✅                          | ✅                           |       |           |            |            |          |
| Call logging                                                                  | ❓       | ✅                          | ✅                           |       |           |            |            |          |
| Data import/export (CSV)                                                      | ✅       | ✅                          | ✅                           |       |           |            |            |          |
| Constituent self-service portal (profile + preferences)                       | ✅       | 🟡                          | [🟠](#note-pipedrive-portal) |       |           |            |            |          |
| Role-based access control (admin vs staff)                                    | ✅       | ✅                          | ✅                           |       |           |            |            |          |
| One-time donations                                                            | ✅       | ✅                          | 🟡                           |       |           |            |            |          |
| Recurring donations                                                           | ✅       | ✅                          | 🟡                           |       |           |            |            |          |
| Donation forms (embeddable)                                                   | ✅       | ✅                          | 🟡                           |       |           |            |            |          |
| Campaign tracking                                                             | ✅       | ✅                          | ✅                           |       |           |            |            |          |
| Pledge tracking                                                               | ✅       | ✅                          | 🟡                           |       |           |            |            |          |
| Donation receipts (auto-generated)                                            | ❓       | ✅                          | 🟡                           |       |           |            |            |          |
| Tax receipt generation                                                        | ❓       | ✅                          | [🟠](#note-pipedrive-tax)    |       |           |            |            |          |
| Offline donation entry                                                        | ✅       | ✅                          | 🟡                           |       |           |            |            |          |
| Fund allocation tracking (annual, monthly, endowment, critical solicitations) | ✅       | ✅                          | 🟡                           |       |           |            |            |          |
| Grant tracking                                                                | 🟡       | ✅                          | 🟡                           |       |           |            |            |          |
| Donor tiers                                                                   | ❓       | 🟡                          | ✅                           |       |           |            |            |          |
| Donor lifetime value calculation                                              | ✅       | 🟡                          | 🟡                           |       |           |            |            |          |
| Donor segmentation                                                            | ✅       | ✅                          | ✅                           |       |           |            |            |          |
| Matching gift workflow automation                                             | 🟡       | 🟡                          | 🟡                           |       |           |            |            |          |
| Planned giving / legacy gift tracking                                         | ✅       | 🟡                          | 🟡                           |       |           |            |            |          |
| Grant deadline and reporting workflow reminders                               | 🟡       | 🟡                          | ✅                           |       |           |            |            |          |
| Donation acknowledgement automation (beyond receipts)                         | ✅       | 🟡                          | 🟡                           |       |           |            |            |          |
| Event creation                                                                | ✅       | ✅                          | 🟡                           |       |           |            |            |          |
| Event landing pages                                                           | ❓       | ✅                          | [🟠](#note-pipedrive-events) |       |           |            |            |          |
| Event ticketing                                                               | ❓       | ✅                          | [🟠](#note-pipedrive-events) |       |           |            |            |          |
| RSVP tracking                                                                 | ✅       | ✅                          | 🟡                           |       |           |            |            |          |
| Guest list management                                                         | 🟡       | ✅                          | 🟡                           |       |           |            |            |          |
| Waitlist management                                                           | 🟡       | 🟡                          | [🟠](#note-pipedrive-events) |       |           |            |            |          |
| Event capacity limits                                                         | ✅       | ✅                          | [🟠](#note-pipedrive-events) |       |           |            |            |          |
| Event reminder automation                                                     | ✅       | ✅                          | 🟡                           |       |           |            |            |          |
| Event feedback surveys                                                        | ✅       | 🟡                          | 🟡                           |       |           |            |            |          |
| Event revenue tracking                                                        | ✅       | ✅                          | 🟡                           |       |           |            |            |          |
| Automated post-event follow-up workflows                                      | 🟡       | 🟡                          | ✅                           |       |           |            |            |          |
| Event registration forms/workflows                                            | ✅       | ✅                          | 🟡                           |       |           |            |            |          |
| Automated event confirmations                                                 | ✅       | ✅                          | 🟡                           |       |           |            |            |          |
| Volunteer sign-up forms                                                       | ✅       | 🟡                          | 🟡                           |       |           |            |            |          |
| Skills tracking                                                               | 🟡       | 🟡                          | 🟡                           |       |           |            |            |          |
| Membership renewal reminders                                                  | ✅       | ✅                          | 🟡                           |       |           |            |            |          |
| Membership dues processing                                                    | ✅       | ✅                          | 🟡                           |       |           |            |            |          |
| Volunteer engagement history                                                  | ✅       | 🟡                          | ✅                           |       |           |            |            |          |
| Volunteer categorization and tagging                                          | ✅       | ✅                          | ✅                           |       |           |            |            |          |
| Automated volunteer communication (SMS + email)                               | ✅       | 🟡                          | 🟡                           |       |           |            |            |          |
| Auto-populate volunteer past participation                                    | ✅       | 🟡                          | 🟡                           |       |           |            |            |          |
| Email campaign builder                                                        | ✅       | ✅                          | ✅                           |       |           |            |            |          |
| Email templates                                                               | ✅       | ✅                          | ✅                           |       |           |            |            |          |
| Automated welcome sequences                                                   | 🟡       | 🟡                          | ✅                           |       |           |            |            |          |
| Triggered emails                                                              | ❓       | 🟡                          | ✅                           |       |           |            |            |          |
| Email open tracking                                                           | 🟡       | ✅                          | ✅                           |       |           |            |            |          |
| Click tracking                                                                | 🟡       | ✅                          | ✅                           |       |           |            |            |          |
| Unsubscribe management                                                        | 🟡       | ✅                          | ✅                           |       |           |            |            |          |
| SMS marketing                                                                 | ✅       | 🟡                          | 🟡                           |       |           |            |            |          |
| Newsletter management                                                         | ✅       | ✅                          | ✅                           |       |           |            |            |          |
| Revenue reporting                                                             | ✅       | ✅                          | ✅                           |       |           |            |            |          |
| Campaign ROI tracking                                                         | ❓       | 🟡                          | 🟡                           |       |           |            |            |          |
| Stripe integration                                                            | 🟡       | ✅                          | ✅                           |       |           |            |            |          |
| PayPal integration                                                            | 🟡       | ✅                          | 🟡                           |       |           |            |            |          |
| QuickBooks integration                                                        | ✅       | 🟡                          | ✅                           |       |           |            |            |          |
| Cashapp/Venmo                                                                 | ✅       | [🟠](#note-wallets-crm)     | [🟠](#note-wallets-crm)      |       |           |            |            |          |
| Website integration path (embed/plugin/API)                                   | ✅       | ✅                          | ✅                           |       |           |            |            |          |
| QuickBooks class-tracking compatibility/workaround                            | ✅       | 🟡                          | 🟡                           |       |           |            |            |          |
| Alternate ways to collect money                                               | 🟡       | 🟡                          | 🟡                           |       |           |            |            |          |
| Monthly platform cost fits target budget                                      | ✅       | ✅                          | 🟡                           |       |           |            |            |          |
| Low ongoing admin overhead                                                    | ✅       | [🟠](#note-civi-admin)      | ✅                           |       |           |            |            |          |
| New-user onboarding usability                                                 | ✅       | [🟠](#note-civi-onboarding) | ✅                           |       |           |            |            |          |

## Notes

### Note: CiviCRM Admin Overhead

<a id="note-civi-admin"></a>
CiviCRM usually needs more initial setup and process definition than turnkey SaaS tools, but ongoing admin can be manageable for Temple Foundation if workflows are documented and ownership is clear.

### Note: CiviCRM Onboarding Usability

<a id="note-civi-onboarding"></a>
CiviCRM has a learning curve for new users, but role-specific SOPs and short task checklists can make day-to-day use approachable for non-technical staff.

### Note: Pipedrive Constituent Portal

<a id="note-pipedrive-portal"></a>
Pipedrive does not include a nonprofit-style constituent self-service portal natively, but this can be delivered through an external portal/form stack with sync back to Pipedrive.

### Note: Pipedrive Tax Receipt Generation

<a id="note-pipedrive-tax"></a>
Pipedrive is not tax-receipt-native for donations; organizations typically generate compliant receipts through integrated fundraising/accounting tools and store references in Pipedrive.

### Note: Pipedrive Event Stack

<a id="note-pipedrive-events"></a>
Event landing pages, ticketing, waitlists, and strict capacity controls are usually handled by an event platform integrated with Pipedrive rather than inside Pipedrive itself.

### Note: Cash App/Venmo In CRM Context

<a id="note-wallets-crm"></a>
Cash App and Venmo are generally collected through external payment tools and then recorded/synced into the CRM; this is feasible operationally but not a native in-CRM payment rail.
