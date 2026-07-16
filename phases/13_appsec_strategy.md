# AppSec Strategy

**Methodology:** AppSec Strategy [Automated]
**Topics:** 1
**Outputs:** [94.01_appsec_strategy.md](94.01_appsec_strategy.md)
**Dependencies:** Should be executed after DDD, CQRS, SDD, EDD, UI/UX, BDD, and TDD phases.

## Goal

To automatically generate a consolidated Application Security (AppSec) strategy document based on the security constraints mapped across all previous technical phases without requiring user intervention.

## Topics

### `appsec.generate`

Do not ask any questions in this phase. The AppSec generation is an autonomous synthesis phase.
Read the contents of all completed technical phases (especially DDD, CQRS, SDD, EDD, UI/UX, BDD, and TDD). Extract the security decisions embedded in those phases (IAM, Encryption, Secrets, Payload Security, Frontend Defenses, Abuse Cases, and DevSecOps) to automatically draft a comprehensive AppSec Strategy document following the template structure. Present this complete draft directly to the user for validation and final approval.

## Completion

When the `appsec.generate` topic draft is approved by the user, read [Templates/94.01_appsec_strategy.md](Templates/94.01_appsec_strategy.md) and generate [94.01_appsec_strategy.md](94.01_appsec_strategy.md).
