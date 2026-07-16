# Developer Onboarding

**Methodology:** Developer Onboarding [Automated]
**Topics:** 1
**Outputs:** [95.01_developer_onboarding.md](95.01_developer_onboarding.md)
**Dependencies:** Should be executed after DDD, CQRS, SDD, EDD, and TDD phases.

## Goal

To automatically generate a technical Onboarding Guide designed for new engineers, pulling the most relevant technical constraints and definitions from the interview without requiring user intervention.

## Topics

### `onboarding.generate`

Do not ask any questions in this phase. The Onboarding Guide generation is an autonomous synthesis phase.
Read the contents of the technical phases (DDD, CQRS, SDD, EDD, TDD). Filter out the business fluff and cross-reference the core technical rules to automatically draft a comprehensive Developer Onboarding guide following the template structure. Present this complete draft directly to the user for validation and final approval.

## Completion

When the `onboarding.generate` topic draft is approved by the user, read [Templates/95.01_developer_onboarding.md](Templates/95.01_developer_onboarding.md) and generate [95.01_developer_onboarding.md](95.01_developer_onboarding.md).
