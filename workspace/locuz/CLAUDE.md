# Locuz — Project Identity (Layer 2)

You are working inside the **locuz** business workspace. Locuz is a growth consultancy that helps companies reach the next level — turning digital presence into measurable, scalable results through technology and digital strategy. It is the **parent ecosystem**; [`psiativa/`](../psiativa/) is a vertical branch of it (psychology-clinic GTM).

This file holds locuz-specific identity and conventions. For routing inside locuz (clients, projects, skills, stages), see [`CONTEXT.md`](CONTEXT.md).

## Project-specific logic

- **Voice, positioning, ICP, design** all live in [`_config/`](_config/). Load only the file the current stage needs.
- **Client overrides win.** A `clients/<slug>/_config/` value supersedes a business-level `_config/` value with the same key. If both exist, use the client one.
- **Stage numbering is the execution contract.** `01_discovery → 02_positioning → 03_landing-page → 04_handoff`. Do not reorder; do not skip. Each stage's `output/` is the next stage's input.
- **Skills here are locuz-specific.** If a procedure is also useful for psiativa, propose promoting it to [`../../knowledge/skills/`](../../knowledge/skills/) rather than copying.

## Working defaults

- New engagement → copy [`clients/client-template/`](clients/client-template/) → fill `CONTEXT.md` first, then `_config/` overrides, then start `stages/01_discovery/`.
- Internal builds → [`projects/<slug>/`](projects/) (same shape as clients, but stage names track the artefact).
- Stage `output/` is an edit surface — humans may edit between stages. Do not regenerate; pick up what's there.

## Hard rules

- **Never** write per-run material into `_config/`. Configure the factory, not the product.
- **Never** mutate `../../knowledge/` to fit a single locuz client. Override locally instead.
- If a request spans multiple clients or stages, name them and ask where to start. Don't silently bundle.

When the about-this-business line in [`CONTEXT.md`](CONTEXT.md) is still a placeholder, ask the user to fill it before producing positioning or voice work.
