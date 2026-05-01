---
name: ascension-conversation
description: Activate the built-in credit policy at the right emotional window after a PsiAtiva project produces visible results. Takes the current product, the result evidence, and the ICP, and runs a re-diagnosis sequence that surfaces the intentional product gap, frames the next step as applying a credit rather than buying again, and closes the ascension difference in the same conversation. Output includes the re-diagnosis questions, the credit frame script, the difference price, and the close.
trigger: User has an active client at a check-in moment (P3K or 45D day 30, GBP day 7–10, P7K month 4–5) and asks to "conduzir a conversa de ascensão", "subir o cliente para o próximo produto", "como apresentar o crédito", "o cliente teve resultado, o que faz agora", or "preparar o check-in de 30 dias". Also fires when a current client mentions a pain that the current product was not scoped to solve.
---

# Ascension Conversation — PsiAtiva

A client who just saw results is the easiest sale in the entire pipeline. The trust is built. The vocabulary is calibrated. The original objections are resolved by the result they are holding. What remains is one job: name the gap the current product was designed not to solve, show the credit that closes most of the distance, and open the next step as a continuation — not a new purchase.

> *"A decisão foi tomada durante a call, não no fechamento. O fechamento só viabiliza o que o lead já decidiu internamente ao longo dos ciclos de concordância."* — FastScale

In ascension, the concordance cycles are already partially built from the prior engagement. The conversation does not start from zero.

**The core mechanic:** Every entry-level product has an intentional gap — a component that was deliberately left out. That gap is not a failure of delivery. It is the designed next problem. The ascension conversation names that gap, connects it to the result the client already has, and frames the next product as the continuation that closes it.

**This skill fires after:**
- P3K or 45D 30-day check-in with confirmed results
- GBP / GBP Scale day 7–10 with presence activated
- P7K month 4–5 with measurable faturamento growth
- Any client conversation where a pain surfaces that the current product does not address

**This skill hands off to:**
- Payment collection → `gerar-contrato` (same session if close is achieved)
- If client is not ready → schedule a specific re-entry date (not "I'll think about it")

## Knowledge base

- [`workspace/psiativa/_config/esteira-de-produtos.md`](../../_config/esteira-de-produtos.md) — full ascension credit table (both ICPs), intentional P3K gap note, built-in check-in trigger, commercial vocabulary map, compact product profiles
- [`workspace/psiativa/_config/comercial-playbook.md`](../../_config/comercial-playbook.md) — concordance cycles, rotulação, closing posture, in-meeting payment rule
- [`workspace/psiativa/_config/icp-clinica.md`](../../_config/icp-clinica.md) — Perfil A desire inventory (previsibilidade, autoridade, crescimento com leveza)
- [`workspace/psiativa/_config/icp-consultorio-solo.md`](../../_config/icp-consultorio-solo.md) — Perfil B desire inventory (captar sem esforço adicional, VPS, autoridade local)
- [`knowledge/sales/courses/fastscale/fastscale.md`](../../../../knowledge/sales/courses/fastscale/fastscale.md) — concordance cycles, ClickUp Ascensão stage, polarity inversion, ROI calculation mechanics
- [`workspace/psiativa/skills/closing-mechanic/SKILL.md`](../closing-mechanic/SKILL.md) — closing structure and in-meeting payment; applies identically in ascension, without the anchor step

---

## The Intentional Gap — Design Principle

Each product below P10K was scoped to produce a specific result and leave a specific problem unsolved. That unsolved problem is not a flaw — it is the product's built-in ascension trigger.

| Current product | What it delivers | What it intentionally omits | Designed next problem |
|---|---|---|---|
| **GBP / GBP Scale** | Presence activated — Google Maps, reviews, local visibility | No conversion page, no WhatsApp process, no confirmation cadence | Contacts arrive but have nowhere to land and no one to respond |
| **45D** | Básico ativo — presence + entry page + first-contact scripts | No campaigns, no 24h agent, no confirmation system | Manual process is running but it does not scale and loses leads when she is in session |
| **P3K** | Channels active, contacts arriving, process structured | **No Agente de Acolhimento 24h** — explicitly not included | She is losing leads during sessions every day — exactly the pain that existed before P3K, now amplified by the new contacts the product is generating |
| **P7K** | Predictable flow, campaigns, 24h agent, 4 KPIs, monthly optimization | No editorial calendar, no referral network, no 6 KPIs, no quarterly calibration, no authority positioning | She is capturing well but capped on quality — cannot move to the authority positioning tier that unlocks higher-VPS clientele and sub-niche referrals |

