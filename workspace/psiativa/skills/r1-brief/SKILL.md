---
name: r1-brief
description: Assemble a one-page R1 pre-call brief from five data sources — ICP config, Renata's NEPQ notes, diagnostic findings, product hypothesis, and prospect profile — into a single 2-3 minute read the closer uses immediately before the call. Output includes call objective, ICP mode, terrain classification, point-in-common, pain signal, pre-loaded SPIN sequence, product hypothesis with prices, and top 2 expected objections with reframes.
trigger: User has a scheduled R1 call and asks to "montar o briefing da call", "preparar a R1", "o que eu preciso saber antes da call", "me dá um resumo do prospect", or "prepara o material pra conversa de amanhã". Also fires after Renata confirms an R1 appointment in her routing notes.
---

# R1 Pre-Call Brief — PsiAtiva

An assembly skill. Every input needed for a well-run R1 already exists — in the diagnostic, in Renata's notes, in the ICP configs, in the product staircase, and in the SPIN engine. This skill pulls from all five, strips what does not change call-to-call, and produces a single brief the closer reads in under 3 minutes.

**The brief does not teach.** The closer already knows the method. The brief answers: who is this specific person, what is her specific pain, what do I open with, what do I sell, and what will she resist. Nothing else.

**This skill fires after:**
- Renata routes the prospect to Route A (R1 scheduled)
- Diagnostic completed for this prospect (at minimum a light 2-min pass)
- ICP classification confirmed

**This skill hands off to:**
- The R1 call itself, guided by `comercial-playbook.md` (Phases 1–3) with SPIN questions from `spin-question-engine` and close from `closing-mechanic`

## Knowledge base

- [`workspace/psiativa/_config/icp-clinica.md`](../../_config/icp-clinica.md) — Perfil A: DISC profile, pain inventory, desire inventory, objection bank, product fit
- [`workspace/psiativa/_config/icp-consultorio-solo.md`](../../_config/icp-consultorio-solo.md) — Perfil B: DISC profile, pain inventory, desire inventory, objection bank, product fit
- [`workspace/psiativa/_config/sdr-renata.md`](../../_config/sdr-renata.md) — Renata's NEPQ output: pain signal captured, terrain classification (ação/curiosidade), verbatim phrases
- [`workspace/psiativa/_config/comercial-playbook.md`](../../_config/comercial-playbook.md) — R1 Phase 1 (point-in-common rule), Phase 2 (NEPQ question sequence), Phase 3 (pitch sequence)
- [`workspace/psiativa/_config/esteira-de-produtos.md`](../../_config/esteira-de-produtos.md) — product prices by ICP track, anchoring sequence, qualification routing
- [`workspace/psiativa/skills/spin-question-engine/SKILL.md`](../spin-question-engine/SKILL.md) — pre-built SPIN banks by ICP × pain signal; pull directly into the brief
- [`workspace/psiativa/skills/diagnostico-2min/SKILL.md`](../diagnostico-2min/SKILL.md) — upstream: diagnostic findings feed the pain signal and the product hypothesis sections

---

## Input

Provide all of these. The brief degrades proportionally with each missing input — flag what is missing and note what was inferred.

| Input | Source | What it feeds |
|---|---|---|
| **Prospect name + handle/URL** | Outbound list or inbound contact | Point-in-common, profile read |
| **ICP classification** | Renata Stage 2 or diagnostic | Every section |
| **Terrain** | Renata Stage 4 | Call objective |
| **Pain signal** | Renata Stage 3 (NEPQ) or diagnostic | SPIN sequence, watch-outs |
| **Verbatim phrase (if captured)** | Renata Stage 3 | SPIN S question calibration |
| **Product hypothesis** | purchase-hypothesis-builder or Renata | Product section |
| **Faturamento estimate** | Renata NEPQ or profile read | Price track confirmation |
| **Any specific detail** (specialty, city, years in practice, Instagram tone) | Profile read | Point-in-common |

**If ICP is unconfirmed:** classify as Perfil B (autônoma) by default and flag it — do not guess Perfil A without signals of a team or reception.

**If terrain is unconfirmed:** treat as curiosidade and set the call objective accordingly — the closer must move her toward ação before any product appears.

---

## Step 1 — Call Objective by Terrain

The objective is not the same for every call. It depends on where the prospect landed after Renata.

