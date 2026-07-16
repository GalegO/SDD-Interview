# 🧠👔 SDD-Interview (Software Design & Discovery)

![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)
![Version](https://img.shields.io/badge/version-2.2-brightgreen.svg)
![AI-Powered](https://img.shields.io/badge/AI-Agentic_Skill-purple.svg)

**Your Agentic AI Chief Software Architect & Mentor.** 

Before writing a single line of code, **SDD-Interview** acts as your Senior Consultant. It guides developers, technical leads, and founders through a structured, multi-phase interview to automatically extract business rules, technical specifications, and design patterns. Say goodbye to the "initial chaos" of software development.

## 📖 Table of Contents
- [Why SDD-Interview?](#-why-sdd-interview)
- [How It Works](#-how-it-works)
  - [Methodologies & Outputs](#️-methodologies--outputs)
- [Installation](#-installation)
- [Usage](#️-usage)
  - [Real Example (Demo V2)](#-real-example-demo-v2)
  - [A La Carte Selection](#️-a-la-carte-selection)
- [Roadmap (Future Horizons)](#️-roadmap-future-horizons)
- [Contributing](#-contributing)
- [License & Attribution](#-license--attribution)

By answering sequential questions, the AI progressively generates comprehensive, interconnected Markdown-based architectural documentation (DDD, BDD, TDD, CQRS, Clean Architecture, and more) inside your IDE.

---

## 🚀 Why SDD-Interview?

Building complex software without mapping it first leads to technical debt, architectural anxiety, and high refactoring costs. 
**No other tool on the market forces you, the user, to critically think and validate your own ideas quite like this.** It challenges your reasoning, validates your logic, and outputs up to **23 distinct enterprise-grade architectural artifacts** covering 15 structural phases—all consolidated in a single place.

Whether you are designing a completely **new project**, scoping out a **new feature**, or trying to untangle a **complex bug**, the interview naturally exposes blind spots and edge cases you hadn't even considered at the start.

### 🌟 Key Points
- **100% Platform & Model Agnostic:** Built purely on Markdown and prompt engineering, the skill is completely decoupled from any specific vendor. You can run it across various AI IDEs, CLI Agents, and plug it into any LLM model (Claude, GPT, Gemini) without breaking the flow.
- **No-Backend & Cost Zero:** Runs entirely via CLI and Markdown in your IDE. Zero cloud infrastructure costs.
- **Fluid Mentorship UX:** Replaces rigid text generators with an interactive, consultative chat.
- **Anti-Amnesia Lifecycle (State Machine):** Physical Markdown files are saved progressively. You can pause, resume (`/interview resume <path>`), and safely backtrack without the AI losing context.
- **Legacy Ingestion (Docs Mode):** Point the AI to your legacy wiki, and it will ingest the context to pre-fill drafts for you automatically.
- **Compliance by Design:** 100% local text generation avoids Vendor Lock-In and protects your IP (Intellectual Property) from unauthorized scraping.
- **Multilingual by Default:** The interview can be conducted and followed in any language supported by your AI, and the artifacts can be generated in the same language for easier reading in your native language.

---

## ✨ How It Works

**SDD-Interview** is not a simple prompt generator; it is a stateful, agentic engine that operates dynamically within your IDE.

- **The Mechanics & Tone (A True Partner):** The AI adopts the persona of a strict, highly analytical Chief Software Architect. It conducts a cadenced, step-by-step interview, asking one question at a time. This paced rhythm ensures the AI rarely loses context or hallucinates. The flow is so natural that the AI quickly feels like a true partner, helping you discover critical edge cases together.
- **Fluid Flexibility & Non-Linearity:** Despite being highly structured, the interview feels like a natural chat. The system is not a rigid top-down script. You are free to change your mind, brainstorm, or abruptly say, "Actually, based on this question, let's change the artifact XYZ previously generated." The AI is intelligent enough to retroactively edit previously generated artifacts without messing up the current context or the overall flow.
- **Cross-Referencing (Semantic JOINs):** As you progress through the phases, the skill intelligently reads the previously generated Markdown files. This ensures that a database decision made in Phase 5 (DDD) perfectly aligns with the UI requirements mapped in Phase 9, preventing architectural contradictions.
- **Safeguards & State Machine:** The entire process is tracked by a physical YAML-like state file (`00.00_tracking_changelog.md`). If you get interrupted or want to backtrack a decision made 3 phases ago, the engine seamlessly patches the documentation and resumes the interview without losing any context.

### 🗂️ Methodologies & Outputs

| Methodology | Artifacts Count | Topics Count |
|---|:---:|:---:|
| **System (Tracking & QA)** | 2 | 4 |
| **0. Initial Discovery & Project Briefing** | 1 | 7 |
| **1. Business Model Canvas (BMC)** | 1 | 7 |
| **2. Discovery Framework (5W1H)** | 1 | 6 |
| **3. Scope Prioritization (MoSCoW)** | 1 | 4 |
| **4. Epic Breakdown (User Request)** | 1 | 5 |
| **5. Domain-Driven Design (DDD)** | 4 | 19 |
| **6. Command Query Responsibility Segregation (CQRS)** | 3 | 11 |
| **7. Software Design Document (SDD) & Clean Architecture** | 2 | 8 |
| **8. Event-Driven Development (EDD)** | 1 | 8 |
| **9. User Interface / User Experience (UI/UX)** | 2 | 8 |
| **10. Behavior-Driven Development (BDD)** | 1 | 4 |
| **11. Test-Driven Development (TDD)** | 2 | 7 |
| **12. Legal & Compliance** | 2 | 4 |
| **13. Application Security (AppSec) Strategy [Automated]** | 1 | 1 |
| **14. Threat Model (STRIDE) [Automated]** | 1 | 1 |
| **15. Request for Comments (RFC) [Automated]** | 1 | 1 |
| **16. Developer Onboarding [Automated]** | 1 | 1 |
| **17. Executive Pitch** | 3 | 5 |
| **Final Outputs (Index & KPIs)** | 2 | 3 |
| **TOTAL** | **33** | **114** |

#### 📋 Detailed Breakdown of All 114 Topics
- **System (Tracking & QA):** Initial Setup (State Machine), Criteria Analysis (QA), Summary and Next Action (Handoffs).
- **0. Initial Discovery & Project Briefing:** Identification, Technical Scope and Platform, Identity.
- **1. Business Model Canvas (BMC):** Problem, Value Proposition, Customer Segments, Viability and Sustainability, Key Partnerships, Cost Structure, Revenue Streams / Gains.
- **2. Discovery Framework (5W1H):** What?, Who?, When?, Where?, Why?, How?.
- **3. Scope Prioritization (MoSCoW):** Must Have, Should Have, Could Have, Won't Have.
- **4. Epic Breakdown (User Request):** Macro Context (Epic), Business View (CEO Opinion), Atomic Subtask Description, Basic Acceptance Criteria, Constraints and Assumptions.
- **5. Domain-Driven Design (DDD):** System Actors, Aggregates/Entities, Commands/Events, Asynchronous Reactions, Architectural Decisions, Domain Types Classification, Bounded Contexts, Context Mapping, Ubiquitous Language, Boundaries/Interactions, Solution Summary, Technical Approach, Trade-offs, Discarded Alternatives, Database/Backend/Frontend/Infra Tasks.
- **6. Command Query Responsibility Segregation (CQRS):** Pattern Evaluation, New Tables/Modifications, Relationships, Indexes, Schema Migrations Strategy, Data Engineer Validation, Specific Business Rules, API Contracts, Expected Error Codes, *Multi-Tenancy Strategy (Opt-in)*.
- **7. Software Design Document (SDD) & Clean Architecture:** Core Isolation, Ports and Adapters, Component Topology, C4 Diagram, Protections and Avoided Violations, Cross-Cutting Concerns, *API Gateway & Edge Security (Opt-in)*.
- **8. Event-Driven Development (EDD):** Main Sequence Flow, Asynchronous Flows (EDD), Messaging Strategy, Resilience and Idempotency, Event Serialization and Contracts, Caching Strategy, Traceability and Correlation IDs.
- **9. User Interface / User Experience (UI/UX):** Responsive Approach, Structure/Hierarchy, Colors/Typography, Interface States/Feedback, Cognitive Accessibility (A11y), Visual References, *Automated A11y Tests (Opt-in)*.
- **10. Behavior-Driven Development (BDD):** Happy Path, Logical Exceptions Handling, Concurrency and Integrity Constraints.
- **11. Test-Driven Development (TDD):** Integration Tests, Frontend/UI Tests, Database Tests, Native Performance Tests, Edge Cases/Compliance, *Mutation Testing & Latency SLAs (Opt-in)*.
- **12. Legal & Compliance:** Privacy Assessment (LGPD/GDPR), Contractual and Tax Aspects, Legal Fallback, *Continuity and Disaster Tolerance (Opt-in)*.
- **13. Application Security (AppSec) Strategy [Automated]:** Generated without user intervention. Consolidates IAM, Encryption, Secrets, and DevSecOps decisions into a unified Application Security document.
- **14. Threat Model (STRIDE) [Automated]:** Generated without user intervention. Automated STRIDE matrix and attack vectors mitigation based on SDD/CQRS/EDD.
- **15. Request for Comments (RFC) [Automated]:** Generated without user intervention. Automated RFC Draft (Motivation, Proposed Implementation, Metrics, Drawbacks, Impact/Dependencies).
- **16. Developer Onboarding [Automated]:** Generated without user intervention. Technical README-DEV.md focused purely on how to navigate the codebase on Day 1.
- **17. Executive Pitch:** Project Overview, Business Value/Goals, High-Level Architecture, Technical Decisions/Trade-offs, Critical Risks/Compliance, Target Audience/Pain Points, Elevator Pitch, Main Selling Points, SEO & Metadata Plan.
- **Final Outputs (Index & KPIs):** Project Summary (Index), Methodologies/Artifacts Index, Legal Aspects/Risk, Timeline, Volume of Outputs, Telemetry/AI Consumption, Operation Curiosities (KPIs).

---

## 📦 Installation

1. Copy the `interview` folder into your agent's skills directory (or the designated location for your specific AI CLI/IDE) and reload your interface or ask the AI to load and use it. 

### Examples for Popular AI Agents:
- **Antigravity IDE:** Run `antigravity install skills/interview` or copy the folder into `.antigravity/skills/`.
- **Claude Code (CLI):** Run `claude` in your terminal and type: *"Read the instructions inside `interview/SKILL.md` and start a new interview."*
- **Cline / Roo Code (VS Code):** Copy the folder into your project (or global `.cline/skills/` directory) and ask the agent to `@read interview/SKILL.md`. 
- **Cursor / GitHub Copilot:** Drag the `interview` folder into your workspace, open the chat, and type: *"Read the instructions inside `interview/SKILL.md` and start a new interview."*
- **Aider / OpenHands (CLI):** Add the skill file to the chat context using `/add interview/SKILL.md` and trigger it with `/interview new <alias>`.
- **Other LLMs (ChatGPT / Claude Web):** While designed for IDE integration, you can upload the `SKILL.md` and `Templates/` directly into a custom GPT or Claude Project and prompt it to act based on those rules.

## 🛠️ Usage

Trigger the skill in your AI interface by typing:
   - `/interview new <alias>` - Start a fresh project from scratch.
   - `/interview docs <path> <alias>` - Start a project by ingesting legacy context first.
   - `/interview resume <path>` - Resume an interrupted interview.
   - `/interview help` - View detailed information on the methodologies.

### 🎛️ A La Carte Selection
You are **not** obligated to go through all 16 methodology phases and 99 topics every single time. At the beginning of the interview, you can select exactly which methodologies you want to use (e.g., only DDD and CQRS for a specific microservice). 
However, **we strongly advise running the full, complete interview at least once**. By experiencing the entire flow and knowing exactly what content is generated in each phase, you will easily be able to determine if those methodologies will be needed in the future or not. Remember: *the more questions you answer, the higher the quality of the final consolidated architecture.*

### 🎯 Real Example (Demo V2)
To see exactly what the output of this skill looks like, check out the **[Demo V2](./examples/demo-v2/README.md)** directory. It contains 23 architectural artifacts generated during a real, extensive interview session. This is a great place to understand the depth and structure of the AI's output.

### ⚠️ Limitations & Not Supported
- **Microsoft Copilot 365 / Standard Web Chatbots:** Assistants without direct read/write access to your local filesystem (like Copilot for M365) cannot automatically generate the `.md` files in your project. You can still chat with them, but you must manually copy and paste the generated content into files.
- **Low-Context Models:** Models with very small context windows may struggle to maintain the state of the `00.00_tracking_changelog.md` deep into the interview. We strongly recommend using modern models (e.g., Claude 3.5 Sonnet, GPT-4o, Gemini 3.1 (Low)).

## 🗺️ Roadmap (Future Horizons)

We are constantly improving the SKILL to handle enterprise-grade and mission-critical architectures. 

*(All current advanced topics have been successfully integrated into Version 2.2! Suggest a new feature via the Issues tab).*

---

## 🤝 Contributing

We welcome contributions! Whether it's reporting a bug, suggesting a new architectural pattern, or improving the methodologies, please see our [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on how to get involved.

---
## 📝 License & Attribution
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

**Attribution Requirement:** While the MIT license allows you to use, modify, and distribute this skill freely, you **must** include the original copyright notice and provide a clear attribution link back to this official repository (`https://github.com/GalegO/SDD-Interview`) in any public forks, ports, or derived works.
