# Threat Model (STRIDE)

**Methodology:** Threat Model [Automated]
**Topics:** 1
**Outputs:** [96.01_threat_model.md](96.01_threat_model.md)
**Dependencies:** Should be executed after SDD, EDD, and Legal phases.

## Goal

To automatically generate a STRIDE Threat Model matrix based on the architectural decisions made in previous phases without requiring user intervention.

## Topics

### `threat.generate`

Do not ask any questions in this phase. The Threat Model generation is an autonomous synthesis phase.
Read the contents of all completed technical phases (especially SDD Clean Architecture, EDD Logic Flows, and Legal & Compliance). Cross-reference the collected data to automatically draft a comprehensive STRIDE matrix and security assessment following the template structure. Present this complete draft directly to the user for validation and final approval.

## Completion

When the `threat.generate` topic draft is approved by the user, read [Templates/96.01_threat_model.md](Templates/96.01_threat_model.md) and generate [96.01_threat_model.md](96.01_threat_model.md).
