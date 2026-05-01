---
name: spin-question-engine
description: Generate a calibrated 4-question SPIN sequence for a specific ICP profile and pain signal, moving the prospect from "this is important" to "this is costing me money right now." Output includes the question sequence, importance-to-priority reframe phrases, and counter-question patterns for common deflections.
trigger: User provides an ICP profile (Perfil A or Perfil B) and a pain signal (from a prior diagnostic, Renata's NEPQ, or the prospect's own words) and asks to "gerar perguntas SPIN", "montar o script de diagnóstico", "conduzir a dor", or "aprofundar o problema" before or during an R1 call.
---

# SPIN Question Engine — PsiAtiva

A question-generation skill for the R1 closer. Renata's NEPQ uncovers the pain signal — this skill deepens it. The goal is to move the prospect from "acho que precisamos de algo assim" to "esse problema está me custando agora" before any product is named. Do not explain the solution until the prospect has verbalized the cost of not solving.

## Knowledge base

- [`knowledge/sources/101_agência/12_Quem pergunta controla a venda.md`](../../../../knowledge/sources/101_agência/12_Quem pergunta controla a venda Quem explica demais.md) — SPIN framework, the "never explain before diagnosing" rule, counter-question patterns
- [`knowledge/sources/101_agência/13_Um cliente não vai comprar na hora.md`](../../../../knowledge/sources/101_agência/13_Um cliente não vai comprar na hora seu produto só.md) — importance vs. priority distinction, 7 mental triggers, commitment/consistency sequence
- [`workspace/psiativa/_config/icp-clinica.md`](../../_config/icp-clinica.md) — Perfil A pain inventory and verbatim prospect language
- [`workspace/psiativa/_config/icp-consultorio-solo.md`](../../_config/icp-consultorio-solo.md) — Perfil B pain inventory and verbatim prospect language
- [`workspace/psiativa/_config/comercial-playbook.md`](../../_config/comercial-playbook.md) — R1 call structure; SPIN fits inside the diagnosis phase

---

## Input

Two required fields:
1. **ICP profile** — Perfil A (clínica com equipe) or Perfil B (psicóloga autônoma)
2. **Pain signal** — the friction uncovered by Renata or by the prospect's own words

**If the pain signal is not yet confirmed:** run the diagnostic (`diagnostico-2min`) first. SPIN only sharpens a pain that already exists — it does not create one from scratch.

---

## Operating Rules

Before generating any question sequence:

1. **Situação questions must be specific.** A generic "como está seu negócio?" reveals nothing and positions you as a lazy vendor. The question should show you already understand the niche.
2. **Never jump to solution before Implicação is landed.** Most closers find the pain and immediately present the product. The prospect's response is "interesting" — and she doesn't buy. Implicação turns a small problem into an expensive one.
3. **One question per turn.** Stacking questions gives the prospect an escape — she answers the easiest one and the harder one disappears.
4. **Necessidade question should invite the prospect to verbalize the value — not hear it from you.** If you state the value, she evaluates it. If she states it, she owns it.
5. **Never use forbidden vocabulary:** *marketing, leads, funil, tráfego, conversão, escalar, fechar* — these register as vendor language and break the consultative frame.

---

## Pre-built SPIN Banks by Pain Signal

### Perfil A — Clínica com Equipe

---

#### Pain: Agenda oscilante / imprevisibilidade de faturamento

**S — Situação**
> *"Hoje, quando a agenda fecha bem, você consegue identificar o que foi diferente — ou fica mais no feeling do que funcionou naquele mês?"*

**P — Problema**
> *"Quando vem um mês mais fraco, vocês conseguem ver onde ficaram os buracos — qual etapa não funcionou — ou o impacto aparece só no faturamento no final?"*

**I — Implicação**
> *"Se esse ciclo de meses bons e ruins continuar pelos próximos seis meses sem um processo que estabilize, o impacto maior pra você é financeiro, ou é a dificuldade de planejar a clínica com alguma segurança?"*

