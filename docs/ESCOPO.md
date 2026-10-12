# Escopo do MVP

Recorte aprovado pelo grupo a partir do projeto do HOW IV. A coluna "HOW IV" mostra de onde cada item vem, para o relatório e os testes ficarem rastreáveis.

## Problema

Moradores do Monte Alegre não sabem os dias da coleta (principalmente os mais jovens), descartam pilhas e óleo de cozinha no lixo comum ou na pia, não separam orgânico de reciclável e não conhecem pontos de descarte para materiais específicos.

## Requisitos funcionais do MVP

| ID | Requisito | HOW IV | Prioridade |
|---|---|---|---|
| RF01 | O usuário escolhe seu endereço/setor de coleta e o app o guarda no aparelho | RF1 | Alta |
| RF02 | O app lembra o usuário (notificação) na véspera da coleta, em horário escolhido por ele | RF2 | Baixa (primeiro a sair se faltar tempo) |
| RF03 | O app mostra calendário com os dias das coletas seletiva e comum do setor (a coleta não tem horário fixo) | RF3 | Alta |
| RF04 | O app lista os pontos de descarte e mostra, para cada um, endereço, horário e materiais aceitos | RF5 | Alta |
| RF05 | O app permite ver a localização do ponto no mapa (começa por coordenadas e abertura no app de mapas) | RF5 | Média |
| RF06 | Os pontos são categorizados por tipo de material (pilhas, óleo, eletrônicos, roupas) | RF6 | Alta |
| RF07 | O usuário filtra os pontos por tipo de material | RF7 | Alta |
| RF08 | O app oferece guia de separação pesquisável (ex.: "caixa de leite") com a orientação de descarte | RF10, RF11 | Alta |

## Requisitos não funcionais mantidos

| ID | Requisito | HOW IV |
|---|---|---|
| RNF01 | Chegar a calendário, pontos e guia em no máximo 2 toques a partir da tela inicial | RNF3 |
| RNF02 | Funcionar em Android 9 ou superior e iOS 14 ou superior | RNF4 |
| RNF03 | O guia de separação funciona sem internet | RNF6 |
| RNF04 | A lista de pontos aparece em até 3 segundos em rede 4G | RNF1 |

## Regras de negócio mantidas

| ID | Regra | HOW IV |
|---|---|---|
| RN01 | Coleta seletiva às terças e quintas, sem horário fixo de passagem do caminhão | RN1 (horário removido, ver D-01) |
| RN02 | Coleta comum às segundas, quartas e sextas, sem horário fixo de passagem | RN2 (horário removido, ver D-01) |
| RN03 | Em feriados nacionais não há coleta; ela passa para o próximo dia útil | RN3 |
| RN04 | Pilhas, baterias e óleo de cozinha usado só vão para pontos de descarte, nunca para a coleta porta a porta | RN6 |
| RN05 | Os pontos seguem seus horários de funcionamento (seg a sex, 9h às 17h; sábado, 9h às 12h) | RN7 |
| RN06 | Eletrônicos aceitos nos pontos do bairro: até 5 kg | RN8 |
| RN07 | O serviço atende somente endereços dentro do bairro Monte Alegre | RN9 |
| RN08 | O endereço do usuário fica só no aparelho e não é exibido ou compartilhado | RN11 |

As regras RN4 (responsabilidade pela separação) e RN5 (horário para colocar o lixo na calçada) do HOW IV viram **conteúdo do guia**, não regra de sistema.

## Fora do escopo (decidido)

Pontuação por ações, marketplace de recompensas, ranking e competições, validação de descarte por foto com IA, check-in por QR Code ou GPS, backoffice administrativo (cadastro de pontos e cronogramas pelo app), relato de problemas com foto, notificações push via servidor, cobertura fora do Monte Alegre.

Esses itens continuam no relatório como visão de evolução, não como compromisso.

## Dados do app

Os pontos de descarte e o conteúdo do guia são **dados de demonstração fictícios**, identificados como tal no app e no relatório (decisão D-04). O app não coleta dados pessoais de terceiros.

## Casos de uso (apoio aos testes)

Não são uma seção exigida na Etapa 2 do HOW VIII (lá o foco é aplicação, testes e validação). Servem de base para escrever os testes e os critérios de aceite.

| ID | Caso de uso | Ator |
|---|---|---|
| CU01 | Definir endereço/setor | Morador |
| CU02 | Consultar calendário de coleta | Morador |
| CU03 | Consultar pontos de descarte (com filtro) | Morador |
| CU04 | Consultar guia de separação | Morador |
| CU05 | Configurar lembrete de coleta | Morador |

Como os dados ficam no aparelho e não há administração pelo app, o único ator é o **Morador**. O Parceiro Comercial e o Administrador do HOW IV saem junto com o marketplace e o backoffice.
