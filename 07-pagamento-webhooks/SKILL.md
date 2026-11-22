---
name: 07-pagamento-webhooks
description: Use quando um SaaS precisar cobrar: configurar Asaas, Cakto, Hotmart, Kiwify, Stripe ou Mercado Pago, o webhook que libera o acesso e os testes de compra, cancelamento e reembolso.
---

# 07 · Pagamento e webhooks

Gate 6. Liga a venda à liberação de acesso, com confirmação em dois lugares.

## Passos
1. **Plataforma:** confirme a pergunta 2. Low ticket: Cakto, Hotmart ou Kiwify. Assinatura: Asaas ou Stripe.
2. **Planos:** crie na plataforma, com os valores do `01-Plano.md`.
3. **Webhook:** endpoint dedicado, com token comparado em tempo constante, limite de 64 KB e idempotência.
4. **Confirmação dupla:** ao receber o evento, consulte status e valor na API da plataforma. Nunca confie só no corpo recebido.
5. **Vínculo:** ache o grupo pelo id da assinatura ou da cobrança. Nunca pelo e-mail.
6. **Estados:** pago libera; cancelado ou reembolsado bloqueia sozinho. O painel admin é só plano B manual.
7. **Testes em homologação:** compra, liberação, cancelamento, reembolso, evento repetido e token errado (deve ser recusado).

## Saídas
- Endpoint e tabela de assinaturas no repositório.
- Checklist de pagamento em `06-Lancamento.md`.
- Plataforma e taxas em `02-Decisoes.md`.

## Segurança
- Token do webhook só nas variáveis da hospedagem.
- Dado de cartão nunca passa pelo servidor do produto.
- Logs sem dado pessoal completo.

## Design
- Tela de assinatura com valor, o que muda e como cancelar, em linguagem simples.

## Aprovação
Antes de ligar a cobrança real.

## Não faz
- Não cobra em produção sem aprovação.
- Não libera acesso por clique do cliente.