**N — Necessidade**
> *"Se você tivesse alguma previsibilidade mínima sobre a ocupação — saber que o mês vai fechar num patamar razoável — isso mudaria como a clínica funciona no dia a dia?"*

---

#### Pain: WhatsApp / resposta tardia / contatos sem processo

**S — Situação**
> *"Quando alguém manda mensagem no WhatsApp da clínica fora do horário — à noite, num sábado — como esse contato é tratado? Existe algum padrão ou depende de quem estiver disponível?"*

**P — Problema**
> *"Quando a recepcionista não consegue responder na hora, vocês têm algum processo para recuperar esse contato depois ou isso fica na memória dela?"*

**I — Implicação**
> *"Se um contato espera três, quatro horas por uma resposta — e enquanto isso recebe resposta rápida de outra clínica — vocês ficam sabendo que perderam ou simplesmente some sem rastro?"*

**N — Necessidade**
> *"Se cada contato recebesse uma resposta útil em poucos minutos, independente do horário ou de quem está atendendo, isso resolveria uma parte relevante do problema de ocupação da agenda?"*

---

#### Pain: No-show / confirmação de sessão

**S — Situação**
> *"Hoje, quando tem falta em sessão, vocês conseguem medir quanto isso custa no mês — ou aparece como número só quando fecha o faturamento?"*

**P — Problema**
> *"Existe alguma rotina de confirmação com antecedência — um processo que o paciente recebe antes da sessão — ou isso depende da recepcionista lembrar?"*

**I — Implicação**
> *"Se um terapeuta tem duas faltas por semana, ao longo de três meses isso representa quanto de receita que saiu da agenda mas não entrou no caixa?"*

**N — Necessidade**
> *"Se houvesse um processo automatizado de confirmação que reduzisse a falta — mesmo que de forma parcial — em quanto tempo isso se pagaria comparado ao que está saindo hoje?"*

---

#### Pain: Instagram sem conversão / presença sem resultado

**S — Situação**
> *"Hoje o Instagram da clínica é usado mais para conteúdo, para captar paciente novo ou é um canal que a equipe mantém sem clareza de resultado?"*

**P — Problema**
> *"Quando alguém indica a clínica e o indicado vai olhar o Instagram antes de chamar — esse perfil hoje ajuda a confirmar a decisão ou pode estar esfriando ela?"*

**I — Implicação**
> *"Se uma parte dos interessados passa pelo Instagram, não encontra clareza suficiente e vai pra outra clínica — isso fica invisível pra vocês ou tem alguma forma de medir?"*

**N — Necessidade**
> *"Se o Instagram funcionasse como um canal que prepara o paciente antes do primeiro contato — passando confiança e conduzindo até o WhatsApp — isso reduziria o trabalho de convencimento na recepção?"*

---

#### Pain: Dependência de indicação como único canal

**S — Situação**
> *"Hoje a maior parte dos pacientes novos chega por indicação, por busca no Google, pelo Instagram ou por outro canal?"*

**P — Problema**
> *"Quando as indicações diminuem — seja por sazonalidade, férias ou mudança de perfil dos pacientes atuais — a clínica tem outro canal que mantém a entrada de contatos?"*

**I — Implicação**
> *"Se num mês a indicação cair 40% sem aviso, qual seria o impacto imediato — agenda com buraco, pressão no caixa ou algo mais grave?"*

**N — Necessidade**
> *"Se existisse um canal previsível além da indicação — que funcionasse mesmo sem depender de nenhuma pessoa específica — isso daria mais segurança pra planejar a clínica?"*

---

### Perfil B — Psicóloga Autônoma

---

#### Pain: Contatos perdidos enquanto está em sessão

**S — Situação**
> *"Hoje, quando você está em sessão e chega mensagem nova no WhatsApp, como você lida com isso — responde depois, tem alguém que olha ou fica até o final do dia?"*

**P — Problema**
> *"Quando você responde horas depois, você consegue medir quantas dessas pessoas já foram embora — ou você nunca fica sabendo o que foi perdido?"*

**I — Implicação**
> *"Se uma dessas pessoas que não respondeu tivesse virado paciente, considerando sessões por mês e o período médio de acompanhamento — quanto isso representa ao longo do tempo?"*

