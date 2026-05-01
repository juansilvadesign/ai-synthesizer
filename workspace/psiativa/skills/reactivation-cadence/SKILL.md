---
name: reactivation-cadence
description: Re-enter a cold or timed-out prospect from the nurture list. Takes the entry state (cold ghost, named timing, financial block, or clean no) and a current external trigger (calendar, competitive, proof, behavioral, or event) and produces a reactivation message that opens with what changed — not with "checking in." Output includes the message, a re-diagnosis question, and the three-touch cadence to exhaustion.
trigger: User has a prospect in the nurture list and asks to "reativar o contato", "como abordar quem disse não agora", "escrever mensagem para quem sumiu", "como voltar com quem disse que era caro", or "o que fazer com a lista de Route C". Also fires when a timing horizon the prospect named has passed, or when a competitive or seasonal trigger makes the problem more expensive to ignore.
---

# Reactivation Cadence — PsiAtiva

A timed-out prospect is not a lost prospect. What changed when she said "not now" was not her problem — it was her priority queue. The problem is still there. What reactivation does is not re-pitch the solution; it re-surfaces the cost of leaving the problem unsolved. Every reactivation message opens with what is now different in her external situation, not with "I'm following up."

> *"O cliente não compra porque disse que era importante. Ele compra quando continuar parado fica caro demais."*

**What reactivation is not:**
- A follow-up (follow-up is within 72h of the same conversation — covered in `contextual-outreach`)
- A pitch replay (sending the same message or offer again)
- A "checking in" message (signals no new information, triggers dismissal)
- An attempt to force a timed-out decision before a new external trigger exists

**This skill fires after:**
- `contextual-outreach` follow-up 2 produced no response → Route C
- Renata routed the prospect to Route C (nurture group)
- `closing-mechanic` produced "Agora não, com motivo claro" → named reason + re-entry date
- `objection-isolator` accepted a clean "no" and left the door open

**This skill hands off to:**
- `r1-brief` + R1 call when reactivation earns a response and terrain is ação
- `contextual-outreach` when response is early-stage curiosidade (re-enter the normal sequence)
- Passive nurture (content group) after three touches with no response

## Knowledge base

- [`knowledge/sources/101_agência/13_Um cliente não vai comprar na hora seu produto só.md`](../../../../knowledge/sources/101_agência/13_Um cliente não vai comprar na hora seu produto só.md) — source: importance vs. priority mechanic, seven triggers, cost-of-waiting framing, "não agora" is a priority gap not a real no
- [`knowledge/sources/101_agência/11_Conseguir atenção não é ter permissão para mandar.md`](../../../../knowledge/sources/101_agência/11_Conseguir atenção não é ter permissão para mandar.md) — source: what not to do after a response, investigate before explaining, real advance vs. polite signal
- [`workspace/psiativa/_config/sdr-renata.md`](../../_config/sdr-renata.md) — Route C definition, passive nurture group, escalation on re-engagement
- [`workspace/psiativa/_config/icp-clinica.md`](../../_config/icp-clinica.md) — Perfil A timing signals, objection bank (caixa, ética, secretária)
- [`workspace/psiativa/_config/icp-consultorio-solo.md`](../../_config/icp-consultorio-solo.md) — Perfil B timing signals, objection bank (VPS identity, sobrecarga, ética)
- [`workspace/psiativa/skills/contextual-outreach/SKILL.md`](../contextual-outreach/SKILL.md) — upstream: two-step follow-up that routes here; message register and channel logic
- [`workspace/psiativa/skills/closing-mechanic/SKILL.md`](../closing-mechanic/SKILL.md) — upstream: "Agora não, com motivo claro" route feeds re-entry date into this skill

---

## Input

Required to write the reactivation message:

| Input | Where it comes from | What it determines |
|---|---|---|
| **Prospect name + handle** | Original outreach record | Message personalization |
| **Entry state** | Last interaction record (see Step 1) | Message angle and wait period |
| **Named reason** (if any) | Renata notes or closing-mechanic route | Whether to honor timing or re-enter early |
| **Original pain signal** | Diagnostic or Renata NEPQ | What the new trigger connects to |
| **Current external trigger** (if any) | Profile check, competitive scan, calendar, news | Whether to fire now or wait |
| **ICP** | Confirmed earlier in the funnel | Vocabulary and message register |

