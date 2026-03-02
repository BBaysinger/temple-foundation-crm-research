# Temple Foundation CRM Requirements (Draft v1)

This is a likely-needs baseline derived from current project context. It should be validated with stakeholders before final scoring.

## Assumptions Used

- Early-stage nonprofit with limited admin capacity
- Monthly software budget target around $50-$100 (excluding payment processing)
- Immediate focus on donor management, events, and communication
- Website platform is not finalized yet

## Core Requirements (Likely Required Now)

| ID | Priority | Requirement | Validation Check |
|---|---|---|---|
| R-01 | Must | Centralized contact database for donors, participants, and volunteers | Create/search/edit contacts; import CSV without data loss |
| R-02 | Must | One-time and recurring donation processing | Complete both donation types in sandbox/live test |
| R-03 | Must | Event registration and attendance tracking | Publish event, collect signups, and mark attendance |
| R-04 | Must | Email segmentation and basic campaign sending | Build at least 2 segments and send test campaigns |
| R-05 | Must | Total monthly platform cost aligns with budget target | Quote includes base plan + required modules |
| R-06 | Must | Low ongoing admin overhead for a small team | New user can run core workflows after onboarding |
| R-07 | Must | Basic reporting for donations, events, and engagement | Generate standard reports without custom development |
| R-08 | Must | Website integration path (embed, plugin, or API) | Donation and event flows can be embedded or connected |
| R-09 | Should | Role-based access for at least admin and staff users | Verify permission differences in user roles |
| R-10 | Should | Receipt and acknowledgement automation | Auto-send donation receipts and event confirmations |
| R-11 | Should | Integration with payment processor(s) and accounting export | Confirm Stripe/PayPal support and finance export format |
| R-12 | Should | Data import/export portability | Export full records in common formats (CSV/API) |

## Growth Requirements (Likely Needed Later)

| ID | Priority | Requirement | Validation Check |
|---|---|---|---|
| G-01 | Later | Membership management workflows | Support levels, renewals, and reminders |
| G-02 | Later | Volunteer scheduling and hours tracking | Create shifts and produce hours report |
| G-03 | Later | Workflow automation for follow-up and stewardship | Trigger task or message from key actions |
| G-04 | Later | Enhanced donor analytics (retention, LTV, pipeline) | Retention/LTV and donor-stage reporting available |
| G-05 | Later | Multi-user scaling with stronger permissions/audit logs | Activity logs and advanced permissions available |

## Out of Scope for Initial Selection

- Enterprise-grade custom architecture
- Heavy consulting-dependent implementation
- Deep feature sets that require dedicated full-time CRM administration