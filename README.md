# SDD-Interview v2

A structured interview skill for extracting business requirements, technical decisions, and architecture documentation before implementation.

## Highlights

- Topic-driven interviews: ask as many questions as necessary to cover each subject well, never a fixed quota.
- Recoverable progress: structured state in [00.00_tracking_changelog.md](00.00_tracking_changelog.md) tracks methodologies, documents, and the current topic.
- Independent validation: `/interview validate <path>` writes a physical validation report.
- Clear status: `/interview status <path>` reads the interview state and reports the next step.
- Safe documentation ingestion: `/interview docs` reads source material without changing it.

## Installation

Copy this folder into an agent's skills directory and retain `Templates/`, `phases/`, and `reference/`.

## Commands

- `/interview new <alias>`
- `/interview docs <docs_path> <alias>`
- `/interview resume <alias_path>`
- `/interview status <alias_path>`
- `/interview validate <alias_path>`
- `/interview help <topic>`

`status`, `resume`, and `validate` require an absolute interview folder path containing [00.00_tracking_changelog.md](00.00_tracking_changelog.md).

## Structure

- [SKILL.md](SKILL.md): core behavior, commands, lifecycle, and safeguards.
- `phases/`: topic scripts for each methodology.
- `reference/`: canonical mapping, validation, I/O, docs-mode, markdown-guidelines, and OKF rules.
- `Templates/`: output document structures, named `xx.yy_methodology_artifact.md` (with phase `99` reserved for the final index).

The original `interview-skill-repo/` remains unchanged; this `interview-skill-repo-2/` folder is the version for A/B testing.

## Compliance & Privacy

> [!WARNING]
> **TERMS OF USE, CUSTODY DISCLAIMER, AND LIABILITY MITIGATION**
> This Skill operates in "Pass-Through" mode, meaning it reads your local files and sends them to your chosen LLM provider.
> **DO NOT** run this Skill in directories containing un-sanitized Personally Identifiable Information (PII), hardcoded API keys, or Confidential Trade Secrets.
> You are entirely responsible for the data you process and for complying with LGPD/GDPR.
> Please read the complete [Terms of Use](TERMS_OF_USE.md) before using this tool.

## License

MIT. See [LICENSE](LICENSE).


