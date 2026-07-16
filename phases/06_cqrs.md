# CQRS

## 09_schema

Read [Templates/06.01_cqrs_schema.md](Templates/06.01_cqrs_schema.md) before generating [06.01_cqrs_schema.md](06.01_cqrs_schema.md).

Cover `cqrs.read_write_imbalance`, `cqrs.eventual_consistency`, `cqrs.tables_modifications`, `cqrs.data_encryption`, `cqrs.relationships`, `cqrs.indexes`, and `cqrs.schema_migrations`. The first two establish whether CQRS is appropriate.

## 10_specs

Read [Templates/06.02_cqrs_specs.md](Templates/06.02_cqrs_specs.md) before generating [06.02_cqrs_specs.md](06.02_cqrs_specs.md).

Cover `cqrs.business_rules`, `cqrs.api_contracts`, and `cqrs.error_codes`. Generate the schema before the specifications.

### `cqrs.multi_tenancy_opt_in` (Bonus)

Analyze the project context (especially from Phase 00 or BMC). If the project appears to be a B2B SaaS or requires data isolation, present a grounded recommendation to the user on whether they should define a Multi-Tenancy strategy (e.g., isolating tenants via column, schema, or physical DB). Explicitly ask the user for the final decision (Yes/No). If Yes, ask the necessary questions and generate `06.03_cqrs_multi_tenancy.md` based on [Templates/06.03_cqrs_multi_tenancy.md](Templates/06.03_cqrs_multi_tenancy.md).

> **Validation Note:** If [05.02_ddd_strategic_design.md](05.02_ddd_strategic_design.md) (or other DDD outputs) exist in the current interview directory (`destination_path`), actively cross-reference them. The *Entities* and *Aggregates* defined in the DDD phase form the exact base for the *Commands* and *Queries* here. Validate and ensure that no command is created for an entity that does not exist in the DDD model.

