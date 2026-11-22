---
name: 10-ativacao-vendas
description: Use depois do lançamento de um SaaS para ativar os primeiros usuários: primeira ação, convite, aviso de fim de teste, página de vendas e acompanhamento das primeiras 10 contas.
---

# 10 · Ativação e vendas

Gate 9. Faz o produto ser usado por duas pessoas do mesmo grupo, que é a medida de sucesso.

## Passos
1. **Primeira ação pequena:** a tela inicial leva direto a ela.
2. **Convite logo depois:** pelo WhatsApp, com link que leva a outra pessoa à mesma lista, sem digitar código.
3. **Ranking "Quem mais fez":** só aparece depois que duas pessoas agiram.
4. **Aviso de fim do teste:** a partir de 2 dias antes, com o que o grupo já fez e as duas opções lado a lado. Nada é apagado e nada é cobrado sem cartão.
5. **Limite do grátis:** bloqueia só criar item novo. O que existe continua editável.
6. **Página de vendas (site separado):** público e resultado no topo; botão com a ação; depoimento só real e autorizado.
7. **Primeiras 10 contas:** escolha pela dor, metade conhecidos e metade desconhecidos. Acompanhe com `funil-primeiras-contas.sql`: teste iniciado, parceiro entrou, primeira ação em dupla, bateu no limite, pagou, voltou no dia 14.
8. **Uma mudança por vez:** preço, limite e página não mudam juntos.

## Saídas
- Funil das 10 primeiras contas em `06-Lancamento.md` ou nota própria no Obsidian.
- Issues de melhoria no milestone `pos-lancamento`.

## Segurança
- Convite com link de uso limitado e expiração.
- Dados de conta de teste não viram depoimento nem anúncio.

## Design
- Primeira tela com uma ação clara.
- Aviso de fim de teste com cor de alerta e texto simples.

## Aprovação
Antes de qualquer mudança de preço ou anúncio pago.

## Não faz
- Não inventa depoimento, número, escassez ou urgência.
- Não aumenta preço nem muda limite sem aprovação.
