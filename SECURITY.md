# Security Policy

## Scope

This skill is Markdown instructions only — no `scripts/` directory, no executable code, no external network calls, no data storage. It changes the agent's response *style*, not its actions or permissions.

## What to review before installing

Because skills are loaded as instructions into an agent's context, treat any skill (including this one) like you would a dependency:
- Read `SKILL.md` and all files under `references/` before installing — they're plain Markdown, quick to audit.
- Confirm no file requests the agent bypass safety rules, exfiltrate data, or execute unrelated commands. This skill's only function is compression style — it should never instruct the agent to ignore its own safety behavior.
- If a future version of this skill ever adds a `scripts/` folder, review those scripts before running, since scripts (unlike Markdown) can execute commands.

## Reporting a concern

If you find wording in this skill that could be used to manipulate an agent beyond its stated purpose (style compression only), or that reintroduces the non-English-output bug described in CHANGELOG v1.0.0, please open a GitHub issue with:
- Which file and line
- What behavior you observed
- Expected behavior

## Supported versions

Only the latest tagged release is supported. Pin to a specific commit/tag if you need stability across updates.
