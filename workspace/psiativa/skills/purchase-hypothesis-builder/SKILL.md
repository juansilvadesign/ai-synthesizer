---
name: purchase-hypothesis-builder
description: Turn a raw list of 30–50 psychology clinics or solo practitioners into a scored, tiered attack list. Each entry gets five qualifying signal scores, a tier classification (A/B/C), an ICP profile (A or B), and a pre-formed product hypothesis — so the first outreach message already knows what it's selling.
trigger: User has a raw list of prospect names or Instagram handles and asks to "qualificar a lista", "montar a hipótese de compra", "classificar os alvos", "priorizar a lista", or "qual produto faz sentido pra cada um". Also fires when building a prospecting list from scratch (Google Maps, Instagram search, referral).
---

# Purchase Hypothesis Builder — PsiAtiva

A list-level qualification skill. The 2-minute diagnostic goes deep on one profile; this skill goes wide across 30–50 in a single pass. The output is not a contact database — it is a commercial hypothesis: every Tier A entry already has an ICP classification, a visible pain signal, and a product hypothesis before the first message is written.

## Knowledge base

- [`knowledge/sales/articles/oultimomentor/101_agencia.md`](../../../../knowledge/sales/articles/oultimomentor/101_agencia.md) — Phase 4: five qualifying signals, enrichment workflow, tier A/B/C logic, "lista como hipótese de compra"
- [`knowledge/sources/101_agência/16_Seu outbound morre antes do script.md`](../../../../knowledge/sources/101_agência/16_Seu outbound morre antes do script se a sua lista.md) — source: minimum useful data per entry, signal reading from Maps + Instagram
- [`workspace/psiativa/_config/esteira-de-produtos.md`](../../_config/esteira-de-produtos.md) — product routing by ICP + revenue + pain signal; qualification routing tables
- [`workspace/psiativa/_config/icp-clinica.md`](../../_config/icp-clinica.md) — Perfil A signals: what a qualifying clinic looks like
- [`workspace/psiativa/_config/icp-consultorio-solo.md`](../../_config/icp-consultorio-solo.md) — Perfil B signals: what a qualifying solo practitioner looks like
- [`workspace/psiativa/skills/diagnostico-2min/SKILL.md`](../diagnostico-2min/SKILL.md) — downstream: Tier A entries from this list go through the full diagnostic before outreach

---

## Input

A raw list of prospects. Each entry needs at minimum:
- Name (person or clinic)
- Instagram handle or Google Maps listing
- City

If you have nothing more than names: open Maps or Instagram and collect the minimum data for each before scoring. A list of names without any reading is not a hypothesis — it is a phone book.

---

## Step 1 — ICP Classification

Before scoring, classify each entry as Perfil A (clínica com equipe) or Perfil B (psicóloga autônoma). This determines which product track applies and which signals matter most.

| Signal | Perfil A | Perfil B |
|---|---|---|
| Profile mentions "equipe", multiple therapists, or receptionist | ✅ | |
| Single practitioner name, no team signals | | ✅ |
| "Consultório" or "atendimento individual" in bio | | ✅ |
| "Clínica", "espaço", "centro" in name or bio | ✅ | |
| Google Maps shows multiple professionals or reviews mentioning staff | ✅ | |
| Instagram posts show solo practitioner only | | ✅ |

**If unclear from available data:** classify as "uncertain" and note it — do not force a classification. This will be confirmed in the diagnostic or by Renata in Stage 2 (ICP profile identification).

---

## Step 2 — Score the Five Qualifying Signals

For each entry, score each signal as ✅ (present), ❌ (absent), or 🔍 (unclear — needs more data). Each check takes under 60 seconds.

---

### Signal 1 — Demanda

> Does this business already have visible demand? Are people looking for them?

**What to check:**
- Google Maps reviews (10+ = strong; 5–9 = moderate; <5 = weak)
- Google Maps listing exists and is active (hours, photos, description filled)
- Instagram: posting at least 1–2x/week in the last 30 days
- Engagement that suggests real patients (comments, DMs, saves)
- Bio or profile indicates time in operation (3+ years = established)

**Signal ✅ when:** listing exists with 5+ reviews OR active Instagram with consistent posts OR bio shows 3+ years in operation  
**Signal ❌ when:** no Google Maps listing, 0–2 reviews, last post 30+ days ago, no visible activity  
**Signal 🔍 when:** listing exists but profile is sparse, or activity is inconsistent

---

### Signal 2 — Problema

> Is there a visible commercial gap — something you can see from the outside without a call?

**What to check (run a light version of the diagnostic):**
- Bio vague, no specialty, no city, no CTA → Clareza failure
- No WhatsApp link, link broken, "manda direct" only → Contato failure
- Visual inconsistency, amateur design, no pattern → Percepção failure
- No faces, no space photos, <5 Google reviews, no proof → Prova failure
- Feed with no CTA, content without commercial direction → Direção Comercial failure

