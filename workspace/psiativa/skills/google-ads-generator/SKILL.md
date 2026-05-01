---
name: google-ads-generator
description: Generates PsiAtiva Google Ads campaigns — keyword strategy, ad copy, visual direction, LP alignment, and pre-launch compliance. Covers two ICPs (Clínica / Solo), three funnel stages (topo/meio/fundo), and Google's health sector policy constraints. Commercial name for the client: "Sistema de Captação por Intenção."
trigger: User asks to "criar campanha Google", "escrever copy de Google Ads", "configurar tráfego pago no Google", "criar anúncio de busca", "gerar keywords", "estratégia de captação por intenção", or references "GAds", "Search Ads", "Performance Max", or "tráfego pago Google" in the PsiAtiva context.
dependencies:
  - workspace/psiativa/_config/voice.md
  - workspace/psiativa/_config/positioning.md
  - workspace/psiativa/_config/marca-identidade-visual.md
  - workspace/psiativa/_config/icp-clinica.md
  - workspace/psiativa/_config/icp-consultorio-solo.md
  - workspace/psiativa/_config/esteira-de-produtos.md
output: workspace/psiativa/projects/[project-name]/ads/google/[campaign-slug]/brief.md
template: workspace/psiativa/skills/google-ads-generator/campaign-template.md
---

## TL;DR

Google Ads for PsiAtiva is intent-capture, not interruption. The person searching is already feeling the problem — the ad just needs to name it correctly and offer the lowest-commitment next step. Every campaign targets one ICP, one conversion event, and one entry point into the product staircase. Copy follows PsiAtiva voice rules (hemorrhage framing, no forbidden vocabulary, low-commitment CTAs). Google's health sector policy adds a second compliance layer: no health claims, no income guarantees in ads.

---

## When to use

- Creating a new Google Search, Performance Max, or Display campaign for PsiAtiva
- Writing or reviewing ad copy for Google Ads
- Building a keyword list for a psychology clinic captation campaign
- Generating a campaign brief to hand off to a media buyer or fill in Google Ads Manager

---

## Prerequisites

- ICP confirmed (Clínica or Solo) — product, promise, and ad spend tier differ between tracks
- Product being advertised confirmed — determines conversion goal and LP
- City/region confirmed — local intent is the primary signal for this audience
- `marca-identidade-visual.md` vocabulary map loaded — forbidden words apply to ad copy
- Google Ads Manager access or intent to create the campaign in-platform confirmed

---

## Key differences vs. instagram-ads-generator

| Dimension | Google Ads (this skill) | Instagram Ads |
|---|---|---|
| **Audience state** | Active intent — person is searching right now | Passive — interrupting a scroll |
| **Hook strategy** | Match the search term language; no need to create urgency | Create urgency from zero |
| **Format** | Text-first (Search/RSA); image+text (PMax/Display) | Visual-first (Reels, Carousel, Single Image) |
| **Compliance layer** | Google health policy + PsiAtiva vocabulary | Meta health policy + PsiAtiva vocabulary |
| **Conversion path** | Search → LP → form/WhatsApp → diagnóstico | Feed → DM or link in bio → diagnóstico |
| **Budget floor** | R$600–1.500/mês (varies by product) | R$300–1.000/mês |

---

## Procedure

### Step 1 — Confirm ICP and product

Before writing a single word of copy, confirm:

1. **ICP:** Clínica (2–15 profissionais, dono/gestor) or Solo (autônomo, sem recepção)?
2. **Product being advertised:** Which entry point in the staircase? (see routing table below)
3. **Conversion goal:** What should the person do after clicking? (form fill, WhatsApp message, phone call)
4. **Geography:** Which city or region? Radius?

**Product → Campaign goal routing:**

| Product | Conversion goal | LP type | Budget (Clínica) | Budget (Solo) |
|---|---|---|---|---|
| Diagnóstico gratuito (entry to P7K/P3K) | Form fill → Diagnóstico | LP diagnóstico | R$1.500–3.000/mês | R$600–1.200/mês |
| P3K — Método de Ativação Previsível | WhatsApp / form fill | LP P3K com garantia | R$1.500/mês | R$600/mês |
| GBP Scale — Protocolo Referência Local | WhatsApp / call | LP GBP com garantia | R$600–1.000/mês | R$400–600/mês |
| IA Solo — Protocolo de Demanda Contínua | Form fill | LP IA Solo | — | R$600/mês |
| P7K / P10K (retargeting only) | WhatsApp direct | LP completa do produto | R$5.000/mês | R$3.000/mês |

