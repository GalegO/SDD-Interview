# Event-Driven Development

## Template

Read [Templates/08.01_edd_logic_flows.md](Templates/08.01_edd_logic_flows.md) before generating [08.01_edd_logic_flows.md](08.01_edd_logic_flows.md).

## Required topics

Cover `edd.sync_flow`, `edd.async_flows`, `edd.messaging_strategy`, `edd.payload_security`, `edd.resilience_idempotency`, `edd.event_serialization`, `edd.caching_strategy`, and `edd.traceability`. Use diagrams for flows when useful.

> **Validation Note:** If [05.01_ddd_domain_events.md](05.01_ddd_domain_events.md) exists in the current interview directory (`destination_path`), actively cross-reference its answers. The *Domain Events* raised in the DDD phase MUST be the exact triggers and messages designed in the EDD async flows. Ensure no new arbitrary events are created here without being added to the DDD model first. Also, if [05.02_ddd_strategic_design.md](05.02_ddd_strategic_design.md) exists, the messaging strategy MUST respect the Context Mapping Relationship Types (e.g., implementing an Anti-Corruption Layer for event translation when crossing context boundaries).