**The P3K gap is the most commercially powerful.** The product creates new contacts and then creates visible contact loss during sessions — the very problem the client originally paid to solve. By day 30, the gap is not theoretical; she can observe it happening.

---

## Step 1 — Ascension Window Check

The window is open when three conditions are true simultaneously:

| Condition | What to look for | Why it matters |
|---|---|---|
| **Result is visible** | Specific, named evidence — new contacts, reviews gained, sessions confirmed, faturamento delta | Ascension without result evidence is just upselling. The result is the permission. |
| **Emotional state is positive** | She is expressing relief, satisfaction, or excitement — not fatigue or complaint | Ascension in a negative emotional state reactivates the original skepticism. Wait for the result celebration. |
| **The designed gap is active** | She has observed or is currently experiencing the problem the current product was not scoped to solve | The gap must be real for the re-diagnosis to land. If she hasn't noticed it yet, the ascension is premature. |

**If any of the three is missing:** do not run the ascension conversation. Either wait for the result to materialize, or use the check-in conversation to surface the gap — and book the ascension for a future call once she has articulated it herself.

---

## Step 2 — Result Acknowledgment

Open with the result, specifically. Generic praise ("o projeto foi ótimo") does not anchor the conversation. The acknowledgment must name what changed — it activates the client's emotional investment in continuing.

**Format:** One specific before/after or one concrete metric.

> *"Antes de qualquer outra coisa: você saiu de [estado inicial] e hoje [resultado específico]. Isso foi real."*

**Examples by product:**

*P3K at 30 days:*
> *"Você ativou os canais, o Google Maps está recebendo busca, e os primeiros contatos já estão chegando por fora da indicação. Isso que você tem na mão agora não existia 30 dias atrás."*

*GBP at day 10:*
> *"Você estava invisível no Google local. Agora aparece nas buscas da região, tem [X] avaliações, e já tem um caminho de contato. Isso é o que mudou."*

*P7K at month 4–5:*
> *"Nos últimos meses a agenda ficou mais estável, os contatos que chegam já têm intenção mais clara, e o processo de confirmação está segurando o no-show. Esses três pontos juntos — você construiu isso aqui."*

**Rule:** only one acknowledgment sentence. Do not extend it. The result is the opening — the conversation moves forward immediately.

---

## Step 3 — Re-Diagnosis Sequence

The re-diagnosis does not start from scratch. It starts from the result and moves to what the result exposed. The question sequence is shorter than a full SPIN because the trust is already established — two to three questions is enough.

### Re-diagnosis structure

**Question 1 — Current state after result:**
Check if the designed gap has become visible to the client.

*P3K:*
> *"Com os canais funcionando e os contatos chegando, o que você está percebendo de diferente no dia a dia?"*

*GBP:*
> *"Desde que a presença ativou, como está chegando o contato — pelo Google direto, pelo Instagram, ou pelo WhatsApp?"*

*P7K:*
> *"Com o processo rodando há [X] meses, onde você ainda sente que tem espaço para melhorar — captação, confirmação, ou a qualidade dos pacientes que chegam?"*

---

**Question 2 — Surface the designed gap:**
Name the specific operational moment where the current product's limit is visible.

*P3K → P7K (24h agent gap):*
> *"E quando você está em sessão e chega uma mensagem nova — como esse contato está sendo tratado agora?"*

*45D → P3K (campaigns and process gap):*
> *"O básico está ativo. O que ainda depende de você para funcionar — o que aconteceria se você ficasse 3 dias sem olhar para isso?"*

*GBP → 45D/P3K (no conversion page):*
> *"Quando alguém te encontra no Google e quer saber mais antes de chamar — onde ela vai?"*

*P7K → P10K (authority ceiling):*
> *"Hoje, quando uma psicóloga da região indica você — ou quando um paciente pesquisa sobre [especialidade] — você aparece como referência nesse subnicho ou ainda fica misturado com os outros perfis?"*

---

**Question 3 — Implication (cost of the gap):**
Connect the gap to what it is costing — not what it could earn.

*P3K → P7K:*
> *"Se uma mensagem chegar às 14h enquanto você está em sessão — e a pessoa não receber resposta por 3, 4 horas — o que acontece com esse contato, na sua experiência?"*

*GBP → 45D/P3K:*
> *"Se alguém te encontra no Google mas não tem uma página clara para entender o que você oferece e como chegar até você — o que acontece com esse interesse?"*

*P7K → P10K:*
> *"Você chegou num ponto em que a captação está funcionando. O que acontece com o valor de sessão que você consegue cobrar quando você é reconhecida como referência no subnicho versus quando é mais uma psicóloga especializada?"*

