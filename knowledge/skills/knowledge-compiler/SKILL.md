---
name: knowledge-compiler
description: Compile a raw learning source (article, book, course, guide) into a compact, AI-readable context pack that can be cited from any workspace.
trigger: User shares a source — link, PDF, transcript, notes — and asks to "compile", "summarise into a context pack", "extract principles from", or "add to knowledge".
---

# Knowledge Compiler

A single skill that turns one source into one context pack. Routes by source type to the right playbook.

## When to fire

- Source is a complete piece of learning material (not a one-off quote or screenshot).
- Output will be **reused** across projects — otherwise inline-summarise instead.
- The source belongs to a known domain: `coding`, `design`, or `marketing`. If none fits, **ask** before creating a new domain.

## Routing — pick the playbook

| Source type | Playbook | Output folder |
|---|---|---|
| Standalone article, essay, blog post, paper | [`article.md`](article.md) | `knowledge/<domain>/articles/` |
| Book or long-form text with chapters | [`book.md`](book.md) | `knowledge/<domain>/books/` |
| Course, workshop, video series | [`course.md`](course.md) | `knowledge/<domain>/courses/` |
| Practitioner guide, playbook, framework write-up | [`guide.md`](guide.md) | `knowledge/<domain>/guides/` |

If the source is mixed (e.g. a course with an accompanying book), compile each form **separately** and cross-link them at the bottom of each pack. One source, one pack — never bundle.

## Shared output contract

Every compiled pack is a single markdown file using this skeleton:

```markdown
---
title: <source title>
author: <author(s)>
type: article | book | course | guide
domain: coding | design | marketing
source: <URL if available; otherwise publisher / citation>
compiled: <YYYY-MM-DD>
tokens_estimate: <rough count>
---

## TL;DR
<3–5 sentences. What this source claims and why it matters.>

## Core ideas
<Bulleted list of the load-bearing claims. One sentence each.>

## Frameworks / models
<Named structures the source introduces, with a one-line definition each.>

## Quotes worth keeping
<Verbatim, with location reference. Sparing — only what's reusable.>

## How to apply
<When to reach for this pack: trigger + the move it unlocks.>

## See also
<Cross-links to related packs in knowledge/.>
```

Filename: `<slug-of-title>.md` (kebab-case, no dates).

## Hard rules

- **One source, one pack.** Never merge two sources into one file.
- **No paraphrased verbatim copies.** A pack is a *compression*, not a transcript.
- **Append, don't mutate.** If a pack already exists, propose an update — don't silently overwrite.
- **Cite the source.** Every pack must carry a `source:` in its frontmatter. Prefer a working URL. Only fall back to publisher / citation when no canonical URL exists (e.g. a printed book without an official online edition).
- **Stay under ~2k tokens per pack.** If you can't compress it that far, the source probably needs splitting.

## Domain placement

If unsure which domain owns the source, look at *what the reader will use it for*, not the surface topic. A book on visual hierarchy used for landing-page copy decisions belongs in `marketing/` if that's where it'll be cited. Cross-link from `design/` if useful.
