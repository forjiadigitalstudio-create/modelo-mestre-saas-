---
name: 06-seguranca-pre-venda
description: Use antes de vender um SaaS, para rodar os testes de segurança, a auditoria de dependências e a varredura local, e gerar o relatório que libera ou bloqueia a venda.
---

# 06 · Segurança pré-venda

Gate 5. Obrigatório antes de qualquer cobrança real. Achado crítico ou alto em aberto bloqueia o Gate 6.

## Passos
1. **Testes automáticos:** a suíte da seção 3 do Modelo Mestre (login, sessão, CSRF, limite de tentativas, isolamento entre grupos, consultas parametrizadas, webhook, fotos, admin, cabeçalhos). Registre o resultado de cada um.
2. **Dependências:** `npm audit --omit=dev`. Sem `high` nem `critical`.
3. **Segredos:** a chave de IA não aparece no HTML nem no JavaScript do navegador. Nenhum `.env` com valor no Git (`git ls-files`).
4. **Varredura passiva (OWASP ZAP em modo passivo):** **somente na cópia local ou de homologação**, nunca no site no ar.
5. **Limites:** limite de gasto mensal e alertas em 50% e 80%, confirmados no painel do provedor, com valor e data.
6. **Pentest:** recomende ao Tales pentest profissional autorizado antes de versões grandes. Não execute.

## Saídas
- `05-Seguranca.md`: teste, resultado, severidade e ação.
- Issues para os achados abertos, no milestone `lancamento`.
- Veredito: liberado ou bloqueado.

## Severidade
- Crítico ou alto: bloqueia a venda.
- Médio: corrigir antes do lançamento ou aceite do Tales.
- Baixo: pós-lançamento.

## Segurança
- Nunca teste sistema no ar. Use contas de teste.

## Design
- Mensagens de erro que não revelam se a conta existe.
- Campo de senha e aviso de erro testados no celular.

## Aprovação
O Tales decide sobre achados médios.

## Não faz
- Não ataca produção.
- Não declara "seguro" sem teste registrado. Opinião de IA não conta.
