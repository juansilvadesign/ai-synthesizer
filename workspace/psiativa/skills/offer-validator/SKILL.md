---
name: offer-validator
description: Audit a raw PsiAtiva offer description against the one-sentence formula "Eu ajudo [quem] a resolver [problema específico] para alcançar [avanço concreto]." Diagnoses the failure mode, critiques the current wording, and rewrites it for each active ICP (Perfil A and Perfil B) in vocabulary-compliant language that sells the transformation, not the tool.
trigger: User provides a draft description of what PsiAtiva does and asks to "validar a oferta", "checar se a oferta está boa", "reescrever a proposta de valor", "testar a frase de posicionamento", or "como explico o que a PsiAtiva faz em uma frase". Also fires when a description sounds like it's selling a tool, a method, or a category instead of a result.
---

# One-Sentence Offer Validator — PsiAtiva

A Phase 2 audit skill. An offer that passes the one-sentence test is buyable. An offer that fails it is not a bad offer — it is an invisible one. The job is to find exactly which part is failing, name it precisely, and rewrite only what is broken.

**The formula:**
> *"Eu ajudo [QUEM] a resolver [PROBLEMA ESPECÍFICO] para alcançar [AVANÇO CONCRETO]."*

Three slots. Each must be filled with specifics. Any slot filled with a category word, a tool name, or a vague concept fails the test.

## Knowledge base

- [`knowledge/sources/101_agência/03_Você não precisa de um império online.md`](../../../../knowledge/sources/101_agência/03_Você não precisa de um império online.md) — source: one-sentence formula, failure examples, weak offer signals, tool vs. transformation distinction
- [`knowledge/sources/101_agência/06_Você não precisa de mais conhecimento.md`](../../../../knowledge/sources/101_agência/06_Você não precisa de mais conhecimento.md) — source: product positioning by result, AI-as-backend rule, compliant positioning sentence structure
- [`knowledge/sales/articles/oultimomentor/101_agencia.md`](../../../../knowledge/sales/articles/oultimomentor/101_agencia.md) — Phase 2: one-sentence test, good/bad examples, transformation vs. tool framing
- [`workspace/psiativa/_config/positioning.md`](../../_config/positioning.md) — PsiAtiva's core problem frame, category positioning (assessoria ≠ agência), GAP mechanism, brand promise by ICP
- [`workspace/psiativa/_config/marca-identidade-visual.md`](../../_config/marca-identidade-visual.md) — vocabulary compliance: forbidden and required terms for both ICPs

---

## Input

Required: a raw description of what PsiAtiva does. Can be:
- A draft pitch sentence
- A bio line
- A verbal description ("eu diria que fazemos...")
- A landing page headline
- Anything the user is trying to say to a prospect

If the input is longer than 2–3 sentences: extract the intended offer core, then audit that. A 10-line description is usually hiding one weak sentence trying not to be seen.

---

## Step 1 — Parse the Three Slots

Map the input to the formula. For each slot, note what was found and whether it passes.

| Slot | What to look for | Passes | Fails |
|---|---|---|---|
| **QUEM** | A specific type of person or business — ICP-level specificity | "psicólogas autônomas", "clínicas de psicologia com equipe" | "empresas", "profissionais", "negócios" |
| **PROBLEMA ESPECÍFICO** | A named operational failure — not a category, a thing that is broken | "perdem pacientes entre o primeiro contato e a sessão confirmada", "agenda oscila mês a mês sem processo" | "presença digital", "marketing", "resultados", "comunicação" |
| **AVANÇO CONCRETO** | A specific change in their situation — something they can picture | "agenda mais estável sem depender só de indicação", "processo ativo em 45 dias" | "melhorar presença", "crescer no digital", "otimizar operações" |

**Rule:** if any slot is filled with a category word rather than a specific, the offer fails that slot — regardless of how good the rest is. One failed slot = the whole sentence is unbuyable.

---

## Step 2 — Failure Mode Diagnosis

Every weak offer belongs to one of four failure modes. Identify which one — or which combination — is present.

---

### Failure Mode 1 — Ferramenta sem problema

**What it looks like:**
> *"Oferecemos assessoria de marketing digital com IA para psicólogos."*  
> *"Criamos presença digital, automações e estratégia de captação para clínicas."*

**Why it fails:** the sentence names the delivery method (marketing digital, automação, IA) without stating the problem the delivery solves. The prospect reads "marketing digital" and immediately hears "agência que vai me pedir para postar todo dia." The word triggers her ethics filter before the offer is understood.

**Diagnostic signal:** a tool, platform, method, or service category sits in the PROBLEMA slot instead of a problem.

**Fix direction:** strip the tool name entirely. Ask: what specific failure in the prospect's operation does this tool resolve? Name that failure.

