---
name: 03-arquitetura-stack
description: Use quando um SaaS já tiver plano aprovado e precisar escolher a ferramenta de construção, modelar o banco com isolamento entre grupos e definir permissões e integrações.
---

# 03 · Arquitetura e stack

Gates 0 e 2. Define como o produto será construído, antes do código.

## Passos
1. **Ferramenta de construção:** compare as opções da pergunta 1 (Next.js + Supabase + Hostinger, PHP + MySQL, Lovable, Floot, v0, Cloudflare). Para cada uma: custo, controle de segurança, exportação para o GitHub e suporte a RLS ou equivalente. Recomende uma e espere a escolha do Tales.
2. **Modelo de dados:** toda tabela de dado de cliente tem `grupo_id`. Defina chaves, índices, sessões e auditoria.
3. **Permissões:** para cada ação, quem pode fazer. `grupo_id` vem sempre da sessão, nunca do formulário. RLS ligado e forçado.
4. **Integrações:** pagamento (pergunta 2), Resend, IA (se houver), storage de fotos, Upstash para limite de tentativas.
5. **Segredos:** liste cada chave e onde fica. Só no painel da hospedagem, nunca no navegador.
6. **Diagrama:** gere `03-Arquitetura.md` com o mapa de conexões.

## Saídas
- `02-Decisoes.md`: stack, motivo e custo mensal.
- `03-Arquitetura.md`: diagrama e tabelas.
- Issues de estrutura no GitHub, com rótulo `fase:mvp`.

## Segurança
- Sem `grupo_id` em toda tabela de dado, o projeto não avança.
- Consultas sempre parametrizadas.
- Nenhuma chave com permissão total no navegador.

## Design
- Defina onde ficam as cores: `styles/tema.css` ou a ferramenta de construção.

## Aprovação
Gate 0 (stack) e Gate 2 (modelo de dados).

## Não faz
- Não escreve telas nem código de tela.
- Não troca a stack sem aprovação do Tales.
