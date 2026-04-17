# Locuz — Workspace Contract (Layer 2)

> **About this business:** _<one or two lines: what locuz does, who it serves, what kind of work runs through here>_

## Shape

```
locuz/
  _config/         ← factory: voice, positioning, ICP, design (loaded by every stage)
  clients/         ← one folder per client (see client-template/)
  projects/        ← internal initiatives not tied to a single client
  skills/          ← business-specific procedures (audits, repeatable workflows)
```

## The factory — `_config/`

Read these only when their content is relevant to the current stage:

- [`voice.md`](_config/voice.md) — tone, vocabulary, do/don't list.
- [`positioning.md`](_config/positioning.md) — what locuz claims, against whom, for whom.
- [`icp-personas.md`](_config/icp-personas.md) — who the work is for.
- [`design-principles.md`](_config/design-principles.md) — visual and structural defaults.

If a stage doesn't need positioning, don't load it. Layered loading > monolithic prompt.

## Clients — `clients/<client-slug>/`

Every client folder follows [`client-template/`](clients/client-template/):

```
<client>/
  CONTEXT.md       ← engagement summary, scope, current stage
  _config/         ← client-specific overrides of business config
  stages/
    01_discovery/
    02_positioning/
    03_landing-page/
    04_handoff/
```

Stage numbering = execution order. Each stage's `output/` becomes the next stage's input. Client `_config/` overrides business `_config/` when both define the same key.

## Projects — `projects/<project-slug>/`

Internal builds (e.g. [`landing-page-v2`](projects/landing-page-v2/), [`pitch-deck-hub`](projects/pitch-deck-hub/)). Same shape as clients, but stages reflect the artefact being built rather than an engagement arc.

## Skills — `skills/<skill-slug>/`

Repeatable procedures specific to locuz (e.g. [`landing-page-audit`](skills/landing-page-audit/), [`seo-audit`](skills/seo-audit/)). Each should contain a `SKILL.md` describing trigger, inputs, steps, output. If a procedure becomes useful across both businesses, promote it to [`knowledge/skills/`](../../knowledge/skills/).

## Routing inside locuz

| Request | Route to |
|---|---|
| New engagement | Copy `clients/client-template/` → `clients/<slug>/`, fill its `CONTEXT.md` |
| Continue an engagement | The relevant `clients/<slug>/stages/NN_*/` |
| Update locuz's voice/positioning/ICP | `_config/` |
| Run a recurring audit | `skills/<skill>/` |

When unsure which client or project owns a request, **ask** before writing.
