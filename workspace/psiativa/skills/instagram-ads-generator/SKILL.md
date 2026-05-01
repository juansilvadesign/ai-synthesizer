---
name: instagram-ads-generator
description: Generates PsiAtiva-branded Instagram/Meta ad copy and creative briefs. Covers three funnel stages (topo/meio/fundo), Meta Ads copy fields (primary text, headline, description), A/B variant pairs, and creative prompts for image or Reels. Applies all brand compliance rules plus Meta Ads platform constraints.
trigger: User asks to "criar anúncio", "escrever copy de ad", "gerar criativo pago", "impulsionar post", "criar campanha", "briefing de ad", or references "Meta Ads", "tráfego pago", or "boosting" in the context of Instagram content.
---

# Instagram Ads Generator — PsiAtiva

Generates paid ad copy and creative briefs for PsiAtiva's Instagram/Meta campaigns. The account is advertising to psychologists who have never heard of PsiAtiva — cold audience, no brand recognition, zero trust capital. Every ad must earn attention in the first 2 seconds and earn trust by the last word, without resorting to the hype, urgency, or guarantees that immediately disqualify this brand with a DISC Analytical+Stable ICP.

**The core tension in PsiAtiva ads:** the brand must convert (it's an ad) while sounding like it never needed to (it's an assessoria). Resolve it by leading hard with the ICP's problem, not with PsiAtiva's offer.

**Success criterion:** *"Isso parece um artigo de uma revista de gestão de clínica — não um anúncio."*

## Knowledge base

- [`workspace/psiativa/_config/marca-identidade-visual.md`](../../_config/marca-identidade-visual.md) — vocabulary compliance map, hemorrhage framing table
- [`workspace/psiativa/_config/voice.md`](../../_config/voice.md) — sentence construction, CTA mechanics, 3-register hierarchy
- [`workspace/psiativa/_config/positioning.md`](../../_config/positioning.md) — core problem frame, GAP mechanism, category positioning, guarantee language
- [`workspace/psiativa/_config/icp-clinica.md`](../../_config/icp-clinica.md) — verbatim pain/desire language for clinic ICP
- [`workspace/psiativa/_config/icp-consultorio-solo.md`](../../_config/icp-consultorio-solo.md) — verbatim pain/desire language for solo ICP
- [`workspace/psiativa/skills/instagram-content-generator/SKILL.md`](../instagram-content-generator/SKILL.md) — organic content skill; consult for pillar rotation and content bank

---

## Input

Required:
- **Funnel stage** — Topo (cold) / Meio (warm/retargeting) / Fundo (hot/retargeting)
- **ICP** — Clínica / Solo / Mixed
- **Format** — single image / carousel / Reels / story

Optional:
- **Campaign objective** — Awareness · Traffic · Mensagens · Leads (affects CTA button choice)
- **Raw pain signal or case** to anchor the creative (*"psicóloga perdeu 3 pacientes no WhatsApp essa semana"*)
- **A/B mode** — generate 2 hook variants for split testing
- **Destination** — link na bio (página diagnóstico) / DM WhatsApp / DM Instagram

If funnel stage is omitted: default to Topo. It's the safest stage for a new ad set and requires no prior audience relationship.

---

## The 3 Funnel Stages

### Topo — audiência fria

The person has never seen PsiAtiva. She scrolls past 200 posts a day. She does not know the brand exists and she did not ask for an ad.

**Job of the ad:** make her stop, recognize her own situation, and feel like whoever made this understands clinic life from the inside.

| Element | Rule |
|---|---|
| Hook (first 2s) | ICP's pain, named with clinical specificity. Never PsiAtiva as subject. |
| Body | Locate the problem (operational, not clinical). One mechanism. One loss. |
| CTA | Lowest-friction action: "Saiba mais" or "Fala com a gente". No promises, no urgency. |
| Pillar match | 1 (Diagnóstico de perda) or 2 (Reframe do problema) |
| Brand appearance | Frame 4–5 of a Reels. Last paragraph of a static post. Never in the first sentence. |

### Meio — audiência morna (retargeting)

She has engaged with organic content, watched a previous ad at 50%+, or visited the profile. She knows the problem exists. She's considering.

**Job of the ad:** deepen the mechanism understanding and introduce PsiAtiva as the specific solution — without closing prematurely.

