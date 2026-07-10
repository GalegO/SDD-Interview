# SDD-Interview 🧠👔

An advanced, interactive Software Architect and Product Manager skill for Agentic AI environments. 

This skill guides users through a structured, multi-phase interview process to extract business requirements, technical specifications, and design decisions BEFORE any code is written. It automatically translates your answers into standardized, Markdown-based architectural documentation.

## ✨ Features

- **12 Supported Methodologies:** From Business Model Canvas to DDD, CQRS, Clean Architecture, BDD, and Compliance.
- **Fast-Track Ingestion:** Point the AI to an existing wiki or legacy documentation directory (`/interview docs`), and it will pre-fill the interview drafts for you.
- **Anti-Amnesia Lifecycle:** Generates physical Markdown artifacts progressively. If you stop halfway, nothing is lost.
- **Context Recovery:** Use `/interview resume` to pick up exactly where you left off based on a robust changelog system.
- **Backtracking Supported:** Change your mind about a database choice made 3 phases ago? The AI will silently patch the previous documents and resume without resetting.

## 🚀 Installation

1. Copy the `interview` folder into your agent's skills directory (e.g., `.agents/skills/interview`).
2. Ensure the `Templates/` directory is kept intact inside the skill folder.
3. Trigger the skill in your AI interface by typing `/interview help` or `/interview new <project_alias>`.

## 🛠️ Usage

- `/interview new <alias>` - Start a fresh project from scratch.
- `/interview docs <path> <alias>` - Start a project by ingesting legacy context first.
- `/interview resume <path>` - Resume an interrupted interview.
- `/interview help` - View detailed information on the 12 available artifacts.

## 🤝 Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details on how to add new templates or improve the AI prompts.

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