---

### Failure Mode 2 — Amplo demais

**What it looks like:**
> *"Ajudamos clínicas e psicólogos com presença, comunicação, atendimento, captação e processos."*  
> *"Trabalhamos com tudo que envolve crescimento digital para profissionais de saúde mental."*

**Why it fails:** an offer that claims to solve everything signals a vendor who has not chosen a specific problem to own. The prospect does not ask "which of these do I need?" — she exits. An offer that covers everything is structurally identical to one that covers nothing.

**Diagnostic signal:** more than one problem category listed, OR the QUEM is "profissionais", "empresas", or any category wider than the actual ICP.

**Fix direction:** pick the single most commercially important problem PsiAtiva solves. If the offer covers two ICP types, split into two sentences — one per ICP.

---

### Failure Mode 3 — Avanço genérico

**What it looks like:**
> *"Ajudamos psicólogas a melhorar sua presença digital."*  
> *"Ajudamos clínicas a crescer de forma sustentável no digital."*

**Why it fails:** the AVANÇO slot is filled with a direction ("melhorar", "crescer") but not a destination. "Melhorar presença digital" does not create a picture. It does not answer "better than what?" or "better in which way?" — so it produces no reaction.

**Diagnostic signal:** the advance contains a comparison without an anchor ("melhorar", "aumentar", "otimizar", "crescer") with no concrete before/after or timeframe.

**Fix direction:** replace the vague advance with a specific state the prospect can picture: what does the operation look like when the problem is solved? Use PsiAtiva's language — agenda estável, pacientes confirmados, processo sem depender de indicação.

---

### Failure Mode 4 — Sofisticação antes de clareza

**What it looks like:**
> *"Somos uma assessoria de processo de captação estruturado com metodologia GAP — Gerador de Agenda Previsível — aplicada às quatro etapas da jornada do paciente online-para-presencial."*

**Why it fails:** this sounds like a conference presentation, not a solution. The prospect needs to understand the problem you solve before she has any reason to learn your method name. Explaining the mechanism before naming the problem puts architecture before the building — and she has no reference to evaluate the architecture against.

**Diagnostic signal:** the PROBLEMA slot contains a mechanism name, a framework, or a methodology label. The sentence requires prior knowledge to decode.

**Fix direction:** move mechanism language to the close, after the problem and advance are stated. Name the GAP only after the problem is understood — and never in the opening sentence.

---

## Step 3 — Rewrite by ICP

After diagnosing the failure, rewrite for each ICP track. Never produce a single "universal" offer — PsiAtiva has two ICPs with different pain vocabularies and different advance definitions.

### Rewrite rules

1. **QUEM must name the ICP type directly.** "Psicólogas autônomas" or "clínicas de psicologia com equipe." Never "profissionais de saúde mental."
2. **PROBLEMA must name an operational failure, not a category.** The problem is the gap between where patients are lost and where they should arrive — not "presença digital."
3. **AVANÇO must be a state, not a direction.** Agenda estável, pacientes confirmados, processo ativo sem depender de indicação. Not "melhorar captação."
4. **No forbidden vocabulary in the rewrite.** Never: marketing, leads, tráfego, vendas, escalar, funil, estratégia digital. Always: captação, presença, processo, agenda, paciente, confirmação.
5. **Use hemorrhage-first language when possible.** Lead with what is being lost, not what could be gained. The ICP responds faster to stopping a leak than to imagining a gain.

---

## Pre-built PsiAtiva Compliant Offers

### Perfil A — Clínica com equipe

**Core problem:** pacientes perdidos entre o primeiro contato e a sessão confirmada — por processo fraco de resposta, confirmação e reativação.

**Core advance:** agenda previsível e faturamento estável sem dependência de um único canal.

**Compliant offers (use verbatim or adapt):**

> *"Ajudamos clínicas de psicologia a parar de perder pacientes entre o primeiro contato e a sessão confirmada — com processo, não com anúncio."*

> *"Ajudamos clínicas com 2 a 10 terapeutas a ter uma agenda mais estável sem depender só de indicação — estruturando o processo entre o contato e a consulta confirmada."*

> *"Ajudamos clínicas de psicologia a adicionar no mínimo R$10.000 de faturamento em até 6 meses fechando os buracos no processo de captação."*

*(Last variant for price-anchoring contexts — use only when the prospect is already past the first filter.)*

---

### Perfil B — Psicóloga autônoma

**Core problem:** contatos chegam e somem — por falta de processo de resposta — enquanto ela está em sessão e não pode responder.

**Core advance:** agenda estável e processo ativo em 45 dias sem depender só de indicação.

**Compliant offers (use verbatim or adapt):**

