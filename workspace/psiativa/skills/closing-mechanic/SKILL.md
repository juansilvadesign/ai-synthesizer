---
name: closing-mechanic
description: Execute the closing sequence for a PsiAtiva R2 call. Takes the post-SPIN, post-objection state and conducts the closer from "certezas built" to "payment confirmed in-meeting." Covers pre-close certeza check, three-part closing structure, price anchoring, post-price silence protocol, escape phrase responses, ICP-split cascade, and in-meeting payment collection. Every call ends in one of five named routes — no ghost pipeline.
trigger: User is at the closing phase of an R1 or R2 call (objections resolved, SPIN complete, solution accepted) and asks to "fechar a venda", "como conduzir o fechamento", "o que fazer depois de apresentar o preço", "como lidar com vou pensar no final da call", or "como não perder a venda no último minuto". Also fires when reviewing a call where the prospect said "me avisa" and no sale was made.
---

# Closing Mechanic — PsiAtiva

The close is not the sale. The close is the prevention of the escape. By the time the closer arrives here, the diagnostic is done, the pain is felt, the solution is understood. What remains is one job: stop the prospect from converting a decision into an analysis.

> *"Quem termina call com 'fica à vontade' trocou condução por abandono elegante."*

**This skill fires after:**
- SPIN sequence complete → prospect verbalized the cost of inaction (Necessidade answered)
- All active objections isolated and resolved (`objection-isolator`)
- ICP confirmed, correct price track loaded

**This skill hands off to:**
- Payment collection → `gerar-contrato`
- Unresolved certeza → back to `spin-question-engine` (Implicação/Necessidade not fully landed) or `objection-isolator`
- Route: Agora não, com motivo claro → Reactivation cadence

## Knowledge base

- [`knowledge/sources/101_agência/18_Fechamento é tirar a venda da análise e levar para.md`](../../../../knowledge/sources/101_agência/18_Fechamento é tirar a venda da análise e levar para.md) — source: five routes, four closing questions, escape phrase responses, closing structure, clean "no" as win
- [`knowledge/sales/articles/oultimomentor/101_agencia.md`](../../../../knowledge/sales/articles/oultimomentor/101_agencia.md) — Phase 13: six certezas pre-close check, three-part closing structure, microcommitment principle
- [`workspace/psiativa/_config/comercial-playbook.md`](../../_config/comercial-playbook.md) — Phase 4 (price anchoring), Phase 5 (closing negotiation), post-price silence, cascade sequence, in-meeting payment rule
- [`workspace/psiativa/_config/esteira-de-produtos.md`](../../_config/esteira-de-produtos.md) — full drop cascade by ICP; Pix vs. table value prices; VP conditions; ascension credit policy
- [`workspace/psiativa/skills/objection-isolator/SKILL.md`](../objection-isolator/SKILL.md) — upstream: handles objections during the close; this skill calls it if an objection surfaces during the cascade

---

## Input

Required before firing this skill:
- **ICP track** — Autônomo or Clínica (prices diverge 2×; wrong track = wrong anchor)
- **SPIN complete** — prospect verbalized the Necessidade answer
- **Objections cleared** — no open certeza gaps from prior objection handling
- **Decision-maker present** — if the decision-maker is absent, do not proceed; close a new call with them included

If any of these is not confirmed: do not run this skill. Running a close before all four conditions are met produces the worst outcome — a fake follow-up that dies quietly.

---

## Step 1 — Pre-Close Certeza Scan

Before the closing structure, do a fast internal check. If any certeza is shaky, the prospect will escape — not because the close was wrong, but because the close was premature.

