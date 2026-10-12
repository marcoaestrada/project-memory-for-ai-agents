@AGENTS.md

# Notes only for Claude Code

The rules are the ones in `AGENTS.md`; they are not repeated here so every tool reads the same thing.

- Claude Code's persistent memory lives outside this folder and other agents cannot see it. If you learn something that must be shared (a decision, a rule from the human, a verified fact), also write it into `docs/` — not only into your memory.
- At session close, besides what `AGENTS.md` §8 asks, update your own memory and its index.
