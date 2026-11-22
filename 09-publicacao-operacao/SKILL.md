---
name: 09-publicacao-operacao
description: Use quando um SaaS estiver pronto para o ar: deploy na hospedagem escolhida, domínio, SSL, variáveis de ambiente, backup, monitoramento e checklist de lançamento, sempre com aprovação do Tales.
---

# 09 · Publicação e operação

Gates 8 e 9. Coloca o produto no ar e mantém o básico funcionando.

## Passos
1. **Ambientes:** produção e homologação separadas. Homologação usa pagamento de teste.
2. **Variáveis:** todas no painel da hospedagem. O app não sobe se faltar uma obrigatória.
3. **Domínio e SSL:** DNS apontado, HTTPS ativo e HSTS confirmado.
4. **Deploy:** a partir da branch principal, com tag de versão. Nunca de cópia local.
5. **Verificação:** `curl` em `/.env`, `/.git/HEAD` e `/db/...` deve dar 404. Cabeçalhos de segurança presentes (CSP, HSTS, X-Frame-Options, nosniff).
6. **Backup:** automático do banco, com teste de restauração em homologação.
7. **Monitoramento:** erros de servidor, tempo de resposta e falhas de webhook, com alerta para o Tales.
8. **Checklist:** `06-Lancamento.md` completo.
9. **Pós-lançamento (Gate 9):** revisão semanal de erros e de custo. Novas issues a partir do feedback.

## Saídas
- URL registrada no Obsidian e na issue final.
- `06-Lancamento.md` preenchido.
- Tag de lançamento no GitHub.

## Segurança
- Nenhum segredo fora do painel da hospedagem.
- 2FA no painel.
- Rota de administração com login e fora de endereço óbvio.

## Design
- Conferir no iPhone e no Android, favicon, título e imagem de compartilhamento.

## Aprovação
Antes do deploy de produção. O Tales autoriza.

## Não faz
- Não publica sem aprovação.
- Não apaga dados sem backup confirmado e autorização.