**The client will name the consequence herself.** Do not anticipate or answer the question. Wait. When the consequence comes from her, the ascension need is established without pressure.

---

## Step 4 — The Credit Bridge

After she articulates the gap and its cost, the credit frame is the transition. It reframes the question entirely:

**Without credit frame:** "Do you want to buy more?"
**With credit frame:** "Do you want to apply what you already invested to close the gap you just named?"

### Credit frame script — standard

> *"O que você construiu nos últimos [30 dias / meses] não vai a lugar nenhum. [Result restatement in one line.] O próximo passo resolve exatamente o ponto que você acabou de descrever — e o melhor: o que você já investiu aqui entra como crédito integral. Você paga só a diferença."*

### Credit frame with specific numbers

After the standard frame, state the credit and the difference immediately:

*P3K (Pix) → P7K — Autônomo:*
> *"Você investiu R$2.980 no [Método de Ativação Previsível]. Esse valor entra como crédito para o [Método de Fluxo Previsível]. A diferença para chegar lá é R$4.000."*

*P3K (Pix) → P7K — Clínica:*
> *"Você investiu R$5.980. Esse valor entra como crédito para o [MFP]. A diferença é R$8.820."*

*45D → P3K — Autônomo:*
> *"Você investiu R$1.980. Esse valor entra como crédito. A diferença para o [Método de Ativação Previsível] é R$1.000."*

*GBP Scale → P3K — Autônomo:*
> *"Você investiu R$1.480. A diferença para o [Método de Ativação Previsível] é R$1.500."*

*P7K (Pix) → P10K — Autônomo:*
> *"Você investiu R$6.980. Esse valor entra como crédito para o [Sistema de Autoridade Clínica]. A diferença é R$5.820."*

### Full credit table — both ICP tracks

**Autônomo:**

| From → To | Credit | Difference |
|---|---|---|
| GBP Scale → 45D | R$ 1.480 | R$ 500 |
| GBP Scale → P3K | R$ 1.480 | R$ 1.500 |
| 45D → P3K | R$ 1.980 | R$ 1.000 |
| P3K (Pix) → P7K | R$ 2.980 | R$ 4.000 |
| P3K (VP) → P7K | R$ 2.480 | R$ 4.500 |
| P7K (Pix) → P10K | R$ 6.980 | R$ 5.820 |
| P7K (VP) → P10K | R$ 5.480 | R$ 7.320 |

**Clínica:**

| From → To | Credit | Difference |
|---|---|---|
| GBP Scale → 45D | R$ 2.980 | R$ 1.000 |
| GBP Scale → P3K | R$ 2.980 | R$ 3.000 |
| 45D → P3K | R$ 3.980 | R$ 2.000 |
| P3K (Pix) → P7K | R$ 5.980 | R$ 8.820 |
| P3K (VP) → P7K | R$ 4.980 | R$ 9.820 |
| P7K (Pix) → P10K | R$ 14.800 | R$ 11.000 |
| P7K (VP) → P10K | R$ 11.800 | R$ 14.000 |

**Never present the full table to the client.** One line: the credit she has and the difference she pays. Nothing else.

---

## Step 5 — New Promise Presentation

After the credit frame, state the next product's promise — one sentence, calibrated to the gap she named. Do not list deliverables. The deliverable list comes after she expresses interest.

*P3K → P7K:*
> *"O [Método de Fluxo Previsível] coloca um Agente de Acolhimento 24h respondendo enquanto você está em sessão, e adiciona as campanhas que o [MAP] não incluía. A promessa é no mínimo [ROI anchor] em 6 meses — ou continuamos até bater, sem custo adicional."*

*45D → P3K:*
> *"O [Método de Ativação Previsível] estrutura o processo completo — não só o básico ativo, mas a cadência de confirmação, os scripts de triagem e a página de captação que funciona sem você ter que tocar todos os dias."*

*GBP → 45D:*
> *"O [Protocolo Intervenção Acelerada] coloca uma página de captação e os primeiros scripts de atendimento em funcionamento — para que quem te encontra no Google tenha um próximo passo claro e você tenha um processo de resposta que não depende de você estar online."*

*P7K → P10K:*
> *"O [Sistema de Autoridade Clínica] é o que acontece depois que o fluxo está previsível — posicionamento de referência no subnicho, editorial de conteúdo, rede de encaminhamento estruturada, e 6 KPIs com calibração trimestral. A promessa é agenda consistente e referência da especialidade em 180 dias."*

### ROI re-anchor