> Note: P7K and P10K are not cold-traffic products. Do not send cold search traffic directly to a high-ticket offer page. Use the diagnóstico gratuito as the universal entry point for topo campaigns.

---

### Step 2 — Define funnel stage

| Stage | Audience | Ad goal | LP focus | CTA intensity |
|---|---|---|---|---|
| **Topo** | Cold search — buscando o problema, não a solução | Awareness + first click | Problem framing → low-commitment CTA | Baixa: "Entenda o que está acontecendo" |
| **Meio** | Retargeting — visitou LP, não converteu | Re-engagement | Mechanism + guarantee visible | Média: "Fale com a gente" |
| **Fundo** | Retargeting — visitou LP 2+ vezes or high-intent signal | Direct conversion | Offer + guarantee + price signal | Alta: "Agende o diagnóstico agora" |

**For new campaigns:** start at Topo (cold search) + Meio retargeting only. Add Fundo retargeting after 30 days of data.

---

### Step 3 — Build keyword strategy

#### Intent tiers for PsiAtiva searches

| Tier | Examples | Action |
|---|---|---|
| **Highest intent (Exact)** | `assessoria captação psicólogos` · `processo agenda clínica psicologia` | Always include; low volume, high conversion |
| **High intent (Phrase)** | `agenda imprevisível psicóloga` · `como captar pacientes psicologia` · `clínica psicologia sem paciente` | Include; monitor CTR |
| **Medium intent (Phrase)** | `marketing psicologia` · `Google para psicólogos` · `instagram psicóloga pacientes` | Test; may attract wrong profile — watch query report |
| **Local intent (Exact or Phrase)** | `psicóloga [especialidade] [cidade]` · `clínica psicologia [bairro]` | Include for GBP Scale campaigns; lower for P7K+ |
| **Low intent / competitor (Negative)** | `curso psicologia` · `plataforma agendamento` · `terapia online` · `grátis` | Always negative |

#### Mandatory negative keyword list

```
grátis · de graça · barato · curso · pós-graduação · estágio · CRP
plataforma · software · app · sistema de agendamento · prontuário
terapia online · psiquiatra · ansiedade (tratamento) · depressão (tratamento)
como fazer terapia · o que é psicologia · psicólogo quanto ganha
```

> Google's health policy flags: avoid keywords that directly target patients searching for mental health treatment. The target is the psychologist professional, not the patient.

#### Keyword structure note

One tight ad group per intent cluster — do not mix "processo/captação" intent with "local search" intent in the same group. Separate ad groups allow separate copy that matches the search language more precisely.

---

### Step 4 — Write ad copy

Apply PsiAtiva voice rules:

1. **ICP is the subject.** Headlines name her problem, not PsiAtiva's solution.
2. **Hemorrhage framing.** Name the loss: "agenda oscilante", "paciente que não confirmou", "buraco entre o contato e a sessão".
3. **No forbidden vocabulary.** Run vocabulary compliance before any output (Step 7).
4. **Short sentences.** Google Search copy has 30-char headlines — every word counts. No filler.
5. **Low-commitment CTA.** "Bate-papo gratuito" / "Entenda o que trava a agenda" / "Diagnóstico sem compromisso".

#### Hook ladder by funnel stage

| Stage | Hook type | Clínica example | Solo example |
|---|---|---|---|
| **Topo** | Problem signal — name the symptom | *"Agenda Oscilante?"* / *"Semana Cheia. Semana Vazia."* | *"Responde Enquanto Atende?"* / *"Perdendo Paciente na Sessão?"* |
| **Meio** | Mechanism — name the gap | *"O Buraco Está no Processo"* / *"GAP: Agenda Previsível"* | *"Processo Que Funciona Sem Você"* |
| **Fundo** | Offer + guarantee | *"Diagnóstico Gratuito Hoje"* / *"Resultado em 45 Dias"* | *"45 Dias ou Ajustamos Sem Custo"* |

#### RSA (Responsive Search Ad) pinning strategy

