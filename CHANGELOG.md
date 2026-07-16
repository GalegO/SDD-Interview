# Changelog

All notable changes to the interview skill are documented in this file.

## Version 2.2

### Added

- **Guided Opt-In Patterns (Advanced Topics):** Added an intelligent opt-in strategy for mission-critical architecture topics to avoid overloading simple projects. The AI now proactively suggests the generation of advanced bonus artifacts based on the project profile, but explicitly waits for user approval before proceeding.
- **Multi-Tenancy Strategy:** Added optional `06.03_cqrs_multi_tenancy.md` generation to Phase 06 (CQRS) for B2B SaaS data isolation.
- **API Gateway & Edge Security:** Added optional `07.02_sdd_api_gateway.md` generation to Phase 07 (SDD) to map Edge routing, rate limiting, and WAF.
- **Automated A11y Tests:** Added optional `09.02_ui_ux_a11y_tests.md` generation to Phase 09 (UI/UX) to map WCAG compliance for public frontends.
- **Advanced TDD Metrics:** Added optional `11.02_tdd_advanced_metrics.md` generation to Phase 11 (TDD) for Mutation Testing and Latency SLAs on high-performance APIs.
- **Disaster Recovery:** Added optional `12.02_legal_disaster_recovery.md` generation to Phase 12 (Legal) to document RTO/RPO for mission-critical systems.
- **Automated AppSec Strategy:** Added a new Methodology (Phase 13) that autonomously compiles security answers from previous phases into a unified CyberSec document (`94.01_appsec_strategy.md`).
- **Security Pulverization (Security by Design):** Injected security questions across existing phases: Identity and Access Management (IAM) in Domain-Driven Design (DDD), Data Encryption in Command Query Responsibility Segregation (CQRS), Secrets Management in Software Design Document (SDD), Payload Protection in Event-Driven Development (EDD), Frontend Defenses in UI/UX, Abuse Cases in Behavior-Driven Development (BDD), and Pipeline Scans in Test-Driven Development (TDD).
- **Automated RFC Draft:** Added a new Methodology (Phase 15) that autonomously generates a standard Request for Comments (RFC) architecture draft based on the technical decisions of the interview, saving engineering hours.
- **Threat Model (STRIDE):** Added a new Methodology (Phase 14) that autonomously generates a security assessment matrix based on SDD, EDD, and Legal inputs.
- **Developer Onboarding:** Added a new Methodology (Phase 16) that autonomously generates a `README-DEV.md` guide for engineers, compiling technical rules without business fluff.

- **Domain Types Classification & Context Mapping:** Added to DDD phase (Phase 05) to map Core/Supporting/Generic domains and define integration patterns.
- **Schema Migrations Strategy:** Added to CQRS phase (Phase 06) to enforce safe structural updates and zero-downtime database migration plans.
- **Cross-Cutting Concerns:** Added to SDD phase (Phase 07) to standardize security, logs, and observability across physical layers.
- **Resilience, Idempotency & Serialization:** Added to EDD phase (Phase 08) to handle DLQs, retry loops, and event payload serialization.
- **SEO & Metadata Plan:** Added optional generation of `98.03_seo_metadata_plan.md` in Phase 17 to define indexability strategy.
- **Traceability and Correlation IDs:** Added to EDD phase (Phase 08) to map distributed tracing strategies in asynchronous flows.
- **Cascading Cross-References:** Added robust Validation Notes across later phases (`07_sdd`, `08_edd`, `10_bdd`, `11_tdd`, `12_legal`) to ensure downstream artifacts correctly implement architectural decisions made in DDD, CQRS, and EDD.

### Changed / Fine-Tuning
- **Granular Draft Validation:** Refined the core interview loop so the AI only generates and asks for validation of the specific Markdown snippet related to the current question, avoiding premature whole-file drafts.
- **Question Header Formatting:** Standardized the interview prompt headers to explicitly include the Methodology ID and Acronym (e.g., `## 05.DDD: Question 1 of 18:`).
- **Methodology Names:** Standardized all methodology references across documentation to consistently use the `Official Name (ACRONYM)` format.

## Version 2.1

### Added

- Added optional Session KPIs report (`99.99_session_kpis.md`) generated at the end of the interview.
- Added `TERMS_OF_USE.md` and Privacy warnings in `README.md` for Legal Compliance (LGPD/GDPR).
- Implemented Smart Validation rules in `reference/validate.md` to prevent false validation failures (`FAIL`) on active, in-progress phases.
- Added path duplication sanitization in `SKILL.md` for setup directories, and path existence validation for the `/interview docs` command.
- Improved `README.md` structure
- Made available a real example (`examples/demo-v2/`) containing all artifacts generated during a complete interview session.

### Changed

