---
name: contextual-outreach
description: Take the output of a 2-minute diagnostic and craft a short, context-specific first message (WhatsApp or Instagram DM) that leads with a visible observation — never with a service pitch. Output includes channel selection rationale, the first message, and the post-response pivot question to transition into Renata's qualification flow.
trigger: User has a completed diagnostic output (from diagnostico-2min) and asks to "escrever a abordagem", "montar a mensagem", "como entrar em contato" or "gerar o primeiro contato" for a specific prospect. Also fires when reviewing an outreach draft that feels too formal, too generic, or reads like a service pitch.
---

# Contextual Outreach Architect — PsiAtiva

A first-contact message skill. It takes the diagnostic output and converts the clearest failure into a 2–3 line message that sounds like someone who actually looked at the profile — not like a service provider copy-pasting a template. The message does one job: earn a response. It does not sell, pitch, explain, or ask for a meeting.

## Knowledge base

- [`knowledge/sources/101_agência/10_Prospecção manual funciona.md`](../../../../knowledge/sources/101_agência/10_Prospecção manual funciona e funciona pra caralho.md) — what kills outreach before the conversation starts: artificial formality, generic problem, long text, AI-smell
- [`knowledge/sources/101_agência/09_Usar o canal errado.md`](../../../../knowledge/sources/101_agência/09_Usar o canal errado mata a venda antes da conversa.md) — channel selection logic: enter where the client operates, not where she appears
- [`knowledge/sources/101_agência/11_Conseguir atenção.md`](../../../../knowledge/sources/101_agência/11_Conseguir atenção não é ter permissão para mandar.md) — what to do after a response: investigate mental stage, never dump information
- [`workspace/psiativa/skills/diagnostico-2min/SKILL.md`](../diagnostico-2min/SKILL.md) — upstream: provides the failure flags this skill converts into message copy
- [`workspace/psiativa/_config/sdr-renata.md`](../../_config/sdr-renata.md) — downstream: Renata's NEPQ qualification flow picks up after the prospect responds
- [`workspace/psiativa/_config/marca-identidade-visual.md`](../../_config/marca-identidade-visual.md) — vocabulary compliance (no "marketing", "leads", "soluções personalizadas")

---

## Input

Required: the completed diagnostic output from `diagnostico-2min`, specifically:
- Which checks **failed** (1–2 most visible ones)
- The prospect's **name** (or clinic name)
- Any **channel signals** from the diagnostic (WhatsApp link in bio, Instagram-only presence, Google Maps listing)

**If no diagnostic has been run:** run `diagnostico-2min` first. A generic message is worse than no message.

---

## Step 1 — Channel Selection

The channel is not the prospect's preferred social platform — it's where she **operates decisions**.

### Channel logic for psychology niche

| Profile signal | Channel verdict |
|---|---|
| Bio has WhatsApp link or button | **WhatsApp — primary entry** |
| Bio says "manda direct" with no WhatsApp | **Instagram DM — entry, escalate to WhatsApp after response** |
| Active Instagram, link to Linktree with WhatsApp listed | **WhatsApp — go directly, skip Linktree friction** |
| Google Maps listing with phone number | **WhatsApp — psychologists rarely convert on phone; use the number to find WhatsApp** |
| No link, no phone, Instagram only | **Instagram DM — only viable entry** |
| Clinic with receptionist visible in bio/posts | **WhatsApp — goes to receptionist first; message must survive the gatekeeping layer** |

**Rule for psychology niche:** Instagram = vitrine. WhatsApp = where decisions happen. Even when the diagnostic finds an Instagram failure, the approach channel is often WhatsApp — because that's where she actually responds.

**Exception:** if the primary failure is visual (Percepção — broken feed, bad design), Instagram DM works better because the problem is visible in the channel you're using.

---

## Step 2 — Message Construction

### The 3 required elements

Every first message must have all three. In this order:

1. **Uma observação específica** — name one specific, visible thing you saw on her profile. Not "analisei seu perfil." Something concrete: "o link da bio não está funcionando", "o perfil não mostra serviços", "vi que não tem CTA nas postagens". If you can't name it specifically, you haven't done the diagnostic.

2. **Uma implicação curta** — one sentence connecting that observation to a possible cost. Not a threat. Not a promise. A connection: "isso costuma esfriar contato antes de chegarem ao WhatsApp" or "paciente que chega por busca pode não entender o que você oferece antes de ir embora".

