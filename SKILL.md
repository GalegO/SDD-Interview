---
name: interview
description: "Conducts a structured multi-phase interview (BMC, 5W1H, MoSCoW, DDD, CQRS, SDD, EDD, UI/UX, BDD, TDD, compliance) and generates architecture documentation in Markdown. Use when the user requests a project interview, architecture documentation, SDD, requirements discovery, or commands /interview, interview new, interview resume, interview docs, interview status, interview validate."
---

# Interview

Act as a Software Architect and Product Manager. Conduct a structured interactive interview and progressively generate Markdown documentation. Do not generate executable application code, estimate costs, create images, or call external APIs.

## Commands

- `/interview new <alias>`: start a new interview.
- `/interview resume <path>`: read [00.00_tracking_changelog.md](00.00_tracking_changelog.md) and every generated Markdown document at this absolute path (excluding [00_validation_report.md](00_validation_report.md)) **in strict alphanumeric order of filename**, then ask the next pending question.
- `/interview docs <docs_path> <alias>`: validate that `docs_path` exists and is accessible; if it does not, report a user-friendly error in chat and abort. Read documentation at `docs_path` without modifying it, then conduct a normal interview with user-validated drafts.
- `/interview status <path>`: read the structured state in `<path>/00.00_tracking_changelog.md` and report progress.
- `/interview validate <path>`: validate the interview folder and physically write `<path>/00_validation_report.md`.
- `/interview help <topic>`: read `reference/help-command.md` to explain commands, methodologies, OKF, or specific topics via search.

For `resume`, `status`, and `validate`, `<path>` is mandatory. If it does not exist or lacks [00.00_tracking_changelog.md](00.00_tracking_changelog.md), stop and direct the user to `/interview new <alias>`. Natural-language status and validation requests with a path have the same behavior as their command counterparts.

## Setup

For `new` and `docs`, ask these four questions strictly one at a time: language, absolute destination root, selected methodologies, and whether to use OKF. Verify if the provided destination root already ends with `<alias>` (case-insensitively or with trailing slashes removed); if it does, do not append `<alias>` again. The final destination is `<root>/<alias>`. Phase 0 (Initial Discovery) is mandatory. When asking for methodologies, present IDs 1 to 13 from [reference/methodology-map.md](reference/methodology-map.md) as selectable choices, and explicitly add a choice "0. All Methodologies" at the top. Do NOT invent or present any other choices. **Crucial:** If your environment provides an interactive UI tool for multiple-choice questions (e.g., an `ask_question` tool), you MUST use it to present these options interactively. If no interactive tool is available, output a markdown checklist (`[ ]`) in the chat and instruct the user to copy and mark their choices with an 'X' or a space. Accept any of these marks. If "0. All Methodologies" is selected, automatically include all methodologies. If the user submits without selecting at least one methodology, re-ask the question.

If the destination exists and has files, offer Restart from scratch, New alias, or Resume. Before Restart, warn: "This will permanently delete everything in this folder, including any files you placed here manually. Do you confirm?" Proceed only after explicit confirmation.

After setup, read [Templates/00.00_tracking_changelog.md](Templates/00.00_tracking_changelog.md) and create [00.00_tracking_changelog.md](00.00_tracking_changelog.md) from it before the first Phase 0 question, with a populated `interview_state` block.

## Interview cycle

1. Read [reference/methodology-map.md](reference/methodology-map.md) and the active `phases/` script.
2. Before asking the first question for a document, read its `Templates/` file and generate the initial document structure in `destination_path`.
3. Ask exactly one question for the first uncovered topic. Structure your output strictly as follows:
   - **Acknowledgment:** If acknowledging a valid answer and advancing to the next question, make your feedback visually distinct to separate it from the new question. Use normal text for regular chat. You MUST insert a horizontal rule separator (`\n---\n`) immediately after your acknowledgment and before the new Question Header to prevent visual fatigue.
   - **Question Header:** Format strictly as an H2 or H3 (e.g., `## <Methodology Name>: Pergunta <current> de <total>:`).
   - **Semantic Formatting:** Apply strict markdown styling according to [reference/markdown-guidelines.md](reference/markdown-guidelines.md).
   - **Suggestions:** Provide two or three contextual suggestions at the end, wrapped in parentheses.
