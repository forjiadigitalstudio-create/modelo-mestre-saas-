---
name: 05-construcao-codigo
description: Use quando um SaaS tiver backlog no GitHub e precisar ser construído: issues, branches, código com testes, CI, pull requests, merge e registro no Obsidian, sempre pelo GitHub.
---

# 05 · Construção de código

Gate 4. Transforma issues em código mesclado, com teste e revisão.

## Regra de ouro
Uma issue = uma branch = um pull request = um merge. Nunca direto na branch principal. Sem issue, sem código.

## Antes da primeira issue
1. Repositório criado a partir do `repo-template-saas`, com `CLAUDE.md`, templates de issue e PR e o workflow de gates.
2. Branch principal protegida: pull request obrigatório e CI verde.
3. Milestones `mvp`, `lancamento` e `pos-lancamento`.
4. Confirme com o Tales o nome, a conta ou organização e a visibilidade antes de criar.

## Ciclo de cada issue
1. Leia contexto, critério de aceite e fora do escopo.
2. Crie a branch `tipo/numero-resumo`, por exemplo `feat/12-anotar-item`.
3. Escreva o teste primeiro quando a issue tiver regra de segurança ou de negócio.
4. Código em commits pequenos, em português, no imperativo.
5. Abra o PR com o template. Use `Closes #numero`.
6. Espere o CI: testes, lint e varredura de segredos.
7. Espere a aprovação do Tales. Depois, merge.
8. Atualize `07-Log.md` e `04-Tarefas.md` no Obsidian.

## Fechamento de milestone
Todas as issues fechadas, CI verde, tag de versão (ex.: `v0.1.0-mvp`).

## Segurança
- `.env` fora do Git. Só `.env.example` sem valor real.
- Segredo commitado por engano: troque a chave no provedor. Apagar o arquivo não basta.
- A varredura de segredos no CI bloqueia o merge.

## Design
- Use os tokens de `styles/tema.css`. Sem cor solta no código.

## Aprovação
Em cada PR. Merge só com aprovação do Tales.

## Não faz
- Não faz merge sem CI verde.
- Não publica (isso é `09-publicacao-operacao`).
