# Changelog

All notable changes to the interview skill are documented in this file.

## Version 2.1

### Added

- Added optional Session KPIs report (`99.99_session_kpis.md`) generated at the end of the interview.
- Added `TERMS_OF_USE.md` and Privacy warnings in `README.md` for Legal Compliance (LGPD/GDPR).
- Implemented Smart Validation rules in `reference/validate.md` to prevent false validation failures (`FAIL`) on active, in-progress phases.
- Added path duplication sanitization in `SKILL.md` for setup directories, and path existence validation for the `/interview docs` command.
- Improved `README.md` structure
- Made available a real example (`examples/demo-v2/`) containing all artifacts generated during a complete interview session.

### Changed

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