- **Pin position 1:** Symptom headline (e.g., *"Agenda Oscilante?"*)
- **Pin position 2:** Mechanism or brand (e.g., *"GAP · Assessoria de Processo"*)
- **Position 3 (unpinned):** Rotate: local relevance · offer · guarantee — let Google optimize

#### Description slots

| Slot | Primary angle | Character budget (90 max) |
|---|---|---|
| Description 1 | Hemorragia + processo: paciente perdido entre contato e sessão | ≤90 |
| Description 2 | Mecanismo + diferenciação de categoria: assessoria ≠ agência | ≤90 |
| Description 3 | Prova + garantia: resultado de processo, prazo, garantia de continuar | ≤90 |
| Description 4 | CTA empático: entender, conversar, bate-papo — não fechar | ≤90 |

---

### Step 5 — Define LP alignment

The LP must do the heavy lifting. The ad's job is the first click only.

**LP checklist before launching ads:**

- [ ] Opening hero matches the ad's problem hook (message match = lower bounce)
- [ ] Process problem framed before PsiAtiva is introduced
- [ ] GAP mechanism named (not explained in full — complexity signal only)
- [ ] Guarantee visible before or alongside the CTA
- [ ] CTA is a low-commitment action (bate-papo, diagnóstico, conversa — not "comprar")
- [ ] WhatsApp CTA carries the pre-filled message from `marca-identidade-visual.md`
- [ ] Privacy policy visible (required for form + health-adjacent content on Google)
- [ ] Google Tag / conversion event fires on the confirmation/thank-you step

---

### Step 6 — Visual direction (Performance Max / Display only)

If the campaign includes PMax or Display, define visual assets using PsiAtiva's identity:

- **Background tokens:** `#1C2B2B` (dark green) or `#1A4B51` (teal) for attention assets; `#F0F7F4` (off-white) for trust assets
- **Typography:** New York Display (headlines) · Lora (body) · DM Sans (UI/CTA text)
- **Forbidden visuals:** stock people in success poses · growth charts · rockets · money · before/after clinical outcomes
- **Approved visuals:** clean editorial text on solid color · abstract process metaphors (line/gap) · logo negative on dark background
- **Icon style:** line icons only, stroke 1.5–2px — never filled
- See [`_config/marca-identidade-visual.md`](../../_config/marca-identidade-visual.md) for full asset compliance checklist

---

### Step 7 — Compliance scan

Run before any campaign goes live.

#### PsiAtiva vocabulary compliance

| Check | Test |
|---|---|
| **Forbidden words** | Zero occurrences of: `marketing · leads · vendas · funil · escalar · contrato · comercial · agência · conversão` |
| **Framing** | Hemorrhage over improvement: loss named directly, no "melhore sua captação" |
| **Sujeito de abertura** | ICP's problem is the subject — not PsiAtiva, not the product |
| **CTA** | Low commitment: "bate-papo", "diagnóstico", "conversa" — never "garanta sua vaga" or exclamation marks |
| **Mechanism name** | If GAP is cited: full form "GAP — Gerador de Agenda Previsível" on first use |
| **Category language** | "Assessoria" not "agência" · "Captação" not "marketing" · "Processo" not "estratégia digital" |

#### Google Ads health sector policy

| Policy area | Check |
|---|---|
| **Health claims** | No claims about treating, preventing, or diagnosing mental health conditions in the ad copy |
| **Patient targeting** | Copy targets the psychologist professional role — not patients seeking therapy |
| **Income guarantee** | No income or revenue guarantees in cold ad copy (guarantee goes on LP only, Fundo only) |
| **Before/after** | No clinical outcome comparisons or "life before/after" framing |
| **Testimonials** | Paraphrased case results are safer than named testimonials in ads; if named, must be real and identifiable |
| **Privacy** | LP must show a visible privacy policy link when collecting personal data via form |

---

### Step 8 — Fill the campaign template and output

Using `campaign-template.md` as the structure, produce a `brief.md` in:

```
workspace/psiativa/projects/[project-name]/ads/google/[campaign-slug]/brief.md
```

The brief must include:
- Campaign overview (ICP, product, goal)
- LP URL and strategy notes
- Full RSA ad copy (headlines + descriptions, character-counted)
- Visual asset direction (if PMax)
- Keyword list with match types and rationale
- Negative keyword list
- Geographic and demographic targeting
- Compliance scan results (both layers)
- Pre-launch validation checklist completed