**If no external trigger exists:** wait. A reactivation message with no external anchor reads as desperate. Schedule a re-check in 14 days rather than sending a message with nothing new to say.

---

## Step 1 — Entry State Classification

Classify the prospect before writing. Entry state determines the waiting period, the message angle, and the re-diagnosis question.

### State 1 — Cold Ghost

**What happened:** initial message sent, follow-up 1, follow-up 2 — no response. No conversation ever started.

**What it means:** the problem may not be urgent enough, the timing was wrong, or the message did not earn a response. No personal investment on her side.

**Wait period:** 30–45 days minimum. Less than that reads as re-sending the same rejected message.

**Re-entry angle:** something external changed (competitive, seasonal, or event trigger). Since there was no conversation, the message cannot reference a prior exchange — it must re-qualify as if approaching fresh, but with a different angle than the original.

---

### State 2 — Named Timing Block

**What happened:** Renata or the closer heard "not now" with a specific reason: *"depois do verão"*, *"quando virar o mês"*, *"em setembro"*, *"quando passar esse caos"*.

**What it means:** the problem was real enough to explain. She showed up enough to give a reason. This is the highest-quality entry state.

**Wait period:** honor the horizon she gave. If she said "depois de agosto" — first contact after August ends. Reaching out before the date she gave signals you were not listening.

**Re-entry angle:** reference the timing she gave directly: *"Você tinha mencionado [mês/período] — chegou nesse momento."* This activates consistency — she set the date, you honored it. The re-diagnosis question checks whether anything changed.

---

### State 3 — Financial Block

**What happened:** problem was confirmed as real, interest was genuine, but caixa was the named barrier. Entry product was offered and declined, or the prospect accepted the nurture route.

**What it means:** the problem is not going away. Financial situations change. A proof trigger (result from a similar profile at a lower investment threshold) or a longer-horizon entry point can re-open the conversation.

**Wait period:** 45–60 days. Faster re-entry looks like it was never about the timing.

**Re-entry angle:** proof from a comparable case + the lowest entry point relevant for her profile (GBP Scale or 45D). Do not jump to the core product — match the financial register she signaled.

---

### State 4 — Clean No After R1/R2

**What happened:** full qualification conversation. Closing-mechanic accepted the clean no. Door was left open with: *"Se a situação mudar, é só chamar."*

**What it means:** she has the most information of any prospect in the list. She evaluated and declined. Reactivation requires the strongest possible external trigger — a competitive signal, a structural change, or a concrete proof story that directly addresses the certeza that was missing.

**Wait period:** 60–90 days minimum. Less than that undermines the dignity of the "I'll leave the door open" close.

**Re-entry angle:** competitive escalation or proof trigger. The message must show that her situation is now materially different from when she decided — not that you have new things to say about the same situation.

---

## Step 2 — Reactivation Trigger Check

Do not send a reactivation message without a real external trigger. The trigger is what justifies the contact. Without it, the message reads as "checking in" — the phrase that signals the sender has nothing new to offer.

**Run this check before writing:**

### Trigger 1 — Calendar (named horizon passed)

*Best for: State 2 (Named Timing Block)*

The date or period she mentioned has arrived. No other hook needed — the trigger is the commitment she made.

**Signal:** the month or event she named has passed or is imminent.

---

### Trigger 2 — Competitive

*Best for: States 1, 3, 4*

A visible competitor in her area or niche has gained ground. More Google reviews, a new professional Instagram, a new clinic opened nearby. The problem's competitive cost has increased since the last conversation.

**How to check:** quick Google Maps search for her area — compare her review count to the nearest visible competitor. Check if any new profiles appeared since last contact.

**Signal:** competitor now has measurably more reviews, or a new competitor appeared in the same search results.

---

### Trigger 3 — Proof (similar case result)

*Best for: States 3, 4 — especially Financial Block and certeza #3 (Solução) failures*

A case was completed with a profile similar to hers that produced a concrete result. The social proof normalizes the problem and makes the solution feel more certain.

**What counts:** same ICP type (autônoma/clínica), same pain signal, same city or similar profile, concrete measurable outcome (reviews gained, confirmed appointments in X days, contact-to-session ratio improved).

**What does not count:** a vague "great results" or a case from a completely different profile.

---

### Trigger 4 — Behavioral

