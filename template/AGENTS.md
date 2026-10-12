# AGENTS.md — {{PROJECT_NAME}}

Standing instructions for any agent (and any person) working in this folder. It is short on purpose: what is not here is in the linked documents, and you only read what the task needs. A direct instruction from {{OWNER}} in the conversation overrides this file; if a rule changes, record it in `docs/DECISIONS.md`.

## 1. What this space is

{{ONE_PARAGRAPH: what the project is, who it serves, and what is out of scope}}

Current status in one line: {{STATUS_LINE}}. The live state is in `docs/CURRENT_STATE.md`.

## 2. What to read, and when

Always read first: this file and `docs/CURRENT_STATE.md`. Then only what applies:

| If the task is… | Read |
|---|---|
| {{TASK_TYPE_1}} | {{FILES_1}} |
| {{TASK_TYPE_2}} | {{FILES_2}} |
| Why something is the way it is | `docs/DECISIONS.md` |
| What is still open | `docs/OPEN_TASKS.md` |
| Names and terms | `docs/GLOSSARY.md` |
| Where a fact came from | `docs/SOURCES.md` |

## 3. Who decides

{{OWNER}} decides on {{DECISION_AREAS}}. Agents investigate, organise, draft, build and verify. They separate **facts** from **proposals** and say where they are unsure.

## 4. Standing rules

Each rule comes from a real correction. Put the date in brackets when it was given. Delete the examples you do not need.

1. **Disagree clearly.** If an idea is not viable or rests on something unchecked, say so *before* building: the objection, the reason, the alternative, briefly. If it is a good idea, say that too.
2. **One deliverable, then stop.** Finish the requested deliverable until it is usable, show it, and wait for approval before starting the next. Mechanical steps inside an agreed task do not need a stop.
3. **Do not touch what is finished.** List folders that are frozen: {{FROZEN_FOLDERS}}. New work goes in new folders. Before overwriting your own working file, keep the previous version in a `previous_versions/` folder.
4. **Language of the human.** Everything the human reads is in {{LANGUAGE}}. If they must click something in another language, give the exact button name in quotes and what it means, one step per action.
5. **Names are spelled one way.** {{NAMING_RULE}}
6. **{{ADD_YOUR_OWN}}**

## 5. What an agent may do alone, and what needs permission

| Category | Actions |
|---|---|
| **Free** | Read, research, analyse, draft, edit local working files, run read-only checks |
| **Explicit OK from {{OWNER}}, every time** | Send emails or messages · publish or upload anything · buy or pay · register accounts or services · change production settings · delete or move in bulk · share information with third parties · issue anything that cannot be undone |
| **Never** | Store passwords, API keys, tokens or bank data in files, or ask for them in the chat. Secrets are pasted by the human into their own terminal or password manager |

These rules set roles and limits. **They do not widen the technical permissions of the environment**: if a tool blocks something, this file does not unblock it.

## 6. How to work

- **Read before you write.** Check the relevant context and do not redo decisions already taken (they are in `docs/DECISIONS.md`). If you think one should change, say so and propose it; do not apply it silently.
- **Sources.** Every figure, legal citation or claim about a registry carries its source and the date it was checked (`docs/SOURCES.md`). A "zero results" answer counts only with a positive control that shows the search can find something.
- **Verify.** After a change, check the result (rebuild, open, compare) and say what you verified and what you did not.
- **Explain at the end:** what changed, where, and what is still open, in plain language.
- **Relative paths** in documents, so they survive renaming a folder.
- **Names:** folders numbered in order of use, no spaces. ISO dates in file names (`session_close_2026-10-02.md`), your usual format inside the text. Living documents are UPPERCASE and overwritten (`CURRENT_STATE.md`); dated records are never rewritten, only added.

## 7. Several agents at once

- Before editing a file, look at its modified time. If it changed today and it was not you, read it whole and do not rewrite it from scratch.
- **Only the main agent of the session updates** `docs/CURRENT_STATE.md`, `docs/DECISIONS.md` and `docs/OPEN_TASKS.md`. Sub-agents return their result in their final message. Every update carries the date and the agent (`2026-10-03 · Agent name`).
- A sub-agent gets a self-contained brief: goal, files to read, what not to touch, and the format of the answer.
- An agent's private memory is invisible to the others. Anything that must be shared goes into these documents.

## 8. Session close

When the human says "save everything" or "see you tomorrow":

1. Write `docs/session_close_YYYY-MM-DD.md`: result, decisions, where each thing is, what was verified, drafts waiting for approval, and the agenda for the next session.
2. Overwrite `docs/CURRENT_STATE.md`, append what was approved to `docs/DECISIONS.md`, and update `docs/OPEN_TASKS.md`.
3. Re-run any cheap checks that expire (links, domains, deadlines) and note the result.

## 9. Map

{{FOLDER_MAP: one line per top-level folder}}
