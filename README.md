# 🧠👔 SDD-Interview (Software Design & Discovery)

An advanced, interactive **Software Architect and Product Manager** skill for Agentic AI environments. 

Before you write a single line of code, **SDD-Interview** guides you through a structured, multi-phase interview process to extract business requirements, technical specifications, and design decisions. It translates your answers into comprehensive, interconnected Markdown-based architectural documentation.

---

## ✨ How It Works

The SKILL acts as a senior consultant. You simply trigger it and answer its questions sequentially. Behind the scenes, it uses reactive loops to generate physical artifacts progressively. 

Based on the highly granular **V2 Engine**, it can generate up to **23 distinct architectural artifacts**, covering the entire software lifecycle.

### 🗂️ Methodologies & Outputs

| Methodology | Artifacts Count | Topics Count |
|---|:---:|:---:|
| **System (Tracking & QA)** | 2 | 4 |
| **00. Initial Discovery** | 1 | 3 |
| **01. Business Model Canvas** | 1 | 3 |
| **02. 5W1H Discovery** | 1 | 6 |
| **03. MoSCoW Prioritization** | 1 | 4 |
| **04. Epic Breakdown** | 1 | 2 |
| **05. Domain-Driven Design (DDD)** | 4 | 8 |
| **06. CQRS** | 2 | 6 |
| **07. Clean Architecture (SDD)** | 1 | 3 |
| **08. Event-Driven (EDD)** | 1 | 2 |
| **09. UI/UX Atomic Design** | 1 | 4 |
| **10. BDD Scenarios** | 1 | 1 |
| **11. TDD Test Strategy** | 1 | 3 |
| **12. Legal & Compliance** | 1 | 3 |
| **13. Executive Pitch** | 2 | 2 |
| **Final Outputs (Index & KPIs)** | 2 | 3 |
| **TOTAL** | **23** | **57** |

#### 📋 Covered Topics Details:
- **System:** Handoffs, State Tracking, Automated QA, Inconsistency Checks.
- **Discovery & Business:** Project Goals, Tech Stack, Branding, Value Proposition, Customer Segments, Revenue Streams, 5W1H (What, Why, Who, When, Where, How), MoSCoW.
- **Requirements & DDD:** User Stories, Acceptance Criteria, Event Storming, Bounded Contexts, Aggregate Roots, Dev Tasks.
- **Architecture & Patterns:** Read/Write Models, Eventual Consistency, CQRS Commands/Queries, Ports, Adapters, Core Business Rules, EDD Asynchronous Communication, Message Brokers.
- **Quality & Design:** Atomic Design Tokens (Atoms, Molecules, Organisms), BDD Scenarios, TDD Unit/Integration/E2E Policies, LGPD/GDPR, PII Handling.
- **Output & Metrics:** C-Level Business Overview, Pitch Deck, Session Insights, Table of Contents.

## ⚖️ Pros and Cons

### ✅ Pros (Why use it?)
- **Anti-Amnesia Lifecycle:** Generates physical Markdown files progressively. If you drop the session, nothing is lost. Context is saved continuously.
- **Context Recovery & Fast-Track:** Easily resume an interrupted interview (`/interview resume`) or point the AI to a legacy wiki to ingest context automatically (`/interview docs`).
- **Forces Robust Design:** Prevents you from jumping into "raw" code by making you think about edge cases, compliance, and event flows beforehand.
- **Traceability:** It maintains a strict `00.00_tracking_changelog.md` to map agent handoffs and decisions.
- **Backtracking Supported:** Change your mind about a database choice made 3 phases ago? The AI will silently patch the previous documents and resume without resetting.

### ❌ Cons (When NOT to use it)
- **Overkill for Simple Scripts:** If you are building a quick throw-away script or a micro-tool, this extensive process is too heavy.
- **Time Consuming:** A full V2 interview requires deep thinking and time to answer properly.
- **Garbage In, Garbage Out:** The quality of the documentation relies heavily on how detailed and thoughtful your answers are during the interview.

## 🚀 Installation & Usage

1. Copy the `interview` folder into your agent's skills directory.
2. Trigger the skill in your AI interface by typing:
   - `/interview new <alias>` - Start a fresh project from scratch.
   - `/interview docs <path> <alias>` - Start a project by ingesting legacy context first.
   - `/interview resume <path>` - Resume an interrupted interview.
   - `/interview help` - View detailed information on the methodologies.

## 🗺️ Roadmap (Future Horizons)

We are constantly improving the SKILL to handle enterprise-grade and mission-critical architectures. Upcoming topics:

- **Domain-Driven Design (DDD):** Domain Types Classification and Context Mapping.
- **CQRS & Data Modeling:** Schema Migrations strategies.
- **SDD & Clean Architecture:** Cross-Cutting Concerns integration.
- **Event-Driven Design (EDD):** Resilience, Idempotency, and Event Serialization Contracts.
- **Observability:** Distributed Tracing and Correlation IDs.
- **SEO & Marketing:** Automated SEO & Metadata strategic planning.

---
## 📝 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
