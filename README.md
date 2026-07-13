# 🧠👔 SDD-Interview (Software Design & Discovery)

**Your Agentic AI Chief Software Architect & Mentor.** 

Before writing a single line of code, **SDD-Interview** acts as your Senior Consultant. It guides developers, technical leads, and founders through a structured, multi-phase interview to automatically extract business rules, technical specifications, and design patterns. Say goodbye to the "initial chaos" of software development.

By answering sequential questions, the AI progressively generates comprehensive, interconnected Markdown-based architectural documentation (DDD, BDD, TDD, CQRS, Clean Architecture, and more) inside your IDE.

---

## 🚀 Why SDD-Interview?

Building complex software without mapping it first leads to technical debt, architectural anxiety, and high refactoring costs. 
SDD-Interview forces you to think about edge cases, compliance, and event flows *beforehand*. It challenges your reasoning, validates your logic, and outputs up to **23 distinct enterprise-grade architectural artifacts** covering 15 structural phases.

### 🌟 Key Points
- **No-Backend & Cost Zero:** Runs entirely via CLI and Markdown in your IDE. Zero cloud infrastructure costs.
- **Fluid Mentorship UX:** Replaces rigid text generators with an interactive, consultative chat.
- **Anti-Amnesia Lifecycle (State Machine):** Physical Markdown files are saved progressively. You can pause, resume (`/interview resume <path>`), and safely backtrack without the AI losing context.
- **Legacy Ingestion (Docs Mode):** Point the AI to your legacy wiki, and it will ingest the context to pre-fill drafts for you automatically.
- **Compliance by Design:** 100% local text generation avoids Vendor Lock-In and protects your IP (Intellectual Property) from unauthorized scraping.

---

## ✨ How It Works

**SDD-Interview** is not a simple prompt generator; it is a stateful, agentic engine that operates dynamically within your IDE.

- **The Mechanics & Tone:** The AI adopts the persona of a strict, highly analytical Chief Software Architect. It conducts a step-by-step interview, asking one question at a time. It challenges your assumptions, validates your logic, and forces you to think strategically.
- **Cross-Referencing (Semantic JOINs):** As you progress through the phases, the skill intelligently reads the previously generated Markdown files. This ensures that a database decision made in Phase 5 (DDD) perfectly aligns with the UI requirements mapped in Phase 9, preventing architectural contradictions.
- **Safeguards & State Machine:** The entire process is tracked by a physical YAML-like state file (`00.00_tracking_changelog.md`). If you get interrupted or want to backtrack a decision made 3 phases ago, the engine seamlessly patches the documentation and resumes the interview without losing any context.

### 🗂️ Methodologies & Outputs

| Methodology | Artifacts Count | Topics Count |
|---|:---:|:---:|
| **System (Tracking & QA)** | 2 | 4 |
| **00. Initial Discovery** | 1 | 4 |
| **01. Business Model Canvas** | 1 | 9 |
| **02. 5W1H Discovery** | 1 | 6 |
| **03. MoSCoW Prioritization** | 1 | 4 |
| **04. Epic Breakdown** | 1 | 3 |
| **05. Domain-Driven Design (DDD)** | 4 | 12 |
| **06. CQRS** | 2 | 6 |
| **07. Clean Architecture (SDD)** | 1 | 4 |
| **08. Event-Driven (EDD)** | 1 | 4 |
| **09. UI/UX Atomic Design** | 1 | 5 |
| **10. BDD Scenarios** | 1 | 3 |
| **11. TDD Test Strategy** | 1 | 4 |
| **12. Legal & Compliance** | 1 | 4 |
| **13. Executive Pitch** | 2 | 8 |
| **Final Outputs (Index & KPIs)** | 2 | 3 |
| **TOTAL** | **23** | **83** |

#### 📋 Covered Topics Details (Exhaustive Map of 83 Topics):
- **System:** Initial Setup (State Machine), Criteria Analysis (QA), Summary and Next Action (Handoffs).
- **Discovery & Business:** Identification, Technical Scope and Platform, Identity. Problem, Value Proposition, Customer Segments, Viability and Sustainability, Key Partnerships, Cost Structure, Revenue Streams / Gains. What?, Who?, When?, Where?, Why?, How? (5W1H). Must Have, Should Have, Could Have, Won't Have (MoSCoW).
- **Requirements & DDD:** Macro Context (Epic), Business View (CEO Opinion), Atomic Subtask Description, Basic Acceptance Criteria, Constraints and Assumptions. System Actors, Aggregates and Entities (Domain Entities), Domain Commands and Events, Asynchronous Events / Reactions. Architectural Domain Decisions, Bounded Contexts Involved, Ubiquitous Language, Boundaries and Interactions. Solution Proposal Summary, Conceptual Technical Approach, Trade-offs, Discarded Alternatives. Database Tasks, Backend Tasks, Frontend Tasks, Infrastructure/Jobs Tasks.
- **Architecture & Patterns:** Pattern Evaluation (CQRS), New Tables / Modifications, Relationships, Indexes, Data Engineer Validation, Specific Business Rules, API Contracts, Expected Error Codes. Core Isolation (Clean Architecture), Ports and Adapters, Component Topology, C4 Diagram, Protections and Avoided Violations. Main Sequence Flow, Asynchronous Flows (EDD), Messaging Strategy, Caching Strategy.
- **Quality & Design:** Responsive Approach and Screen Limits, Structure and Hierarchy, Colors and Typography, Interface States and Feedback (Micro-interactions), Cognitive Accessibility (A11y), Visual References. BDD Scenarios (Happy Path, Logical Exceptions Handling, Concurrency and Integrity Constraints). Integration Tests, Frontend and UI Tests, Database Tests, Native Performance Tests, Edge Cases and Compliance. Privacy Assessment (LGPD/GDPR), Contractual and Tax Aspects, Legal Fallback.
- **Output & Metrics:** Project Overview, Business Value and Goals, High-Level Architecture, Main Technical Decisions and Trade-offs, Critical Risks and Compliance Constraints. Target Audience and Pain Points, Elevator Pitch (Value Proposition), Main Selling Points (Marketing Hooks). Project Summary (Index), Methodologies and Artifacts Index, Legal Aspects, Risk and Compliance. Timeline, Volume of Outputs, Telemetry and AI Consumption, Operation Curiosities (KPIs).

---

## 🛠️ Usage

1. Copy the `interview` folder into your agent's skills directory.
2. Trigger the skill in your AI interface by typing:
   - `/interview new <alias>` - Start a fresh project from scratch.
   - `/interview docs <path> <alias>` - Start a project by ingesting legacy context first.
   - `/interview resume <path>` - Resume an interrupted interview.
   - `/interview help` - View detailed information on the methodologies.

## 🗺️ Roadmap (Future Horizons)

We are constantly improving the SKILL to handle enterprise-grade and mission-critical architectures. Upcoming topics:
- **DDD:** Domain Types Classification and Context Mapping.
- **CQRS:** Schema Migrations strategies.
- **Clean Architecture:** Cross-Cutting Concerns integration.
- **EDD:** Resilience, Idempotency, and Event Serialization Contracts.
- **Observability:** Distributed Tracing and Correlation IDs.
- **SEO & Marketing:** Automated SEO & Metadata strategic planning.

---
## 📝 License & Attribution
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

**Attribution Requirement:** While the MIT license allows you to use, modify, and distribute this skill freely, you **must** include the original copyright notice and provide a clear attribution link back to this official repository (`https://github.com/GalegO/SDD-Interview`) in any public forks, ports, or derived works.