| Element | Rule |
|---|---|
| Hook | Mechanism insight or category contrast. Can reference "processo" directly. |
| Body | Brief case or result in compliant language. Introduce GAP — named only, not diagrammed. |
| CTA | "Entenda como funciona pra sua clínica" or "Conversa de 20 minutos — sem compromisso". |
| Pillar match | 4 (Posicionamento de categoria) or 5 (Prova e resultado) or 6 (Educação de processo) |
| Brand appearance | Slide 2 of carousel, Frame 3 of Reels — can introduce PsiAtiva earlier than Topo. |

### Fundo — audiência quente (retargeting)

She has clicked a link, watched a full video, sent a DM, or engaged multiple times. She knows PsiAtiva and is close to action.

**Job of the ad:** remove the last friction point and issue a direct invitation. The CTA can be the most prominent element.

| Element | Rule |
|---|---|
| Hook | Desire language (not pain). Name the transformation, not the problem. |
| Body | Guarantee visible. One friction-removing statement. CTA as the main event. |
| CTA | "Agendar conversa de diagnóstico — sem compromisso" or "Primeira conversa é gratuita." |
| Pillar match | 7 (Chamada para conversa) or dedicated offer ad |
| Brand appearance | Can lead with PsiAtiva from sentence 2. The audience already trusts the name. |

---

## Meta Ads Copy Fields

Every Meta ad has three distinct text fields. Each has different visibility and character limits.

| Field | Visible where | Hard limit | Visible before cutoff |
|---|---|---|---|
| **Primary text** | Above the creative | 600 chars | ~125 chars (then "ver mais") |
| **Headline** | Below creative, bold | 40 chars | ~27 chars on mobile |
| **Description** | Below headline, smaller | 30 chars | Often hidden on mobile |

### Rules for each field

**Primary text:**
- First 125 characters carry all the weight — assume the rest is not read
- Open with the ICP's problem or a counterintuitive claim (same rule as organic hooks)
- Use line breaks — a wall of text gets scrolled past even in primary text
- The CTA lives here, not in the headline

**Headline:**
- One compressed claim — the single most important idea of the ad
- Not a sentence — a sharp fragment: *"Agenda previsível começa com processo"* not *"Clique para saber como ter uma agenda previsível com a PsiAtiva"*
- Never start with "A PsiAtiva" — waste of 11 characters and a brand-first mistake
- Compliant: avoid forbidden vocabulary even in 27 characters

**Description:**
- Rarely shown on mobile — treat as optional
- If used: one functional line supporting the headline. *"Assessoria de processo para clínicas de psicologia."*

---

## Step 1 — Select Funnel Stage and Load ICP

Confirm:
1. Which funnel stage applies (default Topo if not specified)
2. Which ICP vocabulary to load (Clínica / Solo / Mixed — see vocabulary rules in the organic skill)
3. Which format (single image / carousel / Reels / story)

Do not draft a single word before confirming the funnel stage. Topo copy sounds wrong in Fundo position and vice versa.

---

## Step 2 — Hook Construction

The hook is the most critical element of any paid ad. The ICP makes a keep/scroll decision in under 2 seconds.

### Hook ladder by funnel stage

| Stage | Hook type | Example |
|---|---|---|
| Topo | Hemorrhage statement — loss happening right now | *"Semana cheia. Semana morta. Sem conseguir prever."* |
| Topo | Counterintuitive claim | *"A sua agenda não oscila por falta de paciente."* |
| Meio | Mechanism insight | *"O contato chegou. A consulta não confirmou. Isso tem nome."* |
| Meio | Category contrast | *"Agência traz contato. Processo faz o contato virar consulta."* |
| Fundo | Desire-first | *"Uma agenda previsível começa com uma conversa de 20 minutos."* |
| Fundo | Friction removal | *"Primeira conversa: gratuita. Compromisso: nenhum. Até entender se faz sentido."* |

### Hook rules (same as organic, plus ad-specific additions)
- **ICP is the subject in Topo** — *"Semana cheia. Semana morta."* — "you" is implied; she is the subject of the scene
- **Max 10 words for text-on-screen Reels** — beyond that, the scroll wins
- **No questions in Topo hooks** — a stranger doesn't answer your questions. Questions work in Meio/Fundo when trust exists.
- **No "Você sabia que?"** — kills the scroll-stop. State the fact directly.
- **No brand name in the first sentence** — ever, in any stage

---

## Step 3 — Format Specs for Ads

### Single image