**Signal ✅ when:** 2+ of the five diagnostic checks fail visibly  
**Signal ❌ when:** profile is well-structured, CTA present, reviews exist — minimal gap  
**Signal 🔍 when:** one area looks weak but not clearly broken

---

### Signal 3 — Capacidade

> Does this business have the minimum structure and revenue to invest?

**What to check:**
- **Perfil A:** 2+ therapists visible, own clinic space (not shared room rental), reviews suggesting consistent patient volume, website exists even if outdated
- **Perfil B:** Profile suggests 15+ patients (consistent activity), VPS ≥ R$150 inferred from specialty or city, 3+ years in practice (bio or Maps)
- Premium positioning signal: specialization (TCC, EMDR, psicoterapia analítica, etc.) = higher VPS = stronger capacity
- Location signal: private clinic in an upper-middle neighborhood = stronger capacity than shared space in periphery

**Signal ✅ when:** Perfil A with visible team and established operation; OR Perfil B with 3+ years, specialty signal, and consistent activity  
**Signal ❌ when:** profile appears inactive, no operating signals, student or newly graduated language  
**Signal 🔍 when:** profile is active but revenue/structure signals are unclear

---

### Signal 4 — Entregável Claro

> Before they respond, do you already know what you'd sell them?

Score this only after scoring Signals 1–3. The entregável hypothesis emerges from the combination of ICP + visible problem pattern.

**Hypothesis mapping (quick reference):**

| ICP + Visible Problem Pattern | Product Hypothesis | Notes |
|---|---|---|
| Perfil B + no Google Maps listing or <5 reviews | GBP (R$980) | Entry — can close without R1 |
| Perfil B + invisible on Google + poor Instagram | GBP Scale (R$1.480) | Entry — escalate to Renata |
| Perfil B + loses leads during session (solo, no process) | IA Solo | Standalone — escalate to Renata |
| Perfil B + Instagram with engagement, no conversion + oscillating schedule | P3K via R1 | Min. entry for structured package |
| Perfil B + R$7–15k revenue + clear agenda pain | P7K via R1 | Core product — full R1 |
| Perfil A + invisible on Google locally | GBP Scale (R$2.980) | Entry — escalate to Renata |
| Perfil A + WhatsApp process broken, team of 2–5 | P3K via R1 | Entry package |
| Perfil A + R$15–30k, 2–10 therapists, receptionist overwhelmed | P7K via R1 | Core product — full R1 |
| Perfil A + R$30k+, 5+ therapists, authority positioning goal | P10K via R1 | High-ticket anchor — full R1 |
| Multiple issues, ICP unclear | Schedule R1 — diagnose before hypothesizing | Do not guess |

**Signal ✅ when:** one or two clear product hypotheses emerge from the visible data  
**Signal ❌ when:** no clear gap visible, or profile too sparse to read  
**Signal 🔍 when:** there's a visible problem but ICP profile is not confirmed enough to map to a product

---

### Signal 5 — Timing

> Is there any signal that makes now better than in 3 months?

**What to check:**
- New opening or location change visible in recent posts
- Active competitor in same area with strong Google Maps presence (threat urgency — they are losing patients now)
- NR-1 2026 context: Perfil B with potential corporate clients / company focus
- Low review count next to a competitor with 50+ (visible competitive gap — she may not even know)
- Recent post expressing frustration with schedule volatility, growth, or process
- January–February seasonality (therapy demand spikes post-holiday and at year-start)

**Signal ✅ when:** one or more timing signals are visible  
**Signal ❌ when:** no timing urgency visible — stable, no competitive pressure, no expansion signal  
**Signal 🔍 when:** competitor context is visible but prospect's own situation is unknown

---

## Step 3 — Tier Classification

Count the ✅ scores (confirmed signals). Treat 🔍 as 0 for scoring — incomplete data does not qualify.

| Score | Tier | Action |
|---|---|---|
| 3–5 ✅ | **A — Abordagem agora** | Run full diagnostic (diagnostico-2min), then outreach (contextual-outreach) |
| 2 ✅ | **B — Potencial, não agora** | Watch list — revisit in 30 days or when more data available |
| 0–1 ✅ | **C — Ruído** | Remove from list — not worth the contact cycle time |

**Rule:** never approach a Tier B or C entry because the list looks thin. Better to have 15 Tier A entries than 100 mixed. Tier B is not "approach with lower energy" — it is genuinely not ready.

---

## Step 4 — Enrichment Table

After scoring, capture the minimum useful data per entry. This is what the list looks like before outreach begins.