3. **Uma pergunta diagnóstica** — one question that invites her to confirm or correct the observation. Not "posso te ajudar?". Not "vamos marcar uma call?". Something that makes her think about her own situation: "isso aparece como problema ou costuma funcionar pelo direct?", "alguém já comentou sobre isso?" or "quando chega contato assim, dá pra recuperar depois?".

### The 3 prohibited elements

| Prohibited | Why it kills the message |
|---|---|
| "Espero que esteja bem" / "Tudo bem?" | Signals copy-paste. She knows immediately. |
| "Analisei seu perfil e identifiquei oportunidades" | Every spam message in her inbox sounds like this. |
| "Trabalho com / Oferecemos soluções para" | Leads with "I do X" not "I saw Y" — vendor frame. |
| First message ends with "Podemos agendar uma reunião?" | No diagnosis = no earned meeting. She says no. |
| Message longer than 4 lines | She reads the first two and decides. Long = generic. |
| Emojis as decoration | 0 or 1, only if they fit the register. Never as filler. |

---

## Pre-built First Messages — by Failure Type

### Failure: Clareza (bio vague, specialty not visible)

**WhatsApp:**
> Oi [Nome]! Vi seu perfil — vi que é psicóloga, mas não ficou claro logo de cara a especialidade ou quem você atende. Quando alguém chega por indicação e vai olhar antes de chamar, isso costuma gerar dúvida ou as pessoas chamam mesmo assim?

**Instagram DM:**
> Oi [Nome]! Passei pelo seu perfil e fiquei com curiosidade — a bio não deixa muito claro o tipo de atendimento que você faz. Isso já teve algum reflexo em quem chega perguntando coisas básicas antes de agendar?

---

### Failure: Contato (sem link, link quebrado, sem CTA)

**WhatsApp:**
> Oi [Nome]! Estava olhando o perfil de vocês e o link da bio não tá abrindo — vai pra uma página com erro. Clínica de [cidade], certo? Quando alguém tenta entrar em contato por ali e não consegue, vocês costumam perceber ou só notam depois de um tempo?

**Instagram DM:**
> Oi [Nome]! Vi seu perfil — não tem link nem botão de contato na bio. Quem chega pelo Instagram e quer agendar, como normalmente entra em contato? Pelo direct mesmo?

---

### Failure: Percepção (feed inconsistente, visual amador)

*(Instagram DM preferred — problem is visible in the channel)*

**Instagram DM:**
> Oi [Nome]! Passei pelo seu perfil — vi que você tem bastante conteúdo, mas o visual das postagens tá bem variado em estilo. Paciente que chega por busca e avalia o perfil antes de chamar, você sente que isso influencia na decisão deles?

**WhatsApp:**
> Oi [Nome]! Olhei o Instagram de vocês. O conteúdo tá lá, mas o visual das publicações não tem um padrão claro — cada post parece feito de um jeito diferente. Quando alguém indica a clínica e o indicado vai olhar o perfil antes de chamar, isso costuma ajudar ou pode estar esfriando a decisão?

---

### Failure: Prova (sem avaliações Google, sem rosto, sem bastidor)

**WhatsApp:**
> Oi [Nome]! Vi o perfil e o Google Maps — vocês têm [X] avaliações lá. A clínica [concorrente próxima] do mesmo bairro tem [Y]. Paciente novo que pesquisa psicólogo na [cidade] e compara os dois, você sente que isso faz diferença na hora de escolher com quem chamar?

**WhatsApp (solo, sem rosto visível):**
> Oi [Nome]! Vi seu perfil — tem bastante post de conteúdo, mas não aparece seu rosto nem o consultório em nenhum deles. Para quem está considerando começar terapia e quer ter uma ideia de com quem vai falar antes do primeiro contato, isso costuma ser uma dúvida?

---

### Failure: Direção Comercial (conteúdo sem CTA, presença sem destino)

**WhatsApp:**
> Oi [Nome]! Vi o Instagram de vocês — tem bastante conteúdo bom, mas nenhuma postagem termina com uma chamada clara pra agendar ou pra chamar no WhatsApp. Paciente que leu e se interessou, como normalmente dá o próximo passo?

**Instagram DM:**
> Oi [Nome]! Passei pelo seu perfil — posts com bom engajamento, mas sem nenhum CTA. Quem lê e quer conversar, como geralmente chega até você?

---

## Step 3 — After the Response

Getting a response is not a sale. It's permission to start a commercial conversation.

**What to do after she responds:**

Do not explain what PsiAtiva does. Do not list deliverables. Do not ask for a meeting yet. Ask one question to identify her mental stage.