| Certeza | How to check it quickly | If shaky |
|---|---|---|
| **Problema** | Did she name the problem in her own words? | Return to SPIN P question |
| **Prioridade** | Did she say this is costing her now (not someday)? | Return to SPIN I question |
| **Solução** | Did she accept that GAP addresses her specific gap? | Restate the mechanism match before closing |
| **Você** | Did she ask about process or show trust? | Add a proof point before closing |
| **Investimento** | Did she respond to the ROI framing (calculator technique)? | Re-anchor cost of inaction before showing price |
| **Timing** | Is there a reason to act in the next 30 days? | NR-1 tailwind or competitor visibility gap if applicable |

**Rule:** all six must be at least stable. If two or more are shaky, do not close — return to the diagnosis phase and land the missing certeza first. A close attempted before certeza #1 or #2 is solid will always produce "vou pensar."

---

## Step 2 — The Three-Part Closing Structure

Run this in exact order. Do not skip the recap. Do not re-sell during the close — the job here is to tie the reasoning, not to explain the product again.

### Part 1 — Recap the Diagnosis

Restate the problem in her words. This anchors the decision in the conversation that just happened — not in the product features.

> *"Pelo que você me trouxe, o gargalo hoje não parece ser falta de procura. Parece ser o que acontece entre o interesse e a sessão confirmada — o contato chega, mas o processo de resposta e confirmação ainda não está estruturado."*

Adapt to what she actually said in the SPIN phase. Never use generic language here — a recap with her own words activates consistency: she already agreed that this is her problem.

### Part 2 — Position the Solution as the Logical Response

Do not sell the product again. Connect the structure already presented to the specific gap named in the recap.

> *"Por isso o que a gente propôs não começa com mais volume de contatos. Começa corrigindo exatamente essa etapa — para que cada interessado que já chega chegue de verdade ao agendamento."*

One or two sentences. No new features. No additional benefits. The framing is: this is not a pitch, it is a conclusion.

### Part 3 — The Definition Question

This is the close. The question must reduce the space for escape — not ask for an opinion.

**Standard close:**

> *"Dito isso, seu cenário hoje está mais para avançar com isso agora ou existe alguma trava real que precisa ser esclarecida antes da decisão?"*

This opens two exits: advance, or name the trava. Both are acceptable — neither is "me avisa."

**If she has already heard the price and has not objected:**

> *"Faz sentido avançarmos com isso agora?"*

Stop. Do not add words. Wait.

---

## Step 3 — Price Anchoring

Present the anchor (P10K) before the target product (P7K) in every call. Do not skip anchoring even if the qualification signals P3K as the likely close — the polarity inversion is the mechanic that makes P7K feel proportionate.

### Anchoring Sequence

**Step 1 — Present table value of anchor (P10K):**

Do not open with the Pix price. The table value is the anchor. Present it first, briefly.

*Autônomo:*
> *"A estrutura mais completa que montamos — o Sistema de Autoridade Clínica — tem um investimento de R$16.000. Ela faz sentido para psicólogas com meta de referência de especialidade e agenda cheia nos próximos 6 meses."*

*Clínica:*
> *"A estrutura mais completa que montamos tem um investimento de R$33.540. É o que faz sentido para clínicas que estão buscando liderança de mercado local em 6 meses."*

**Step 2 — Introduce the target product (P7K) as the calibrated solution:**

> *"Para o que você me descreveu — [restate the specific problem] — a estrutura que mais faz sentido é o [Método de Fluxo Previsível / MFP]."*

**Step 3 — Present table value of target:**

*Autônomo:*
> *"O investimento é R$9.074."*

Stop. Let her react. Then ask: *"O que aperta mais: o valor total ou o valor da parcela?"*

**Step 4 — Offer Pix as condição especial:**

> *"Se você conseguir fechar hoje via Pix, o investimento cai para R$6.980."*

Do not explain why Pix is cheaper. Present it as a condition, not a discount.

### Anchor table — both ICP tracks

| Step | Autônomo | Clínica |
|---|---|---|
| P10K table (anchor) | R$ 16.000 | R$ 33.540 |
| P7K table | R$ 9.074 | R$ 15.340 |
| P7K Pix (target) | R$ 6.980 | R$ 14.800 |