**N — Necessidade**
> *"Se existisse uma forma de esse primeiro contato ser atendido com uma resposta útil enquanto você está em sessão — sem que você precise parar — isso resolveria o problema sem mudar sua rotina de atendimento?"*

---

#### Pain: VPS abaixo do mercado / medo de aumentar o valor

**S — Situação**
> *"Hoje o seu valor de sessão está no patamar que você considera justo pra sua formação e experiência, ou está mais no patamar que você acha que o paciente aceita?"*

**P — Problema**
> *"Quando você pensa em subir o valor, o que trava mais — a preocupação de perder pacientes atuais, a dificuldade de atrair pacientes novos com o valor mais alto ou outro motivo?"*

**I — Implicação**
> *"Se você manter o valor atual por mais 12 meses enquanto colegas com formação equivalente cobram 30, 40% a mais — qual o impacto no quanto você consegue investir na própria carreira, na especialização, na estrutura?"*

**N — Necessidade**
> *"Se você chegasse em pacientes novos com uma presença que já passa autoridade antes do primeiro contato — perfil, Google, credencial visível — isso ajudaria a sustentar um valor mais alto sem precisar justificar na conversa?"*

---

#### Pain: Instagram com engajamento mas sem conversão em paciente

**S — Situação**
> *"Hoje o seu Instagram tem engajamento razoável — curtidas, comentários, seguidores — mas quanto desse engajamento virou conversa no WhatsApp ou agendamento de verdade?"*

**P — Problema**
> *"Quando alguém salva um post seu ou te segue, mas não chama — o que você acha que falta pra ela dar esse passo?"*

**I — Implicação**
> *"Se 10% das pessoas que interagem com seu conteúdo por mês chegassem a mandar mensagem — quantos contatos por mês isso seria? E quantos desses poderiam virar paciente?"*

**N — Necessidade**
> *"Se o seu perfil tivesse uma estrutura que conduzisse o seguidor pra um próximo passo claro — sem parecer comercial — isso resolveria a lacuna entre engajamento e agenda?"*

---

#### Pain: Ausência ou pouca presença no Google Maps

**S — Situação**
> *"Hoje, quando alguém pesquisa no Google algo como 'psicóloga em [bairro/cidade]', sua clínica aparece com destaque ou fica em segundo plano?"*

**P — Problema**
> *"Se ela não te encontra ali, que alternativa ela tem — indicação de alguém, Instagram ou a primeira opção que aparecer?"*

**I — Implicação**
> *"Considerando que quem pesquisa psicólogo no Google já passou da fase de só 'pensar em fazer terapia' — é alguém pronta pra dar o próximo passo — quantos desses você acha que passam por você sem te ver?"*

**N — Necessidade**
> *"Se você aparecesse com avaliações e presença consolidada nessas buscas, o esforço de captar paciente novo seria menor ou o perfil de quem chega seria diferente?"*

---

## Importance → Priority Reframe Phrases

Use when the prospect acknowledges the problem but shows no urgency. Pick one — never stack them.

| Scenario | Reframe phrase |
|---|---|
| Prospect says "sim, é importante" without urgency | *"Entendo. O ponto que me interessa entender é se hoje isso está só no campo do incômodo ou já está afetando a entrada de pacientes de alguma forma."* |
| Prospect says "vou pensar" after agreeing | *"Faz sentido. Só quero deixar claro antes de você pensar: o custo de resolver e o custo de não resolver — eles continuam iguais enquanto você decide, ou um deles cresce?"* |
| Prospect validates but delays | *"Não quero tratar isso como urgente se ainda não é. Mas me diz: se esse problema continuar igual pelos próximos três meses, o impacto que você descreveu — agenda oscilando, contato sem resposta — ele fica estável ou tende a piorar?"* |
| Prospect says "já estamos pensando em algo" | *"Que bom. Curioso: o que tá travando mais — a decisão de qual solução, o momento financeiro ou a dificuldade de colocar em prática sem tirar você do atendimento?"* |