> *"Ajudo psicólogas autônomas a ter uma agenda mais estável sem depender só de indicação — com um processo de captação ativo em até 45 dias."*

> *"Ajudo psicólogas autônomas a parar de perder pacientes no WhatsApp enquanto estão em sessão — sem contratar recepcionista e sem abrir mão da identidade clínica."*

> *"Ajudo psicólogas a converter os contatos que já chegam em sessões confirmadas — resolvendo o processo entre o interesse e o agendamento."*

*(Second and third variants for profiles where the WhatsApp loss or conversion gap is the visible diagnostic failure.)*

---

## Step 4 — Weak Offer Signals Checklist

Use these four signals to validate any offer draft before it ships. If one fires, the offer needs rework before it reaches a prospect.

| Signal | What it means | Action |
|---|---|---|
| Prospect says "legal, mas como funciona?" | The advance was not concrete — she understood the category but not the result | Go back to Step 3: sharpen the AVANÇO slot |
| Conversation dies fast after the sentence | WHO or PROBLEM is too broad to create recognition | Go back to Step 2: diagnose Failure Mode 1 or 2 |
| You need more than 2 sentences to explain | The offer is not crystallized — it's still a description, not a sentence | Run Step 1 again: strip until the formula fits in one line |
| You describe it differently every time | The offer is not owned internally — means the PROBLEMA slot is still unfixed | Go back to Step 2: Failure Mode 2 or 3 |

---

## Output Format

```
## Oferta Auditada — [Label or first words of the input]

**Parsing:**
- QUEM: [what was found] → [✅ Passes / ❌ Fails — reason]
- PROBLEMA: [what was found] → [✅ Passes / ❌ Fails — reason]
- AVANÇO: [what was found] → [✅ Passes / ❌ Fails — reason]

---

**Failure mode(s) detected:** [Mode 1 / 2 / 3 / 4 — one-line reason]

**Critique:**
[2–4 lines. What is actually broken and why it fails at the prospect's reading level. No hedging — name the problem directly.]

---

**Rewrite — Perfil A (clínica com equipe):**
[one sentence]

**Rewrite — Perfil B (psicóloga autônoma):**
[one sentence]

---

**Vocabulary compliance check:**
[Any forbidden terms found in the input — listed with replacement. If clean: "✅ Sem termos proibidos."]
```

---

## Watch out for

- **Treating "assessoria de processo" as the offer** — this is PsiAtiva's category positioning, not the offer. The prospect does not wake up thinking she needs an assessoria; she wakes up thinking she is losing patients between the contact and the confirmed session. The offer names the problem, not the service label.
- **Keeping GAP in the opening offer sentence** — GAP belongs in the commercial presentation, after the problem is recognized. In a bio, pitch sentence, or outreach hook, it creates complexity before the prospect has a reason to decode it. Remove it; reintroduce it in the R1 call after Situação and Problema are landed.
- **Writing one universal offer for both ICPs** — the vocabulary that moves a clinic owner (previsibilidade, faturamento, equipe, processo) does not move a solo practitioner (alívio, presença, agenda, sem depender de indicação). One sentence serves neither well.
- **Mistaking the rewrite for a tagline** — the one-sentence offer is a diagnostic and outreach tool, not a brand tagline. It can be direct, even blunt. It does not need to sound elegant — it needs to produce recognition: "that is exactly my problem."
- **Using "melhorar" as the AVANÇO** — "melhorar presença", "melhorar captação", "melhorar atendimento" are all directional words with no destination. Always replace with a state: what does the operation look like when the problem is solved?
- **Leaving "marketing digital" anywhere in the offer** — the word "marketing" in any PsiAtiva-facing copy activates the prospect's ethics filter immediately. "Captação" is the replacement for external use; "processo de presença" for contexts where even captação feels commercial.

---

## See also

- [`workspace/psiativa/_config/positioning.md`](../../_config/positioning.md) — the core problem frame ("psicólogos excelentes perdem pacientes por falta de processo") and brand promise by ICP; the offer must align with this.
- [`workspace/psiativa/_config/marca-identidade-visual.md`](../../_config/marca-identidade-visual.md) — full vocabulary compliance map (forbidden and required terms).
- [`workspace/psiativa/skills/diagnostico-2min/SKILL.md`](../diagnostico-2min/SKILL.md) — downstream: once the offer is validated, the diagnostic identifies which specific failure makes a given prospect a priority target for that offer.
- [`workspace/psiativa/skills/contextual-outreach/SKILL.md`](../contextual-outreach/SKILL.md) — the offer sentence structure feeds directly into the outreach message register.
- [`knowledge/sources/101_agência/03_Você não precisa de um império online.md`](../../../../knowledge/sources/101_agência/03_Você não precisa de um império online.md) — source: full four failure patterns, verbatim good/bad examples.
