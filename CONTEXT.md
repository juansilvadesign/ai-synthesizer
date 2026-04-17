# Workspace Routing

Use this file to decide **where a request belongs** before touching anything else.

## Top-level map

```
ai-synthesizer/
  knowledge/              ← shared library (Layer 3, read-mostly)
    coding/  design/  marketing/
      articles/  books/  courses/  principles/
    skills/               ← reusable compilation procedures
  workspace/              ← active work (Layer 4)
    locuz/                ← business workspace
    psiativa/             ← business workspace
```

## Routing rules

| Request looks like… | Route to |
|---|---|
| "Summarise / compile this article, book, or course" | `knowledge/<domain>/<form>/` using the matching skill in `knowledge/skills/knowledge-compiler/` |
| "Distil principles from these sources" | `knowledge/<domain>/principles/` |
| "Work on a client deliverable" | `workspace/<business>/clients/<client>/` |
| "Work on an internal project (landing page, deck, audit)" | `workspace/<business>/projects/<project>/` |
| "Update voice, positioning, ICP, or design principles" | `workspace/<business>/_config/` |
| "Run an audit or repeatable workflow for a business" | `workspace/<business>/skills/<skill>/` |

If two routes apply, ask. Don't silently choose.

## Active businesses

- **`locuz/`** — see [`workspace/locuz/CONTEXT.md`](workspace/locuz/CONTEXT.md) when present.
- **`psiativa/`** — see [`workspace/psiativa/CONTEXT.md`](workspace/psiativa/CONTEXT.md) when present.

Each business has the same shape: `_config/` (factory), `clients/`, `projects/`, `skills/`.

## Shared skills

- [`knowledge/skills/knowledge-compiler/`](knowledge/skills/knowledge-compiler/) — turns a source (article, book, course) into a compact context pack.
- Add new shared skills here only when the procedure is stable and used across more than one business.

## What lives where (the factory/product distinction)

- **Factory (Layer 3, stable):** `knowledge/**`, `workspace/<business>/_config/`, all `skills/`.
- **Product (Layer 4, per-run):** anything under `workspace/<business>/clients/` or `workspace/<business>/projects/`.

Never write per-run output into the factory. Never bury stable configuration inside a project folder.
