# CRM Evaluation Matrix

## Key: Feature Priority

- `✅` Required
- `🟡` Possibly required (probably)
- `❓` Don't know (maybe)

## Key: Feature Availability (per CRM)

- `✅` Present (native)
- `🟡` Available with configuration or native add-on (no external product required)
- `[#]` Depends on separate external product, but known to integrate (linked footnote names product)
- `❓` Yet to be confirmed
- `❌` Not present

## Key: Notes Marker

- `[#]` Click marker to jump to numbered footnote/context

| Criteria & Priority                                                              | CiviCRM      | Pipedrive    | Zeffy        | DonorView    | Givebutter   | Bloomerang   | Givebutter + Bloomerang | Neon CRM     |
| -------------------------------------------------------------------------------- | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ----------------------- | ------------ |
| Contact records ✅                                                               | ✅           | ✅           | ✅           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| Custom fields ✅                                                                 | ✅           | ✅           | 🟡           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| Tagging ✅                                                                       | ✅           | ✅           | 🟡           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| Segmentation ✅                                                                  | ✅           | ✅           | 🟡           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| Notes on records ✅                                                              | ✅           | ✅           | ❌           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| File attachments ✅                                                              | ✅           | ✅           | ❌           | ✅           | 🟡           | ✅           | ✅                      | ✅           |
| Contact timelines ✅                                                             | ✅           | ✅           | 🟡           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| Interaction history ❓                                                           | ✅           | ✅           | 🟡           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| Activity tracking ❓                                                             | ✅           | ✅           | ❌           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| Call logging ❓                                                                  | ✅           | ✅           | ❌           | 🟡           | ❌           | ❌           | ❌                      | ❌           |
| Data import/export (CSV) ✅                                                      | ✅           | ✅           | ✅           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| Constituent self-service portal (profile + preferences) ✅                       | 🟡           | [3](#note-3) | ❌           | ❌           | ❌           | ❌           | ❌                      | 🟡           |
| Role-based access control (admin vs staff) ✅                                    | ✅           | ✅           | 🟡           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| One-time donations ✅                                                            | ✅           | 🟡           | ✅           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| Recurring donations ✅                                                           | ✅           | 🟡           | ✅           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| Donation forms (embeddable) ✅                                                   | ✅           | 🟡           | ✅           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| Campaign tracking ✅                                                             | ✅           | ✅           | ✅           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| Pledge tracking ✅                                                               | ✅           | 🟡           | ❌           | 🟡           | ❌           | ✅           | ✅                      | ✅           |
| Donation receipts (auto-generated) ❓                                            | ✅           | 🟡           | ✅           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| Tax receipt generation ❓                                                        | ✅           | [4](#note-4) | ✅           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| Offline donation entry ✅                                                        | ✅           | 🟡           | 🟡           | ✅           | 🟡           | ✅           | ✅                      | ✅           |
| Fund allocation tracking (annual, monthly, endowment, critical solicitations) ✅ | ✅           | 🟡           | 🟡           | 🟡           | 🟡           | 🟡           | 🟡                      | 🟡           |
| Grant tracking 🟡                                                                | ✅           | 🟡           | ❌           | 🟡           | ❌           | ❌           | ❌                      | 🟡           |
| Donor tiers ❓                                                                   | 🟡           | ✅           | 🟡           | ✅           | 🟡           | ✅           | ✅                      | ✅           |
| Donor lifetime value calculation ✅                                              | 🟡           | 🟡           | 🟡           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| Donor segmentation ✅                                                            | ✅           | ✅           | 🟡           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| Matching gift workflow automation 🟡                                             | 🟡           | 🟡           | ❌           | 🟡           | 🟡           | 🟡           | 🟡                      | 🟡           |
| Planned giving / legacy gift tracking ✅                                         | 🟡           | 🟡           | ❌           | 🟡           | ❌           | 🟡           | 🟡                      | 🟡           |
| Grant deadline and reporting workflow reminders 🟡                               | 🟡           | ✅           | ❌           | 🟡           | ❌           | ❌           | ❌                      | 🟡           |
| Donation acknowledgement automation (beyond receipts) ✅                         | 🟡           | 🟡           | 🟡           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| Event creation ✅                                                                | ✅           | 🟡           | ✅           | ✅           | ✅           | 🟡           | ✅                      | ✅           |
| Event landing pages ❓                                                           | ✅           | [5](#note-5) | ✅           | 🟡           | ✅           | 🟡           | ✅                      | ✅           |
| Event ticketing ❓                                                               | ✅           | [5](#note-5) | ✅           | 🟡           | ✅           | 🟡           | ✅                      | ✅           |
| RSVP tracking ✅                                                                 | ✅           | 🟡           | ✅           | ✅           | ✅           | 🟡           | ✅                      | ✅           |
| Guest list management 🟡                                                         | ✅           | 🟡           | ✅           | ✅           | ✅           | 🟡           | ✅                      | ✅           |
| Waitlist management 🟡                                                           | 🟡           | ❌           | ❌           | ❌           | 🟡           | ❌           | 🟡                      | 🟡           |
| Event capacity limits ✅                                                         | ✅           | ❌           | ✅           | 🟡           | ✅           | 🟡           | ✅                      | ✅           |
| Event reminder automation ✅                                                     | ✅           | 🟡           | 🟡           | ✅           | ✅           | 🟡           | ✅                      | ✅           |
| Event feedback surveys ✅                                                        | 🟡           | 🟡           | 🟡           | 🟡           | 🟡           | 🟡           | 🟡                      | 🟡           |
| Event revenue tracking ✅                                                        | ✅           | 🟡           | ✅           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| Automated post-event follow-up workflows 🟡                                      | 🟡           | ✅           | 🟡           | 🟡           | 🟡           | 🟡           | 🟡                      | 🟡           |
| Event registration forms/workflows ✅                                            | ✅           | 🟡           | ✅           | ✅           | ✅           | 🟡           | ✅                      | ✅           |
| Automated event confirmations ✅                                                 | ✅           | 🟡           | ✅           | ✅           | ✅           | 🟡           | ✅                      | ✅           |
| Volunteer sign-up forms ✅                                                       | 🟡           | 🟡           | ✅           | 🟡           | 🟡           | ❌           | 🟡                      | 🟡           |
| Skills tracking 🟡                                                               | 🟡           | 🟡           | ❌           | ❌           | ❌           | ❌           | ❌                      | 🟡           |
| Membership renewal reminders ✅                                                  | ✅           | 🟡           | 🟡           | ✅           | 🟡           | 🟡           | 🟡                      | ✅           |
| Membership dues processing ✅                                                    | ✅           | 🟡           | ✅           | ✅           | 🟡           | 🟡           | 🟡                      | ✅           |
| Volunteer engagement history ✅                                                  | 🟡           | ✅           | ❌           | 🟡           | ❌           | ❌           | ❌                      | 🟡           |
| Volunteer categorization and tagging ✅                                          | ✅           | ✅           | ❌           | 🟡           | 🟡           | ❌           | 🟡                      | 🟡           |
| Automated volunteer communication (SMS + email) ✅                               | 🟡           | 🟡           | ❌           | ❌           | 🟡           | ❌           | 🟡                      | 🟡           |
| Auto-populate volunteer past participation ✅                                    | 🟡           | 🟡           | ❌           | 🟡           | ❌           | ❌           | ❌                      | 🟡           |
| Email campaign builder ✅                                                        | ✅           | ✅           | 🟡           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| Email templates ✅                                                               | ✅           | ✅           | 🟡           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| Automated welcome sequences 🟡                                                   | 🟡           | ✅           | ❌           | 🟡           | 🟡           | 🟡           | 🟡                      | 🟡           |
| Triggered emails ❓                                                              | 🟡           | ✅           | ❌           | 🟡           | 🟡           | 🟡           | 🟡                      | 🟡           |
| Email open tracking 🟡                                                           | ✅           | ✅           | 🟡           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| Click tracking 🟡                                                                | ✅           | ✅           | 🟡           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| Unsubscribe management 🟡                                                        | ✅           | ✅           | ✅           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| SMS marketing ✅                                                                 | 🟡           | 🟡           | ❌           | ❌           | ✅           | ❌           | ✅                      | 🟡           |
| Newsletter management ✅                                                         | ✅           | ✅           | 🟡           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| Revenue reporting ✅                                                             | ✅           | ✅           | ✅           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| Campaign ROI tracking ❓                                                         | 🟡           | 🟡           | [8](#note-8) | 🟡           | 🟡           | 🟡           | 🟡                      | 🟡           |
| Stripe integration 🟡                                                            | ✅           | ✅           | ❌           | ✅           | ✅           | 🟡           | ✅                      | 🟡           |
| PayPal integration 🟡                                                            | ✅           | 🟡           | ❌           | ✅           | 🟡           | 🟡           | 🟡                      | 🟡           |
| QuickBooks integration ✅                                                        | 🟡           | ✅           | [7](#note-7) | ✅           | 🟡           | 🟡           | 🟡                      | 🟡           |
| Cashapp/Venmo ✅                                                                 | [6](#note-6) | [6](#note-6) | [6](#note-6) | [6](#note-6) | [6](#note-6) | [6](#note-6) | [6](#note-6)            | [6](#note-6) |
| Embeddable forms/widgets flexibility ✅                                          | ✅           | 🟡           | ✅           | ✅           | ✅           | ✅           | ✅                      | ✅           |
| API/webhook depth for custom site workflows ✅                                   | ✅           | ✅           | 🟡           | 🟡           | 🟡           | 🟡           | 🟡                      | ✅           |
| CMS/plugin ecosystem support 🟡                                                  | ✅           | 🟡           | 🟡           | 🟡           | 🟡           | 🟡           | 🟡                      | 🟡           |
| QuickBooks class-tracking compatibility/workaround ✅                            | 🟡           | 🟡           | [7](#note-7) | 🟡           | 🟡           | 🟡           | 🟡                      | 🟡           |
| Alternate ways to collect money 🟡                                               | 🟡           | 🟡           | 🟡           | 🟡           | ✅           | 🟡           | ✅                      | 🟡           |
| Monthly platform cost fits target budget ✅                                      | ✅           | 🟡           | ✅           | ❓           | ✅           | ❓           | ❓                      | ❓           |
| Initial setup/config/deployment simplicity ✅                                    | ❌           | ✅           | ✅           | 🟡           | ✅           | ✅           | 🟡                      | 🟡           |
| Low ongoing admin overhead ✅                                                    | [1](#note-1) | ✅           | ✅           | ✅           | ✅           | ✅           | ✅                      | [9](#note-9) |
| New-user onboarding usability ✅                                                 | [2](#note-2) | ✅           | ✅           | ✅           | ✅           | ✅           | ✅                      | [9](#note-9) |
| Score (✅=3, 🟡=2, [#]=1, ❓=0, ❌=0)                                            | 194          | 175          | 130          | 181          | 175          | 158          | 179                     | 187          |

## Notes

### Note 1: CiviCRM Admin Overhead

<a id="note-1"></a>
CiviCRM usually needs more initial setup and process definition than turnkey SaaS tools, but ongoing admin can be manageable for Temple Foundation if workflows are documented and ownership is clear.

### Note 2: CiviCRM Onboarding Usability

<a id="note-2"></a>
CiviCRM has a learning curve for new users, but role-specific SOPs and short task checklists can make day-to-day use approachable for non-technical staff.

### Note 3: Pipedrive Constituent Portal

<a id="note-3"></a>
Pipedrive does not include a nonprofit-style constituent self-service portal natively, but this can be delivered through an external portal/form stack with sync back to Pipedrive.

### Note 4: Pipedrive Tax Receipt Generation

<a id="note-4"></a>
Pipedrive is not tax-receipt-native for donations; organizations typically generate compliant receipts through integrated fundraising/accounting tools and store references in Pipedrive.

### Note 5: Pipedrive Event Stack

<a id="note-5"></a>
Pipedrive can integrate with event tools for contact/deal sync and registration status updates, but waitlists and strict capacity enforcement should remain in the event platform itself (with summary status synced back to Pipedrive via native connectors, Zapier/Make, or API).

### Note 6: Cash App/Venmo In CRM Context

<a id="note-6"></a>
Cash App and Venmo are generally collected through external payment tools and then recorded/synced into the CRM; this is feasible operationally but not a native in-CRM payment rail.

### Note 7: Zeffy QuickBooks Integration Path

<a id="note-7"></a>
Zeffy documents QuickBooks connectivity via Zapier (Zeffy trigger -> Zapier -> QuickBooks action), which supports an integration path for accounting sync and related mapping workarounds, but not a native direct QuickBooks connector inside Zeffy.

### Note 8: Zeffy Campaign ROI Tracking Path

<a id="note-8"></a>
Zeffy documents integrations via Zapier (including Google Sheets and other tools) and data export/reporting; campaign ROI tracking can be implemented in an external analytics/reporting tool with Zeffy data synced/exported through that path.

### Note 9: Neon Onboarding and Overhead Context

<a id="note-9"></a>
Neon CRM onboarding and ongoing administration are generally steeper than turnkey fundraising-first tools, but typically easier and less admin-intensive than CiviCRM.

## Evaluation Rules

- `✅` Use when the feature is natively present in the CRM.
- `[#]` Use when the feature is achievable only by integrating a separate external product/platform. The note must name the specific product(s) This should not be used when the externally-available feature can't integrate into the \[core\] product.
- `🟡` Use when the feature is achievable inside the CRM via configuration, workflow setup, or native add-ons/extensions, without requiring a separate full external product.
- `❓` Use when the criterion definitely has a value but the value is not yet confirmed (for example: monthly platform cost). Do not use `❓` as a default for undocumented features.
- `❌` Use when the feature is not available and not reasonably integratable.
- Leave a cell blank when that CRM/criterion pair has not been evaluated yet.
