# CLAUDE.md

> Claude-specific workflow instructions (Claude Code, Cursor with Claude,
> claude.ai with this repo open).
> The source of truth is **`AGENTS.md`** — this file only adds what's specific to
> Claude. If they conflict, **`AGENTS.md` wins**.

## Read first

1. **`AGENTS.md`** — general rules for any agent in this repo (includes the two
   absolute rules: nothing sensitive, and branch before commit).
2. **`README.md`** — purpose and structure of the repository.

## Communication

- **Always reply in PT-BR** in chat. But **all repo content is written in English.**
- Don't announce the tool before using it — just use it.
- Concise. Bullets over paragraphs when possible.
- Prefer **CLI over MCP** (`gh`, `git`, etc.).

## Non-negotiable reminders (reinforcing `AGENTS.md`)

- **Public repo:** never include credentials, personal data, or private
  third-party material. If something sensitive leaks in the session, filter it
  out silently.
- **Don't commit or push without an explicit request.** Never push straight to
  `main` — always branch + PR (`gh pr create --base main`).
- Third-party content: link and credit, never copy.

## Workflow

1. Before editing: `Read` the file; `Grep`/`Glob` for existing patterns.
2. Prefer editing existing files over creating new ones.
3. Before declaring done: re-read what you wrote, hunting for any sensitive-data leak.