**Vocabulary rule:** never say "desconto", "ancoragem", "VP", "VT", or internal product codes (P10K, P7K) out loud. Use commercial names: "Sistema de Autoridade Clínica", "Método de Fluxo Previsível."

---

## Step 4 — Post-Price Protocol

After stating the Pix price, do two things in sequence:

1. **Stop sharing the screen.** This shifts focus from the slide to the conversation.
2. **Ask the definition question, then go silent for 7–12 seconds.**

> *"Isso aqui funciona para você?"*

**Do not fill the silence.** The discomfort of silence lands on the person who speaks first. If you speak, you take the discomfort back. Wait.

**If she answers yes:** move directly to payment. Do not circle back. Do not add benefits. Do not give her time to reconsider.

> *"Perfeito. Vamos resolver o acesso agora pra já sair daqui com tudo encaminhado."*

**If she objects:** do not defend immediately. Go to Step 5.

---

## Step 5 — Escape Phrase Handling

Every escape phrase must be converted from vague to specific. Do not accept the fog.

**The rule:** the closer's job is not to confront. It is to name what is unnamed.

### "Vou pensar" / "Vou analisar" / "Preciso ver com calma"

> *"Perfeito. Só pra eu não responder errado depois: esse 'pensar' hoje está mais em cima do valor, da prioridade disso agora ou da confiança no caminho?"*

After she picks one → route to the appropriate certeza response (see isolation scripts in `objection-isolator`).

---

### "Me manda" / "Me envia a proposta que eu analiso"

> *"Mando sim. Antes, quero só deixar isso em decisão. Quando você diz que vai ver, você vai olhar mais para validar o investimento, alinhar com alguém ou decidir se isso entra como prioridade agora?"*

After she answers → same certeza routing.

---

### "Preciso ver com meu sócio" / "Preciso alinhar com minha equipe"

> *"Perfeito. E o ponto que seu sócio mais precisaria validar seria o investimento, a urgência disso agora ou se esse formato resolve o problema certo?"*

- If **investimento** → confirm her own position first: *"Você pessoalmente, pelo que conversamos, faz sentido avançar?"* → If yes: escalate to schedule R2 with the partner.
- If **urgência** → same sequence.
- If she is genuinely not the decision-maker → *"Faz sentido. Teria como incluir ele numa conversa rápida para a decisão não ficar dependendo de repasse?"* → close a new call, not a follow-up.

---

### "Faz sentido, mas talvez não agora" / "Mais pra frente" / "Quando virar o mês"

> *"Justo. O que faz não ser agora: caixa, timing operacional ou isso ainda não ter virado prioridade suficiente?"*

- If **caixa** → go to cascade (Step 6).
- If **timing operacional** → name a re-entry date: *"Faz sentido. Qual seria o momento nos próximos 30 dias que ficaria mais viável?"*
- If **prioridade** → cost-of-waiting question: *"Pelo que você me contou, cada mês sem processo é faturamento que sai sem rastrear. Se isso ficar igual pelos próximos 3 meses, a situação fica estável ou tende a piorar?"*

---

### "Gostei. É só um pouco caro."

Defend table value before cascade:

> *"Entendo. Quando você fala caro, quero só entender se estamos falando de caixa neste momento ou se o valor ainda não parece proporcional ao problema que conversamos?"*

- If **proporcionalidade** → the Implicação was not fully landed. Return to the cost of inaction: *"Me diz: no cenário atual, quantos contatos chegam por mês e quantos desses viram sessão confirmada? Vamos abrir o calculador."* Rerun the calculator before cascading.
- If **caixa** → ask the financial isolation question: *"É só a condição financeira que te impede de fechar hoje?"* → If yes, cascade.

---

### The "Adulto" close — when she is trying to exit politely without naming the reason