*Best for: States 1, 2 — when they were never fully qualified or the conversation was early-stage*

The prospect posted something that reveals the original pain is still active — a complaint about agenda instability, a question about process, a post about growth frustration, or any content that names the gap PsiAtiva solves.

**How to check:** check their Instagram feed and stories since last contact.

**Signal:** a post or story that directly references the original pain signal identified in the diagnostic.

---

### Trigger 5 — External Event

*Best for: all states, especially Perfil B*

A structural change in the market makes her situation more urgent than it was before. NR-1 2026 compliance (corporate demand for psychologists), seasonal therapy demand spike (January, August), local event creating new patient flow to the area.

**NR-1 2026 window:** if she has any corporate client potential or is positioned in a business district, this trigger gains strength as the enforcement date approaches. The competitive advantage of being positioned early decreases the closer the date gets.

**Seasonal signal:** January (post-holiday demand spike for therapy, new-year motivation for change), August (second semester restart, strong for clinics and autônomas alike).

---

### Trigger 6 — Urgency Escalation

*Best for: States 1, 3 — problems that grow worse over time without action*

The cost-of-waiting has compounded since the last contact. A prospect who had 5 Google reviews 3 months ago now has 4 (one was removed or competitors gained more). An autônoma who was losing contacts in session has now had another full quarter of invisible losses. The problem's calendar has moved.

**How to frame:** *"O problema não ficou em standby enquanto você esperava — ele continuou custando."*

---

## Step 3 — Message Construction

### The two rules that distinguish reactivation from spam

**Rule 1: Open with what is now different in her external situation — not with "checking in."**

The first line must reference the trigger. If the trigger is competitive: name the competitive change. If timing: honor the date. If proof: name the result. If event: name the event. The prospect must read the first line and think "something changed" — not "they're following up."

**Rule 2: Re-diagnose, do not re-pitch.**

The message earns a response. The response earns a conversation. The conversation earns the product. A reactivation message that presents a product before re-diagnosing the current state is a cold pitch wearing a reactivation costume.

After the trigger + observation: one re-diagnosis question. Not "are you interested now?" — something that checks whether her situation has changed in the relevant dimension.

---

## Pre-built Reactivation Messages by Trigger

### Trigger 1 — Calendar (named timing honored)

> *"[Nome], você tinha mencionado [mês/período] como o momento para retomar isso. Chegou nesse ponto — você chegou a avaliar como ficou a situação de [pain she named] nesse tempo?"*

*Perfil B version:*
> *"[Nome], lembro que você tinha falado que [depois de agosto / quando virar o mês] seria um momento melhor. Passou esse período — como tá a agenda agora?"*

**After she responds:** *"Faz sentido. Desde que a gente conversou, [external trigger if applicable — competitive, proof, etc.]. Vale a gente retomar?"*

---

### Trigger 2 — Competitive

*Perfil A:*
> *"[Nome], passei no Maps hoje — vi que [clínica X] na [região] agora tem [Y] avaliações. Da última vez que a gente conversou estava em [número anterior]. A diferença foi crescendo. Isso ainda é um ponto que você acompanha ou ficou em segundo plano?"*

*Perfil B:*
> *"[Nome], fiz uma busca rápida por psicólogas em [bairro/cidade] hoje. Apareceu um perfil novo que não estava antes, bem posicionado no Google. Dado o que você me contou [about her pain], achei que valia te contar. Como tá a situação por aí?"*

**Do not name the competitor by full name if it might feel threatening.** "Uma clínica próxima" or "um perfil novo na região" is enough — specificity is in the review count, not in calling out a rival by name.

---

### Trigger 3 — Proof (similar case result)

*Perfil A:*
> *"[Nome], acabamos de encerrar um projeto com uma clínica em [cidade similar] — mesma situação que você descreveu: [pain in one line]. Em [number of days], [concrete result, e.g.: 'saiu de 6 pra 22 avaliações no Google e a agenda fechou com 3 semanas de antecedência']. Pensei em te contar porque é exatamente o perfil da nossa conversa."*

*Perfil B:*
> *"[Nome], acabei de encerrar um projeto com uma psicóloga autônoma em [cidade similar] que tinha o mesmo gargalo que você me descreveu — [pain]. Em [number of days], [specific result]. Achei que valia te falar porque o cenário era muito parecido com o seu."*

