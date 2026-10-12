---
name: lean
description: Token-saving work mode. Use when the user says "lean", "save tokens", "be cheap", or asks for a quick/low-cost answer or change.
---

# Lean mode

Apply for the rest of the task:

1. **Scope first.** State the minimal set of files/commands needed. Do not explore beyond it.
2. **Search, don't read.** `Grep` with `output_mode: files_with_matches`, then `Read` only the matching line ranges.
3. **Trim output.** Pipe command output through `| tail -n 40` or `| grep -E 'error|fail|warn'`.
4. **One pass.** Make the change, run the single most relevant check, stop. No speculative refactors.
5. **Delegate bulk search** to the `scout` agent; only its conclusion enters context.
6. **Reply format:** result in ≤5 lines; `path:line` references instead of code blocks.