| Terrain | What Renata captured | Call objective for R1 |
|---|---|---|
| **Ação** | *"Preciso resolver logo"*, specific urgency signal | Build certezas 3 (solução), 4 (você), 5 (investimento) — #1 and #2 already active. Target: close in R1 or commit to R2 with date confirmed. |
| **Curiosidade ativa** | *"Estou pesquisando"*, open but not decided | Land certeza #1 (problema) and #2 (prioridade) first. No product until both are verbalized by her. Target: close in R2, R1 ends with her naming the pain as urgent. |
| **Curiosidade fria** | Vague interest, no clear signal | R1 is purely diagnostic. Do not pitch. Target: confirm if there is a real problem worth solving — if not, route cleanly to Route C. |

---

## Step 2 — ICP Mode

Load the correct behavioral profile for this call. The closer adapts tone, vocabulary, and pace — not the script.

### Perfil A — Clínica com Equipe

| Dimension | Profile |
|---|---|
| **DISC** | Analytical/Stable — decides on logic + security, not enthusiasm |
| **Decision pace** | Faster when schedule is visibly oscillating; slower when stable |
| **What moves her** | Previsibilidade, organização, crescer sem perder a essência da clínica |
| **Deepest fear** | Growing commercially while losing the human and ethical touch of the clinic |
| **Energy register** | Calm authority — *"modo buda"*. Hype and urgency trigger resistance |
| **Decision-maker check** | Owner / sócia must be in R2. If absent → reschedule, do not proceed |

**Vocabulary switches — Perfil A:**

| Forbidden | Replace with |
|---|---|
| "marketing", "lead" | "captação", "paciente" |
| "fechamento", "vender" | "parceria", "avançar" |
| "escalar", "explodir" | "crescer com previsibilidade" |
| "né?" | remove — converts every statement into an approval request |

---

### Perfil B — Psicóloga Autônoma

| Dimension | Profile |
|---|---|
| **DISC** | Stable/Influential — decides on relief + personal mission, not logic |
| **Decision pace** | Slower — secondary ICP; expect more follow-up cycles |
| **What moves her** | Ter algo que responde enquanto ela atende; cobrar o que merece; ser encontrada |
| **Deepest fear** | Being seen as commercial, losing patient trust, raising prices and losing patients |
| **Energy register** | Warm, personal, mission-aligned — connect to *helping more people*, not to growing a business |
| **Decision-maker check** | She IS the only decision-maker — shorter authority check, higher ética sensitivity |

**Vocabulary switches — Perfil B:**

| Forbidden | Replace with |
|---|---|
| "marketing", "lead" | "captação", "paciente" |
| "sua equipe", "sua recepção" | she is her own team — remove |
| "escalar", "crescer" | "ter mais estabilidade", "atender melhor" |
| "implementação interna" | "configura uma vez e funciona" |

---

## Step 3 — Point-in-Common

One of the 12 High-Performance Principles in the comercial-playbook: *"deliver one genuine point-in-common before moving to diagnostic — do not skip."*

**Rule: it must be real.** A manufactured connection is worse than none — this ICP detects inauthentic signals immediately. If no genuine point-in-common exists, skip the principle and rely on strong NEPQ opening instead.

### Where to find it (in order of quality)

| Source | What to look for | Example |
|---|---|---|
| **City / bairro** | Shared location or familiarity with the area | *"Você está em Pinheiros — conheço bem aquela região, atendemos algumas clínicas por lá"* |
| **Specialty** | Specific therapeutic approach she works with | *"Vi que você trabalha com TCC — tenho trabalhado bastante com psicólogas especializadas nesse modelo"* |
| **Content she posts** | A genuine observation about something she talks about | *"Vi um post seu sobre ansiedade em adultos que eu achei muito honesto — é exatamente esse tipo de profissional que a gente gosta de trabalhar"* |
| **Detail from Renata's conversation** | Something she mentioned organically | *"Você mencionou pra Renata que está tentando organizar o atendimento há meses — isso me chamou atenção"* |
| **Competitive context** | If she is in a high-density area you know | *"Consolação tem uma concorrência bastante intensa — trabalhei com algumas psicólogas da região nesse contexto"* |
| **Timing signal** | Seasonal, NR-1 2026, or recent expansion | *"Você me falou que abriu sala nova — é exatamente esse momento que faz mais diferença organizar o processo"* |

**Format:** one short sentence, delivered in Phase 1 (rapport) after confirming technical setup. Do not extend it into a story. One sentence, then move to diagnostic.