---

## Copy bank — ready to use

### Topo · Clínica · Search RSA

**Headlines:**
```
Agenda Oscilante na Clínica?      (27)
Semana Vazia. Semana Cheia.       (27)
Processo, Não Improviso           (22)
PsiAtiva · Assessoria de Processo (32) [over limit — trim: "PsiAtiva · Assessoria" = 21 ✅]
Diagnóstico Gratuito              (22)
Psicólogos em [Cidade]            (varies)
Captação Ética · Processo         (24)
Agenda Previsível em 45 Dias      (28)
O Buraco Está no Processo         (27)
Sem Depender de Indicação         (26)
```

**Descriptions:**
```
D1: Pacientes que chegam e não confirmam sessão: quase sempre é falta de processo, não de qualidade. (96) → trim: "Pacientes que somem entre o contato e a sessão. É processo, não falta de qualidade." (84 ✅)
D2: GAP — Gerador de Agenda Previsível. Assessoria de captação ética para clínicas de psicologia. (93) → trim: "GAP: captação estruturada para clínicas de psicologia. Sem parecer agência." (72 ✅)
D3: Resultado em até 6 meses — ou continuamos sem custo. Diagnóstico gratuito, sem compromisso. (91) → trim: "Resultado em 6 meses ou continuamos sem custo. Diagnóstico gratuito." (68 ✅)
D4: Entenda por onde a agenda está vazando. Bate-papo de 20 min — sem compromisso. (81 ✅)
```

---

### Topo · Solo · Search RSA

**Headlines:**
```
Perdendo Paciente na Sessão?      (28)
Agenda Previsível Sem Equipe      (28)
Algo Responde Enquanto Você Atende (33) → trim: "Resposta 24h Enquanto Atende" (28 ✅)
PsiAtiva · Captação Ética         (26)
Diagnóstico Gratuito              (22)
Psicóloga Autônoma em [Cidade]    (varies)
Sem Depender de Indicação         (26)
Processo Que Funciona Sozinho     (28)
```

**Descriptions:**
```
D1: "Quando saio da sala já perdi o paciente." Isso tem solução — sem precisar de equipe. (85 ✅)
D2: Presença ativa no Google e WhatsApp respondendo enquanto você atende. Captação ética. (86 ✅)
D3: Canais ativos em 45 dias — ou ajustamos sem custo. Diagnóstico gratuito, sem compromisso. (89 ✅)
D4: Entenda por que sua agenda oscila. Uma conversa de 20 min, sem compromisso. (74 ✅)
```

---

### Meio · Retargeting · Display copy

```
Headline: "O Processo Que Fecha o Buraco"
Description: "Você visitou a PsiAtiva. Ainda com agenda oscilante? Bate-papo gratuito — entenda o que está travando."
```

---

## Output format reference

```markdown
# Brief · Google Ads · [Campaign Slug]

> Skill aplicada: [skills/google-ads-generator](../../../skills/google-ads-generator/SKILL.md)
> ICP: [Clínica / Solo] · Produto: [nome] · Estágio: [Topo / Meio / Fundo]

## Visão geral
[...]

## Cópia do anúncio (RSA)

### Headlines
| # | Texto | Contagem |
|---|---|---|
[...]

### Descriptions
[...]

## Keywords

### Foco
[...]

### Negativas
[...]

## LP de destino
URL: [...]
[...]

## Direção visual (se PMax)
[...]

## Compliance scan
[...]

## Checklist pré-lançamento
[...]
```

---

## See also

- [`_config/positioning.md`](../../_config/positioning.md) — GAP mechanism, category positioning, ICP promise by track
- [`_config/marca-identidade-visual.md`](../../_config/marca-identidade-visual.md) — vocabulary map, color tokens, font stack, compliance checklist
- [`_config/esteira-de-produtos.md`](../../_config/esteira-de-produtos.md) — product staircase, ad spend by product, ROI anchors
- [`skills/instagram-ads-generator/SKILL.md`](../instagram-ads-generator/SKILL.md) — companion skill for paid Instagram/Meta content; shared brand compliance rules
- [`skills/google-ads-generator/campaign-template.md`](campaign-template.md) — the fill-in template this skill outputs to
