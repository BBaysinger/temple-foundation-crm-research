# CRM Exit / Migration-Out Notes

This note captures a preliminary assessment of how difficult it would be to migrate away from each shortlisted CRM later.

## Short Answer

Almost none of these platforms are designed to make leaving easy.

- Some are tolerable to migrate out of.
- Very few actively facilitate exit as a product strength.
- The difference is usually between `can export some data` and `can preserve most system fidelity with reasonable effort`.

That second standard is what makes migration painful.

## Signals Used

This assessment is based primarily on the following criteria already present in the evaluation work:

- `Data migration complexity`
- `Backup/export resilience (full-fidelity exit path)`
- `API/webhook depth for custom site workflows`
- `Record model flexibility for nonprofit edge cases`
- `Scalability switch risk`

## Preliminary Migration-Out Assessment

| CRM option              | Migration-out posture                                     | Practical read                                                                                                                                                                                                  |
| ----------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CiviCRM                 | Best exit posture in current shortlist                    | Clear outlier on exit flexibility. Strongest API/export posture here, and the only option in this group with forkable source code. Still not trivial to leave, but the least structurally hostile to migration. |
| Pipedrive               | Usually manageable, but not especially migration-friendly | Likely workable through export plus cleanup and remapping. Better than the most locked-in paths, but not a platform that treats clean exit as a core product strength.                                          |
| DonorView               | Usually manageable, but not especially migration-friendly | Feels more like `you can get data out with work` than `the platform helps you leave cleanly`. Moderate exit posture.                                                                                            |
| Givebutter              | Usually manageable, but not especially migration-friendly | Public fundraising can move, but preserving history, mappings, and operational logic is still likely to require significant cleanup.                                                                            |
| Bloomerang              | Usually manageable, but not especially migration-friendly | Likely offers a practical export path, but not a full-fidelity low-friction exit path.                                                                                                                          |
| Neon CRM                | Usually manageable, but not especially migration-friendly | Stronger than many SaaS options in breadth, but still more `export and rebuild` than `migrate cleanly with low loss`.                                                                                           |
| Zeffy                   | Most likely to be painful                                 | Weakest exit posture in the current set. Strong for quick launch, but not attractive from a long-term migration-out perspective.                                                                                |
| Givebutter + Bloomerang | Most likely to be painful                                 | Even if each tool is workable on its own, leaving a multi-system stack is harder because truth is split across system boundaries and integration logic.                                                         |

## What Usually Makes Migration Painful

The main issue is not raw export alone. The painful parts are usually:

- preserving relationships between records
- preserving attachments and historical activity
- recreating automations and workflows
- reconstructing website integrations and form flows
- preserving accounting mappings, campaign attribution, and operational context
- separating clean data from duplicate, partial, or integration-generated records

Many platforms support CSV export. Far fewer support a clean, full-fidelity exit.

## Practical Grouping

### Best If Avoiding Lock-In Matters

- `CiviCRM`

### Usually Tolerable, But Not Exit-Friendly

- `Pipedrive`
- `DonorView`
- `Givebutter`
- `Bloomerang`
- `Neon CRM`

### Highest Exit Pain Risk

- `Zeffy`
- `Givebutter + Bloomerang`

## Practical Takeaway

If avoiding future lock-in matters materially, `CiviCRM` is the strongest option in the current shortlist.

Most of the SaaS options appear to offer an export path, not a clean exit path.

Multi-system stacks are especially important to watch: even when they are strong operationally, they are often harder to unwind later.

## Next Useful Step

If needed, this can be expanded into a more formal comparison table with columns such as:

- raw export quality
- API completeness
- relationship fidelity on exit
- attachment/history portability
- automation portability
- overall exit pain
