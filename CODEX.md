# AI Synthesizer - Codex Operating Context

You are working inside an Interpretable Context Methodology (ICM) workspace. The filesystem is the orchestration layer: folders are stages, Markdown files are contracts, and outputs are meant to stay editable by a human.

This file is Codex's repo-level context. It was synthesized from every `CLAUDE.md` currently in the repo plus the root and Psiativa `CONTEXT.md` files. When a more specific `CODEX.md`, `CLAUDE.md`, `CONTEXT.md`, or `SKILL.md` applies to the folder you are working in, treat that local file as the stronger rule.

## What This Repo Is

`ai-synthesizer/` is a personal knowledge synthesizer and delivery studio.

- `knowledge/` is the shared library: raw sources, compiled context packs, principles, and reusable cross-business skills.
- `workspace/` is active business work: one folder per business, with `_config/`, `clients/`, `projects/`, and `skills/`.
- `workspace/locuz/` is the parent growth consultancy ecosystem.
- `workspace/psiativa/` is a psychology-clinic GTM consultancy and vertical branch of Locuz.

The core distinction is factory versus product:

- Factory: `knowledge/**`, `workspace/<business>/_config/`, and `skills/`.
- Product: per-run work under `workspace/<business>/clients/**` and `workspace/<business>/projects/**`.

Do not bury stable configuration inside product folders. Do not write per-run outputs into factory folders.

## Reading Order

Before editing or producing a deliverable, load context in this order:

1. `CODEX.md` for Codex-specific repo rules.
2. `CONTEXT.md` at the repo root for routing.
3. The relevant folder's `CODEX.md`, `CLAUDE.md`, and/or `CONTEXT.md`.
4. Only the `_config/`, client, project, skill, or source files needed for the current stage.
5. The working artifact you will edit or create.

Load lean and late. Do not preload the entire workspace.

## Routing Rules

Use `CONTEXT.md` to decide where the request belongs before touching files.

- Summarize or compile articles, books, courses, or guides: route to `knowledge/<domain>/<form>/` and use the relevant compiler skill if present.
- Distill reusable principles: route to `knowledge/<domain>/principles/`.
- Work on client deliverables: route to `workspace/<business>/clients/<client>/`.
- Work on internal initiatives: route to `workspace/<business>/projects/<project>/`.
- Update voice, positioning, ICP, design, sales motion, or brand defaults: route to `workspace/<business>/_config/`.
- Run repeatable procedures: route to `workspace/<business>/skills/<skill>/` or `knowledge/skills/<skill>/`, depending on scope.

If two businesses, clients, stages, or ICPs clearly apply at once, name the ambiguity and ask where to start.

## Workspace Defaults

### Knowledge

`knowledge/` is read-mostly shared infrastructure.

- Append carefully; do not mutate shared knowledge to fit one client or project.
- Raw material belongs in `knowledge/sources/` before compilation.
- Compiled material belongs in the appropriate `knowledge/<domain>/<form>/` folder.
- Cross-business skills belong in `knowledge/skills/` only after the procedure is useful across more than one business.
- Principles should be extracted from repeated patterns across sources, not asserted from one-off preference.

### Locuz

`workspace/locuz/` is the parent growth consultancy.

- Load `workspace/locuz/CLAUDE.md` and `workspace/locuz/CONTEXT.md` for Locuz work.
- Business defaults live in `workspace/locuz/_config/`.
- Client `_config/` overrides business `_config/`.
- Stage numbering is part of the execution contract; do not reorder or skip stages silently.
- If a Locuz-specific skill becomes useful for Psiativa too, propose promotion to `knowledge/skills/` instead of copying.

### Psiativa

`workspace/psiativa/` is a psychology-clinic and private-practice GTM consultancy focused on predictable schedules, fewer no-shows, ethical patient acquisition, Google, WhatsApp, and digital presence.

- Load `workspace/psiativa/CLAUDE.md` and `workspace/psiativa/CONTEXT.md` for Psiativa work.
- Portuguese (BR) is the default language for client-facing Psiativa copy unless the user says otherwise.
- Read `workspace/psiativa/_config/voice.md` before writing user-facing copy.
- Pick the relevant ICP before writing: solo psychologists (`icp-consultorio-solo.md`) and clinic owners (`icp-clinica.md`) need different positioning, pricing, and tone.
- Do not mix the two Psiativa ICPs in a single deliverable.
- Use Psiativa commercial skills for sales and outreach workflows instead of improvising scripts.
- Client overrides win over business defaults. The currently named active client is `workspace/psiativa/clients/leonardo-lima/`.
- Do not mutate `knowledge/` to fit a Psiativa client; override locally.

## Local Skills And Special Repos

Several `CLAUDE.md` files live inside skill repositories. Use them only when working in that skill's folder or when the user explicitly asks for that skill's workflow.

- `knowledge/skills/scientific-writer/CLAUDE.md`: scientific writing workflow. It emphasizes complete execution, real verifiable citations, saved research artifacts, LaTeX/BibTeX by default, versioned drafts, figure-rich outputs, PDF review via page images, and final peer review. Adapt any Claude-specific tool names to the tools actually available to Codex.
- `knowledge/skills/ui-ux-pro-max/CLAUDE.md`: Antigravity Kit / UI-UX Pro Max guidance. Source of truth is `knowledge/skills/ui-ux-pro-max/src/ui-ux-pro-max/`; edit canonical data, scripts, and templates there, then sync CLI assets before publishing.
- `knowledge/skills/caveman/CLAUDE.md`: product-specific maintenance guidance for that skill repo. Respect its source-of-truth files, generated-file boundaries, benchmark/eval accuracy rules, hook safety rules, and README voice when working there.

For normal workspace deliverables, do not load these large skill contexts unless they are relevant.

## Editing And Output Rules

- Prefer small, scoped edits that match the existing folder contract.
- Preserve user edits and dirty worktree changes you did not make.
- Stage `output/` folders are edit surfaces. If output already exists, continue from it instead of regenerating from scratch.
- Markdown is the default prose format; JSON is for structured data.
- Keep stable preferences in `_config/` or shared principles, not inside one-off deliverables.
- Keep per-client or per-run material in the relevant client, project, or stage folder.
- When source material or context seems missing, propose adding it in the right folder rather than inlining it into an unrelated artifact.

## Codex Working Style

- Read first, then act decisively once the route is clear.
- Use existing local skills and templates before inventing a new procedure.
- For frontend work, follow the repo's design context first, then Codex's general frontend standards.
- For research or current information, verify with available tools and cite sources in the deliverable when appropriate.
- For ambiguous routing, ask a concise question. For ordinary implementation details, make a conservative choice aligned with the existing system.

The factory stays stable. The products change with each run.
