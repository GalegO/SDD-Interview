# Test-Driven Development

## Template

Read [Templates/11.01_tdd_test_strategy.md](Templates/11.01_tdd_test_strategy.md) before generating [11.01_tdd_test_strategy.md](11.01_tdd_test_strategy.md).

## Required topics

Cover `tdd.backend_integration`, `tdd.frontend_ui`, `tdd.database`, `tdd.native_performance`, `tdd.edge_compliance`, and `tdd.devsecops_pipeline`.

### `tdd.advanced_metrics_opt_in` (Bonus)

If the project indicates high-performance or mission-critical requirements, present a grounded recommendation to define Mutation Testing and Latency SLAs. Explicitly ask the user for the final decision (Yes/No). If Yes, ask the necessary questions and generate `11.02_tdd_advanced_metrics.md` based on [Templates/11.02_tdd_advanced_metrics.md](Templates/11.02_tdd_advanced_metrics.md).

> **Validation Note:** If [04.01_user_request_epic_breakdown.md](04.01_user_request_epic_breakdown.md) exists in the current interview directory (`destination_path`), actively cross-reference its answers. The *Acceptance Criteria* defined in the Epic Breakdown form the exact basis for the unit and integration tests proposed here. Proactively suggest tests that explicitly validate those criteria. Additionally, if [10.01_bdd_scenarios.md](10.01_bdd_scenarios.md) exists in the directory, cross-reference its Given/When/Then scenarios and concurrency specifications to design automated tests that directly validate those behavior flows. If [05.02_ddd_strategic_design.md](05.02_ddd_strategic_design.md) exists, the testing strategy should focus its highest coverage and most rigorous integration tests on Bounded Contexts classified as Core Domains. Also, if [08.01_edd_logic_flows.md](08.01_edd_logic_flows.md) exists, ensure integration tests explicitly cover Resilience and Idempotency behaviors (e.g., duplicate message handling and DLQ routing).

