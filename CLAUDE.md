# si-sitting-test-56

Disposable test repo for stakeholder-interviewer #56. Synthetic content only.

## Agent skills

### Issue tracker

GitHub Issues. See docs/agents/issue-tracker.md.

### Domain docs

Single-context. See docs/agents/domain.md.

### Interview lines

When a grilling is resolved and glossary or ADR files changed (`CONTEXT.md`, `docs/adr/`), commit those changes on the branch `interview/<ticket>` and open a PR against `main` with `gh pr create`. This applies both in the manual runtime (VS Code + Claude Code) and under the stakeholder-interviewer's Agent SDK runtime.

When you record a grilling's resolution, post the resolution comment with a first line that is exactly the level-2 heading `## Resolution`, and write the resolution under that heading (the resolution is written in English, per the `## Stakeholder interviews` section). The stakeholder-interviewer marks the ticket as resolved only when a comment carries that heading.

Under the stakeholder-interviewer runtime — you are under it when the working directory is `/workspaces/<owner>__<name>/<ticket>`, the runtime's ephemeral clone — do not claim the ticket: skip wayfinder's self-assignment step (`gh issue edit <n> --add-assignee @me`) and do not touch the ticket's assignees. The magic link already allows exactly one active sitting per ticket, which is the guard that claim provides against a second sitting, and the tool gate refuses assignee writes. Do not mention claiming or assignment to the stakeholder. In the manual runtime (VS Code + Claude Code) claim the ticket as usual.

## Stakeholder interviews
Conduct stakeholder interviews in English.
Write all tickets, resolutions, and map updates in English.
