# Psiativa - Codex Context

You are working inside the PsiAtiva business workspace. PsiAtiva helps psychology clinics and private practices build predictable schedules, reduce no-shows, and create a structured, non-salesy patient acquisition process that preserves clinical identity through Google, WhatsApp, and digital presence.

PsiAtiva is a vertical branch of the Locuz ecosystem: Locuz's growth playbook applied to the psychology niche, influenced by the FastScale 1:1 mentoring track.

This file is the Codex companion to `CLAUDE.md`. Inherit the root `CODEX.md`, then apply this file for anything under `workspace/psiativa/`. Use `CONTEXT.md` for routing inside this workspace.

## Shape

```text
psiativa/
  _config/
  clients/
  projects/
  skills/
```

- `_config/` is the factory: voice, positioning, ICP, brand, design, sales motion, and offer ladder.
- `clients/` contains one folder per client engagement.
- `projects/` contains internal initiatives not tied to one client.
- `skills/` contains PsiAtiva-specific repeatable procedures.

## Reading Order

1. Root `CODEX.md`.
2. `workspace/psiativa/CODEX.md`.
3. `workspace/psiativa/CONTEXT.md`.
4. The relevant client, project, stage, skill, or `_config/` files.
5. The artifact being edited or produced.

Load only what the current task needs.

## Factory And Overrides

Load factory files selectively:

- Surface identity: `_config/voice.md`, `_config/positioning.md`, `_config/marca-identidade-visual.md`.
- Audience segments: `_config/icp-personas.md`, `_config/icp-clinica.md`, `_config/icp-consultorio-solo.md`.
- Sales motion: `_config/comercial-playbook.md`, `_config/esteira-de-produtos.md`, `_config/sdr-renata.md`.
- Design defaults: `_config/design-principles.md` when visual or structural choices matter.

Client `_config/` overrides business `_config/`. The currently named active client is `clients/leonardo-lima/`.

Never write per-run material into `_config/`. Never mutate `../../knowledge/` to fit a PsiAtiva client. Override locally.

## ICP Rules

PsiAtiva has two distinct ICPs:

- Solo psychologists: use `icp-consultorio-solo.md`.
- Clinic owners: use `icp-clinica.md`.

Confirm or infer the ICP before writing copy. Never mix the two ICPs in a single deliverable.

## Language And Voice

- Portuguese (BR) is the default for client-facing copy unless the user says otherwise.
- Read `_config/voice.md` before writing anything user-facing, even short messages.
- Keep the tone psychology-aware, ethical, concrete, and non-salesy.

## Clients, Projects, And Stages

- New engagement: copy `clients/client-template/`, fill its `CONTEXT.md`, then add any `_config/` overrides.
- Continue an engagement: work inside the relevant `clients/<slug>/stages/NN_*/` folder.
- Internal builds belong under `projects/<project-slug>/`.
- Stage `output/` folders are edit surfaces. If output exists, continue from it instead of regenerating.

## Skills

Sales and commercial skills are central to PsiAtiva. Use the matching skill instead of improvising sales scripts, especially for:

- `spin-question-engine`
- `closing-mechanic`
- `objection-isolator`
- `reactivation-cadence`
- `contextual-outreach`
- `purchase-hypothesis-builder`
- `offer-validator`

If a procedure becomes useful across both Locuz and PsiAtiva, propose promoting it to `../../knowledge/skills/`.

If a request spans multiple clients, stages, or ICPs, name the ambiguity and ask where to start.
