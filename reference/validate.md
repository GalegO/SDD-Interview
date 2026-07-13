# Validation

`/interview validate <path>` reads [00.00_tracking_changelog.md](00.00_tracking_changelog.md), the map, templates, and generated outputs, then reads [Templates/00_validation_report.md](Templates/00_validation_report.md) and writes [00_validation_report.md](00_validation_report.md) in the interview folder. Every template-based output must have the exact same filename as its source template. It checks: parseable `interview_state`; expected documents for selected and completed methodologies; populated template sections without placeholders; OKF consistency; the final index containing only Phase 0 and selected methodologies; light cross-methodology consistency; and apparent PII or credentials.

Report each criterion as `PASS`, `WARNING`, or `FAIL`, cite affected files, and conclude with an overall summary and next action. A warning does not invalidate an interview; a failure does.

**Smart Validation Rule (Placeholders vs. Active Phases):**
When checking for populated template sections without placeholders (such as empty items, brackets, or literal template comments), the validator must cross-reference `completed_methodologies` in [00.00_tracking_changelog.md](00.00_tracking_changelog.md):
- If the methodology corresponding to a file is marked as complete, any remaining placeholders trigger a `FAIL`.
- If the methodology is currently active (in progress) or selected but not yet completed, any remaining placeholders in its files must only trigger a `WARNING` or a `PASS` (marked as "in progress"), preventing a false overall validation failure.