Use one of these pivot questions to transition into the diagnosis (Renata's NEPQ or the SPIN engine):

| Her response tone | Pivot question |
|---|---|
| Confirms the problem exists | *"Entendi. Pra não mandar algo genérico — hoje o maior gargalo é gerar mais contatos ou converter melhor os que já chegam?"* |
| Minimizes the problem ("funciona pelo direct mesmo") | *"Faz sentido. E quando chega contato pelo direct, existe algum processo de resposta ou depende do atendimento do dia?"* |
| Curious, asks what you do | *"Funciona por etapas, mas antes de eu explicar qualquer coisa — hoje a agenda tá estável ou tem oscilação mês a mês?"* |
| Defensive ("não estou interessada em marketing") | *"Entendo, e nem era essa a direção. Só fiquei com curiosidade sobre como vocês lidam com os contatos que chegam — não tem nada a ver com anúncio."* |
| Asks for price immediately | *"Depende do que precisa ser resolvido. Mas antes disso: o problema principal hoje é mais a entrada de contatos ou o que acontece depois que eles chegam?"* |

**Rule:** Never send more than 2 consecutive messages without a response. If no response after 2nd follow-up → Route C (nurture).

---

## Follow-up Sequence (if no response)

**Follow-up 1 (24–48h after first message):**
A single short message referencing the same observation — different angle, still no pitch.

> *"[Nome], só pra checar — o link da bio ainda tá com erro ou já resolveram?"*
> *"[Nome], passando pra conferir se a pergunta fez sentido ou se não é o momento."*

**Follow-up 2 (48–72h after follow-up 1):**
A soft exit — no pressure, opens the door to nurture.

> *"Sem problema nenhum se não for o momento. Se algum dia quiser entender como clínicas parecidas com a de vocês estão resolvendo isso, é só chamar."*

After follow-up 2 with no response → stop. Do not send a third message. Route to nurture list.

---

## Output Format

```
## Abordagem — [Nome / Handle]

**Canal selecionado:** [WhatsApp / Instagram DM]
**Motivo:** [1 line justification based on channel signals]

**Falha principal usada:** [which diagnostic failure this message is built on]

---

**Primeira mensagem:**

[message text — 2–4 lines max]

---

**Se ela responder:**
[1 pivot question to transition to NEPQ or SPIN]

**Follow-up 1 (se não responder):**
[follow-up text]

**Follow-up 2 (se não responder):**
[soft exit text]
```

---

## Watch out for

- **Starting with any form of "Olá, tudo bem? / Espero que esteja bem"** — signals template immediately. She has received this opening 40 times this month.
- **Naming PsiAtiva in the first message** — she should ask what you do, not receive a pitch. The brand name appears after she shows interest.
- **Using two failures in the first message** — pick one, the most specific and visible. Two observations = catalogue. One observation = someone who actually paid attention.
- **Asking for a meeting in the first message** — the first message earns a response. The meeting is earned after diagnosis.
- **Using forbidden vocabulary in outreach copy:** *"marketing digital", "leads qualificados", "presença online", "soluções personalizadas", "aumentar resultados"* — she's been targeted with this exact language by agencies she doesn't trust. A single forbidden word marks the message as generic.
- **Sending to a psychology professional the same message you'd send to a dental clinic** — the niche signals that you know her world. If the message works for any health business, rewrite it.
- **After she responds: dumping information** — explain nothing until a pain signal is confirmed. Question first, always.

---

## See also

- [`workspace/psiativa/skills/diagnostico-2min/SKILL.md`](../diagnostico-2min/SKILL.md) — upstream: must be run before this skill to generate the failure flags used in message construction.
- [`workspace/psiativa/_config/sdr-renata.md`](../../_config/sdr-renata.md) — downstream: Renata's 5-stage NEPQ flow picks up after the prospect responds to this message.
- [`workspace/psiativa/skills/spin-question-engine/SKILL.md`](../spin-question-engine/SKILL.md) — downstream (R1): SPIN deepening after Renata qualifies the lead.
- [`knowledge/sources/101_agência/10_Prospecção manual funciona.md`](../../../../knowledge/sources/101_agência/10_Prospecção manual funciona e funciona pra caralho.md) — source: what kills outreach (formality, generic problem, AI-smell).
- [`knowledge/sources/101_agência/09_Usar o canal errado.md`](../../../../knowledge/sources/101_agência/09_Usar o canal errado mata a venda antes da conversa.md) — source: channel selection logic.