For P3K → P7K and P7K → P10K, re-anchor ROI using numbers she already has.

*P3K → P7K — Autônomo:*
> *"Com o agente respondendo 24h, quantos contatos por semana você acha que não precisariam mais esperar você sair da sessão para receber resposta? Se um desses virar paciente por mês, com [VPS] de sessão, em 4 meses o diferencial de R$4.000 já se pagou."*

*P7K → P10K — Clínica:*
> *"A autoridade de subnicho muda o perfil do paciente que chega. Um aumento de R$[delta VPS] por sessão, ao longo de [X therapists] profissionais, em 6 meses — qual seria o impacto no faturamento da clínica?"* → Open calculator, let her calculate.

---

## Step 6 — Closing the Ascension

The ascension close follows the same mechanics as `closing-mechanic` — but without the anchor step. Trust is already established. There is no polarity inversion needed. The close is direct.

### The ascension definition question

> *"Dito isso: faz sentido aplicar o crédito e seguir para o próximo passo agora?"*

Stop. Wait. Do not fill the silence.

**If she says yes:** collect payment immediately. Do not end the call without confirmed payment. The same rule from `closing-mechanic` applies: verbal commitment without payment converts under 10%.

> *"Ótimo. Vamos formalizar o acesso agora para a gente já começar a próxima etapa."*

**If she hesitates or gives a soft objection:**

*"Preciso pensar":*
> *"Perfeito. Para eu não responder errado: o que está pesando mais — o valor da diferença, o momento operacional ou alguma dúvida sobre o que o próximo passo entrega?"*

*"Agora não tenho caixa":*
> *"Entendo. Esse 'agora não' é mais de timing — você estaria aberta em 15, 30 dias — ou o valor está travando independente do momento?"*

*"Deixa eu ver com meu sócio":*
> *"Faz sentido. O que o teu sócio precisaria entender mais — o resultado que tivemos até aqui, o que o próximo produto entrega, ou o valor da diferença?"* → Schedule a second call with both present.

**Do not cascade on an ascension conversation.** The ascension has one offer: the next step with the credit applied. There is no downsell in ascension. If the client cannot proceed now, name a re-entry date and honor it.

> *"Faz sentido. Qual seria o momento nos próximos 30 dias que ficaria melhor para isso?"*

---

## Pre-built Ascension Conversations — by Path

### P3K → P7K (the most common path)

*Full sequence:*

**Result acknowledgment:**
> *"Você saiu de zero presença digital para canais ativos gerando contato por fora da indicação. Nos últimos 30 dias isso foi real."*

**Gap question 1:**
> *"Com os contatos chegando, o que você está percebendo de diferente no dia a dia?"* [Let her speak]

**Gap question 2 (designed gap):**
> *"E quando você está em sessão e chega uma mensagem nova — como esse contato está sendo tratado agora?"* [She names the loss]

**Implication:**
> *"Se uma mensagem chegar às 14h enquanto você está em sessão e a pessoa não receber resposta por 3 horas — o que acontece com esse contato, na sua experiência?"* [She confirms the cost]

**Credit bridge:**
> *"O que você construiu não vai a lugar nenhum. O próximo passo resolve exatamente isso — e o [Método de Ativação Previsível] já entra como crédito integral. Você paga só a diferença de R$4.000 [autônomo] / R$8.820 [clínica]."*

**New promise:**
> *"O [Método de Fluxo Previsível] coloca um Agente de Acolhimento 24h respondendo enquanto você está em sessão — nenhum contato fica sem resposta útil porque você estava atendendo."*

**ROI anchor:**
> *"Com o agente respondendo, se um contato a mais por mês virar paciente — com sua sessão de R$[VPS] — em quanto tempo o diferencial de R$4.000 se paga?"* [Calculator]

**Close:**
> *"Faz sentido aplicar o crédito e seguir para o próximo passo agora?"*

---

### 45D → P3K

*Condensed version:*

**Result:**
> *"O básico está ativo — você tem presença, página, e um primeiro processo de contato funcionando. Isso é real."*

**Gap:**
> *"O que ainda depende de você para não perder nada — o que aconteceria se você ficasse 3 dias sem olhar?"* [She names the manual dependency]

**Implication:**
> *"E esse esforço de manutenção, somado ao tempo de atendimento — quanto isso está pesando no dia a dia?"*

**Credit + promise:**
> *"O que você investiu entra como crédito. A diferença para o [Método de Ativação Previsível] é R$1.000 [autônomo] / R$2.000 [clínica]. O MAP estrutura o processo completo para rodar sem você precisar tocá-lo todos os dias."*