**After she responds:** *"Fico feliz que fez sentido. A sua situação mudou em alguma coisa desde que a gente conversou ou continua parecida?"*

---

### Trigger 4 — Behavioral (she posted about the pain)

> *"[Nome], vi um post seu sobre [specific topic that reveals the pain — e.g., 'variação de agenda', 'paciente que sumiu', 'mês imprevisível']. Isso ainda tá sendo um ponto de atenção ou a situação melhorou?"*

**This message is the most natural because it references something she published herself.** It signals that someone is paying attention — not following up. Use only if the post is recent (within 7–10 days) and genuinely related to the original pain.

---

### Trigger 5 — External Event (NR-1 2026 / seasonal)

*NR-1 2026 — Perfil B:*
> *"[Nome], com a NR-1 entrando em vigor em 2026, empresas vão precisar oferecer suporte psicológico. Psicólogas bem posicionadas online — Google Maps, perfil claro — vão capturar essa demanda antes das outras. Você chegou a pensar nesse ângulo depois que a gente conversou?"*

*Seasonal — January (both ICPs):*
> *"[Nome], janeiro costuma ser um dos meses com mais procura espontânea por terapia. Faz sentido com o que você me descreveu sobre [pain]. A agenda por aí está recebendo isso ou ainda tá estável?"*

*Seasonal — August (Perfil A):*
> *"[Nome], agosto marca o início do segundo semestre — historicamente um dos períodos de maior retomada de agenda para clínicas. Dado o que a gente conversou sobre [pain], queria saber se o cenário por aí mudou desde então."*

---

### Trigger 6 — Urgency Escalation

> *"[Nome], faz [X meses] desde que a gente conversou. Nesse tempo, [specific compounding — e.g., 'a diferença de avaliações no Google entre você e os perfis mais bem posicionados da região cresceu'] / ['você ficou mais um trimestre sem processo de resposta enquanto estava em sessão']. O problema não pausou nesse período. Vale dar uma olhada nisso agora?"*

---

## Step 4 — Re-entry Sequence by Entry State

Do not send all three touches close together. Space matters — it is part of the signal that you are not desperate.

### State 1 — Cold Ghost

| Touch | Timing | Trigger | Message angle |
|---|---|---|---|
| Touch 1 | 30–45 days after Route C | Competitive or seasonal | Fresh angle, no reference to prior silence |
| Touch 2 | 21–28 days after Touch 1 | Proof or behavioral | Case story or content reference |
| Touch 3 | 21–28 days after Touch 2 | Soft exit | Clean "I'll leave the door open" — see below |

---

### State 2 — Named Timing Block

| Touch | Timing | Trigger | Message angle |
|---|---|---|---|
| Touch 1 | On or just after the horizon she named | Calendar | Honor the date she gave, re-diagnose |
| Touch 2 | 14–21 days after Touch 1 (if no response) | Competitive or proof | Escalate the cost, different angle |
| Touch 3 | 14–21 days after Touch 2 (if no response) | Soft exit | Clean close, route to nurture group |

---

### State 3 — Financial Block

| Touch | Timing | Trigger | Message angle |
|---|---|---|---|
| Touch 1 | 45–60 days after Route C | Proof (same ICP, low entry) | Similar case + entry product at floor |
| Touch 2 | 21–28 days after Touch 1 | Urgency escalation | Cost of waiting compounded |
| Touch 3 | 21–28 days after Touch 2 | Soft exit | Clean close |

---

### State 4 — Clean No After R1/R2

| Touch | Timing | Trigger | Message angle |
|---|---|---|---|
| Touch 1 | 60–90 days after close | Competitive or proof (strong) | External change — not what PsiAtiva can offer, but what her situation now looks like |
| Touch 2 | 28–35 days after Touch 1 | Urgency escalation | Direct cost framing |
| Touch 3 | 28–35 days after Touch 2 | Soft exit | Clean close |

---

## Step 5 — Touch 3 / Soft Exit

After two touches without response, the third and final contact is a soft exit. Its job is twofold: give her a final low-friction option to respond, and route her to passive nurture if she does not.

**Do not pitch in Touch 3. Do not reference the prior silence. One sentence, one open door.**

> *"[Nome], última vez que entro em contato por agora. Se algum dia quiser entender como psicólogas com um cenário parecido com o seu estão organizando a captação, é só chamar — sem compromisso nenhum."*

