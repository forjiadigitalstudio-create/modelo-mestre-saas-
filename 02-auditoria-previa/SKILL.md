---
name: 02-auditoria-previa
description: Use antes de escrever código de um SaaS, para fazer modelagem de ameaças, mapear dados pessoais (LGPD), calcular custo mensal e definir os testes de segurança da auditoria final.
---

# 02 · Auditoria prévia

Gate 1, em paralelo ao plano. Descobre riscos antes de existir código.

## Entradas
- `01-Plano.md` (de `01-ideia-escopo`).
- Módulos e integrações prováveis: pagamento, e-mail, IA, storage.

## Passos
1. **Ativos:** dados de cliente, senhas, sessões, fotos, dinheiro, chaves de API, acesso de admin.
2. **Atores:** visitante, cliente, membro do grupo, admin, atacante, plataforma de pagamento (webhook).
3. **Ameaças por ativo:** acesso entre grupos, força bruta, CSRF, injection, webhook falso, chave vazada, IA sem limite, foto com localização.
4. **Dados pessoais (LGPD):** para cada dado, o que é, para quê, onde fica, por quanto tempo e quem acessa. Registre a base legal.
5. **Custo mensal:** hospedagem, banco, e-mail, IA, storage, domínio e taxa do pagamento.
6. **Testes da auditoria final:** para cada ameaça, o teste que `06-seguranca-pre-venda` vai rodar.

## Saídas
- `05-Seguranca.md` no Obsidian, com a seção "Ameaças" e a lista de testes.
- `02-Decisoes.md`: custo mensal e decisões sobre dados.
- Issues no GitHub, uma por ameaça relevante, com rótulo `tipo:seguranca`.

## Segurança
- Nenhum dado real de cliente nesta etapa.
- Nenhuma chave real nas notas.

## Design
- Cadastro só com o necessário.

## Aprovação
Pare. O Tales aprova `05-Seguranca.md` junto com o plano.

## Não faz
- Não testa nada em sistema no ar.
- Não decide stack (isso é `03-arquitetura-stack`).
