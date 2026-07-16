# SDD & Clean Architecture

## Template

Read [Templates/07.01_sdd_clean_architecture.md](Templates/07.01_sdd_clean_architecture.md) before generating [07.01_sdd_clean_architecture.md](07.01_sdd_clean_architecture.md).

## Required topics

Cover `sdd.core_isolation`, `sdd.ports_adapters`, `sdd.component_topology`, `sdd.c4_diagram`, `sdd.boundaries_violations`, `sdd.secrets_management`, and `sdd.cross_cutting_concerns`. Use a Mermaid C4-style diagram when it clarifies the result.

### `sdd.api_gateway_opt_in` (Bonus)
If the project exposes synchronous endpoints to the internet or uses a microservices architecture, present a grounded recommendation to define an API Gateway & Edge Security strategy. Explicitly ask the user for the final decision (Yes/No). If Yes, ask the necessary questions and generate `07.02_sdd_api_gateway.md` based on [Templates/07.02_sdd_api_gateway.md](Templates/07.02_sdd_api_gateway.md).

> **Validation Note:** If [00.01_initial_discovery_project_briefing.md](00.01_initial_discovery_project_briefing.md) exists in the current interview directory (`destination_path`), actively cross-reference its answers for Platform and Tech Stack. Use those definitions to proactively suggest the Infrastructure layer, Adapters, and specific frameworks in your SDD questions. Additionally, if [05.02_ddd_strategic_design.md](05.02_ddd_strategic_design.md) exists, use the Domain Types Classification to ensure that Core Domains are strictly isolated at the center of the architecture, while Generic and Supporting Domains are handled via Adapters.

