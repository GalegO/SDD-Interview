# Help Command Reference

When the user executes the `/interview help` command, you must provide a comprehensive, structured, and easy-to-read guide explaining how the Interview Skill operates. Your response must strictly be in the language of the interview (or default to the user's language) and follow this structure:

## 1. Introduction
Briefly explain that this Skill acts as a Software Architect and Product Manager. Its goal is to conduct an interactive interview to progressively discover requirements and generate structured Markdown documentation for a software project. Emphasize that it does not generate executable code.

## 2. Available Commands
List and explain all available commands:
- `/interview new <alias>`: Starts a new project interview from scratch. Creates a new folder.
- `/interview resume <path>`: Resumes a previously paused interview from an existing folder by reading its [00.00_tracking_changelog.md](00.00_tracking_changelog.md) state.
- `/interview docs <docs_path> <alias>`: Starts a new interview but first reads existing documentation (legacy code/docs) to contextualize the AI.
- `/interview status <path>`: Reports the current progress of the interview (completed methodologies, generated files, current topic).
- `/interview validate <path>`: Audits the generated architecture and creates a [00_validation_report.md](00_validation_report.md) with gaps and recommendations.
- `/interview help`: Displays this general help message.
- `/interview help <topic>`: Provides a deep-dive explanation of any specific methodology, concept, or framework (e.g., `/interview help BMC`, `/interview help OKF`, or `/interview help Clean Architecture`). When this command is used, the AI bypasses the general help menu and acts as your personal architecture tutor. It will search its internal knowledge base or the web to deliver a comprehensive, easy-to-understand explanation of the requested topic and how it applies to software design.

## 3. Supported Methodologies
Explain that the user can choose from a menu of 14 structured phases. Briefly list the core ones to give context, starting with their acronyms:
- **Briefing**: Initial Discovery & Project Briefing
- **BMC**: Business Model Canvas
- **5W1H**: Discovery Framework
- **MoSCoW**: Scope Prioritization
- **Epic**: Epic Breakdown & User Requests
- **DDD**: Domain-Driven Design (Events, Strategic Design, Solution Proposal, Implementation Tasks)
- **CQRS**: Command Query Responsibility Segregation (Schema & Specs)
- **SDD**: Software Design Document (Clean Architecture)
- **EDD**: Event-Driven Design (Logic Flows)
- **UI/UX**: Atomic Design & Specifications
- **BDD**: Behavior-Driven Development (Scenarios)
- **TDD**: Test-Driven Development (Test Strategy)
- **Legal**: Legal Compliance & GDPR/LGPD
- **Executive & Pitch**: Executive Summary & Marketing Pitch Deck
- **KPIs**: Session KPIs & Curiosities

## 4. OKF (Object Key Framework)
Briefly explain the OKF (if the user asks or as a small note). Explain that it is an optional rigid frontmatter metadata structure for the generated markdown files.

## 5. The Golden Rule (Draft Validation)
Explicitly inform the user about the **Draft Validation Rule**. Explain that the AI will ask exactly one question at a time. After the user answers, the AI will *always* generate a Markdown draft in the chat. The physical Markdown files are only updated after the user gives their explicit approval of the draft. This gives the user full control over what is written.

---
**Note for the AI:** Format the output clearly using Markdown styling (bolding, lists, and code blocks for commands) according to the [reference/markdown-guidelines.md](reference/markdown-guidelines.md).
