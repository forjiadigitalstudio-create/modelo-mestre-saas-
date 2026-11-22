---
name: 08-email-resend
description: Use quando um SaaS precisar enviar e-mails transacionais pelo Resend: domínio verificado, SPF e DKIM, confirmação de conta, acesso liberado, recuperação de senha e teste de entrega.
---

# 08 · E-mail com Resend

Gate 7. Garante que os e-mails chegam na caixa de entrada.

## Passos
1. **Domínio:** adicione no Resend. Crie os registros SPF e DKIM no DNS e confirme a verificação.
2. **DMARC:** comece em `p=none` para observar.
3. **Remetentes:** um por função (`contato@`, `nao-responda@`). Nada de remetente pessoal.
4. **Modelos:** confirmação de conta, acesso liberado, recuperação de senha (link de uso único, 30 min), aviso de fim de teste, comprovante de compra.
5. **Envio:** chave só no servidor. Limite de envios por usuário e por IP.
6. **Teste real:** cada modelo em Gmail e iPhone, na caixa de entrada e não no spam.
7. **Falha:** registre o erro e tente de novo com limite. Nunca marque a conta como confirmada sem o clique no link.

## Saídas
- Domínio verificado e DMARC configurado.
- Modelos no repositório.
- Resultado do teste de cada modelo em `06-Lancamento.md`.

## Segurança
- Tokens de uso único, guardados como hash.
- Nenhuma senha ou token completo em log.
- Resposta de "esqueci a senha" igual, com ou sem conta.

## Design
- Mesmo tema do produto, texto curto, botão claro e versão em texto simples.

## Aprovação
O Tales aprova os modelos antes do primeiro envio real.

## Não faz
- Não envia campanha em massa sem autorização.
- Não compra lista de e-mail.
