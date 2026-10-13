# O que o app NÃO vai conter (e o que o grupo trouxe de volta)

Esforço: **P** (até 1 sprint de 1 pessoa), **M** (1 sprint de 2 pessoas), **G** (mais que isso). A Etapa 2 tem 3 sprints (26/10 a 06/12) e o grupo é novo em mobile.

## Aprovado pelo grupo para voltar ao MVP

| Item | HOW IV | Esforço | No projeto |
|---|---|---|---|
| Pontuação simples por descarte registrado, com limite diário | pontuação, RN002 e RN006 | M | PB16, RF09, RN08, RN09 |
| Saldo e histórico de pontos (feedback visual) | feedback visual | P | PB16, RF10 |
| Dicas de reciclagem | RF14 | P | PB17, RF11 |
| Abrir a rota até o ponto no app de mapas | RF8 | P | RF05 (explícito) |

**Limitação assumida:** sem QR Code, GPS ou foto, o registro de descarte é autodeclarado. O limite de 3 registros por dia (RN09) é a contenção; a validação automática continua fora (risco R-04 do plano).

## Continua fora do MVP

### A. Estavam na proposta do HOW IV

| # | Item | HOW IV | Esforço | Por que fica fora |
|---|---|---|---|---|
| 1 | Relato de problema (lixeira cheia, coleta não realizada) | RF12, RF13 | M | Precisa de um destino para os relatos (servidor) |
| 2 | Check-in no ponto por QR Code ou GPS | check-in | M | Permissões e testes de localização; deixaria a pontuação validável, ficou para evolução |
| 3 | Ranking do bairro e competição entre ruas/condomínios | ranking | M | Precisa de servidor e dados de vários usuários |
| 4 | Marketplace de recompensas e parcerias com o comércio | marketplace, RN003, RN005 | G | Depende de parceiros reais |
| 5 | Validação do descarte por foto com IA ou moderador | IA | G | Fora do alcance do prazo |
| 6 | Notificação push enviada por servidor (12 h antes) | RF2 | G | Servidor, FCM e APNs; o lembrete local cobre o essencial |
| 7 | Painel administrativo para cadastrar pontos e cronogramas (login e 2FA) | RF4, RF9, RF15, RF16, RNF7 | G | Hoje os dados são cadastrados em arquivo |
| 8 | Rastreamento do caminhão em tempo real | exclusão original | G | Depende de dados externos |
| 9 | Chat, fórum ou comunicação entre usuários | exclusão original | G | Fora do foco |

### B. Nunca estiveram na proposta

| # | Item | Esforço | Observação |
|---|---|---|---|
| 10 | Conta de usuário, login e sincronização na nuvem | G | Exige servidor; o MVP é local de propósito |
| 11 | Mapa interativo com localização atual e pontos próximos | M | Chave de API e permissões; decisão D-02 deixou para depois |
| 12 | Dados reais e atualizados de todos os municípios do Vale | G | Depende de cada prefeitura; o MVP usa dados de demonstração |
| 13 | Modo escuro, idiomas, acessibilidade avançada | P a M | Só se sobrar tempo |

## Candidatos naturais para uma próxima rodada

Se o grupo quiser reavaliar depois, os mais baratos de trazer são o **QR Code ou GPS** (item 2, torna a pontuação verificável) e o **mapa interativo** (item 11). Os demais exigem servidor ou parceiros.
