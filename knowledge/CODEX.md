# Knowledge - Codex Context

You are inside the shared library. This folder feeds every business workspace, so changes here are edits to shared infrastructure, not one-off project work.

This file is the Codex companion to `CLAUDE.md`. Inherit the root `CODEX.md`, then apply this file for anything under `knowledge/`. If a specific skill has its own `SKILL.md` or local instructions, load only the relevant files for that task.

## What Lives Here

```text
knowledge/
  coding/
  design/
  marketing/
  sales/
    articles/
    books/
    courses/
    guides/
    principles/
  skills/
  sources/
```

- `knowledge/<domain>/<form>/` holds compiled context packs. One source, one file.
- `knowledge/<domain>/principles/` holds distilled reusable rules extracted from multiple sources.
- `knowledge/skills/` holds reusable procedures that work across more than one business workspace.
- `knowledge/sources/` holds raw, uncompiled inputs.

## Operating Rules

- Treat this folder as read-mostly and append-careful.
- Do not mutate shared knowledge to fit one client, project, or campaign.
- If a business needs a local tweak, put the override in `workspace/<business>/_config/`.
- Do not let raw sources leak into compiled domain folders.
- Use the `knowledge-compiler` skill when compiling sources instead of inventing a new format.
- Add principles only when a pattern appears across multiple compiled sources.
- Promote business-specific skills to `knowledge/skills/` only after they are useful across both Locuz and Psiativa.

## Routing

- New raw source: place or reference it under `knowledge/sources/`, then compile.
- Article, book, course, or guide compilation: route to the matching `knowledge/<domain>/<form>/` folder.
- Reusable principle extraction: route to `knowledge/<domain>/principles/`.
- Cross-business procedure: route to `knowledge/skills/<skill>/`.
- One-business procedure: keep it under `workspace/<business>/skills/`.

If the dominant domain is unclear, ask before filing. Cross-domain pieces usually belong to the dominant frame with a short cross-reference.

