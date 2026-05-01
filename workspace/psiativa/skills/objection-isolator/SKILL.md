---
name: objection-isolator
description: Real-time objection support for R1/R2 calls. Takes the objection phrase heard and outputs the missing certeza diagnosis, a 3-step validation-location-isolation response, and the return-to-line action based on what the prospect reveals.
trigger: User hears an objection during a sales conversation ("tá caro", "vou pensar", "já tentei isso", "preciso ver com meu sócio", "não quero parecer comercial", "agora não é o momento") and asks to "como responder", "isolar a objeção", "o que fazer quando ela diz X", or "qual certeza está faltando".
---

# Objection Isolator & Redirector — PsiAtiva

A real-time support skill for the R1/R2 closer. An objection is not a wall — it is a signal pointing to the exact certeza that was not consolidated. The job is never to rebate the surface phrase; it is to locate the real cause behind it and isolate it with one clean question. Do not explain more. Do not discount. Do not collapse into "fico no aguardo."

## Knowledge base

- [`knowledge/sales/articles/oultimomentor/101_agencia.md`](../../../../knowledge/sales/articles/oultimomentor/101_agencia.md) — Phase 12 (objection isolation) and Phase 13 (closing); Six Certezas framework; Straight Line mechanics
- [`knowledge/sources/101_agência/17_Objeção é o caminho da venda fechada.md`](../../../../knowledge/sources/101_agência/17_Objeção é o caminho da venda fechada.md) — source: 6 certeza failures, 3-step structure, verbatim isolation scripts
- [`workspace/psiativa/_config/sdr-renata.md`](../../_config/sdr-renata.md) — PsiAtiva-specific objection families (ética/identidade, tempo, dinheiro, confiança/risco); escalation rules
- [`workspace/psiativa/_config/comercial-playbook.md`](../../_config/comercial-playbook.md) — R1+R2 call structure; where objection handling fits in the flow
- [`workspace/psiativa/_config/positioning.md`](../../_config/positioning.md) — guarantee language for investment objections; process vs. marketing framing for ethics objections

---

## The Six Certezas — Diagnostic Map

Every objection signals a missing certeza. Locate it before responding.

| Certeza | What it means | Signal phrases |
|---|---|---|
| **1 — Problema** | She has not felt the pain as real or central | *"Não vejo tanta urgência"*, *"Acho que tô bem"*, *"Não sei se preciso disso"* |
| **2 — Prioridade** | She sees the problem but has not moved it to the top of her queue | *"Faz sentido mas agora não"*, *"Mais pra frente"*, *"Tem outras coisas primeiro"* |
| **3 — Solução** | She doubts this specific path resolves her problem | *"Já tentei isso antes"*, *"Não sei se vai funcionar"*, *"Não é bem o que eu precisava"*, *"Não quero parecer comercial"* |
| **4 — Você** | She is not yet convinced you can conduct this | *"Deixa eu analisar melhor"*, *"Me manda material"*, *"Vou dar uma pesquisada"*, *"Vou pensar com calma"* |
| **5 — Investimento** | She has not seen the proportionality or has real cash constraint | *"Tá caro"*, *"Não esperava esse valor"*, *"Não tenho orçamento agora"* |
| **6 — Timing** | "Not now" may be real or may be a polite exit | *"Agora não é o momento"*, *"Quando passar [event]"*, *"Quando virar o mês"* |

---

## The 3-Step Response Structure

Apply this structure to every objection, in this order. Do not skip Step 1. Do not stack steps.

### Step 1 — Validar (without collapsing)

One short phrase. Acknowledge without agreeing, without defending, without apologizing.

> *"Perfeito."*  
> *"Faz sentido."*  
> *"Entendi."*  
> *"Justo."*

Do not say "mas" or "porém" immediately after. One beat of space.

### Step 2 — Localizar (ask for permission to diagnose)

One sentence that positions what comes next as a question, not a defense.

> *"Só quero entender onde está a trava pra não responder no escuro."*  
> *"Antes de responder, preciso entender onde exatamente está a dúvida."*  
> *"Não quero assumir o que está pesando — deixa eu perguntar direto."*

### Step 3 — Isolar (the single diagnostic question)

One question that names 2–3 possible root causes and asks her to pick the one that fits. Do not offer more than three options — she picks the easiest.

---

## Pre-built Isolation Scripts — by Objection

### "Tá caro" / "Não esperava esse valor"

**Certeza ausente:** 5 — Investimento  
*(Could also be Certeza 1 — Problem not felt as costly enough, or Certeza 3 — Solution not seen as proportionate)*

**Isolation question:**
> *"Perfeito. Quando você diz caro, quero só entender: estamos falando de caixa neste momento ou o valor ainda não parece proporcional ao problema que conversamos?"*