- Explicitly listed all available commands with short descriptions in the `SKILL.md` root prompt to prevent LLMs from aggressively summarizing and omitting setup options (UX improvement).
- Added proactive typo/convention correction rule to the Draft Validation block (Point 4), instructing the AI to identify and gently propose corrections for hardcoded naming errors (e.g., project names) when presenting drafts.
- Extracted setup and command logic from `SKILL.md` to a separate `reference/setup-workflow.md` file (lazy-loading) to significantly reduce context window overhead during the interview loop.
- Merged Phase 14 (Marketing & Commercial Pitch) into Phase 13, creating a consolidated "Executive Summary & Pitch" phase (`phases/13_executive_pitch.md`) that generates both `98.01_executive_summary_business_view.md` and `98.02_marketing_pitch_deck.md` sequentially.
- Aligned the `title` frontmatter field of all template files in `Templates/` to match their actual filenames (excluding `.md`), resolving duplicate OKF indexing collisions.
- Updated templates `06.01_cqrs_schema.md`, `07.01_sdd_clean_architecture.md`, and `08.01_edd_logic_flows.md` with dedicated sections to cover all mandatory topics requested in the methodology scripts (CQRS pattern assessment, core isolation, ports and adapters, and messaging strategy).
- Sanitized template guidelines and comments in `10.01_bdd_scenarios.md` and `06.02_cqrs_specs.md` to be fully platform-agnostic, offering multi-paradigm alternatives (CLI arguments, HTTP statuses, exception classes) to prevent web-only generation biases.
- Updated `SKILL.md` to explicitly exclude `00_validation_report.md` from `/interview resume` file ingestion to avoid context polution.
- Updated `phases/11_tdd.md` to cross-reference BDD scenarios (`10.01_bdd_scenarios.md`) for stronger test case alignment.
- Added explicit Validation Notes (cross-checks) in phase scripts (`01_bmc`, `02_5w1h`, `03_moscow`, `05_ddd`, `09_ui_ux`, `10_bdd`, `12_legal`) to ensure platform-agnostic consistency across the architectural documents.
- Replaced explicit color syntax with pure Markdown formatting rules to simplify UX.
- Enforced a horizontal separator rule (`\n---\n`) to prevent visual fatigue between Q&A blocks.
- Reinforced the strict "Draft Validation" rule to prevent the AI from writing files without explicit user approval.

## Version 2.0

### Added

- Complete refactoring of the skill architecture.
- Topic-driven methodology scripts in `phases/`.
- Structured `interview_state` in `00.00_tracking_changelog.md` for reliable resume and status reporting.
- `/interview status <path>` and `/interview validate <path>` commands.
- Physical `00_validation_report.md` output.
- Canonical methodology map and reusable reference rules for OKF, file I/O, validation, and docs mode.
- Dynamic README template that includes only selected methodologies.
- Explicit safe-restart warning before deleting an existing interview folder.
- Executive Summary phase (Phase 13) to generate a business-focused overview.
- Strict Markdown formatting guidelines (`reference/markdown-guidelines.md`).

### Changed

- Replaced fixed question counts with coverage of required topics, allowing the interview to adapt to answer quality.
- Reorganized the skill from a single large instruction file into core, phase, and reference documents.
- Standardized terminology around methodologies and generated documents.
- Renamed templates to `xx.yy_methodology_artifact.md`, removing the redundant `_template` suffix.
- Updated every phase script and lifecycle instruction to reference the exact renamed template file.
- Aligned every template-based generated filename with its template filename; 00_validation_report.md remains validation-only.
- Moved optional ticket, issue, and source-material collection to the Epic Breakdown interview flow; generated documents no longer contain ticket metadata.
- Made documentation ingestion explicitly read-only and added a chat fallback when physical writing is unavailable.
- Moved source material/ticket question to Initial Discovery phase.
- Enforced strict alphanumeric filename reading order during `/interview resume` to maintain logical progression and prevent context hallucination.
- Enforced progressive document generation: artifacts are created before the first question and updated directly with the user's answers.
- Added strict Draft Validation rule: the AI must generate and iterate on a chat draft, requiring explicit user approval before writing any final content to physical files.
- Enforced checkpointing to `00.00_tracking_changelog.md` after every single answer to update the structural state (without duplicating answer content) and prevent data loss.
- Explicitly restricted reading methodology templates until the exact moment of generating their respective initial document structure.
- Enforced a standardized question format (`## <Methodology Name>: Pergunta <current> de <total>:`) and implemented explicit Semantic Formatting to map Markdown elements (bold, backticks, quotes) directly to CLI color accents (Yellow, Blue, Orange, Green) for a premium UX.
- Implemented strict Cross-Validation rules (Validation Notes) across phases (04, 06, 07, 08, 09, 10, 11) to create "long-term memory" and prevent the AI from generating architectures or entities that violate previously defined scopes, platforms, or domain events.
- Converted Phase 13 (Executive Summary) into an autonomous synthesis phase that drafts the final document silently based on previous business phases.

### Compatibility

- Version 2.0 is designed for A/B testing alongside the original `interview-skill-repo`.
- Existing interviews without an `interview_state` block are not automatically migrated.

## Version 1.0

- Initial version.






