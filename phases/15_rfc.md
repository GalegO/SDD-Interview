# Request for Comments (RFC)

**Methodology:** Request for Comments (RFC)
**Topics:** 1
**Outputs:** [97.01_rfc.md](97.01_rfc.md)
**Dependencies:** Should be executed after the core technical methodologies (DDD, CQRS, SDD, EDD) are complete.

## Goal

To automatically generate a standard Request for Comments (RFC) document that synthesizes the technical and architectural decisions made during the interview, facilitating review and alignment with engineering teams.

## Topics

### `rfc.generate`

Do not ask any questions in this phase. The RFC generation is an autonomous synthesis phase.
Read the contents of all completed technical and business phases in the destination path (particularly the Initial Discovery, Epic Breakdown, DDD Bounded Contexts, CQRS Strategies, and SDD Clean Architecture). Cross-reference the collected data to automatically draft a comprehensive RFC following the provided structure. Present this complete draft directly to the user for validation and final approval.

## Completion

When the `rfc.generate` topic draft is approved by the user, read [Templates/97.01_rfc.md](Templates/97.01_rfc.md) and generate [97.01_rfc.md](97.01_rfc.md).