One clear visual hierarchy: one idea, one claim, maximum one sub-line.

Creative direction principles:
- Topo: typographic, dark background, ICP pain as the only text — no brand name
- Meio: can introduce logo as footer — text focuses on mechanism
- Fundo: brand name prominent, CTA visible in the image itself

Copy structure (Meta fields):

```
Primary text (first 125 chars = hook + one line of body):
[Hook — 1–2 short sentences, ICP as subject]
[One mechanism or loss statement]
[CTA — one line]

Headline (≤ 27 chars for full display):
[Compressed claim or brand tagline]

Description (optional):
[One functional line]
```

---

### Carousel

3–5 slides for ads (vs. 6 for organic). First slide must function as a standalone hook — many users never swipe.

| Slide | Topo content | Meio content | Fundo content |
|---|---|---|---|
| 1 (hook) | Pain/loss — max 8 words | Mechanism insight | Desire + transformation |
| 2 | How the loss happens | Why PsiAtiva solves it | What the conversation looks like |
| 3 | What it costs | Brief case result | What happens after |
| 4 | Reframe or process gap | GAP named | Guarantee |
| 5 (CTA) | Low-friction invite | CTA + destination | Direct CTA + destination |

**Rule:** swipe fatigue hits at slide 3. If the ad hasn't hooked by slide 2, slides 4–5 are seen only by people who were already going to respond.

---

### Reels (video — 15s)

5-frame structure. Text-on-screen is mandatory — most plays are mute. Voice-over is optional enhancement.

| Frame | Duration | Topo content |
|---|---|---|
| 1 | 0:00–0:03 | Pain/hemorrhage hook — large display type on teal |
| 2 | 0:03–0:06 | Mechanism — where the loss is happening |
| 3 | 0:06–0:10 | Location of the problem — one operational gap named |
| 4 | 0:10–0:12 | Reframe or resolution signal |
| 5 | 0:12–0:15 | CTA + brand — logo + low-friction invite |

For Meio/Fundo Reels: compress frames 1–3 into 8s and dedicate frames 4–5 (7s) to solution + CTA.

**Production notes:**
- Kinetic typography on solid brand backgrounds — no stock footage, no people
- Subtitles/captions on by default (Meta can auto-generate — verify accuracy before publishing)
- Aspect ratio: 9:16 (1080×1920px) for native Reels; export 1:1 variant for Feed placement

---

### Story

Story ads play between organic Stories. 5-second attention window. One idea only.

| Element | Rule |
|---|---|
| Text | Max 3 short lines. If it doesn't fit, it's two stories. |
| CTA | Swipe up / tap the link — Meta provides this natively. Do not write it in the image. |
| Format | Same typographic style as feed — no custom Story aesthetic. Consistency across placements. |
| Use case | Fundo retargeting only. Story is rarely effective for cold audience. |

---

## Step 4 — A/B Variant Pairs

Every ad set should launch with two hook variants. Generate both in a single run.

### A/B rules

- Change **one variable at a time** — hook type (pain vs. counterintuitive), frame order, CTA phrasing
- Keep all other elements identical between variants
- Minimum spend before declaring a winner: 1,000 impressions per variant
- Never A/B test the brand claim, the compliance language, or the ICP vocabulary — those are constants

### Standard A/B pair structure

**Variant A — Hemorrhage hook:**
> *"Semana cheia. Semana morta. Sem conseguir prever."*
> — Opens with the concrete recurring loss

**Variant B — Counterintuitive hook:**
> *"A agenda oscilante de uma clínica quase nunca é falta de paciente."*
> — Opens with a claim that reframes the ICP's existing belief

Generate both variants with identical body copy and CTA. Only the opening 2 seconds differ.

---

## Step 5 — Compliance Scan

### Brand compliance (same as organic)

| Check | Passes | Fails — fix |
|---|---|---|
| **Vocabulary** | Zero forbidden words: marketing · leads · vendas · funil · escalar · contrato · comercial · conversão · agência | Replace per vocabulary map |
| **Framing** | Every benefit stated as loss stopped | Rewrite improvement framing to hemorrhage |
| **Opening subject** | ICP is subject in frames 1–2 of Reels; first 125 chars of primary text | Rewrite if PsiAtiva leads |
| **CTA tone** | Low-commitment; no fake urgency | Strip "garanta sua vaga", "não perca", exclamation marks |

### Meta Ads platform compliance