> *"Perfeito. Não quero forçar você a decidir nada sem clareza. Só não quero também deixar isso numa zona vaga. Hoje o ponto está mais em não fazer sentido agora, em faltar alguma certeza ou em precisar envolver outra pessoa?"*

This is the safety valve. Use when all specific escape phrases have been tried and the prospect is still fog. Forces a named route.

---

## Step 6 — The Cascade

Only enter the cascade after confirming financial block is the isolated objection. Never cascade because the conversation "feels hard" — cascade only when the financial is the confirmed and isolated barrier.

**ICP-split cascade — work down in this order, one step at a time:**

### Autônomo

| Step | Product | Price | What to say |
|---|---|---|---|
| 1 | P7K VP | R$ 5.480 | *"Se o Pix de R$6.980 não encaixa agora, tem uma condição parcelada de R$5.480 que funciona?"* |
| 2 | P3K | R$ 2.980 | *"Tem um caminho mais leve para começar — o [Método de Ativação Previsível] em 45 dias, por R$2.980. Você entra com escopo menor, e quando bater o resultado, tem crédito integral para subir para o [MFP]."* |
| 3 | P3K VP | R$ 2.480 | Offer only if P3K table value is the financial block. |
| 4 | 45D | R$ 1.980 | *"O caminho mais compacto é o Protocolo de Intervenção Acelerada, por R$1.980. É a porta de entrada — e o valor entra como crédito depois."* |
| 5 | GBP Scale | R$ 1.480 | Final floor. *"O ponto de partida mínimo é o [Protocolo Referência Local] por R$1.480 — ativação de presença local com resultado visível em 15 dias."* |

### Clínica

| Step | Product | Price | What to say |
|---|---|---|---|
| 1 | P7K VP | R$ 11.800 | *"Se R$14.800 Pix não encaixa agora, tem uma condição de R$11.800 que funciona?"* |
| 2 | P3K | R$ 5.980 | Same P3K framing as above, adjusted for clínica values. |
| 3 | P3K VP | R$ 4.980 | Offer only if P3K Pix is the block. |
| 4 | 45D | R$ 3.980 | Entry / test. Credit applies on ascension. |
| 5 | GBP Scale | R$ 2.980 | Final floor. |

### Cascade rules

- **Present one step at a time.** Never show the full cascade — presenting R$6.980, R$2.980, and R$1.480 simultaneously destroys anchoring and trains the prospect to wait for the floor.
- **Credit framing is mandatory for P3K and below.** Every downsell product below P7K carries a credit toward ascension — always state this: *"O valor do [produto de entrada] entra como crédito quando você subir para o [MFP]."*
- **Do not cascade below P3K to a lead who qualifies for P7K.** An under-scoped sale produces a weak result and no case study. If the financial block is real and P3K does not close, accept the clean "no" and re-enter in 30–60 days.
- **No improvised discounts.** Every price step in the cascade is designed. A price outside the table destroys the structure and signals desperation.

---

## Step 7 — In-Meeting Payment Collection

Once she says yes to any product, collect payment before ending the call.

> *"Perfeito. Vamos resolver o acesso agora pra já sair daqui com tudo encaminhado. Você prefere Pix ou cartão?"*

Do not end the call without confirmed payment. Do not trust:
- *"Faço depois"* — conversion of unpaid commitments is under 10%.
- *"Amanhã cedo"* — the same applies.
- *"Mando o Pix assim que eu chegar em casa"* — same.

If she cannot pay in the moment due to a technical reason (bank limit, needs to transfer), schedule a concrete window within 2 hours and stay available. Never leave it open-ended.

**Rotulação transition before payment:**

> *"Bom, quando chegamos nesse momento, entendemos que você já tomou a decisão de que precisa investir em captação. Então vamos só formalizar o acesso agora."*

This activates cognitive consistency — she has already decided, payment is just the administrative step.

---

## The Five Routes — Every Call Ends in One

