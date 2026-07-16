# Setup & Commands Workflow

This file contains the initialization logic, command interpretation, and generation of status/validation reports for the Skill. It should ONLY be read when the user triggers a specific command that deviates from the standard flow of the interview.

## Commands

- `/interview new <alias>`: start a new interview.
- `/interview resume <path>`: read `00.00_tracking_changelog.md` and every generated Markdown document at this absolute path (excluding `00_validation_report.md`) **in strict alphanumeric order of filename**, then ask the next pending question.
- `/interview docs <docs_path> <alias>`: validate that `docs_path` exists and is accessible; if it does not, report a user-friendly error in chat and abort. Read documentation at `docs_path` without modifying it, then conduct a normal interview with user-validated drafts.
- `/interview status <path>`: read the structured state in `<path>/00.00_tracking_changelog.md` and report progress.
- `/interview validate <path>`: validate the interview folder and physically write `<path>/00_validation_report.md`.
- `/interview help <topic>`: read `reference/help-command.md` to explain commands, methodologies, OKF, or specific topics via search.

For `resume`, `status`, and `validate`, `<path>` is mandatory. If it does not exist or lacks `00.00_tracking_changelog.md`, stop and direct the user to `/interview new <alias>`. Natural-language status and validation requests with a path have the same behavior as their command counterparts.

## Setup Workflow (For `new` and `docs`)

1. Ask these four questions strictly one at a time: 
   - Language
   - Absolute destination root
   - Selected methodologies
   - Whether to use OKF. 
2. Verify if the provided destination root already ends with `<alias>` (case-insensitively or with trailing slashes removed); if it does, do not append `<alias>` again. The final destination is `<root>/<alias>`.
3. Phase 0 (Initial Discovery) is mandatory.
4. When asking for methodologies, present IDs 1 to 17 from `reference/methodology-map.md` as selectable choices, and explicitly add a choice "0. All Methodologies" at the top. Do NOT invent or present any other choices. **Crucial:** Immediately below the choices, briefly explain to the user that methodologies marked with `[Automated]` do not require an interview; the AI will automatically generate their content based on the answers from previous phases. 
5. **Crucial:** If your environment provides an interactive UI tool for multiple-choice questions (e.g., an `ask_question` tool), you MUST use it to present these options interactively. If no interactive tool is available, present the numbered list and instruct the user to reply with a comma-separated list of the methodology IDs they want to use (e.g., "1, 4, 7"). If "0. All Methodologies" or "0" is selected, automatically include all methodologies. If the user submits without selecting at least one valid methodology ID, re-ask the question.
6. If the destination exists and has files, offer Restart from scratch, New alias, or Resume. Before Restart, warn: "This will permanently delete everything in this folder, including any files you placed here manually. Do you confirm?" Proceed only after explicit confirmation.
7. After setup, read `Templates/00.00_tracking_changelog.md` and create `00.00_tracking_changelog.md` from it before the first Phase 0 question, with a populated `interview_state` block.

## Status and Validation Outputs

For `/interview status <path>`, read `interview_state` and report: absolute path, mode, language, overall status, selected methodologies, completed methodologies, current methodology, current topic, number of covered topics in the current methodology against that methodology's total from the map, generated file count, and the next step. This count is informative only; never present it as a global completion percentage.

For `/interview validate <path>`, validate every selected methodology according to `reference/validate.md` and physically create `00_validation_report.md`. Do not overwrite or alter interview outputs other than this report.
