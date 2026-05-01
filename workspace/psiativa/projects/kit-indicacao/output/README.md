# Kit de Indicação — Como usar

Pasta com os assets prontos para compartilhar a PsiAtiva via indicação (família, colegas, ex-clientes). Stand-alone: cada arquivo se basta.

## O que tem aqui

| Arquivo | O que é | Quando usar |
|---|---|---|
| [`messages-clinica.md`](messages-clinica.md) | 4 variantes de copy (WhatsApp curto, WhatsApp longo, e-mail, ultra-curto) | A indicação é dona/sócia de **clínica com equipe** (2+ profissionais e recepção). |
| [`messages-solo.md`](messages-solo.md) | 4 variantes de copy nos mesmos formatos | A indicação é **psicóloga autônoma**, sem equipe nem recepção. |
| [`referrer-template.md`](referrer-template.md) | Estrutura para a pessoa que está indicando — como costurar a voz dela com a copy oficial | Sempre. A indicação só funciona com a voz pessoal de quem indica. |
| [`one-pager.md`](one-pager.md) | One-pager auto-suficiente em PT-BR — fonte para `https://psiativa.com.br/indicacao` | Como conteúdo da landing page de indicação, ou como fallback (PDF/print) se a página ainda não estiver no ar. |

## Fluxo recomendado

1. A pessoa que vai indicar pergunta: *"o que mando?"*
2. Você (Juan) pergunta de volta: *"é dona de clínica com equipe ou atende sozinha?"*
3. Pega a variante correspondente em `messages-clinica.md` ou `messages-solo.md`. WhatsApp curto resolve 80% dos casos.
4. Manda para a pessoa indicando, junto com a estrutura do `referrer-template.md`.
5. Ela cola a copy depois da frase pessoal de aval dela.
6. O destinatário clica em `https://psiativa.com.br/indicacao` → cai no conteúdo do `one-pager.md` → CTA para WhatsApp do diagnóstico.

## Regra de ouro

**Nunca misture os dois ICPs no mesmo envio.** Clínica e consultório solo respondem a promessas e linguagens diferentes — o `one-pager.md` faz o split internamente, mas as mensagens curtas precisam ser **escolhidas**, não fundidas.

## Antes de distribuir

- [ ] Confirmar que `https://psiativa.com.br/indicacao` está no ar (ou substituir o link nas mensagens pelo destino real)
- [ ] Substituir o `SEU_NUMERO` no link de WhatsApp do `one-pager.md` pelo número real
- [ ] Decidir se o `one-pager.md` será publicado como página web ou exportado como PDF para anexar — o conteúdo é o mesmo

## Manutenção

- Mudou a promessa de uma das esteiras (R$10k em 6 meses / 45 dias)? Atualizar o `one-pager.md`, depois propagar para `messages-clinica.md` e `messages-solo.md`.
- Mudou a garantia? Mesma ordem de propagação.
- Surgiu um terceiro ICP (corporativo via NR-1, por exemplo)? Criar um terceiro arquivo de mensagens, **não** misturar com os existentes.

Versão: v1, 2026-04-29.