| Check | Rule |
|---|---|
| **No health claims** | Do not imply the ad targets people "with depression", "anxiety disorders", or specific DSM conditions. Target the professional, not the patient. |
| **No before/after** | Do not structure the ad as "before treatment vs. after treatment". The copy is about business operations (agenda, process, WhatsApp), not clinical outcomes. |
| **No income claims** | "Ganhe mais" or implied guaranteed revenue is a Meta policy violation. Use: "agenda mais previsível" — not "faturamento que dobra". The guarantee from `esteira-de-produtos.md` (R$10k em 6 meses) is for proposals, not ads. |
| **No discriminatory targeting language** | Do not write copy that implies the ad is targeting people because of a health-related characteristic. The ICP filter is professional role (psicóloga dona de clínica), not a personal attribute. |
| **Testimonials** | If used: must be identifiable (real name or real @), cannot make specific claims not verifiable. Paraphrased case results are safer than direct quotes with numbers. |

---

## Step 6 — Output Format

```
## Ad Brief · [Stage] · [Format] / ICP: [Clínica / Solo / Mixed]

---

### Meta Ads copy

**Primary text:**
[Full primary text — line breaks preserved]

**Headline:**
[≤ 27 chars]

**Description (optional):**
[≤ 30 chars]

**CTA button:** [Saiba mais / Enviar mensagem / Cadastre-se]

---

### A/B variant (if requested)

**Variant A — [hook type]:**
[Primary text — variant A]

**Variant B — [hook type]:**
[Primary text — variant B]

---

### Creative brief

**Format:** [single image / carousel / Reels / story]
**Dimensions:** [1080×1350px / 1080×1080px / 1080×1920px]
**Funnel stage:** [Topo / Meio / Fundo]

[Slide-by-slide or frame-by-frame direction]
[Background color tokens]
[Typography notes]
[Text on creative — verbatim]

---

### Generation prompt

[Image or video generation prompt — ready to paste into Ideogram / Canva / Kling]

---

### Compliance scan

- Brand vocabulary: [✅ / ❌ + fix]
- Framing: [✅ hemorrhage / ❌ improvement + fix]
- Opening subject: [✅ ICP / ❌ PsiAtiva leads + fix]
- CTA tone: [✅ low-commitment / ❌ aggressive + fix]
- Meta policies: [✅ clean / ❌ flag + fix]

---

### Segmentação sugerida (Meta)

- Público: [descrição]
- Interesse: [tags]
- Exclusões: [público a excluir]
- Posicionamentos: [Reels + Feed / Stories / etc.]
- Objetivo de campanha: [Traffic / Mensagens / etc.]
```

---

## Pre-Built Ad Copy Bank

### Topo — Single image / Clínica

**Primary text:**
```
Semana cheia. Semana morta. Sem conseguir prever.

A agenda oscilante de uma clínica quase nunca é falta de paciente.

É falta de processo entre o primeiro contato e a consulta confirmada.

Fala com a gente e entenda o que está acontecendo na sua clínica.
→ Link na bio.
```
**Headline:** `Agenda previsível. Com processo.`
**CTA button:** Saiba mais

---

### Topo — Reels / Clínica (15s, 5 frames)

```
Frame 1 (0:00–0:03): "Semana cheia. / Semana morta. / Sem conseguir prever."
Frame 2 (0:03–0:06): "A agenda oscilante de uma clínica quase nunca é falta de paciente."
Frame 3 (0:06–0:10): "É falta de processo entre o primeiro contato e a consulta confirmada."
Frame 4 (0:10–0:12): "Isso tem nome. E tem solução."
Frame 5 (0:12–0:15): [Logo PsiAtiva] "Fala com a gente. Link na bio."
```
**Caption (primary text):**
```
Semana cheia. Semana morta. Sem conseguir prever.

O processo entre o primeiro contato e a consulta confirmada é onde a maioria das clínicas está perdendo paciente — sem saber.

→ Link na bio para entender o que está acontecendo na sua clínica.
```

---

### Topo — Single image / Solo

**Primary text:**
```
Quantas mensagens chegaram enquanto você estava em sessão essa semana?

E quantas viraram consulta confirmada?

O paciente que não recebe resposta rápida vai para quem respondeu primeiro.

→ Essa é uma conta que vale a pena fazer. Link na bio.
```
**Headline:** `O buraco está no processo.`
**CTA button:** Saiba mais