*After sending Touch 3:*
- No response → route to passive nurture (content group via Renata's Route C)
- Response received at any point → diagnose mental stage, treat as new conversation, do not reference how many times you reached out

---

## Passive Nurture — After Three Touches

Route to the WhatsApp content group that Renata manages. The group provides:
- Periodic value content (captação, processo, ICP-relevant topics)
- Indirect presence without pressure
- A natural re-entry point when her timing changes

This is not abandonment. The group maintains the relationship without requiring active sales effort. When she posts a question or reacts to something, that behavioral signal can restart a new reactivation cycle.

**Group invitation phrase (from Renata):**
> *"Sem problema nenhum! O que posso fazer é te incluir num grupo que a PsiAtiva mantém com conteúdo sobre captação e gestão pra psicólogas, de graça e sem compromisso. Quando o momento chegar, você já vai ter uma ideia bem clara do que a gente faz. Topa?"*

---

## Output Format

```
## Reativação — [Nome / Handle]

**Entry state:** [State 1–4 + brief reason]
**Last contact:** [date or approximate]
**Original pain:** [named pain signal from diagnostic or Renata]
**Trigger available:** [Trigger 1–6 + specific evidence]

---

**Mensagem de reativação:**

[message text — 3–5 lines max]

---

**Se ela responder:**
[1 re-diagnosis question to check current state]

**Se não responder (próximo toque):**
[Touch 2 trigger + message approach]

**Touch 3 / soft exit:**
[exact soft exit phrase]

**Após Touch 3 sem resposta:**
→ Rota para grupo de nutrição passiva
```

---

## Watch out for

- **Sending a reactivation message with no external trigger** — "Oi, passando para saber como você está" is the most common reactivation failure. It signals that nothing changed, which confirms her original decision was right. Wait until a real trigger exists.
- **Re-pitching the product in the reactivation message** — the message earns a response, the response earns a conversation, the conversation earns the sale. A product in the reactivation message skips two steps and positions you as a vendor who ignored the "not now."
- **Contacting before the horizon she named has passed** — if she said "depois de agosto" and you reach out in July, you signal that you did not respect the timing she gave. Honor the date — it is the consistency trigger that makes the re-entry feel natural.
- **Sending Touch 2 within 48–72 hours of Touch 1** — reactivation touches need space. Less than 2 weeks between touches reads as pressure. Pressure confirms the original "not now."
- **Treating all "not nows" the same** — a State 2 (named timing) is a near-purchase with a pending re-entry date. A State 1 (cold ghost) may never have been qualified. A State 4 (clean no post-R1) has the highest bar for reactivation. The message, trigger, and waiting period differ substantially between states.
- **Running three touches within a single month** — the three-touch maximum is a safeguard, not a sprint. Exhausting it in 30 days leaves no channel open. Space the touches across 6–10 weeks minimum.
- **Not routing to passive nurture after Touch 3** — the ghost pipeline is the outcome of not routing. "I'll follow up later" with no system behind it produces the same outcome as no reactivation at all. Route to the content group — that is the system.
- **Using the same message angle twice** — if Touch 1 was competitive and she did not respond, Touch 2 should be proof or behavioral. Repeating the competitive angle in Touch 2 is the same message, not a new signal.

---

## See also

- [`workspace/psiativa/skills/contextual-outreach/SKILL.md`](../contextual-outreach/SKILL.md) — upstream: follow-up 2 is the trigger for State 1 (cold ghost) entry into this skill
- [`workspace/psiativa/skills/closing-mechanic/SKILL.md`](../closing-mechanic/SKILL.md) — upstream: "Agora não, com motivo claro" route produces State 2 and State 4 entries
- [`workspace/psiativa/_config/sdr-renata.md`](../../_config/sdr-renata.md) — Route C definition, passive nurture group, re-engagement escalation
- [`workspace/psiativa/skills/r1-brief/SKILL.md`](../r1-brief/SKILL.md) — downstream: when reactivation earns a response and terrain is ação, fire this before the R1
- [`knowledge/sources/101_agência/13_Um cliente não vai comprar na hora seu produto só.md`](../../../../knowledge/sources/101_agência/13_Um cliente não vai comprar na hora seu produto só.md) — source: importance vs. priority mechanic, seven triggers, cost-of-waiting framing