---

## Counter-Question Patterns

When the prospect deflects with a common question before the diagnosis is complete, do not answer directly. Use the question to advance the diagnosis.

| Prospect asks | Weak response | Strong counter-question |
|---|---|---|
| *"Como funciona?"* | Descrever entregáveis | *"Funciona por etapas, mas antes de explicar o processo inteiro — pelo que você me contou, parece que o gargalo maior está entre o primeiro contato e a sessão confirmada. Confere?"* |
| *"Quanto custa?"* | Dar o preço | *"Depende do que precisa ser resolvido. Mas pra não passar um número desconectado: estamos falando de resolver a presença, o processo de atendimento, os dois juntos?"* |
| *"Já tentei anúncio e não funcionou"* | Defender anúncio | *"Faz sentido. Na maioria dos casos que vi, o problema não era o anúncio — era que o contato chegava e não tinha processo do outro lado. Como foi o atendimento dos contatos que entraram?"* |
| *"Não tenho tempo pra isso agora"* | Argumentar | *"Entendo. Só me diz: o que toma mais tempo hoje — a falta de processo ou o gerenciamento das consequências de não ter processo?"* |

---

## Output Format

```
## SPIN Sequence — [ICP Profile] × [Pain Signal]

**Contexto:** [brief description of what the prospect revealed before this sequence]

---

**S — Situação**
[question]

**P — Problema**
[question]

**I — Implicação**
[question]

**N — Necessidade**
[question]

---

**Se a prospecto validar a dor mas não mostrar urgência:**
[1 importance→priority reframe phrase]

**Se ela perguntar sobre preço ou entrega antes do fim:**
[1 counter-question]
```

---

## Integration with R1 Call Flow

This skill fits inside the **Diagnóstico** phase of the R1 call (`comercial-playbook.md`). Sequence:

1. Renata's NEPQ identifies which pain signal is active → passes context to human closer
2. Closer opens R1 with rapport, then runs **Situação** to confirm and expand the scenario
3. **Problema** → **Implicação** deepen the cost
4. **Necessidade** closes the diagnosis — the prospect has verbalized the value
5. Only after N is answered does the closer introduce the GAP mechanism and the relevant product

**Rule:** Never name the product during S or P. Never explain GAP until N is answered. A prospect who hears "GAP — Gerador de Agenda Previsível" before she has verbalized her own problem hears a product name. After she has verbalized her own problem, she hears an answer.

---

## Watch out for

- Rushing to Implicação before Problema is confirmed — the prospect needs to admit the friction first, or the implication has no anchor
- Asking Situação questions the diagnostic already answered — it wastes R1 time and signals you didn't prepare
- Using "leads", "marketing", "conversão", "tráfego" in any of these questions — the ICP hears vendor language and shifts to evaluation mode
- Stacking I and N into the same question — they require separate processing; break them
- Answering "quanto custa?" with the price before Implicação is landed — a number without a problem is always "too expensive"
- Treating this as a script to read verbatim — it's a question bank; pick the sequence that fits the specific pain, then adapt the phrasing to the live conversation

---

## See also

- [`workspace/psiativa/skills/diagnostico-2min/SKILL.md`](../diagnostico-2min/SKILL.md) — identifies which pain signal to feed into this engine before the R1 call
- [`workspace/psiativa/_config/comercial-playbook.md`](../../_config/comercial-playbook.md) — full R1+R2 call structure; SPIN operates inside the Diagnóstico phase
- [`workspace/psiativa/_config/sdr-renata.md`](../../_config/sdr-renata.md) — NEPQ qualification that pre-warms the pain signal this skill deepens
- [`knowledge/sources/101_agência/12_Quem pergunta controla a venda.md`](../../../../knowledge/sources/101_agência/12_Quem pergunta controla a venda Quem explica demais.md) — source method with niche examples
- [`knowledge/sources/101_agência/13_Um cliente não vai comprar na hora.md`](../../../../knowledge/sources/101_agência/13_Um cliente não vai comprar na hora seu produto só.md) — importance vs. priority distinction and 7 mental triggers