**After she answers:**
- If **caixa** → ask: "Se o caixa não fosse a trava agora, o resto faria sentido pra você?" → route to entry product (GBP) or adjusted timing  
- If **proporcionalidade** → Implicação was not landed: return to the invisible cost question before re-anchoring price  
- If she conflates both → isolate the dominant one: *"Entre os dois, qual pesa mais na decisão hoje?"*

---

### "Vou pensar" / "Deixa eu analisar" / "Me manda material"

**Certeza ausente:** unknown — must isolate

**Isolation question:**
> *"Justo. Pra eu não te responder errado: você vai pensar mais sobre o investimento, sobre a prioridade disso agora ou sobre confiar que esse formato resolve o problema?"*

**After she answers:**
- If **investimento** → go to Certeza 5 path above  
- If **prioridade** → go to Certeza 2 path (cost of waiting)  
- If **confiança no formato** → go to Certeza 3 path (solution doubt)  
- If still vague → *"Das três opções que coloquei, qual mais se aproxima?"* — do not accept silence as an answer

---

### "Não quero parecer comercial" / "Isso vai parecer que estou me vendendo"

*(PsiAtiva-specific — ethics/identity objection. Most common blocker for this ICP.)*

**Certeza ausente:** 3 — Solução  
*(She is not doubting the problem — she is doubting that this solution is compatible with who she is as a professional)*

**Do not defend the solution yet.** Diagnose first.

**Isolation question:**
> *"Entendo essa preocupação. O que você está imaginando que isso pareceria — anúncio de oferta, post de venda ou algo mais sutil que ainda passe a mensagem certa?"*

**After she answers:**
- If she imagines **advertising/promotion style** → reframe: *"Faz sentido. O que estamos falando é diferente — é organizar o processo pra quem já está buscando psicólogo, não divulgar pra quem não pediu. Quem te encontra hoje por indicação vai no Google confirmar. Se não encontra nada, vai embora. Isso incomoda você ou parece razoável?"*
- If she imagines **social media selling tone** → use PsiAtiva positioning: *"A ideia aqui não passa por tom comercial. Passa por processo. Confirmar uma sessão com antecedência não é pressão — é cuidado. Faz sentido essa distinção?"*
- If still resistant after second attempt → escalate to human (same objection twice = escalation trigger)

---

### "Já tentei isso antes e não funcionou" / "Já paguei agência e não deu resultado"

**Certeza ausente:** 3 — Solução  
*(She has evidence the vehicle fails. Do not defend your version before diagnosing where the failure was.)*

**Isolation question:**
> *"Entendi. E quando não funcionou, o problema maior foi a entrada de contatos, a qualidade de quem chegava, o atendimento no WhatsApp depois ou a conversão de contato pra sessão confirmada?"*

**After she answers:**
- She will point to a specific stage → this is where the prior solution failed  
- Confirm that PsiAtiva's process addresses that stage specifically, not just the stage she mentioned to the prior vendor  
- If she says "tudo junto, foi uma bagunça" → *"Faz sentido. Quando não existe processo, tudo parece falhar junto mas a causa costuma ser um ponto. O que mais incomodou — gente chegando e sumindo, ou o número de contatos nunca decollou?"*

---

### "Preciso ver com meu sócio" / "Preciso alinhar com a equipe"

**Certeza ausente:** 4 — Você or wrong decisor in the room

**Isolation question:**
> *"Perfeito. E teu sócio hoje entraria mais pra validar o investimento, a prioridade do projeto ou a confiança no formato da solução?"*

**After she answers:**
- If **investimento** → get her position first: *"Você pessoalmente, pelo que conversamos, vê sentido nisso?" → If yes: "Então eu preciso montar um argumento que funcione pra ele também. Me conta: o que costuma pesar mais nas decisões do teu sócio — retorno esperado, processo, ou risco?"*
- If **prioridade** → same dynamic above — identify her own position first
- If she is genuinely not the decision-maker → *"Faz sentido. Teria como incluí-lo numa conversa rápida pra não depender de repasse?"* → escalate to schedule R2 with both

---

### "Não tenho tempo pra isso" / "Não dá pra tocar mais uma coisa agora"

**Certeza ausente:** 2 — Prioridade  
*(She sees the problem but it has not risen above the daily noise)*

**Isolation question:**
> *"Entendo. Só quero confirmar: o que faz o tempo ser a trava hoje — a operação está num momento de caos que não permite mudança, ou isso ainda não subiu na fila de prioridades?"*

**After she answers:**
- If **caos/timing** → go to Certeza 6 path (timing) — may be real, ask for a re-entry date  
- If **priority** → activate cost-of-waiting: *"Pelo que você me contou, quanto tempo a agenda tem ficado oscilando? Porque cada mês de oscilação sem processo é faturamento que não volta — não é culpa, é como a perda funciona. Isso faz sentido olhar agora ou você realmente prefere esperar?"*

---

