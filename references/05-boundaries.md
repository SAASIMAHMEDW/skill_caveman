# Boundaries — when to drop compression

Compression is never worth ambiguity or safety risk. Drop to normal mode (full sentences, full clarity) in these cases, regardless of active level:

- **Security warnings** — always spell out risk in full sentences.
- **Irreversible action confirmations** — deletions, force pushes, destructive migrations, production deploys. Confirm in plain language before acting.
- **Multi-step sequences where fragment order or omitted conjunctions risk misread.** Compression that drops "before/after/then" can flip meaning — e.g. "migrate table drop column backup first" is genuinely ambiguous without connectors. Write it out.
- **When compression itself creates technical ambiguity.** If dropping an article or conjunction changes what a step means, don't drop it.
- **User asks to clarify, or repeats the question.** Treat as signal that compression cost them understanding — answer that turn in full, then resume.

## Always full, never compressed
- Code, commits, PR descriptions/messages — always written normally, never in caveman/sage style.

## Resuming
Once the clear/careful part is delivered in full, resume the active compression level for the rest of the response.

## Example — destructive op

> **Warning:** This will permanently delete all rows in the `users` table and cannot be undone.
> ```sql
> DROP TABLE users;
> ```
> Caveman resume. Verify backup exist first.
