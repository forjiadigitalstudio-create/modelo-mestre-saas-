---
name: 04-design-interface
description: Use quando um SaaS precisar de telas, sistema visual, tokens de design e checagem de acessibilidade e de celular, em Figma, Penpot, Canva, Framer ou direto na ferramenta de construção.
---

# 04 · Design de interface

Gate 3. Define como o produto parece e se usa, sem mudar a segurança.

## Passos
1. **Ferramenta:** use a da pergunta 9. Com o Figma e o conector disponível, leia variáveis e telas direto. Penpot, Canva e Framer seguem o mesmo fluxo de exportação.
2. **Tokens:** cor, tipografia, espaçamento, raio e sombra, exportados para `styles/tema.css`. Sem ferramenta externa, extraia o tema do código gerado.
3. **Telas:** uma por módulo, mais cadastro, login, convite, erro e assinatura. A primeira ação aparece em destaque.
4. **Componentes:** botão, campo, lista, cartão, aviso, modal. Cada um com estados normal, foco, erro e desativado.
5. **Acessibilidade:** contraste AA, foco visível, toque de 44 px, fonte de 16 px nos campos, teclado adequado a cada campo.
6. **Celular:** teste em iPhone e Android. `viewport-fit=cover` com `env(safe-area-inset-*)`. Teclado não cobre o campo ativo.
7. **Página de vendas (se houver):** público e resultado no topo, botão com a ação, o que acontece no 8º dia, "como funciona" logo abaixo. Depoimento só real e autorizado.

## Saídas
- Link das telas na ferramenta de design, na issue de design.
- `styles/tema.css` no repositório.
- Checklist de acessibilidade no PR.

## Segurança
- Nenhum token ou chave em arquivo de design.
- Mensagens de login iguais, com ou sem conta.

## Design (regras fixas)
- Trocar o tema não muda contraste, foco, toque, fonte ou segurança.
- Cada e-book ou PDF ganha cor e estilo novos.

## Aprovação
O Tales aprova telas e tema antes do Gate 4.

## Não faz
- Não escreve regra de negócio nem de segurança.
- Não usa imagem de terceiros sem licença.