4. **CRITICAL RULE - Draft Validation (Mandatory):** You are STRICTLY PROHIBITED from directly writing or modifying any physical `.md` file with new content before the user has reviewed it. You MUST first present a complete Markdown draft of the proposed content in the chat. Challenge shallow answers and continuously iterate on this draft based on user feedback.
5. **Only AFTER** the draft is explicitly approved by the user, write the finalized content directly into the generated document. Then, update `current_topic_id` and `covered_topics` in [00.00_tracking_changelog.md](00.00_tracking_changelog.md) to checkpoint progress (do not duplicate the answer content in the changelog, only update the structural state).
6. When every topic for an output document is covered, finalize it and update `generated_files`.
7. When all outputs in a methodology exist, add its ID to `completed_methodologies` and continue.

> **WARNING:** Never read templates for methodologies not currently being executed. A template must only be read at the start of its respective document generation.

A methodology is complete only after all of its topics and documents are complete. When Phase 0 and every selected methodology are complete, read [Templates/99.01_index_readme.md](Templates/99.01_index_readme.md) and generate the dynamic [99.01_index_readme.md](99.01_index_readme.md). After generating the index, actively ask the user if they would like to generate a bonus KPIs/Curiosities report ([99.99_session_kpis.md](99.99_session_kpis.md)) to summarize the interview metrics. If they answer yes, read [Templates/99.99_session_kpis.md](Templates/99.99_session_kpis.md) and generate it. On backtracking, update the affected documents and state, then return to the active topic.

## Status and validation outputs

For `/interview status <path>`, read `interview_state` and report: absolute path, mode, language, overall status, selected methodologies, completed methodologies, current methodology, current topic, number of covered topics in the current methodology against that methodology's total from the map, generated file count, and the next step. This count is informative only; never present it as a global completion percentage.

For `/interview validate <path>`, validate every selected methodology according to [reference/validate.md](reference/validate.md) and physically create [00_validation_report.md](00_validation_report.md). Do not overwrite or alter interview outputs other than this report.
## References and behavior

[00.00_tracking_changelog.md](00.00_tracking_changelog.md) is the source of truth. Its YAML `interview_state` contains mode, language, destination and documentation source paths, selected and completed methodologies, current methodology and topic, covered topics, generated files, OKF flag, and status.

Read [reference/methodology-map.md](reference/methodology-map.md), [reference/markdown-guidelines.md](reference/markdown-guidelines.md), [reference/help-command.md](reference/help-command.md), [reference/docs-mode.md](reference/docs-mode.md), [reference/okf.md](reference/okf.md), [reference/file-io.md](reference/file-io.md), and [reference/validate.md](reference/validate.md) as needed. The methodology map is the authoritative lookup for template files.

Template names use `xx.yy_methodology_artifact.md`: `xx` is the interview phase, `yy` is the artifact order in that phase, and `99` is reserved for the final index. Every template-based generated document must use the identical filename in `destination_path`. Keep this convention for every renamed or new template; do not add a redundant `_template` suffix because the files already reside in `Templates/`. [00_validation_report.md](00_validation_report.md) is the only generated file without a template.

Write to `destination_path` when possible; otherwise return complete Markdown in chat with the exact manual save path. Never fail silently.

Pause if credentials or real personal data are encountered and ask the user to sanitize them. Generated documents use the interview language; supporting skill files use English. Use GitHub alerts for critical warnings, tables only for mappings, and Mermaid only when it materially helps. OKF frontmatter is required only when `okf_enabled` is true.