### "Agora não é o momento" / "Depois da alta temporada" / "Quando virar o mês"

**Certeza ausente:** 6 — Timing  
*(May be real constraint or a polite exit — you only find out by asking)*

**Isolation question:**
> *"Justo. O que faz o momento não ser bom hoje: caixa, operação, foco em outras prioridades ou o problema ainda não estar doendo o suficiente?"*

**After she answers:**
- If **caixa** → offer entry product (GBP at R$680 à vista) or scheduled start: *"Se for caixa, faz sentido. Existe um momento nos próximos 30 dias que seria mais viável — ou é um horizonte maior?"*
- If **operational chaos** → validate + anchor cost: *"Faz sentido. E enquanto a operação fica assim, o padrão da agenda e dos contatos — ele fica estável ou tende a piorar?"*
- If **não está doendo o suficiente** → this is really Certeza 1 (Problema) — return to the invisible cost question

---

### Compound Objection (two objections at once)

> "Tá caro **e** preciso ver com meu sócio."  
> "Vou pensar **porque** já fiz algo parecido antes."

**Rule:** never try to address both at once. Isolate the dominant one first.

**Isolation question:**
> *"Entre [objeção 1] e [objeção 2], qual dos dois pesa mais na sua decisão hoje?"*

After she picks one → resolve that certeza completely before returning to the second.

---

## Accepting a Clean "No"

Not every conversation ends in a sale. A clear "no" is more valuable than a fake follow-up.

> *"Vendedor ruim coleciona conversas abertas. Vendedor bom coleciona clareza."*

**When to accept and close cleanly:**
- She cannot or will not identify a specific certeza gap
- She has confirmed that the problem is not a priority and sees no urgency
- The same objection appears twice after isolation — escalate to human, then accept if human cannot break it either
- The decision-maker is absent and cannot be included in a follow-up

**Closing cleanly:**
> *"Entendo perfeitamente. Nesse caso o melhor que posso fazer é deixar a porta aberta. Se a situação mudar e quiser entender como isso funciona na prática, é só chamar — sem nenhum compromisso."*

Route to nurture (Route C in Renata's flow). Do not leave it as a phantom "vamos ver".

---

## Output Format

```
## Objeção Isolada — "[verbatim phrase]"

**Certeza ausente (diagnóstico):** Certeza no X — [brief reason]

---

**Step 1 — Validar:**
[phrase]

**Step 2 — Localizar:**
[phrase]

**Step 3 — Isolar:**
[isolation question]

---

**Se ela responder [X]:**
[next action + phrase]

**Se ela responder [Y]:**
[next action + phrase]

**Se não conseguir isolar após 2 tentativas:**
[escalate or accept clean no]
```

---

## Watch out for

- **Answering "tá caro" with price justification before diagnosing** — "mas está incluso X, Y, Z" and "consigo parcelar" are the two most common premature responses; both signal you're in defense mode
- **Accepting "vou pensar" without isolating** — "fico no aguardo" closes zero sales; it opens a ghost pipeline that dies quietly
- **Defending the solution when the real objection is ethics/identity** — for PsiAtiva's ICP, "não quero parecer comercial" is Certeza 3, not Certeza 5; explaining the deliverables does nothing; you need to reframe the solution's nature first
- **Stacking more than 3 certeza options in the isolation question** — she picks the easiest escape, not the real cause; limit to 2 or 3 named options
- **Re-entering price before Implicação is fully landed** — if she says "tá caro" and you did not make the problem feel expensive enough in the SPIN phase, the fix is SPIN, not discount
- **Using "marketing", "leads", or "resultado" in objection handling language** — these words activate vendor mode exactly when you need to be in consultant mode
- **The same objection appearing twice** — per Renata's escalation rules: if the same objection surfaces twice without breaking, escalate to human; do not attempt a third pass on the same certeza

---

## See also

- [`workspace/psiativa/skills/spin-question-engine/SKILL.md`](../spin-question-engine/SKILL.md) — if the objection reveals a certeza gap in Problema or Prioridade, return to SPIN (Implicação not fully landed)
- [`workspace/psiativa/_config/comercial-playbook.md`](../../_config/comercial-playbook.md) — full R1+R2 flow; this skill operates during the objection phase of R1 and the closing phase of R2
- [`workspace/psiativa/_config/sdr-renata.md`](../../_config/sdr-renata.md) — Renata's 5-family objection bank (ética, tempo, dinheiro, necessidade não percebida, confiança); same validate→reframe→question structure applies
- [`workspace/psiativa/_config/esteira-de-produtos.md`](../../_config/esteira-de-produtos.md) — entry product options for investment objections where caixa is the confirmed block
- [`knowledge/sales/articles/oultimomentor/101_agencia.md`](../../../../knowledge/sales/articles/oultimomentor/101_agencia.md) — Phase 12 and Phase 13 source; Six Certezas and closing structure
