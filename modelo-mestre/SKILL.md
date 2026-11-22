---
name: modelo-mestre
description: Use quando o Tales chamar /modelo-mestre ou pedir para criar um SaaS do zero até o ar. Orquestra as skills numeradas de 01 a 10, sempre com GitHub como fonte.
---

# Modelo Mestre · orquestrador

Conduz um SaaS da ideia ao ar, chamando uma skill especialista por etapa. As regras de segurança, pagamento, fotos, IA e ativação ficam no `MODELO-MESTRE.md` do Drive (id `1XqUomKOCocRKfc7E4exnVRoT2kn6b5i-`), lido a cada execução.

## Passo 0 · Regras que valem sempre
1. Leia `MODELO-MESTRE.md` no Drive. Use a versão atual.
2. **GitHub antes de tudo.** Antes do código, o projeto precisa estar no GitHub com as issues criadas. Se o repositório não existir, peça ao Tales nome, conta ou organização e visibilidade (recomendado: privado) antes de criar.
3. Todo trabalho segue issue → branch → pull request → merge. Nunca enviar direto para a branch principal.
4. Leia `00-Visao.md`, `01-Plano.md` e `02-Decisoes.md` no Obsidian, se já existirem.

## Passo 1 · Perguntas (toda execução)
Uma por vez, com a opção padrão primeiro. **As perguntas 1, 2 e 9 são obrigatórias em toda execução.**

1. **Stack e hospedagem:** Next.js + Supabase + Hostinger (padrão), PHP + MySQL, Lovable, Floot, v0 ou Cloudflare.
2. **Pagamento:** Asaas (padrão), Cakto, Hotmart, Kiwify, Stripe ou Mercado Pago.
3. **Grupo:** casa, estúdio, equipe, turma ou clínica.
4. **Módulos:** quais telas o produto tem.
5. **Público e primeira ação** que já mostra valor.
6. **Preço e teste:** valor por grupo, dias de teste e limite do plano grátis.
7. **IA e custo por uso:** se usar IA ou API paga, limite de gasto e de uso por grupo (seção 3B do Modelo Mestre).
8. **Design:** design system existente, tema novo ou tema do Rotina.
9. **Ferramenta de design:** Figma (padrão), Penpot, Canva, Framer ou nenhuma.

Sem resposta, use a opção padrão e registre em `02-Decisoes.md`.

## Passo 2 · Sequência
- `01-ideia-escopo` e `02-auditoria-previa` (gate 1)
- `03-arquitetura-stack` (gates 0 e 2)
- `04-design-interface` (gate 3)
- `05-construcao-codigo` (gate 4)
- `06-seguranca-pre-venda` (gate 5)
- `07-pagamento-webhooks` (gate 6)
- `08-email-resend` (gate 7)
- `09-publicacao-operacao` (gates 8 e 9)
- `10-ativacao-vendas` (gate 9)

Avance um gate por vez. Pare em cada aprovação e espere o Tales.

## Regras que não mudam
- Nenhum segredo no código, no Obsidian, no GitHub ou no chat.
- Nada apagado sem backup confirmado e autorização do Tales.
- Nenhum depoimento, número ou escassez inventados.
- Antes de trocar a stack, aumentar custo ou mudar cobrança: parar e perguntar.
- Limite de tentativas com Upstash; se cair, contador na memória (a porta não abre).

## Saída em cada parada
- Projeto:
- Gate atual:
- Feito:
- Pendente:
- Precisa de decisão do Tales:
