# Markdown Guidelines

To ensure all generated documentation is easily portable, clean, and consistent across tools (like Notion, GitHub Wiki, Confluence, etc.), you must follow these strict formatting rules:

1. **Use Only Native Markdown:** Do NOT use HTML tags (e.g., `<b>`, `<br>`, `<table>`, `<div>`) under any circumstances.
2. **Heading Hierarchy:** 
   - The document title must always be an `H1` (`#`).
   - Top-level sections must be `H2` (`##`).
   - Sub-sections must be `H3` (`###`) and so on. Do not skip heading levels (e.g., jumping from `H1` to `H3`).
3. **Code and Scripts:** Always use fenced code blocks (```) and specify the language (e.g., ```json, ```yaml, ```csharp). 
4. **Mermaid Diagrams:** When generating diagrams, use fenced code blocks with the `mermaid` language identifier. Ensure the syntax is standard and supported by GitHub.
5. **Tables:** Use standard markdown table syntax. Do not use HTML tables.

## Semantic Formatting
Use markdown to trigger the UI's syntax highlighting for interview interactions and generated texts:
- Key architectural concepts and terms: use `**bold**`.
- Filenames, paths, and CLI tools/commands: use `` `backticks` ``.
- Parameters, variables, domain events, and literal values: use `'single quotes'` or `<brackets>`.

## Structural Styling and Lists

To ensure visual and semantic consistency across all generated artifacts, strictly apply the following structural patterns:

1. **Direct Text (No bullets)**
   - **When to use:** Exclusively for introductory paragraphs, high-level summaries, or contextual descriptions located immediately below a heading (`#`, `##`, or `###`).
   - **Rule:** Never use direct text to enumerate features or list elements. If there is more than one entity, property, or statement to highlight, the text MUST be converted into a list.

2. **Unordered Lists (Dash `-`)**
   - **When to use:** Primary standard for the vast majority of architecture listings (e.g., Actors, DDD Entities, Test Cases, Business Rules, Non-functional Requirements).
   - **Rule:** Use a dash whenever the order of factors does not alter the result.
   - **Style:** If the list item has a title and a description, standardize it by using bold for the title followed by a colon. 
     *Example:* `- **Admin User:** Responsible for platform management.`

3. **Simple Ordered Lists (`1.`, `2.`)**
   - **When to use:** Only when there is a mandatory chronological order, step-by-step execution flows (e.g., EDD Synchronous Flows), or strict priority hierarchy (e.g., MoSCoW Prioritization or Epic ordering).
   - **Rule:** Do not use numbering just for aesthetics to list isolated items. If the order can be shuffled without breaking architectural logic, use an unordered list (`-`).

4. **Nested Topic Numbering (`1.1`, `1.2`, `1.2.1`)**
   - **When to use:** Exclusively for traceability of Technical Requirements in headings (e.g., `###` headings dividing Epics and User Stories) or in complex logical diagrams (e.g., BDD Scenarios).
   - **Rule:** Outside of strict requirement traceability, avoid this. For explanatory sub-items within a common list, use only indentation (2 spaces) with a dash (`-`).

**Why this rule works:**
- Eliminates "block text": Forces the AI to break long answers into `bullets`, facilitating quick reading.
- Gives purpose to numbers: Numbers (`1.`) indicate order/priority, while dashes (`-`) indicate a collection of elements. This creates an immediate mental pattern for those reading the documentation.
