# Psiativa — Project Identity (Layer 2)

You are working inside the **psiativa** business workspace. PsiAtiva is a consultancy that gives psychology clinics and private practices predictable schedules, fewer no-shows, and a structured (non-salesy) patient acquisition process that preserves clinical identity — Google, WhatsApp, and digital presence, with ethics and measurable results. It is a **vertical branch of the [`locuz/`](../locuz/) ecosystem** (Locuz's growth playbook applied to the psychology niche), and it grew out of the FastScale 1:1 mentoring track.

For routing (clients, projects, skills, stages), see [`CONTEXT.md`](CONTEXT.md).

## Project-specific logic

- **Factory lives in [`_config/`](_config/).** Load only what the current stage needs:
  - [`voice.md`](_config/voice.md), [`positioning.md`](_config/positioning.md), [`marca-identidade-visual.md`](_config/marca-identidade-visual.md) — surface-level identity
  - [`icp-personas.md`](_config/icp-personas.md), [`icp-clinica.md`](_config/icp-clinica.md), [`icp-consultorio-solo.md`](_config/icp-consultorio-solo.md) — audience segments; pick the one that matches the engagement
  - [`comercial-playbook.md`](_config/comercial-playbook.md), [`esteira-de-produtos.md`](_config/esteira-de-produtos.md), [`sdr-renata.md`](_config/sdr-renata.md) — sales motion and offer ladder
- **Two distinct ICPs.** Solo psychologists (`icp-consultorio-solo`) and clinic owners (`icp-clinica`) need different positioning, pricing, and tone. Confirm which one applies before writing copy.
- **Sales/commercial skills are central.** Most procedures in [`skills/`](skills/) (e.g. [`spin-question-engine`](skills/spin-question-engine/), [`closing-mechanic`](skills/closing-mechanic/), [`objection-isolator`](skills/objection-isolator/), [`reactivation-cadence`](skills/reactivation-cadence/)) implement the commercial playbook. Use them — don't improvise sales scripts.
- **Client overrides win.** `clients/<slug>/_config/` beats `_config/` on conflict. Active client: [`leonardo-lima/`](clients/leonardo-lima/).

## Working defaults

- Portuguese (BR) is the default language for any client-facing copy unless explicitly stated otherwise.
- Sales / outreach output should pass through the matching skill in [`skills/`](skills/) rather than being written ad-hoc.
- Voice is anchored to a specific psychology-aware tone — read [`voice.md`](_config/voice.md) before writing anything user-facing, even short messages.
- Stage `output/` is an edit surface; humans edit between stages. Pick up what's there, don't regenerate.

## Hard rules

- **Never** mix the two ICPs in a single deliverable. Pick one frame.
- **Never** write per-run material into `_config/` — that's the factory.
- **Never** mutate `../../knowledge/` to fit a psiativa client. Override locally.
- If a request spans multiple clients, stages, or ICPs, name them and ask where to start. Don't silently bundle.