---

### Meio — Carousel / Mixed (4 slides)

```
Slide 1 (hook): "Agência traz contato. Processo faz o contato virar consulta confirmada."
Slide 2: "A maioria das clínicas investe em presença online antes de ter o processo de atendimento funcionando. Resultado: paga para levar o paciente para quem respondeu primeiro."
Slide 3: "O GAP — Gerador de Agenda Previsível — estrutura os 4 estágios da jornada do paciente: da busca online à consulta confirmada. Cada etapa tem um gargalo. A PsiAtiva mapeia e fecha cada um."
Slide 4 (CTA): "Fala com a gente. Uma conversa de 20 minutos para entender onde está o buraco na sua clínica. Sem compromisso."
```
**Primary text:**
```
Você já investiu em presença online. A agenda continua oscilando.

O problema quase nunca está na visibilidade — está no processo entre o contato e a consulta confirmada.

→ Arrasta para entender onde está o buraco.
```
**Headline:** `Processo que fecha agenda.`
**CTA button:** Saiba mais

---

### Fundo — Single image / Clínica (retargeting)

**Primary text:**
```
Você já viu o problema. Sabe onde está o buraco.

O próximo passo é uma conversa de 20 minutos sobre a sua clínica — gratuita, sem compromisso.

A PsiAtiva apresenta uma proposta só se fizer sentido para os dois lados.

→ Link na bio para agendar.
```
**Headline:** `Conversa de diagnóstico — gratuita.`
**CTA button:** Enviar mensagem

---

## Watch out for

- **Opening with PsiAtiva in Topo ads** — cold audience has zero brand equity with the name. "A PsiAtiva é uma assessoria..." as frame 1 loses the scroll instantly. Save the brand reveal for frame 4–5 of Reels, last paragraph of static.
- **Importing organic post copy verbatim into Meta Ads fields** — organic captions are formatted for followers; ads are formatted for strangers. The primary text first 125 chars does the heavy lifting; restructure accordingly.
- **Using the guarantee (R$10k / 6 meses) in ad copy** — this belongs in the proposal stage, verified by the closer in R1/R2. In cold ads, a financial guarantee without context reads as a promise Meta may flag and the ICP may distrust. Use it in Fundo only, with supporting context.
- **Stacking all 3 funnel stages in one ad** — a Topo ad that ends with a Fundo CTA ("Agende agora sua sessão de diagnóstico") creates friction at the wrong moment. Match the CTA intensity to the stage.
- **Forgetting Meta's health content policies** — copy that implies the audience has a health condition (even indirectly) can trigger review. Keep copy professional-role-facing: "psicóloga dona de clínica", not "você que atende pacientes com ansiedade".
- **Running Pillar 3 (objeção ética) as a cold Topo ad** — this pillar requires the ICP to already be thinking about going commercial. Cold audience hasn't reached that internal conflict yet. It reads as addressing an objection they haven't formed.
- **Using income improvement framing as CTA** — "Aumente seu faturamento" or "Mais pacientes = mais receita" are brand violations AND Meta policy risks. The CTA is always an invitation to a conversation, never a revenue promise.
- **No A/B test structure** — ads without variant testing waste budget. Always generate 2 hook variants in the first run. One variable at a time.
- **Forgetting the primary text fold** — Meta shows ~125 chars before "ver mais". Test the copy by reading only the first 125 chars: does it stand alone? If not, rewrite the opening.

---

## See also

- [`workspace/psiativa/skills/instagram-content-generator/SKILL.md`](../instagram-content-generator/SKILL.md) — organic content; consult for pillar rotation and pre-built copy bank
- [`workspace/psiativa/_config/marca-identidade-visual.md`](../../_config/marca-identidade-visual.md) — vocabulary map, hemorrhage framing, creative compliance checklist
- [`workspace/psiativa/_config/voice.md`](../../_config/voice.md) — 3-register hierarchy, sentence construction, CTA mechanics
- [`workspace/psiativa/_config/positioning.md`](../../_config/positioning.md) — GAP mechanism usage rules, guarantee language, NR-1 tailwind framing
- [`workspace/psiativa/_config/esteira-de-produtos.md`](../../_config/esteira-de-produtos.md) — guarantee and offer language (Fundo stage copy only)
- [`workspace/psiativa/projects/instagram-content/ads/`](../../../projects/instagram-content/ads/) — active ad briefs and creative outputs
