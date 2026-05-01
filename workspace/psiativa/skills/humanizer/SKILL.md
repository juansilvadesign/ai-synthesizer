---
name: humanizer-psiativa
description: Humanize Portuguese text into PsiAtiva voice. Removes generic AI patterns, then applies the brand-specific layer — vocabulary compliance (forbidden/approved), hemorrhage framing over improvement framing, 3-register hierarchy (clínico → empático → firme), and the 7 sentence-construction rules. Detects and rewrites bureaucratic/academic Portuguese AI registers that the generic humanizer does not catch.
trigger: User asks to "humanizar este texto", "passar esse texto pela voz da PsiAtiva", "tirar cara de IA", "auditar tom de voz", "revisar copy PsiAtiva", or pastes generated text and asks "isso está soando bem para a PsiAtiva?". Also fires when reviewing landing pages, posts, captions, WhatsApp scripts, emails, proposals, or client reports for tone drift.
---

# Humanizer — PsiAtiva Voice

A two-layer humanizer. Layer 1 strips the generic AI tells documented in the parent skill. Layer 2 applies the PsiAtiva-specific brand voice — the layer that turns "clean Portuguese without AI signs" into "copy that could only have been written by someone who understands clinic life from the inside."

**Success criterion:** *"Isso foi escrito por quem entende de clínica — não por quem vende curso, não por uma IA."*

## Knowledge base

- [`knowledge/skills/humanizer/SKILL.md`](../../../../knowledge/skills/humanizer/SKILL.md) — parent skill: 29 generic AI patterns (em dash overuse, rule of three, vague attributions, AI vocabulary, copula avoidance, signposting, etc.)
- [`workspace/psiativa/_config/voice.md`](../../_config/voice.md) — 3-register hierarchy, 7 sentence rules, opening patterns by format, CTA mechanics
- [`workspace/psiativa/_config/marca-identidade-visual.md`](../../_config/marca-identidade-visual.md) — vocabulary compliance map (forbidden/approved), hemorrhage framing table, Instagram/LP/WhatsApp/Email tone calibration
- [`workspace/psiativa/_config/positioning.md`](../../_config/positioning.md) — process problem frame, category positioning, GAP usage rules
- [`workspace/psiativa/_config/icp-clinica.md`](../../_config/icp-clinica.md) — verbatim Perfil A pain language
- [`workspace/psiativa/_config/icp-consultorio-solo.md`](../../_config/icp-consultorio-solo.md) — verbatim Perfil B pain language

---

## Input

Required:
- The text to humanize (any length; Portuguese or with PT/EN mix)

Optional:
- **ICP** — Clínica / Solo / Mixed. If omitted, infer from the text or ask before rewriting.
- **Format** — landing page, Instagram post, carousel, WhatsApp, email, proposal, internal doc. Determines opening pattern and CTA tone.
- **Length constraint** — preserve, shorten, or rewrite freely.

Never invent facts. If the source omits a detail, leave it out — do not pad with plausible-sounding filler.

---

## Step 1 — Generic AI Pattern Scan (Layer 1)

Run the input through the parent skill's 29 patterns first. Most apply directly to Portuguese. The high-frequency offenders in PT are:

| Pattern | What it looks like in PT |
|---|---|
| Em dash overuse | *"O processo é simples — direto — eficiente."* → use commas or periods |
| Rule of three | *"clareza, organização e previsibilidade"* repeated ad nauseam |
| Synonym cycling | *"o profissional... a especialista... a terapeuta... a psicóloga"* in 4 consecutive sentences |
| Copula avoidance | *"se apresenta como" / "constitui" / "configura-se como"* → use *"é"* |
| Promotional adjectives | *"vibrante" · "robusto" · "inovador" · "transformador" · "estratégico"* |
| Superficial -ndo phrases | *"otimizando processos"*, *"garantindo resultados"*, *"alavancando potencial"* |
| Vague attributions | *"Especialistas afirmam"*, *"Estudos indicam"*, *"Dados apontam"* — without source |
| Title case in headings | *"Como Estruturar Sua Captação"* → *"Como estruturar sua captação"* |
| Curly quotes | `"texto"` → `"texto"` |
| Generic positive close | *"O futuro é promissor"*, *"Tempos empolgantes pela frente"* |
| Persuasive authority | *"No fundo"*, *"Em essência"*, *"O que realmente importa"* |
| Signposting | *"Vamos explorar"*, *"Vamos entender"*, *"Aqui está o que você precisa saber"* |

