# project-memory-for-ai-agents

A small, plain-Markdown template that gives a project a **shared memory** for people and AI agents (Claude Code, Codex, Cursor, any agent that reads files). It answers four questions every time work starts:

1. **What are the rules?** → `AGENTS.md`
2. **Where are we right now?** → `docs/CURRENT_STATE.md`
3. **What was already decided, and why?** → `docs/DECISIONS.md`
4. **What is still open, and who owns it?** → `docs/OPEN_TASKS.md`

No tooling, no dependencies. Copy the files, fill the placeholders, commit.

> It was extracted from a real multi-agent workflow where several agents and one human worked on the same folder over weeks. Every rule in the template exists because something went wrong without it.

## Why it exists

AI agents start every session with no memory. A person returning after a week has the same problem. Without a shared record:

- an agent redoes a decision that was already made, or quietly reverses it;
- two agents edit the same file and one overwrites the other;
- a fact that was verified once is "remembered" wrongly later;
- nobody can tell what was approved and what was only proposed.

This template fixes that with a few habits, not with software.

## What is in the box

```
template/
  AGENTS.md              rules for any agent: what to read, who decides, what needs permission
  CLAUDE.md              one line that imports AGENTS.md (for tools that look for this name)
  docs/
    CURRENT_STATE.md     a living snapshot: overwritten at the start and end of each session
    DECISIONS.md         an append-only log: what was decided, by whom, why
    OPEN_TASKS.md        one row per task, with a concrete next step and an owner
    GLOSSARY.md          names and terms, so agents stop inventing synonyms
    SOURCES.md           where each fact came from, with the date it was checked
examples/bakery/         the same files filled in for a fictional project
es/                      Spanish version of the template
docs/PRINCIPLES.md       the reasoning behind each rule
```

## How to use it

1. Copy `template/` into the root of your project.
2. Open `AGENTS.md` and replace every `{{PLACEHOLDER}}`. Delete the sections you do not need; **shorter is better**.
3. Tell your agent tool to read `AGENTS.md` first (Claude Code reads `CLAUDE.md`, which imports it).
4. At the end of every session, ask the agent to run the *session close* routine in `AGENTS.md`.

## The five habits that matter most

1. **One source of rules.** `AGENTS.md` is the only place rules live. Other files point to it.
2. **Living documents are overwritten; records are appended.** State is a snapshot. Decisions and dated logs are never rewritten.
3. **Only one agent updates the shared files.** Others report back in their final message. This prevents merge fights.
4. **Proposed is not decided.** Decisions are recorded only when the human approved them. Agent suggestions go to the task list.
5. **Every fact has a source and a date.** "Zero results" counts only with a positive control that proves the search can find something.

## What this is not

- Not a framework or a tool. It is a convention written in Markdown.
- Not a security boundary. Documents describe roles and limits; they do **not** extend or restrict what an agent's tools can technically do. Use real permissions for that.
- Not legal, tax or compliance advice.

## Support

This is shared as-is. There is **no guaranteed support**; issues and pull requests may take a long time to be answered or may not be answered.

## License

MIT. See [LICENSE](LICENSE).
