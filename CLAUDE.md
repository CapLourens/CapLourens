# Working rules (token efficiency)

- Answer briefly. No preamble, no recap of the request, no closing summary of unchanged facts.
- Read only what the task needs: use Grep/Glob first, then Read with `offset`/`limit`. Never re-read a file just edited.
- Batch independent tool calls in one turn. Do not poll or re-run commands to "double-check".
- Do not spawn subagents unless the task needs a broad search; prefer the `scout` agent (cheap model) for that.
- Do not restate code in chat that is already in a diff or file. Reference `path:line` instead.
- Ask a question only when blocked on a real decision; otherwise pick the conventional default and state it in one line.
- For large outputs (logs, test runs), pipe through `tail`, `head`, or `grep` before reading.