---

## Step 4 — Pain Signal

The most important section of the brief. The SPIN sequence is only as sharp as the pain signal feeding it.

### Pain signal map — Perfil A

| Pain category | Verbatim signal | Qualification cadence |
|---|---|---|
| **Falta de previsibilidade** | *"Nunca sei como vai ser o próximo mês"*, *"Semana morta e semana cheia"* | Sintomas → perda financeira (calculator) → cansaço + previsibilidade |
| **WhatsApp / processo de atendimento** | *"Recepção não dá conta"*, *"Contatos chegam e somem"* | Response time → invisible loss per week → process gap |
| **No-show / confirmação** | *"Falta muito em primeira sessão"*, *"Não tem protocolo de confirmação"* | No-show rate → monthly revenue drain (calculator) → process fix |
| **Instagram sem conversão** | *"Tenho conteúdo mas não vem paciente"*, *"Seguidores mas nada"* | Content vs. commercial gap → invisible funnel leak → conversion process |
| **Dependência de indicação** | *"Aqui é só indicação"*, *"Se minha fonte seca, acaba"* | Single-channel dependency → what happens in a bad month → diversification need |

### Pain signal map — Perfil B

| Pain category | Verbatim signal | Qualification cadence |
|---|---|---|
| **Perda silenciosa durante atendimento** | *"Quando saio da sala, o paciente já foi"*, *"Mensagem sem resposta enquanto atendo"* | Lost contacts while in session → invisible cost × months → automation as relief |
| **Agenda oscilante / indicação** | *"Mês bom e mês ruim sem previsão"*, *"Aqui é tudo boca a boca"* | Instability → financial impact → captation beyond referrals |
| **VPS abaixo do potencial** | *"Cobro pouco por medo de perder paciente"*, *"Não sei como subir sem parecer ganancioso"* | VPS calculator → delta × patient count → identity belief (iPhone analogy) |
| **Invisibilidade online** | *"Ninguém me acha no Google"*, *"Maps está vazio"* | Search invisibility → patients going to whoever appears first → GBP as entry |
| **Sobrecarga acumulada** | *"Sou terapeuta, secretária e gestora ao mesmo tempo"*, *"Não sobra nada pra mim"* | Role overload → time cost → "configura uma vez e funciona" |

**Pull the verbatim phrase Renata captured.** If she said it in her words to Renata, it is the exact phrase to use as the Situação question anchor in SPIN.

---

## Step 5 — Pre-loaded SPIN Sequence

Pull the matching sequence from `spin-question-engine` based on ICP × active pain signal. Write the four questions in the brief so the closer does not need to recall them from memory mid-call.

**Format for the brief:**

```
S — [question]
P — [question]
I — [question]
N — [question]

Se validar a dor mas não mostrar urgência:
[importance → priority reframe phrase]

Se perguntar preço antes do N:
[counter-question]
```

### Quick-reference pain signal → SPIN bank mapping

| ICP | Pain signal | SPIN bank to pull |
|---|---|---|
| Perfil A | Agenda oscilante / faturamento | spin-question-engine → Perfil A × Agenda oscilante |
| Perfil A | WhatsApp / atendimento | spin-question-engine → Perfil A × WhatsApp |
| Perfil A | No-show / confirmação | spin-question-engine → Perfil A × No-show |
| Perfil A | Instagram sem conversão | spin-question-engine → Perfil A × Instagram |
| Perfil A | Dependência de indicação | spin-question-engine → Perfil A × Dependência |
| Perfil B | Contatos perdidos em sessão | spin-question-engine → Perfil B × Contatos perdidos |
| Perfil B | VPS abaixo do mercado | spin-question-engine → Perfil B × VPS |
| Perfil B | Instagram sem conversão | spin-question-engine → Perfil B × Instagram |
| Perfil B | Ausência no Google Maps | spin-question-engine → Perfil B × Google Maps |

**If the pain signal is unclear:** open the S question wide:
- Perfil A: *"Me conta como está o processo de entrada de pacientes novos aqui na clínica — como funciona hoje do começo ao fim?"*
- Perfil B: *"Hoje, quando alguém te encontra e quer marcar sessão — como esse contato chega até você?"*

---

## Step 6 — Product Hypothesis

Two lines: anchor and target. One line for the first downsell if needed.

**Route the product** using the qualification signals from the diagnostic and Renata:

| Scenario | Anchor | Target | First downsell |
|---|---|---|---|
| Perfil A + faturamento R$15–30k + agenda oscilante | P10K R$33.540 tabela | P7K R$14.800 Pix | VP7 R$11.800 |
| Perfil A + faturamento R$30k+ + autoridade local | P10K R$33.540 tabela | P10K R$25.800 Pix | P7K R$14.800 |
| Perfil A + faturamento R$10–20k + estruturação inicial | P10K R$33.540 tabela | P3K R$5.980 Pix | VP3 R$4.980 |
| Perfil B + faturamento R$7–15k + agenda clara | P10K R$16.000 tabela | P7K R$6.980 Pix | VP7 R$5.480 |
| Perfil B + faturamento R$3–7k + entrada | P10K R$16.000 tabela | P3K R$2.980 Pix | VP3 R$2.480 |
| Perfil B + invisível no Google | P10K R$16.000 tabela | GBP Scale R$1.480 ou GBP R$980 | — (standalone entry) |
| Perfil B + perde leads em sessão | P10K R$16.000 tabela | IA Solo (escalate to Renata) | — |

**Always open with P10K table value as anchor — even when the target is P3K.** The polarity inversion is the mechanic. The table value is the anchor. Never skip it.

**Note the guarantee** for the target product — it must appear before price in every presentation:
- Perfil A / P7K: *"Adicionamos no mínimo R$10.000 de faturamento em até 6 meses — ou continuamos até bater, sem custo adicional."*
- Perfil B / P7K: *"Processo ativo em até 45 dias — ou ajustamos sem custo adicional se os canais não gerarem contato."*

---

## Step 7 — Top 2 Expected Objections

Do not prepare for every possible objection — prepare for the two most likely given this ICP × pain combination. Pull from the ICP objection banks.

### Perfil A — most common by pain signal

| Pain active | Most likely objection | Reframe ready |
|---|---|---|
| Previsibilidade / faturamento | *"Não sei se vai se pagar"* | Calculator: current patients × VPS × delta com 3–4 a mais. Never promise — show the number. |
| WhatsApp / process | *"Minha secretária não vai conseguir implementar"* | *"A proposta é simplificar o que ela já faz, não adicionar complexidade. No início ela treina junto."* |
| ética / identidade | *"Não quero parecer que estou vendendo terapia"* | *"Organizar follow-up é cuidado, não pressão. Você garante que o paciente que precisa de você vai ser atendido."* |
| Timing | *"Agora não tenho caixa"* | Entry with 45D or GBP Scale + *"Cada semana sem processo é perda silenciosa de paciente que já chegou."* |

### Perfil B — most common by pain signal

| Pain active | Most likely objection | Reframe ready |
|---|---|---|
| VPS | *"Se eu subir o preço vou perder paciente"* | iPhone analogy: *"Um iPhone barato gera desconfiança. Seu paciente pode estar sentindo o mesmo com R$130 num bairro nobre."* |
| Sobrecarga | *"Não tenho tempo para implementar"* | *"Por isso começa com o que funciona sem execução ativa da sua parte. Você configura uma vez — roda sozinho."* |
| Invisibilidade | *"Meu consultório ainda é pequeno para isso"* | *"É exatamente quando é pequeno que o Google Maps faz mais diferença — você aparece antes de precisar investir em anúncio."* |
| ética / identidade | *"Não quero parecer comercial"* | *"Aparecer no Google não é publicidade — é facilitar o acesso de quem já está buscando ajuda e ainda não te encontrou."* |

---

## Output Format — The Brief

The brief is written in this template. Fill every field. Mark *[não confirmado]* for anything missing rather than leaving it blank.

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
R1 BRIEF — [Nome do Prospect]
[Data e horário da call]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

OBJETIVO DA CALL
Terrain: [Ação / Curiosidade ativa / Curiosidade fria]
Meta: [Ex: "Construir certezas #1 e #2 — ela ainda não verbalizou o custo real. Não chegar em produto."]

─────────────────────────────
PERFIL
ICP: [Perfil A — Clínica / Perfil B — Autônoma]
Especialidade: [Ex: TCC, psicanálise, infantil — ou não confirmado]
Cidade / bairro: [Ex: Pinheiros, SP]
Tempo de prática: [Ex: 6 anos — ou não confirmado]
Faturamento estimado: [Ex: R$8–12k/mês — ou não confirmado]

