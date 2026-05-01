# Arte de Indicação — Brief de Design

> Peça única para acompanhar a mensagem do kit de indicação. **Card de acompanhamento, anexado à mensagem** (WhatsApp, e-mail, Stories do indicador). A copy textual já está na mensagem; a arte só precisa gerar **reconhecimento em <2 segundos** e **ancorar a categoria de assessoria de processo** (afastando o card da estética de agência de marketing).
>
> Skill aplicada: [`skills/instagram-content-generator`](../../../skills/instagram-content-generator/SKILL.md). Adaptação: formato single image, ICP Mixed, função híbrida (Pilar 2 + Pilar 4).

---

## Especificações técnicas

| Item | Valor |
|---|---|
| **Formato principal** | 1080 × 1350 px (4:5) — ideal para anexo de WhatsApp, feed do Instagram, e crop razoável em Stories |
| **Formato alternativo** | 1080 × 1080 px (1:1) — para preview de link em mensagem |
| **Aspecto secundário (Story)** | 1080 × 1920 px (9:16) — variação dedicada se usado como Story |
| **Margem interna** | 80 px em todos os lados |
| **Nome do arquivo** | `psiativa-indicacao-card-v1.png` (mais `-stories.png` se exportar a versão 9:16) |

---

## Composição (de cima para baixo)

```
┌──────────────────────────────────────┐
│                                      │  ← padding 80 px
│                                      │
│   O buraco está                      │  ← Hook, New York Display
│   no processo.                       │     ~88 pt, #FAFFFF
│                                      │     alinhado à esquerda
│                                      │     (1 quebra de linha,
│                                      │      mais ar vertical que v0)
│                                      │
│   ━━━━━━━━━━━━━━                     │  ← 2 segmentos curtos em
│                  ━━━━━━━━━━━━━━      │     #266D74, stroke 1.5pt,
│                                      │     sem se tocarem (metáfora
│   ─────────                          │     do buraco entre contato
│                                      │     e consulta)
│                                      │
│   Assessoria de captação ética       │  ← Sub-hook, Lora ~22pt,
│   para clínicas e consultórios       │     #E4E6E3
│   de psicologia.                     │
│                                      │
│                                      │
│  [logo PsiAtiva]   psiativa.com.br/  │  ← Footer: logo negativo
│                    indicacao         │     à esquerda, URL à
│                                      │     direita em #7EAE89,
│                                      │     ~14pt
└──────────────────────────────────────┘

       Background: #1C2B2B (dark green)
```

### Camadas detalhadas

1. **Background** — `#1C2B2B` (Dark Green, hero/footer da paleta da marca). **Nunca** branco puro nem off-white para esta peça.

2. **Hook** — *"O buraco está no processo."*
   - Tipografia: **New York** (Display, serifa)
   - Tamanho: ~88 pt (gera 1 quebra de linha visível no formato 4:5; mais ar vertical do que a v0)
   - Cor: `#FAFFFF` (warm white)
   - Peso: regular em "O buraco está"; **semibold na palavra "processo"** para criar ênfase sem usar caixa alta nem sublinhado
   - Alinhamento: esquerda
   - Leading apertado (line-height ~0.95)

3. **Grafismo de linha (opcional, recomendado)** — duas barras horizontais curtas, **sem se encontrarem**, em `#266D74`, stroke de 1.5 pt. Posição: logo abaixo do bloco do hook, deslocadas em ~50 px no eixo X. Função simbólica: visualizar o gap entre o primeiro contato e a sessão confirmada. Pode sair do design se ficar visualmente ruidoso.

4. **Divider** — linha fina horizontal de 1 px em `#7EAE89`, cobrindo ~30% da largura. Separa hook do sub-hook.

5. **Sub-hook** — *"Assessoria de captação ética para clínicas e consultórios de psicologia."*
   - Tipografia: **Lora**
   - Tamanho: ~22 pt
   - Cor: `#E4E6E3` (sage BG, mas usado aqui como tom de texto secundário sobre fundo escuro)
   - 2–3 linhas, leading confortável

6. **Footer** — logo PsiAtiva versão **negativa** (branca, `#FAFFFF`) à esquerda + URL `psiativa.com.br/indicacao` à direita, em **Source Serif Pro** ou **DM Sans**, ~14 pt, cor `#7EAE89`. Alinhamento na linha base. Sem botão, sem CTA visual.

---

## Por que essas escolhas

### Por que esse hook (Pilar 2 — Reframe), em vez da hemorragia clássica do Pilar 1

A frase canônica de PsiAtiva — *"Você está perdendo pacientes entre o primeiro contato e a sessão confirmada"* — é mais forte para conteúdo de feed orgânico, onde a peça precisa carregar a tese inteira sozinha. No contexto de indicação, a **mensagem que acompanha a arte já entrega essa tese em prosa**. Repetir a mesma frase na arte gera redundância e desperdiça os 2 segundos que a peça tem para fazer o segundo movimento da copy.

O hook do reframe — *"O buraco está no processo."* — faz exatamente esse segundo movimento: **localiza o problema antes da auto-culpa entrar em cena**. A arte planta a bandeira direto no processo. A versão por afirmação direta (em substituição à estrutura clássica "não é X, é Y", descartada pelo `humanizer-psiativa` no Step 2b) deixa a destinatária deduzir sozinha: se o buraco está no processo, a competência clínica está fora do escopo do problema. Reframe por afirmação, em 6 palavras.

