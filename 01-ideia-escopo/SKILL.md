---
name: 01-ideia-escopo
description: Use quando o Tales tiver uma ideia de SaaS ou app e precisar transformá-la em visão, público, MVP e primeira ação que mostra valor, antes de qualquer código.
---

# 01 · Ideia e escopo

Gate 1. Transforma a ideia em plano aprovado, sem código.

## Entradas
- A ideia em linguagem livre.
- Respostas às perguntas 3 a 6 do Modelo Mestre.

## Passos
1. Escreva o problema e o público, cada um em uma frase.
2. Defina a **primeira ação** que mostra valor. Ela vira o critério de aceite da primeira issue.
3. Liste os módulos do MVP: o que fazem, quem usa, o que acontece se faltarem.
4. Liste o que fica **fora do MVP**.
5. Liste riscos: técnicos, de custo, de dados pessoais e de mercado.
6. Defina cobrança e limite do plano grátis.

## Saídas
- `00-Visao.md` e `01-Plano.md` no Obsidian.
- Issue de planejamento no GitHub, com o plano anexado.

## Segurança
- Marque os dados pessoais que o produto vai guardar. Eles seguem para `02-auditoria-previa`.
- Não colete dado que o MVP não usa.

## Design
- Registre o tema (pergunta 8) e a ferramenta de design (pergunta 9). Sem telas nesta etapa.

## Aprovação
Pare. Só avance quando o Tales aprovar `01-Plano.md`.

## Não faz
- Não escolhe stack (isso é `03-arquitetura-stack`).
- Não cria issues de código (isso é `05-construcao-codigo`).