─────────────────────────────
PONTO EM COMUM
[Uma frase genuína. Ex: "Você está em Consolação — conheço bem a densidade de concorrência daquela região."]
[Se não encontrado: "Nenhum ponto genuíno identificado — abrir com NEPQ direto."]

─────────────────────────────
DOR ATIVA
Categoria: [Ex: Perda silenciosa durante atendimento]
Verbatim (Renata): [Ex: "Quando saio da sala o paciente já foi pra outra clínica"]
Cadência: [Ex: Perda em sessão → custo invisível × meses → automação como alívio]

─────────────────────────────
SEQUÊNCIA SPIN
S — [question]
P — [question]
I — [question]
N — [question]

Se validar mas sem urgência:
→ [importance→priority reframe phrase]

Se perguntar preço antes do N:
→ [counter-question]

─────────────────────────────
PRODUTO
Âncora: [Ex: P10K → "Sistema de Autoridade Clínica" → R$16.000 tabela]
Alvo: [Ex: P7K → "Método de Fluxo Previsível" → R$6.980 Pix]
Downsell 1: [Ex: VP7 → R$5.480]
Garantia: [Ex: "Processo ativo em 45 dias — ou ajustamos sem custo adicional."]

─────────────────────────────
OBJEÇÕES ESPERADAS
1. [Objection phrase] → [Reframe — one sentence]
2. [Objection phrase] → [Reframe — one sentence]

─────────────────────────────
ATENÇÃO
[Any specific watch-out for this prospect: decision-maker absent? Ethics objection likely? Competitor context? VPS ceiling belief?]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Watch out for

- **Skipping the terrain classification** — a Terrain Ação call and a Terrain Curiosidade call have fundamentally different objectives. Running a Curiosidade call as if it is Ação produces premature product presentation and triggers "vou pensar" before certezas #1 and #2 are built.
- **Putting a SPIN sequence for the wrong pain** — the SPIN bank is calibrated by pain signal, not just by ICP. A Perfil B × VPS pain needs different questions than Perfil B × Google Maps invisibility. Pull the matching bank, not just the ICP track.
- **Leaving the point-in-common blank rather than flagging it** — a missing point-in-common is better than a fabricated one. If nothing genuine was found, write "Nenhum ponto genuíno identificado" and the closer knows to open directly with NEPQ Phase 2.
- **Using the brief as a script** — the brief is a warm-up, not a screenplay. The closer should internalize the sections and speak freely, not read from the brief during the call.
- **Showing both product tracks** — confirm the ICP track before loading prices. A Perfil B psychologist seeing Perfil A prices reads it as a mismatch and loses trust. If ICP is uncertain, default to Perfil B and flag it.
- **Omitting the guarantee from the product section** — the guarantee must land before price in the pitch. If the closer forgets to load it in the brief, it will likely be forgotten in the call — and the trust objection that the guarantee pre-empts will surface at the close instead.
- **Treating Renata's terrain classification as final** — Renata classifies based on a WhatsApp conversation. By the time the closer opens the R1 call, the prospect may have done research, shared with a partner, or cooled. Re-check terrain in the first 2 minutes of Phase 1 before committing to the call objective.

---

## See also

- [`workspace/psiativa/_config/comercial-playbook.md`](../../_config/comercial-playbook.md) — the full R1 call structure this brief prepares for; Phase 1 (rapport + point-in-common), Phase 2 (NEPQ), Phase 3 (pitch)
- [`workspace/psiativa/skills/spin-question-engine/SKILL.md`](../spin-question-engine/SKILL.md) — source for Step 5: pull the pre-built SPIN sequence for this ICP × pain combination
- [`workspace/psiativa/skills/diagnostico-2min/SKILL.md`](../diagnostico-2min/SKILL.md) — upstream: provides pain signal and product hypothesis when Renata's NEPQ notes are incomplete
- [`workspace/psiativa/skills/closing-mechanic/SKILL.md`](../closing-mechanic/SKILL.md) — downstream: fires in Phase 4–5 of the same call; product section of this brief feeds directly into it
- [`workspace/psiativa/skills/objection-isolator/SKILL.md`](../objection-isolator/SKILL.md) — the top-2 objections in the brief are pulled from the objection banks here
- [`workspace/psiativa/_config/sdr-renata.md`](../../_config/sdr-renata.md) — source for terrain, verbatim phrases, and product hypothesis when Renata qualified the lead
