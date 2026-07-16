# Legal & Compliance

## Template

Read [Templates/12.01_legal_compliance.md](Templates/12.01_legal_compliance.md) before generating [12.01_legal_compliance.md](12.01_legal_compliance.md).

## Required topics

Cover `legal.privacy`, `legal.contractual_tax`, and `legal.fallback_decision`. Do not give legal advice; document risks and require specialist review where appropriate.

### `legal.disaster_recovery_opt_in` (Bonus)

If the project is mission-critical or handles highly sensitive data, present a grounded recommendation to define Continuity and Disaster Tolerance (RTO/RPO). Explicitly ask the user for the final decision (Yes/No). If Yes, ask the necessary questions and generate `12.02_legal_disaster_recovery.md` based on [Templates/12.02_legal_disaster_recovery.md](Templates/12.02_legal_disaster_recovery.md).

> **Validation Note:** If [06.01_cqrs_schema.md](06.01_cqrs_schema.md) exists in the current interview directory, cross-reference its database fields. The Privacy Opinion must actively check if the defined tables and columns contain sensitive user data (PII like SSN, CPF, email, or financial fields) and verify if mitigation/masking policies were documented. Additionally, if [07.01_sdd_clean_architecture.md](07.01_sdd_clean_architecture.md) exists, ensure the Cross-Cutting Concerns (security, logs, telemetry) adequately address the compliance requirements for auditing and access control.


