# Contributing to SDD-Interview v2

## Updating a methodology

1. Name its template `xx.yy_methodology_artifact.md`; do not use `_template`, because the containing folder already provides that context.
2. Update its topic script in `phases/`.
3. Keep topic IDs stable unless a breaking migration is documented.
4. Update the canonical row, exact template filename, and topic count in `reference/methodology-map.md`.
5. Update the matching template when required.
6. Confirm the methodology can be resumed, reported by status, and validated.

## Adding a methodology

Add the template, phase script, methodology-map entry, setup/help content in `SKILL.md`, and final-index behavior. Preserve the naming convention and keep the skill technology-agnostic, one question at a time, without executable code or cost estimates.

## Reporting defects

Include the command used, exact observed behavior, expected behavior, and a sanitized `00.00_tracking_changelog.md` when possible.


