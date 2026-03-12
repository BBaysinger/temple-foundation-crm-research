# CiviCRM Solo Implementation Timeline (Independent Estimate)

This estimate is independent and does **not** rely on prior timeline docs in this repo.

## Scope and Assumptions

- Solo implementer (you): implementation, QA, documentation, training prep, and go-live support.
- Existing hosting/domain are available.
- Scope is CiviCRM with web forms and integrations aligned to `evaluation-matrix.md`.
- Estimates are **calendar time** ranges, not pure engineering hours.
- `Non-widget implementation path (API-first/headless)` is treated as an optional maybe add-on.

## Phase Estimates (Without AI vs With AI)

| Phase                                                                                                                  |        Without AI |           With AI |
| ---------------------------------------------------------------------------------------------------------------------- | ----------------: | ----------------: |
| 1. Civi running (no form setup)                                                                                        | 3-7 business days | 2-5 business days |
| 2. Basic features after setup (forms, recurring + one-time donations, memberships, tickets/events, volunteer baseline) |        8-14 weeks |        6-11 weeks |
| 3. Low-hanging required features (from grid)                                                                           |        +4-7 weeks |        +3-5 weeks |
| 4. Medium-effort required features                                                                                     |       +6-10 weeks |        +4-8 weeks |
| 5. Hard/hardest required features                                                                                      |      +10-18 weeks |       +7-14 weeks |

## Cumulative Timeline (From Zero)

- Without AI: **29-50 weeks** (~7-12 months)
- With AI: **20-39 weeks** (~5-9 months)

These cumulative ranges exclude optional headless/forking add-ons.

Optional add-on impact (if selected):

- Headless/API-first implementation: **+3-6 weeks**
- Forking/extensibility approach: **context-dependent** (can reduce custom build time for some features)

## Where AI Helps Most

- Configuration-heavy setup and repetitive form/report/template work.
- Data mapping drafts and checklist/test artifact generation.
- Integration scaffolding and first-pass workflow automation logic.

## Where AI Helps Less

- Business-rule decisions and stakeholder sign-off.
- Final UAT confidence and production cutover decisions.
- Compliance and policy interpretation for edge cases.

## Hardest Items (Most Likely in Phase 5)

1. QuickBooks integration + accounting linkage + class-tracking workaround.
2. Constituent self-service portal with secure auth + profile/preferences sync.
3. Reliable volunteer auto-history and coordination automation.
4. Multi-channel automation (email/SMS) with compliance-safe logic and auditability.

## Optional Very-Hard Add-Ons (If Selected)

1. API-first/non-widget flows with robust retry/monitoring.
2. Fork/extension program setup for in-house feature development.
