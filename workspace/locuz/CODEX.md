# Locuz - Codex Context

You are working inside the Locuz business workspace. Locuz is the parent growth consultancy ecosystem: it helps companies turn digital presence into measurable, scalable results through technology and digital strategy. `workspace/psiativa/` is a vertical branch of Locuz for psychology-clinic GTM.

This file is the Codex companion to `CLAUDE.md`. Inherit the root `CODEX.md`, then apply this file for anything under `workspace/locuz/`. Use `CONTEXT.md` for routing inside this workspace.

## Shape

```text
locuz/
  _config/
  clients/
  projects/
  skills/
```

- `_config/` is the factory: voice, positioning, ICP, and design defaults.
- `clients/` contains one folder per client engagement.
- `projects/` contains internal initiatives not tied to a single client.
- `skills/` contains Locuz-specific repeatable procedures.

## Reading Order

1. Root `CODEX.md`.
2. `workspace/locuz/CODEX.md`.
3. `workspace/locuz/CONTEXT.md`.
4. The relevant client, project, stage, skill, or `_config/` files.
5. The artifact being edited or produced.

Load only what the current stage needs.

## Factory And Overrides

- Business defaults live in `_config/`.
- Load only the relevant config file: `voice.md`, `positioning.md`, `icp-personas.md`, or `design-principles.md`.
- Client `_config/` overrides business `_config/` when both define the same thing.
- Never write per-run material into `_config/`.
- Never mutate `../../knowledge/` to fit one Locuz client. Override locally.

## Clients And Projects

- New engagement: copy `clients/client-template/`, fill its `CONTEXT.md`, then add any `_config/` overrides.
- Continue an engagement: work inside the relevant `clients/<slug>/stages/NN_*/` folder.
- Internal builds belong under `projects/<project-slug>/`.
- Stage numbering is the execution contract: `01_discovery`, `02_positioning`, `03_landing-page`, `04_handoff`.
- Each stage's `output/` becomes the next stage's input. If output exists, continue from it instead of regenerating.

## Skills

- Use `skills/<skill-slug>/` for Locuz-specific recurring workflows.
- If a procedure also becomes useful for Psiativa, propose promoting it to `../../knowledge/skills/` instead of copying it.
- Each skill should have a `SKILL.md` with trigger, inputs, steps, and expected output.

If a request spans multiple clients, projects, or stages, name the ambiguity and ask where to start.

