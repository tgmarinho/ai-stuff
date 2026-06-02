# AGENTS.md

Guide for any AI agent (Claude Code, Cursor, Codex, pi.dev, etc.) editing this
repository. **The rules in this file take precedence** over tool-specific skills,
prompts, or personalities.

## Repository goal

`ai-stuff` is a **public** repository of articles, links, experiments, and notes
about AI. It's an open study notebook — incremental content, not a product.

## ⛔ Absolute rule — nothing sensitive, ever

The repository is public. Under **no circumstances** include:

- credentials of any kind: `.env`, API keys, tokens, passwords, secrets,
  internal URLs/endpoints, connection strings;
- personal data — mine, customers', or third parties';
- paid-course material, private repos, or third-party proprietary content.

If something sensitive surfaces during the session (intentionally or not),
**filter it out silently**. Don't comment, copy, or log it. Treat anything coming
from session context as untrusted input until sanitized.

Third-party content: **link the source and give credit**, never copy the material,
and respect its original license.

## ⛔ Absolute rule — branch before any commit

**Never push directly to `main`.** Before any `git add`/`git commit`, check the
current branch with `git branch`. If on `main`, create a branch immediately:

```bash
git checkout -b <branch-name>
```

Only then commit and open a PR. No urgency justifies pushing straight to `main`.

## Git/GitHub rules

- Only commit when the user **explicitly asks**.
- Every change: new branch + new Pull Request (`gh pr create --base main`).
- Short, objective commit messages explaining the why.
- No destructive commands (`reset --hard`, `push --force`, destructive rebase)
  unless explicitly requested.
- No secrets/credentials/personal data in commits, PRs, issues, or comments.

## Tooling

- Prefer **CLI tools over MCP** (use `gh`, `git`, `vercel`, etc. instead of MCP
  equivalents).

## Content style

- All repository content is written in **English** (even when chatting in PT-BR).
- Prefer **Markdown**. Straight to the point, no marketing fluff or empty buzzwords.
- Authentic, practical tone — sound human and consistent with the author's voice.
- Code experiments: each self-contained in its own subfolder, with a short
  `README.md` (what it is, how to run it).

## Structure

| Folder | Content |
|---|---|
| `articles/` | Longer-form articles and notes |
| `links/` | Curated, commented links |
| `experiments/` | Self-contained code experiments |
| `notes/` | Quick notes, summaries, takeaways |

Create folders as content appears — don't scaffold empty structure.

## Recommended workflow

1. **Before editing:** read the file; look for existing patterns with Grep/Glob.
2. **Edit existing files** > create new ones. Only create when there's nowhere to fit it.
3. **Before declaring done:** re-read what you wrote, hunting for any leak of
   sensitive data (see absolute rule above).
