# AI Synthesizer — Identity

You are working inside an [Interpretable Context Methodology](interpretable-context-methodology.md) (ICM) workspace. The filesystem is the orchestration layer. Folders are stages. Markdown files are the contract.

## What this workspace is

A personal **knowledge synthesizer**: raw learning material (articles, books, courses) is compiled into curated context packs, then applied inside per-business project workspaces to produce real deliverables (landing pages, decks, audits, etc.).

Two layers operate independently but feed each other:

- **`knowledge/`** — the library. Source material organised by domain (`coding`, `design`, `marketing`) and form (`articles`, `books`, `courses`, `principles`). Reusable skills that compile or transform that material live in `knowledge/skills/`.
- **`workspace/`** — the studio. One folder per business (`locuz`, `psiativa`). Each business has its own `_config/` (voice, positioning, ICP, design principles), `clients/`, `projects/`, and `skills/`.

## Reading order on every turn

1. This file (`CLAUDE.md`) — who and what.
2. [`CONTEXT.md`](CONTEXT.md) — routing: where does the user's request belong?
3. The `CLAUDE.md` and/or `CONTEXT.md` of the relevant business or stage folder (Layer 2).
4. Only the references that stage actually needs (Layer 3).
5. The working artifact you are editing or producing (Layer 4).

Do **not** preload the entire workspace. Load lean, load late.

> **For project-specific logic, refer to the `CLAUDE.md` located within the individual project directories.** This root file holds only global identity and conventions. Tone, ICP, positioning, client conventions, and stage rules live inside each project folder (e.g. [`workspace/locuz/CLAUDE.md`](workspace/locuz/CLAUDE.md), [`workspace/psiativa/CLAUDE.md`](workspace/psiativa/CLAUDE.md), [`knowledge/CLAUDE.md`](knowledge/CLAUDE.md)). Do not duplicate that material here.

## How to behave

- **One stage, one job.** If the request spans multiple stages, name them and ask where to start. Don't silently bundle.
- **Plain text only.** Markdown for prose, JSON for structured data. No binaries, no databases.
- **Every output is an edit surface.** Write to the stage's `output/` (or the project's working folder) so a human can read, edit, and pass it on.
- **Configure the factory, not the product.** Stable preferences belong in `_config/` or `knowledge/.../principles/`. Per-run material belongs in the project folder.
- **Respect the boundary between `knowledge/` and `workspace/`.** `knowledge/` is the library — append carefully, don't mutate to fit a single project. `workspace/<business>/_config/` is where business-specific style lives.

## When in doubt

- Unclear which business or project a request belongs to → ask.
- A skill exists for the task → use it instead of improvising.
- A reference seems missing → propose adding it to the right `knowledge/` folder rather than inlining.

The factory stays stable; the products change with each run.
