# File I/O

Write generated Markdown to `interview_state.destination_path` whenever the environment permits. When it does not, return complete Markdown in chat and identify the exact absolute path for manual saving. Never silently omit an output.

Docs mode is read-only for `docs_source_path`. Ignore system and dependency folders such as `.git`, `node_modules`, `bin`, and `obj` while reading source documentation.

