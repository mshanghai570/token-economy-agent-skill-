---
name: token-economy
description: "Reduce token and context usage without losing quality. Use on every task, especially long sessions, large codebases, big files, logs, multi-step work, or whenever efficiency, cost, or context limits matter."
---

# Token Economy

Spend tokens on thinking and verifying, not on re-reading and re-stating.

## Reading

- Search first, read second. Use grep, glob, or symbol search to locate exact lines, then read only that range. Don't open whole files just to get a feel.
- Read line ranges, not entire files, when a file is large (over ~300 lines).
- Never re-read a file already in context unless it may have changed. After editing a file, rely on the contents already in context.
- For logs and command output, filter at the source with `tail`, `head`, `grep`, `wc -l`, or quiet flags. Don't dump thousands of lines into context.
- Skip generated, vendored, and build directories (`node_modules`, `Pods`, `build`, `dist`, `.git`, lockfiles) unless the task concerns them.

## Writing

- Edit in place with targeted replacements. Don't rewrite or re-print whole files for small changes.
- Don't echo back code the user just gave you or code that didn't change.
- Skip preambles, recaps, and closing summaries that repeat the diff.
- Answer first, then add detail only if it changes a decision.
- Use short bullets or one tight paragraph. Avoid headers for answers under about 10 lines.

## Planning

- Batch independent tool calls in parallel instead of one at a time.
- Prefer one specific search over several vague queries. Don't explore "just in case"; every read should serve a clear question.

## Long sessions

- Once a subtask is done, carry forward a 2–3 line summary of decisions, file paths, and open issues, not the transcript.
- If context is getting heavy, say so and propose a checkpoint: summarize state, then continue fresh.
- Delegate wide, noisy exploration (such as large searches or log triage) when possible so only the conclusion returns.

## Never save tokens by

- Skipping verification of code you wrote.
- Dropping a needed warning or hiding uncertainty.
- Truncating an answer so it's incomplete. Be short, not partial.
