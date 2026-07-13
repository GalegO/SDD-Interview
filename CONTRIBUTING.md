# 🤝 Contributing to SDD-Interview v2

First off, thank you for considering contributing to **SDD-Interview**! It's people like you that make the open-source community such a powerful place to learn, inspire, and create.

This document provides guidelines and instructions for contributing to this Agentic AI Skill.

---

## 📑 Table of Contents
1. [Code of Conduct](#-code-of-conduct)
2. [How Can I Contribute?](#-how-can-i-contribute)
   - [Reporting Bugs](#reporting-bugs)
   - [Suggesting Enhancements](#suggesting-enhancements)
   - [Pull Requests](#pull-requests)
3. [Skill Development Guidelines](#-skill-development-guidelines)
   - [Updating a Methodology](#updating-a-methodology)
   - [Adding a New Methodology](#adding-a-new-methodology)
4. [Attribution & Licensing](#-attribution--licensing)

---

## 📜 Code of Conduct

This project and everyone participating in it is governed by a standard Open Source Code of Conduct. By participating, you are expected to uphold this code. Please be welcoming, inclusive, and respectful to all contributors.

---

## 💡 How Can I Contribute?

### Reporting Bugs
If you find a loophole where the AI hallucinates, loses context, or generates broken markdown, please submit an issue.
**Include in your report:**
- The exact prompt/command used to trigger the error.
- The expected behavior vs. the actual observed behavior.
- A sanitized version of your `00.00_tracking_changelog.md` (remove any sensitive/company data before uploading) so we can debug the State Machine.

### Suggesting Enhancements
Have an idea for a new architectural pattern (e.g., Hexagonal Architecture, Micro-frontends)? We'd love to hear it!
- Check if the feature has already been requested in the Issues tab.
- Provide a clear use-case and explain why it adds value to the standard interview flow.

### Pull Requests
1. Fork the repo and create your branch from `main` (`git checkout -b feature/amazing-feature`).
2. Make sure your changes do not break the core constraints (e.g., *No-Code Generation* policy).
3. Test the skill locally with your AI IDE to ensure the State Machine (`tracking_changelog`) updates correctly.
4. Open a PR with a detailed description of the changes.

---

## 🛠️ Skill Development Guidelines

Since this is an AI Skill based purely on Markdown instructions and Prompts, follow these strict rules to maintain the engine's integrity:

### Updating a Methodology
If you are tweaking an existing phase (e.g., DDD, CQRS):
1. **Naming Convention:** Name the template `xx.yy_methodology_artifact.md`. Do **not** use the suffix `_template` in the filename, because the containing folder already provides that context.
2. **Phase Scripts:** Update the corresponding topic script inside the `phases/` directory.
3. **Stability:** Keep topic IDs stable to prevent breaking the State Machine. If you must change them, document a breaking migration.
4. **Registry:** Update the canonical row, exact template filename, and topic count in `reference/methodology-map.md`.
5. **Validation:** Run a mock interview and confirm the methodology can be safely resumed (`/resume`), reported by status, and validated.

### Adding a New Methodology
If you are introducing a completely new phase to the software lifecycle:
1. **Core Integration:** Add the template, the phase script, and update the `methodology-map` entry.
2. **Setup Instructions:** Add the setup and help content to the main `SKILL.md` file.
3. **Index Behavior:** Ensure the new methodology is automatically tracked by the final-index generator.
4. **Philosophical Constraints:** 
   - Preserve the numbering/naming convention (e.g., `14.01_new_concept.md`).
   - Keep the skill **technology-agnostic** (avoid forcing specific frameworks).
   - Ask **one question at a time**.
   - **Crucial:** Do not allow the AI to generate executable code or financial cost estimates. The tool is strictly analytical and architectural.

---

## ⚖️ Attribution & Licensing

By contributing, you agree that your contributions will be licensed under the MIT License. 
Please note the **Attribution Requirement** detailed in the [README.md](README.md) and [LICENSE](LICENSE) files: any public forks or derived versions of this skill must include a clear attribution link back to this official repository.

Thank you for helping us build better software architectures! 🚀
