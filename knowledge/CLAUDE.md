# Knowledge — Library Identity (Layer 2)

You are inside the **library**. Read-mostly. Append-careful. This folder feeds every business workspace; treat changes here as edits to shared infrastructure.

## What lives here

```
knowledge/
  coding/  design/  marketing/  sales/    ← domains
    articles/  books/  courses/  guides/  principles/
  skills/                                  ← reusable procedures (cross-business)
  sources/                                 ← raw, uncompiled inputs
```

- **`<domain>/<form>/`** — compiled context packs, one source per file. Compact, AI-readable, citation-friendly.
- **`<domain>/principles/`** — distilled rules extracted from multiple sources in that domain.
- **`skills/`** — procedures that work across `locuz` and `psiativa` (e.g. [`knowledge-compiler/`](skills/knowledge-compiler/)). Each contains a `SKILL.md`.
- **`sources/`** — raw material before compilation. Do not let raw sources leak into a domain folder.

## Rules of the library

- **Append, don't mutate to fit a single project.** If a project needs a tweak, override it in `workspace/<business>/_config/`, not here.
- **One source, one file.** Use the [`knowledge-compiler`](skills/knowledge-compiler/) skill to produce these — don't improvise the format.
- **Promote, don't duplicate.** A skill that emerges in a business workspace stays there until it's used by both businesses; only then promote it to `skills/`.
- **Principles are earned, not asserted.** Add to `<domain>/principles/` only after a pattern shows up across multiple compiled sources.

## When in doubt

- New raw material → drop into `sources/`, then compile.
- Unclear which domain → ask. Cross-domain pieces usually belong to the dominant frame, with a one-line cross-reference.
- A skill might apply elsewhere → leave it in the business workspace until proven; promotion is cheap, demotion is messy.
