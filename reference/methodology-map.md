# Methodology Map

This is the canonical mapping for setup, resume, status, validation, and the final index. Topic IDs are stable; `phases/` files describe how to explore them. Every template-based output uses the same filename as its template. Template files follow `xx.yy_methodology_artifact.md`: `xx` is the interview phase, `yy` is the artifact order within that phase, and phase `99` is reserved for the final index.

| ID | Methodology | Generated files and template files | Script | Topics |
|---:|---|---|---|---:|
| 0 | Initial Discovery & Project Briefing | 00.01_initial_discovery_project_briefing.md | 00_discovery | 7 |
| 1 | Business Model Canvas (BMC) | 01.01_bmc_business_canvas.md | 01_bmc | 7 |
| 2 | Discovery Framework (5W1H) | 02.01_5w1h_discovery.md | 02_5w1h | 6 |
| 3 | Scope Prioritization (MoSCoW) | 03.01_moscow_prioritization.md | 03_moscow | 4 |
| 4 | Epic Breakdown (User Request) | 04.01_user_request_epic_breakdown.md | 04_user_request | 5 |
| 5 | Domain-Driven Design (DDD) | 05.01_ddd_domain_events.md; 05.02_ddd_strategic_design.md; 05.03_ddd_solution_proposal.md; 05.04_ddd_implementation_tasks.md | 05_ddd | 18 |
| 6 | Command Query Responsibility Segregation (CQRS) | 06.01_cqrs_schema.md; 06.02_cqrs_specs.md; 06.03_cqrs_multi_tenancy.md | 06_cqrs | 10 |
| 7 | Software Design Document (SDD) & Clean Architecture | 07.01_sdd_clean_architecture.md; 07.02_sdd_api_gateway.md | 07_sdd | 7 |
| 8 | Event-Driven Development (EDD) | 08.01_edd_logic_flows.md | 08_edd | 7 |
| 9 | User Interface / User Experience (UI/UX) | 09.01_ui_ux_atomic_design.md; 09.02_ui_ux_a11y_tests.md | 09_ui_ux | 7 |
| 10 | Behavior-Driven Development (BDD) | 10.01_bdd_scenarios.md | 10_bdd | 3 |
| 11 | Test-Driven Development (TDD) | 11.01_tdd_test_strategy.md; 11.02_tdd_advanced_metrics.md | 11_tdd | 6 |
| 12 | Legal & Compliance | 12.01_legal_compliance.md; 12.02_legal_disaster_recovery.md | 12_legal | 4 |
| 13 | Application Security (AppSec) Strategy [Automated] | 94.01_appsec_strategy.md | 13_appsec_strategy | 1 |
| 14 | Threat Model (STRIDE) [Automated] | 96.01_threat_model.md | 14_threat_model | 1 |
| 15 | Request for Comments (RFC) [Automated] | 97.01_rfc.md | 15_rfc | 1 |
| 16 | Developer Onboarding [Automated] | 95.01_developer_onboarding.md | 16_developer_onboarding | 1 |
| 17 | Executive Summary & Pitch | 98.01_executive_summary_business_view.md; 98.02_marketing_pitch_deck.md; 98.03_seo_metadata_plan.md | 17_executive_pitch | 5 |

The tracking state is stored in [00.00_tracking_changelog.md](00.00_tracking_changelog.md). The final index is [README.md](README.md). [00_validation_report.md](00_validation_report.md) is a validation-only report based on [Templates/00_validation_report.md](Templates/00_validation_report.md). The full selection contains 100 topics. Phase 0 is always selected; IDs 1–17 are selectable.