No call ends in fog. If the call ends and you cannot name which route it took, the sale was abandoned, not closed.

| Route | Signal | What to say to close it cleanly |
|---|---|---|
| **Sim** | She agreed and payment is confirmed | *[proceed directly to payment — no words needed]* |
| **Não** | Problem is not a priority or never will be | *"Entendo perfeitamente. Nesse caso o melhor que posso fazer é deixar a porta aberta. Se a situação mudar, é só chamar."* |
| **Sim, com ajuste** | Scope, timing, or format needs to change | Name the adjustment explicitly and close the adjusted version in the same call |
| **Sim, com outro decisor** | She wants to advance but needs the partner | *"Faz sentido. Teria como incluir ele numa conversa de 20 minutos esta semana?"* → book the date on the call |
| **Agora não, com motivo claro** | Real caixa or timing constraint with a named horizon | *"Faz sentido. Qual seria o momento nos próximos 30 a 60 dias que ficaria mais viável?"* → book a specific date |

**If the call ends outside these five:** the closer did not conduct — the prospect conducted. Diagnose which certeza was never landed and correct it before the next call.

---

## Watch out for

- **Running the close before Necessidade is answered** — a prospect who has not verbalized the cost of inaction will always escape at the price presentation. SPIN must complete before this skill fires.
- **Asking opinion questions instead of definition questions** — "O que você achou?", "Curtiu?", "Faz sentido?" all invite vague, comfortable answers. The close must ask for a decision, not a reaction.
- **Accepting "me avisa" as a route** — it is not a route. It is fog. If a call ends with "me avisa", it ended with no close. Diagnose and re-approach.
- **Cascading before isolating the financial objection** — presenting a lower price without confirming that money is the only remaining block is a price signal without a reason. She learns that waiting produces lower prices.
- **Saying "né?" at the close** — it converts every statement into an approval request and collapses the authority built across the entire call. From the comercial-playbook: "saying 'né?' destroys authority in real time."
- **Ending the call after a verbal yes without collecting payment** — verbal commitment without payment has under 10% conversion. Collect before hanging up.
- **Using the word "fechamento", "me paga", or "desconto" out loud** — these activate the vendor frame at the most critical moment. "Avançar", "formalizar o acesso", "condição especial" are the replacements.
- **Presenting the cascade as a menu** — showing multiple price options simultaneously removes the anchoring effect. One step, one question, one decision.
- **Selling P3K to a P7K-qualified lead because the call is feeling hard** — under-scoped sale is worse than no sale. It produces a weak result, no case study, and a client who was never properly served. Accept the clean no and re-enter at the right moment.

---

## See also

- [`workspace/psiativa/skills/objection-isolator/SKILL.md`](../objection-isolator/SKILL.md) — fires during the escape phrase handling phase when a certeza gap surfaces mid-close
- [`workspace/psiativa/skills/spin-question-engine/SKILL.md`](../spin-question-engine/SKILL.md) — fires when pre-close scan reveals certeza #1 (Problema) or #2 (Prioridade) is not stable — Implicação/Necessidade must be re-landed before closing
- [`workspace/psiativa/_config/comercial-playbook.md`](../../_config/comercial-playbook.md) — R1+R2 full call structure; this skill operates in Phases 4 and 5
- [`workspace/psiativa/_config/esteira-de-produtos.md`](../../_config/esteira-de-produtos.md) — full cascade prices by ICP, credit policy, and qualification routing
- [`workspace/psiativa/skills/gerar-contrato/SKILL.md`](../gerar-contrato/SKILL.md) — downstream: fires immediately after payment is confirmed
- [`knowledge/sources/101_agência/18_Fechamento é tirar a venda da análise e levar para.md`](../../../../knowledge/sources/101_agência/18_Fechamento é tirar a venda da análise e levar para.md) — source: five routes, four closing questions, escape phrase responses, adult close