If any fire, fix at this layer before moving to Layer 2.

---

## Step 2 — Portuguese AI-Register Scan (Layer 2a)

These are bureaucratic / academic / corporate Portuguese registers that ChatGPT and Claude default to. The generic humanizer does not catch them because they sound "professional." For PsiAtiva, they read as written by no one.

| ❌ AI-register PT | ✅ PsiAtiva replacement |
|---|---|
| *"É importante destacar que..."* | (cut entirely; just say the thing) |
| *"Neste contexto, podemos observar que..."* | (cut; start with the observation) |
| *"Vale ressaltar que..."* | (cut) |
| *"Cabe destacar..."* | (cut) |
| *"No que tange a..."* | *"Sobre..."* |
| *"Diante do exposto..."* | (cut; the conclusion stands without preamble) |
| *"Em síntese..."* | (cut; if a summary is needed, write the summary) |
| *"É fundamental compreender..."* | (cut; if it's fundamental, just state it) |
| *"Posto isto..."* / *"Assim sendo..."* | (cut) |
| *"Tendo em vista..."* | *"Considerando..."* (or cut) |
| *"de forma a..."* / *"a fim de..."* | *"para..."* |
| *"no sentido de..."* | (cut) |
| *"em um cenário cada vez mais..."* | (cut entire phrase; the cenário trope is dead on arrival) |
| *"na era digital"* / *"no mundo digital"* | (cut) |
| *"alavancar seus resultados"* | *"parar de perder pacientes"* (hemorrhage replacement) |
| *"otimize sua presença online"* | *"sua clínica não aparece para quem está buscando agora"* |
| *"conquiste mais pacientes"* | *"deixe de perder os que já chegam"* |
| *"transforme sua agenda"* | *"agenda mais estável sem depender só de indicação"* |
| *"explore novas possibilidades"* | (cut; specify which possibility) |
| *"abrace o futuro da..."* | (cut) |

---

### Comparison & negation structures — kill all of them

The *"Não é X. É Y."* pattern (and every variant) is one of the loudest AI tells in Portuguese. It mimics rhetorical contrast — "I'll correct your misconception" — but no human writes three of them in a row. The parent skill catches it as negative parallelism; in PT it has many flavors and all of them must go. Replace with a **straight affirmation**: state Y directly, drop the contrast.

| ❌ Comparison / negation structure | ✅ Straight affirmation |
|---|---|
| *"Não é X. É Y."* | State Y directly. |
| *"Não é apenas X; é Y."* | State Y directly. |
| *"Mais do que X, é Y."* | State Y directly. |
| *"X não é Y, é Z."* | State Z directly. |
| *"Não se trata de X, mas sim de Y."* | State Y directly. |
| *"Não é por X. É porque Y."* | State Y directly. |
| *"Não é falta de X. É falta de Y."* | *"O buraco está em Y."* / *"Y é o que está faltando."* |
| *"Sem X. Sem Y."* (tailing negation pair) | Reescrever no afirmativo: *"Com X. Com Y."* / fundir em uma frase positiva. |

**Worked example:**

❌ *"Não é falta de qualidade clínica. É falta de processo entre o contato e a confirmação."*
✅ *"O buraco está no processo entre o contato e a confirmação."*

**Why kill it:** the contrast structure flatters the reader by pretending to correct a misconception. Real clinical voice does not argue with itself — it states the observation. One contrast structure is forgivable; two in the same piece is AI signal; three is a giveaway.

---

## Step 3 — PsiAtiva Vocabulary Compliance (Layer 2b)

Run the forbidden vocabulary scan. Zero tolerance — even one instance leaks the wrong category onto PsiAtiva.

| ❌ Forbidden | ✅ Approved |
|---|---|
| marketing | captação · presença online · processo |
| leads | pacientes |
| vendas | fechamento de agenda · parceria |
| funil | processo de atendimento · jornada do paciente |
| escalar / escala | crescer com previsibilidade |
| contrato | parceria |
| comercial | processo de captação |
| cliente (do psicólogo) | paciente |
| reunião | bate-papo · conversa |
| agência | assessoria |
| campanha | estratégia de presença |
| conversão | confirmação · agenda fechada |
| pitch | apresentação · proposta |
| estratégia digital | processo de captação · presença estruturada |

**Hemorrhage framing override:** every benefit must be stated as a loss being stopped, not a gain being acquired.

| ❌ Improvement framing | ✅ Hemorrhage framing |
|---|---|
| *"Melhore sua captação"* | *"Pare de perder paciente entre o contato e a sessão"* |
| *"Atraia mais pacientes"* | *"Deixe de perder os que já chegam"* |
| *"Otimize sua presença online"* | *"Sua clínica não aparece para quem busca agora"* |
| *"Cresça seu consultório"* | *"Depender só de indicação é apostar que o mês vai ser bom"* |
| *"Aumente sua receita"* | *"Cada semana com buraco na agenda é dinheiro que não volta"* |

---

## Step 4 — 3-Register Voice Calibration

Read the draft and ask in this order:

1. **Clínico** — does it read as written by someone who knows psicóloga life from the inside? Specific signals: agenda oscilante, no-show, CRP, WhatsApp tarde da noite, mês bom e mês ruim, primeira semana cheia depois vazia. If the text could work for a dentist, accountant, or lawyer, it has not landed yet.

2. **Empático** — does it acknowledge the silent tension between wanting to grow and not wanting to *parecer comercial*? At least once per piece, the ethics frame must surface — directly or by implication.

3. **Firme** — does it have a clear position? Or is it hedging with *"talvez"*, *"possivelmente"*, *"em alguns casos"*, *"pode ser que"*? PsiAtiva says the hard thing with care, not with hedging.

**Priority rule:** *empático* without *clínico* reads as generic copywriting. *Firme* without *empático* reads as a sales pitch. Lead with *clínico* — let the others follow.

---

## Vocabulário Clínico — Living Reference

A curated list of words and expressions psychologists actually use in their professional life. Dropping one of these into copy at the right moment is the cheapest, fastest way to reinforce the *clínico* register from Step 4 — it signals "written by someone who speaks the language" without any extra effort.

**This table is fed weekly.** New entries are added by the team as fluency-marker words surface. The point is not exhaustiveness — it is to keep a small, deliberate vocabulary of in-group terms ready to use.

**How to use:**
1. Before drafting, scan the table for a term that fits the piece's angle.
2. After humanization, check whether at least one clínico-vocabulary term landed naturally in the copy. If zero, the *clínico* register may be weak — consider revising.
3. Never force a term in. If the word doesn't earn its place, leave it out — performative clinical jargon is worse than no clinical signal.

| Termo | Sentido clínico | Aplicação em copy PsiAtiva |
|---|---|---|
| **projetar** | mecanismo de defesa: atribuir ao outro o que é seu; também usado no sentido de planejar a longo prazo | *"Você está projetando na agenda o controle que ainda não construiu no processo."* — uso metafórico em hooks de Instagram ou em reframes do problema |
| | | |
| | | |
| | | |

*(Linhas em branco para entradas semanais. Ao adicionar um termo: preencher Sentido clínico em uma frase, e Aplicação com um exemplo verbatim de uso em copy PsiAtiva — Instagram, LP, WhatsApp ou proposta.)*

---

## Step 5 — Sentence Mechanics Check

Apply the 7 rules from `voice.md`:

| # | Rule | Failure signal | Fix |
|---|---|---|---|
| 1 | Short sentences | Compound sentence with semicolon or 3+ commas | Break into two |
| 2 | Active voice + *você* | *"Os profissionais enfrentam..."* / *"As clínicas precisam..."* | Rewrite to *você* |
| 3 | Concrete nouns | *"impactos na previsibilidade do faturamento"* | *"Semana com buraco. Mês ruim."* |
| 4 | Problem-first | Opens with PsiAtiva, the solution, or the method | Rewrite opening to ICP's problem |
| 5 | Questions as openers | First sentence makes PsiAtiva the subject | Use a question that puts *você* as subject |
| 6 | No padding | *"com certeza" · "é muito importante" · "de forma eficiente" · "no sentido de"* | Cut entirely |
| 7 | One idea per sentence | Two claims joined by *"e"* | Split into two sentences |

---

## Step 6 — Final Audit Loop

After applying Steps 1–5, run the parent skill's final audit:

1. Read the draft aloud (or simulate reading aloud — line by line, with pauses).
2. Ask: *"O que ainda soa como IA neste texto?"* — answer briefly with the remaining tells.
3. Ask: *"Agora reescreva sem soar como IA."* — produce the final version.

Common Portuguese tells that survive the first pass:
- Excessive parallelism (every sentence the same length)
- Even rhythm (no short interrupting beats)
- Zero opinions, zero edge, zero acknowledgment of trade-offs
- Closing line that summarizes what was said
- Final sentence that goes meta ("Por isso é importante...")

If any survive, revise once more.

---

## Pre-Built Before/After Bank — PsiAtiva Context

### Example 1 — Landing page hero

**Before (AI-flavored):**
> Em um cenário cada vez mais competitivo, é fundamental que clínicas de psicologia adotem estratégias digitais robustas para alavancar seus resultados e conquistar mais pacientes. A PsiAtiva oferece soluções inovadoras que transformam sua presença online, otimizando processos e garantindo o sucesso da sua jornada digital.

**After Layer 1 (generic AI removed):**
> A PsiAtiva ajuda clínicas de psicologia a melhorar sua captação digital e conquistar mais pacientes através de processos estruturados.

**After Layer 2 (PsiAtiva voice):**
> Você está perdendo pacientes entre o primeiro contato e a sessão confirmada.
>
> O buraco está no processo entre esses dois momentos. A maioria das clínicas só percebe quando o mês vira.
>
> A PsiAtiva é a assessoria que estrutura esse processo com método clínico e respeito à identidade da clínica.

---

### Example 2 — Instagram post

**Before (AI-flavored):**
> 🚀 **Transforme sua clínica!** No mundo digital de hoje, é importante destacar que estratégias eficientes de marketing podem alavancar seus resultados de forma significativa. Vale ressaltar que a PsiAtiva oferece soluções completas para psicólogos! Não perca essa oportunidade de crescer! ✨

**After:**
> Sua clínica tem demanda. A agenda não fecha cheia.
>
> Esse é o sinal de que o processo entre o contato e a confirmação tem buraco — e a maioria das clínicas só percebe quando o mês vira.
>
> *→ Quando fizer sentido olhar para isso, a gente está aqui.*

---

### Example 3 — WhatsApp outreach

**Before (AI-flavored):**
> Olá! Tudo bem? Espero que esteja tendo um ótimo dia! Gostaria de apresentar a você uma oportunidade incrível para alavancar a captação de pacientes da sua clínica através das nossas soluções estratégicas de marketing digital. Posso te enviar mais informações?

**After:**
> Oi, [nome]. Aqui é a Renata, da PsiAtiva.
>
> Como tá a agenda hoje — cheia, oscilando ou ainda construindo?
>
> Se quiser, em uns 15 minutos a gente entende o cenário e vê se faz sentido seguir uma conversa.

---

### Example 4 — Email assunto + abertura

**Before (AI-flavored):**
> Assunto: Transforme a captação da sua clínica de forma estratégica!
>
> Prezado(a) Doutor(a),
> É com grande satisfação que entramos em contato. No contexto atual da saúde mental, é fundamental compreender que estratégias digitais bem estruturadas são essenciais para o crescimento sustentável da sua clínica.

**After:**
> Assunto: Mês bom, mês ruim, sem conseguir prever
>
> Doutora,
>
> Mês bom e mês ruim sem conseguir prever. Essa é a realidade de quem depende só de indicação.
>
> O gargalo está entre o primeiro contato e a consulta confirmada.

---

### Example 5 — Proposta intro

**Before (AI-flavored):**
> A presente proposta tem como objetivo apresentar nossas soluções inovadoras para a sua clínica, visando otimizar seus processos e alavancar seus resultados de forma estratégica e sustentável.

**After:**
> Com base no que você nos contou, o gargalo está entre o primeiro contato e a sessão confirmada.
>
> É exatamente o que o GAP — Gerador de Agenda Previsível — resolve.

---

## Output Format

```
## Humanização — [Format] / [ICP]

### Draft (após Layer 1 + Layer 2)
[texto humanizado]

---

### O que ainda soa como IA?
- [tell residual 1]
- [tell residual 2]
- [se nenhum: "Nada residual identificado."]

---

### Versão final
[texto após o pass de auditoria]

---

### Mudanças aplicadas
- [Layer 1] removido: [padrão genérico]
- [Layer 2a] removido: [registro AI-PT]
- [Layer 2b] substituído: [vocabulário proibido → aprovado]
- [Layer 2b] reframe: [improvement → hemorrhage]
- [Voice] calibração: [clínico/empático/firme aplicado]
- [Mechanics] correção: [regras 1–7 violadas e corrigidas]
```

If the input is short (single sentence, hook line, CTA), collapse the output: just final version + 1-line change summary.

---

## Watch out for

- **Cleaning the AI signs but leaving the text voiceless** — a sterile Portuguese sentence without AI tells is still not PsiAtiva voice. The 3-register check (clínico → empático → firme) is non-negotiable, especially the *clínico* layer. If the text could work for a dentist, it has not landed.
- **Replacing forbidden words mechanically without rewriting the framing** — swapping *"marketing"* for *"captação"* in a sentence built on improvement framing produces compliant-but-wrong copy. The framing must flip to hemorrhage *before* the vocabulary swap matters.
- **Adding "de processo" everywhere as a fake fix** — *"processo de captação", "processo de atendimento", "processo de presença"* repeated three times in five lines reads as panicked compliance, not voice. Use the word once where it earns its place; let the rest stand without it.
- **Letting comparison/negation structures slip back in** — *"Não é X. É Y."*, *"Não é apenas X; é Y."*, *"Mais do que X, é Y."* — every variant goes. The contrast pattern is the single loudest AI tell in PT, and the parent skill flags it as negative parallelism (#9). Zero tolerance. Always rewrite as a straight affirmation: state the fact, drop the contrast.
- **Forgetting to consult the Vocabulário Clínico table** — a piece can pass every compliance check and still feel voiceless. A single in-group clinical term, used naturally, lands the *clínico* register more than a paragraph of corrected vocabulary. Scan the table before drafting; check for at least one clinical signal after humanizing.
- **Preserving an AI-generated structure (intro → 3 bullets → conclusion) while only swapping words** — humanization is structural, not lexical. If the draft has a tidy 3-bullet rule-of-three list, kill the list and write prose.
- **Inventing facts to fill humanized text** — humans leave gaps. AI fills them with plausible filler. If the source did not name the clinic, the result, the timeframe — leave the gap. Specificity must come from the source, not from the rewrite.
- **Using exclamation marks even after the cleanup** — calm authority never needs them. Maximum one per page (LP), zero in body copy. Strip and never reintroduce.
- **Closing with a meta-sentence** — *"E é por isso que o processo importa"*, *"Esse é o caminho"*, *"Pense nisso"* are all AI closers. PsiAtiva text ends on the last claim or the CTA. No coda.
- **Keeping "né?" or "tá?" as fake humanization** — these are oral fillers, not voice. They register as someone trying too hard to sound casual. Cut.
- **Treating the final audit loop as optional** — Step 6 catches the 5–10% of AI signal that survives Steps 1–5. Skipping it produces "almost human" text, which is more uncanny than obvious AI text.

---

## See also

- [`knowledge/skills/humanizer/SKILL.md`](../../../../knowledge/skills/humanizer/SKILL.md) — parent skill: 29 generic AI patterns and the audit-loop methodology
- [`workspace/psiativa/_config/voice.md`](../../_config/voice.md) — 3-register hierarchy, 7 sentence rules, opening patterns by format
- [`workspace/psiativa/_config/marca-identidade-visual.md`](../../_config/marca-identidade-visual.md) — full vocabulary map and hemorrhage framing table
- [`workspace/psiativa/_config/positioning.md`](../../_config/positioning.md) — process problem frame, GAP usage rules, NR-1 tailwind framing
- [`workspace/psiativa/skills/instagram-content-generator/SKILL.md`](../instagram-content-generator/SKILL.md) — generates content; pair with this skill for end-to-end on-brand output
- [`workspace/psiativa/skills/offer-validator/SKILL.md`](../offer-validator/SKILL.md) — for offer-statement humanization, validate the offer first, then humanize the framing
