# O que o app NÃO vai conter (para o grupo reavaliar)

Lista do que ficou de fora do MVP, com esforço estimado, risco e uma recomendação. A decisão é do grupo: marque o que quer trazer de volta e o que muda no Product Backlog.

Esforço: **P** (até 1 sprint de 1 pessoa), **M** (1 sprint de 2 pessoas), **G** (mais que isso). A Etapa 2 tem 3 sprints (26/10 a 06/12) e o grupo não tem experiência em mobile; o PB12 (lembrete) já é o primeiro a sair.

## A. Vieram do HOW IV (estavam na proposta original)

| # | Item | HOW IV | Esforço | Risco | Recomendação |
|---|---|---|---|---|---|
| 1 | Pontuação simples por descarte correto (pontos por tipo de resíduo, limite diário) | RF de pontuação, RN002 e RN006 | M | Baixo: é regra de negócio pura, ótima para TDD | **Trazer** (candidato principal) |
| 2 | Histórico e feedback visual do impacto (quantos descartes, pontos) | feedback visual | P | Baixo, depende do item 1 | Trazer junto com o 1, se der tempo |
| 3 | Dicas de reciclagem e informação ambiental | RF14 | P | Baixo: conteúdo estático | **Trazer** (barato) |
| 4 | Navegação até o ponto via app de mapas | RF8 | P | Baixo | **Já cabe no RF05**; só explicitar |
| 5 | Relato de problema (lixeira cheia, coleta não realizada), sem foto | RF12, RF13 | M | Médio: precisa de destino para os relatos | Talvez; só se houver servidor |
| 6 | Check-in no ponto por QR Code ou GPS | check-in | M | Médio: permissões, testes de localização | Fora |
| 7 | Ranking do bairro e competição entre ruas/condomínios | ranking | M | Alto: precisa de servidor e dados de vários usuários | Fora |
| 8 | Marketplace de recompensas e parcerias com o comércio | marketplace, RN003, RN005 | G | Alto: depende de parceiros reais | Fora |
| 9 | Validação do descarte por foto com IA ou moderador | IA | G | Alto | Fora |
| 10 | Notificação push enviada por servidor (12 h antes) | RF2 | G | Alto: servidor, FCM e APNs | Fora (o lembrete local cobre o essencial) |
| 11 | Painel administrativo para cadastrar pontos e cronogramas (com login e 2FA) | RF4, RF9, RF15, RF16, RNF7 | G | Alto | Fora; hoje os dados são cadastrados em arquivo |
| 12 | Rastreamento do caminhão em tempo real | exclusão original | G | Alto | Fora |
| 13 | Chat, fórum ou comunicação entre usuários | exclusão original | G | Alto | Fora |

## B. Nunca estiveram na proposta, mas o grupo pode se perguntar

| # | Item | Esforço | Observação |
|---|---|---|---|
| 14 | Conta de usuário, login e sincronização na nuvem | G | Exige servidor; o MVP é local de propósito |
| 15 | Mapa interativo com localização atual e pontos próximos (RF05 completo) | M | Chave de API, permissões e configuração; decisão D-02 deixou para depois |
| 16 | Dados reais e atualizados de todos os municípios do Vale | G | Depende de cada prefeitura; o MVP usa dados de demonstração |
| 17 | Modo claro/escuro, idiomas, acessibilidade avançada | P a M | Só se sobrar tempo |
| 18 | Painel de administração para prefeituras | G | Mesma causa do item 11 |

## Combinação que eu recomendo trazer de volta

1. **Pontuação simples (item 1) com histórico (item 2):** mantém a ligação com a gamificação do HOW IV e dá o melhor material para mostrar TDD (regras de pontuação com testes escritos antes). Estimativa: 1 sprint (dentro da Sprint 3 ou 4), ao custo de empurrar o lembrete (PB12).
2. **Dicas de reciclagem (item 3):** custo baixo, conteúdo estático.

Se o grupo aprovar, os itens viram PB16 (pontuação) e PB17 (dicas) no Product Backlog, com RN08 e RN09 no escopo.
