# Principles behind the template

Short explanations of *why* each habit exists. Read them if you want to change a rule: remove a rule only when you understand the failure it prevents.

## 1. One source of rules

When rules live in several files, they drift apart, and each agent follows a different copy. `AGENTS.md` is the only place rules are written; tool-specific files such as `CLAUDE.md` just import it. **Failure prevented:** two agents with two different rule sets on the same folder.

## 2. Living documents versus records

- *Living* documents (`CURRENT_STATE.md`) answer "where are we now". They are overwritten, so they are never stale.
- *Records* (`DECISIONS.md`, `session_close_*.md`) answer "what happened". They are only appended, so history is never lost or quietly rewritten.

Mixing them gives you a "current state" that nobody dares to edit and a "history" that is quietly wrong.

## 3. Proposed is not decided

Agents are good at producing plausible recommendations. If those enter the decision log as if they were approved, the human loses control without noticing. Only **human-approved** items enter `DECISIONS.md`. Everything else is a task with an owner.

## 4. Only one writer for the shared files

When several agents update the same state file at once, the last one wins and the others' work disappears. The rule is simple: sub-agents report in their final message; the main agent of the session writes the shared files.

## 5. Permissions are a table, not a mood

A three-row table (free, needs OK, never) removes most ambiguity. The "needs OK" row lists actions that are **outward-facing or hard to reverse**: sending, publishing, paying, registering, changing production, deleting in bulk, sharing with third parties. Approval in one context does not extend to the next.

The file also says what it cannot do: it does not grant or remove any technical permission.

## 6. Secrets never enter documents or chat

Passwords, keys and tokens do not belong in files an agent can read, nor in a conversation that may be logged. The human pastes them into their own terminal or password manager. If a step needs a credential and the tool blocks the agent, that is the system working, not a problem to route around.

## 7. Sources, dates and positive controls

A claim without a source and a date becomes a "fact" within two sessions. A search that returns nothing proves nothing unless the same method finds something it should. Writing "verified" or "unverified" next to each conclusion stops the second from being quietly promoted.

## 8. Disagree early

An agent that agrees by default is expensive: the human discovers the problem after building on it. The rule asks for the objection, the reason and the alternative, in a few lines, *before* building, and also asks the agent to say when an idea is good.

## 9. One deliverable, then stop

Chaining one deliverable into the next removes the human's chance to correct course. The rule: finish what was asked until it is usable, show it, wait. Mechanical steps inside an agreed task do not need a stop.

## 10. Keep it short

Every rule costs reading time on every session. If a rule has not prevented a failure in months, delete it.