### Por que ICP Mixed em vez de um par dividido (clínica + solo)

Tecnicamente o skill autoriza Mixed apenas com vocabulário neutro entre os dois ICPs. *"Não é falta de qualidade. É falta de processo."* + *"clínicas e consultórios de psicologia"* não tem nenhuma linguagem que pertença exclusivamente a um perfil — sem mencionar equipe, recepção, "responder enquanto atende", VPS, ou qualquer marcador específico.

Operacionalmente: um par dividido criaria 2 decisões para o indicador (qual arte + qual variante de copy). Uma arte única reduz a 1 decisão (qual variante de copy) e mantém o kit ergonômico. Vale o pequeno custo de não amplificar especificidade na arte.

### Por que dark green (`#1C2B2B`) em vez do off-white default

Off-white é o default das páginas longas da marca; dark green é o token reservado para hero/footer (modo "primeira impressão" ou "fechamento"). **Um card de indicação é literalmente um hero** — é a primeira impressão visual que a destinatária terá da marca, antes mesmo de ler a mensagem. Usar dark green:

- Cria contraste alto contra o feed claro do WhatsApp e Instagram (a peça "salta" do thumbnail)
- Sinaliza categoria de "clínica premium" / "publicação editorial", afastando da estética de anúncio digital
- Faz o tipo serifado em branco quente parecer impresso, não digital — um dos sinais que separa "assessoria" de "agência" para esse ICP

### Por que composição 100% tipográfica, sem foto e sem ícone

A `marca-identidade-visual.md` é explícita: *"Photos of business-success poses, money visuals, growth charts, rockets — these destroy trust with the DISC Analytical+Stable ICP"*. O ICP deste kit é exatamente esse perfil. Qualquer foto de psicóloga sorrindo, ícone de foguete, gráfico ascendente — desqualificação imediata.

A composição puramente tipográfica funciona como uma **citação editorial de revista de saúde**. É o registro visual mais próximo de "isto foi feito por quem entende de clínica, não por quem vende curso."

### Por que o sub-hook carrega o sub-hook completo da categoria

A frase *"Assessoria de captação ética para clínicas e consultórios de psicologia"* é compacta e faz três trabalhos simultâneos:

1. **assessoria** (não agência) — desambigua categoria
2. **ética** (não growth hacking) — desativa a objeção silenciosa antes dela aparecer
3. **clínicas e consultórios de psicologia** (não healthcare genérico) — sinaliza nicho profundo, não fornecedor genérico

Essas três disambiguações em 11 palavras são exatamente o que o ICP precisa estabelecer **antes de ler a mensagem**. A arte deixa o caminho limpo para a copy fazer o trabalho dela.

### Por que a URL no rodapé, e não como botão

Botão tipo "saiba mais" ou "agende agora" é linguagem de mídia paga. URL como assinatura editorial é linguagem de marca/autoridade. A regra de CTA do skill (Step 3, Format A) bane explicitamente CTAs agressivos. Manter a URL como crédito discreto reforça que a peça é uma cortesia, não uma captura.

---

## Variação para Stories (9:16) — opcional

Se for distribuir também como Stories, manter a mesma composição com 3 ajustes:

- Hook quebrado em mais linhas (4–5 versus 4 no 4:5) e centralizado verticalmente
- Sub-hook movido para mais perto do rodapé
- Adicionar sticker de link com `https://psiativa.com.br/indicacao` (Stories permitem link clicável; aproveitar)
- Logo + URL do rodapé podem ser substituídos pelo sticker de link, evitando duplicação

---

## Compliance scan (Step 5 do skill)

| Check | Resultado |
|---|---|
| **Vocabulário** | ✅ Limpo. *Assessoria, captação, ética, processo, paciente, clínica, consultório, psicologia* — todos approved. Zero ocorrências de *marketing · leads · vendas · funil · escalar · contrato · comercial · campanha · agência · cliente (do psicólogo)*. |
| **Estruturas de comparação/negação (Step 2b)** | ✅ Hook reescrito como afirmação direta. A v0 usava *"Não é falta de qualidade. É falta de processo."* — descartada pelo zero-tolerance de "não é X, é Y" no `humanizer-psiativa`. |
| **Framing** | ✅ Hook é hemorragia direta (buraco = perda silenciosa, sem prometer ganho). Sub-hook é declarativo de categoria, neutro em direção. |
| **Subject opening** | ✅ A frase abre com o "buraco" como sujeito metafórico. A destinatária olha para o gap; PsiAtiva só aparece no rodapé. |
| **CTA** | ✅ URL como assinatura editorial. Quem clica, clica por curiosidade. |

---

## Variantes futuras (não para v1)

Se o kit ganhar tração e for útil expandir, dois próximos cards naturais seriam:

1. **Card "promessa+garantia"** — fundo off-white `#F0F7F4`, hook: *"Agenda previsível começa com processo."* + sub-hook citando a garantia (sem citar valor). Função: reforço para destinatária já aquecida.
2. **Card NR-1 2026** — fundo `#FAFFFF`, hook: *"A partir de 2026, empresas vão precisar contratar psicólogos."* + sub-hook: *"Quem está bem posicionado online captura essa demanda primeiro."* Função: usar a janela estrutural como gatilho de urgência sem pressão.

Ambas as variantes podem entrar como v2 do kit, sem substituir a peça única atual.
