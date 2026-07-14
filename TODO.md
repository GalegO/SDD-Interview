# TODO: Advanced Architectural Methodologies and Topics (Enterprise/Mission-Critical)

This file consolidates the list of improvements and advanced topics that can be added to the Skill's methodologies in the future to raise the level of generated documentation for large-scale projects.

## 1. Domain-Driven Design (DDD)
- [ ] **Domain Types Classification:**
  - Explicitly map whether each Bounded Context is a *Core Domain* (heart of the business/custom), *Supporting Domain* (auxiliary/custom), or *Generic Domain* (generic/off-the-shelf/SaaS).
- [ ] **Context Mapping Relationship Types:**
  - Define and detail integration patterns for communication between contexts (e.g., *Shared Kernel*, *Customer-Supplier*, *Conformist*, *Anti-Corruption Layer (ACL)*).

## 2. CQRS & Data Modeling
- [ ] **Schema Migrations Strategy:**
  - Detail the strategy for structural updates and physical database migration (e.g., safe migrations, backward compatibility, and rollback/zero-downtime plans).

## 3. SDD & Clean Architecture
- [ ] **Cross-Cutting Concerns:**
  - Add sections to standardize the behavior of security/authentication, logs/auditing, and metrics/observability (telemetry) across the physical layers of the application.

## 4. EDD (Event-Driven Design)
- [ ] **Resilience and Idempotency:**
  - Define handling for *at-least-once* message delivery, idempotency control in consumers, retry loops, and failure management via *Dead Letter Queues (DLQ)*.
- [ ] **Event Serialization and Contracts:**
  - Specify transmission formats and serialization protocols for events (e.g., Avro, Protobuf, JSON Schema) and their respective contract versioning to avoid breakages.

## 5. SEO & Marketing (Phase 13 - Executive Summary & Pitch)
- [ ] **SEO & Metadata Plan:**
  - Create an optional automatic bonus artifact (e.g., `98.03_seo_metadata_plan.md`) generated in Phase 13. It will define the product's indexability strategy, mapping meta tags (Title, Description, OpenGraph), structured data (JSON-LD/Schema.org), semantic hierarchy of headings (H1-H3), and crawling directives (sitemaps, robots.txt) if the target platform is geared towards the public web.

## 6. Distributed Observability (Phase 08 - EDD)
- [ ] **Traceability and Correlation IDs:**
  - Add distributed tracing design in asynchronous logical flows, specifying how Correlation IDs will be propagated between microservices/workers for auditing and debugging.

## 7. Future Ideas / Possibilities (Maybe)
> [!NOTE]
> The topics below descend to a very high level of detail and technical granularity. They should be considered with caution ("Icebox" Backlog) to avoid overloading or restricting the Skill's high-level planning flow.

- [ ] **Multi-Tenancy Strategy (CQRS/Data):** Map whether the solution will isolate tenants via a column (ID), segregated logical schemas, or independent physical databases.
- [ ] **Mutation Testing and Latency SLAs (TDD):** Add conceptual guidelines to test the actual effectiveness of unit test asserts and rules to fail the suite if throughput/latency thresholds are exceeded.
- [ ] **Automated A11y Tests (TDD/UI):** Integrate automatic accessibility checks (e.g., axe-core) into the frontend test suite for legal compliance (WCAG).
- [ ] **Continuity and Disaster Tolerance (SDD/Legal):** Plan and document RTO (Recovery Time Objective) and RPO (Recovery Point Objective) goals for infrastructure and database.

## 8. Token and Context Usage Optimization (Prompt)
- [x] **Initial Setup Logic Extraction (Lazy-Loading):**
  - Move the Setup and Commands instructions (the initial lines of SKILL.md that are long and detailed) to a separate file (e.g., `reference/setup-workflow.md`). Leave in the main prompt only the directive to read this file if the user starts with `/interview new`, removing this overhead from the main question loop.