```
| # | Name / Handle | City | ICP | D | P | Ca | E | T | Score | Tier | Product Hypothesis | Decisor | Next Step |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | @clinica_xyz | Campinas | A | ✅ | ✅ | ✅ | ✅ | 🔍 | 4 | A | P7K via R1 | Owner (appears in posts) | Run diagnostic |
| 2 | @dra_carol | São Paulo | B | ✅ | ✅ | 🔍 | ✅ | ❌ | 3 | A | GBP Scale | Solo | Run diagnostic |
| 3 | @espaco_zen | Curitiba | A | ❌ | ✅ | ❌ | ✅ | ❌ | 2 | B | — | Unknown | Watch 30d |
| 4 | @psi_fulano | Remote only | B | ❌ | ❌ | 🔍 | ❌ | ❌ | 0 | C | — | — | Remove |
```

**Column key:** D=Demanda, P=Problema, Ca=Capacidade, E=Entregável, T=Timing

---

## Step 5 — Attack Sequence

From the scored list, extract the Tier A entries and order them for attack. Attack order within Tier A:

1. **Strongest signal count first** (5 > 4 > 3)
2. **Tie-break: timing signal present** — competing pressures or visible urgency first
3. **Tie-break: ICP classification confirmed** — "uncertain" entries go last within the tier
4. **Tie-break: clear product hypothesis** — entries where the deliverable is obvious outperform entries needing more R1 discovery

Run the full diagnostic (`diagnostico-2min`) for the top 10 Tier A entries before writing any messages. Do not build 50 outreach messages at once — attack in batches of 10, learn from response patterns, adjust the hypothesis before the next batch.

---

## Subgroup Refinement — PsiAtiva Context

Do not build a list of "psicólogas". Build a list of a specific subgroup.

**Perfil A examples:**
- Clínicas de psicologia urbanas em capitais e cidades médias, 2–8 terapeutas, presença digital ativa mas sem lógica comercial, faixa de faturamento R$15–30k/mês
- Clínicas multidisciplinares (psicologia + nutrição + fisioterapia) com Instagram ativo mas agenda preenchida por indicação apenas

**Perfil B examples:**
- Psicólogas autônomas em Pinheiros, Consolação, Moema ou outros bairros com alta densidade de planos de saúde e demanda clínica, 3–6 anos de carreira, consultas entre R$150–250
- Psicólogas especializadas (TCC, psicanálise, EMDR) com Instagram com engajamento mas zero conversão em paciente

**A list built by subgroup** produces higher Tier A density. A generic "psychologist list" from all of São Paulo produces low density and low signal quality.

---

## Useful Sources for List Building — Psychology Niche

| Source | What it reveals |
|---|---|
| **Google Maps** — "psicólogo [bairro/cidade]" | Review count, listing quality, local competition density |
| **Instagram search** — "#psicologaclinica", "#terapiasp", "#tcc[cidade]" | Active practitioners, posting frequency, commercial vs. content focus |
| **CRP regional websites** | Registered professionals by specialty and location — use for verification, not prospecting |
| **Google search** — "psicólogo clínico [bairro] WhatsApp" | Practitioners with pages but weak SEO structure — signal for Site/LP and GBP |
| **Indication from current clients** | Highest quality signal — psychologists trust peer referrals; ask clients who they know |

---

## Watch out for

- **Classifying every entry as Tier A to inflate the list** — if 80% of the list is Tier A, the scoring was not rigorous. A well-scored list of 50 typically produces 10–20 Tier A entries.
- **Assigning a product hypothesis before the ICP is confirmed** — showing clinic pricing to a solo practitioner doubles the perceived investment and kills the deal before it starts. Mark ICP as "uncertain" and confirm in Stage 2 of Renata's flow.
- **Treating 2-signal entries (Tier B) as soft Tier A** — the difference between 2 and 3 signals is a full tier, not a small gap. Tier B exists to revisit in 30 days, not to approach now with lower energy.
- **Skipping Signal 3 (Capacidade) because the problem is obvious** — a clear Problema + clear Demanda with no Capacidade signal produces a lead that cannot buy. Visible problem ≠ ability to invest.
- **Building a list of 200 and calling it thorough** — 200 unscored entries is a phone book, not a commercial hypothesis. 30 scored entries outperform 200 unscored every time.
- **Using any product's technical name in the hypothesis column** — write "GBP" or "P7K via R1" for internal tracking only; never say "Google Business Profile" or "P7K" to the prospect.

---

## See also

- [`workspace/psiativa/skills/diagnostico-2min/SKILL.md`](../diagnostico-2min/SKILL.md) — downstream step 1: run this on every Tier A entry before writing the outreach message.
- [`workspace/psiativa/skills/contextual-outreach/SKILL.md`](../contextual-outreach/SKILL.md) — downstream step 2: uses the diagnostic output to write the first message.
- [`workspace/psiativa/_config/esteira-de-produtos.md`](../../_config/esteira-de-produtos.md) — product qualification routing tables for both ICP tracks; confirms or adjusts the hypothesis after R1.
- [`knowledge/sources/101_agência/16_Seu outbound morre antes do script.md`](../../../../knowledge/sources/101_agência/16_Seu outbound morre antes do script se a sua lista.md) — source: list as commercial hypothesis, minimum useful data, tier logic.
