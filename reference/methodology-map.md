# Methodology Map

This is the canonical mapping for setup, resume, status, validation, and the final index. Topic IDs are stable; `phases/` files describe how to explore them. Every template-based output uses the same filename as its template. Template files follow `xx.yy_methodology_artifact.md`: `xx` is the interview phase, `yy` is the artifact order within that phase, and phase `99` is reserved for the final index.

| ID | Methodology | Generated files and template files | Script | Topics |
|---:|---|---|---|---:|
| 0 | Initial Discovery | 00.01_initial_discovery_project_briefing.md | 00_discovery | 7 |
| 1 | Business Model Canvas | 01.01_bmc_business_canvas.md | 01_bmc | 7 |
| 2 | Discovery (5W1H) | 02.01_5w1h_discovery.md | 02_5w1h | 6 |
| 3 | Prioritization (MoSCoW) | 03.01_moscow_prioritization.md | 03_moscow | 4 |
| 4 | Epic Breakdown (User Request) | 04.01_user_request_epic_breakdown.md | 04_user_request | 5 |
| 5 | Domain-Driven Design | 05.01_ddd_domain_events.md; 05.02_ddd_strategic_design.md; 05.03_ddd_solution_proposal.md; 05.04_ddd_implementation_tasks.md | 05_ddd | 16 |
| 6 | CQRS | 06.01_cqrs_schema.md; 06.02_cqrs_specs.md | 06_cqrs | 8 |
| 7 | SDD & Clean Architecture | 07.01_sdd_clean_architecture.md | 07_sdd | 5 |
| 8 | Event-Driven Development | 08.01_edd_logic_flows.md | 08_edd | 4 |
| 9 | UI/UX (Atomic Design) | 09.01_ui_ux_atomic_design.md | 09_ui_ux | 6 |
| 10 | Behavior-Driven Development | 10.01_bdd_scenarios.md | 10_bdd | 3 |
| 11 | Test-Driven Development | 11.01_tdd_test_strategy.md | 11_tdd | 5 |
| 12 | Legal & Compliance | 12.01_legal_compliance.md | 12_legal | 3 |
| 13 | Executive Summary & Pitch | 98.01_executive_summary_business_view.md; 98.02_marketing_pitch_deck.md | 13_executive_pitch | 4 |

The tracking state is stored in [00.00_tracking_changelog.md](00.00_tracking_changelog.md). The final index is [99.01_index_readme.md](99.01_index_readme.md). [00_validation_report.md](00_validation_report.md) is a validation-only report based on [Templates/00_validation_report.md](Templates/00_validation_report.md). The full selection contains 83 topics. Phase 0 is always selected; IDs 1–13 are selectable.