**Close:** same definition question.

---

### GBP / GBP Scale → Next

*Condensed:*

**Result:**
> *"Você aparece no Google local, tem avaliações e um CTA direto. Antes disso não existia."*

**Gap:**
> *"Quando alguém te encontra no Google e quer saber mais antes de chamar — onde ela vai agora?"* [She names the missing landing page or process]

**Implication:**
> *"Se ela não tem um próximo passo claro, o que você acha que acontece com esse interesse?"*

**Credit + promise:**
> Credit: R$1.480 (autônomo) / R$2.980 (clínica). Difference: R$500 to 45D, R$1.500 to P3K.
> *"O [próximo produto] coloca a página de captação e o processo de primeiro contato — para que quem te encontra no Google tenha um caminho claro até você."*

---

### P7K → P10K

*This is a longer conversation — emotional state must be at peak, results must be well-documented.*

**Result:**
> *"Em [X] meses, [specific metric: agenda mais estável, X pacientes novos, no-show caiu de X% para Y%]. Você construiu um processo previsível."*

**Gap:**
> *"Hoje, quando alguém da sua área busca referência em [especialidade] — você aparece como a nome mais reconhecido ou ainda há psicólogas com mais visibilidade nesse espaço?"* [She names the authority ceiling]

**Implication:**
> *"Quanto você acha que a percepção de autoridade de subnicho — ser a referência, não só uma especialista — afeta o VPS que você consegue cobrar e o perfil de paciente que chega?"* [Calculator]

**Credit + promise:**
> *"Você investiu R$6.980 [autônomo] / R$14.800 [clínica]. Esse crédito vai integralmente para o [Sistema de Autoridade Clínica]. A diferença é R$5.820 / R$11.000. O SAC é o que acontece depois que o fluxo está previsível — referência de especialidade, editorial, rede de encaminhamento e 6 KPIs com calibração trimestral."*

**Close:** same definition question.

---

## Watch out for

- **Running the ascension before the result is visible** — without a specific, named result, the ascension is just an upsell with no earned permission. The client will hear "buy more" instead of "continue what's working." Wait for the result.
- **Skipping the gap question and going straight to the credit** — the credit is powerful only after the client has articulated the cost of the gap herself. If she hasn't named the problem, the credit frame answers a question she hasn't asked.
- **Presenting the full credit table** — one line: what she invested, what the difference is. The table is for the account manager's navigation, not for the client's reading.
- **Running a full anchor/polarity inversion on an ascension** — the trust is established. Presenting P10K as an anchor to sell P7K to an existing P3K client creates confusion, not polarity inversion. Skip the anchor — go directly to the credit frame for the specific next step.
- **Accepting "I'll think about it" as a close** — same rule as `closing-mechanic`. The ascension is also a decision, not an evaluation. Isolate the hesitation, name it, and close to a date if not to payment.
- **Offering a downsell in the ascension** — there is no downsell here. The client either ascends to the next step or books a specific date to do so. Offering a smaller product after she declined the ascension undermines the result narrative and signals that you are negotiating against yourself.
- **Collecting the ascension verbally and following up later** — in-meeting payment rule applies identically to ascension. Verbal commitment converts under 10%. Formalize in the same call.
- **Waiting too long after results materialize** — the emotional window is open right after results appear and for a short period after. A check-in at day 30 that becomes a check-in at day 60 because the account manager was busy loses the emotional peak. The 30-day check-in trigger is not a suggestion.

---

## See also

- [`workspace/psiativa/_config/esteira-de-produtos.md`](../../_config/esteira-de-produtos.md) — full credit table, intentional gap notes per product, built-in check-in trigger, compact product profiles for new promise statements
- [`workspace/psiativa/skills/closing-mechanic/SKILL.md`](../closing-mechanic/SKILL.md) — Step 6 of this skill; closing the ascension uses the same definition question, silence, and in-meeting payment rule
- [`workspace/psiativa/skills/spin-question-engine/SKILL.md`](../spin-question-engine/SKILL.md) — the re-diagnosis questions in Step 3 are abbreviated SPIN sequences; for P7K → P10K conversations where the gap requires deeper development, pull the full Necessidade sequence
- [`workspace/psiativa/_config/comercial-playbook.md`](../../_config/comercial-playbook.md) — concordance cycles and rotulação apply to ascension; the client's consistency with prior stated desires is the re-commitment lever
- [`workspace/psiativa/skills/gerar-contrato/SKILL.md`](../gerar-contrato/SKILL.md) — downstream: fires immediately after payment is confirmed in the ascension close
