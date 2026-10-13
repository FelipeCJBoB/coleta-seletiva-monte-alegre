<!-- Dono: Integrante 2 (Product Owner); 4.1.6 revisada pelo Integrante 5. Seção 4 (Etapa 1). Mantenha igual a docs/ESCOPO.md. -->

## Etapa 1

Esta seção apresenta os resultados parciais do projeto: o problema, o objetivo, o escopo, os envolvidos, as atividades, as ferramentas, as métricas e o cronograma.

## Definição do Escopo do Projeto

O projeto tem como tema a gestão de resíduos e a coleta seletiva no bairro Monte Alegre. A definição do escopo usa o pensamento computacional para decompor o problema e a engenharia de requisitos para alinhar a solução às necessidades dos moradores.

## Compreensão do Problema na Comunidade

A pesquisa de campo foi realizada no bairro Monte Alegre, com observação e entrevistas com moradores, para compreender a realidade local em relação aos resíduos e à coleta seletiva. Os moradores mais velhos conhecem melhor os dias em que o caminhão passa, enquanto os mais jovens têm menos informação, o que sugere falta de engajamento. Embora o caminhão cumpra os dias regulares, não há horário fixo de passagem, o que causa confusão e atrasos no descarte.

O descarte incorreto em ruas e terrenos baldios é comum, com acúmulo de sujeira, mau cheiro e proliferação de insetos. Todos os entrevistados desconhecem locais adequados para óleo de cozinha, pilhas e baterias: a maioria descarta pilhas e baterias no lixo comum e o óleo na pia ou na terra. Nenhum separa orgânico de reciclável.

O principal problema é, portanto, a falta de informação e de estrutura local para a destinação correta dos resíduos, sobretudo entre o público mais jovem.

**Dados e relatos de fontes públicas do Vale do Itajaí.** Como não foi possível ampliar a pesquisa de campo, o grupo ampliou o recorte geográfico e passou a analisar o que já foi publicado sobre a coleta seletiva na região: matérias jornalísticas com relatos de moradores, comunicados de prefeituras e do Samae e estudos acadêmicos. São fontes de terceiros e complementam, sem substituir, a pesquisa de campo do HOW IV.

Em Itajaí, moradores dos bairros São Vicente, Fazenda, Vila Operária, São João e Ressacada relataram que o caminhão da coleta seletiva nem sempre passa no dia previsto; uma moradora da rua Expedicionário Marquetti, no Fazenda, contou que a família acaba misturando o reciclável com o orgânico por falta de espaço para guardá-lo (DIARINHO, 2024). A empresa responsável, procurada pela reportagem, disse não ter registros de queixas e atribuiu o problema à desinformação sobre a mudança de horário da coleta, que passou das 8h para as 6h em vários bairros (DIARINHO, 2024). A coleta passa uma vez por semana nas residências e duas nos condomínios (DIARINHO, 2022).

Em Blumenau, um levantamento do Samae divulgado em 2020 apontou que cerca de 45% do material coletado como reciclável (315 de 700 toneladas por mês) não era aproveitado, porque chegava misturado a rejeitos orgânicos nas residências e nos contêineres, ao custo de R$ 194 por tonelada para o município (INFORME BLUMENAU, 2020). O Samae orienta que eletrônicos, lâmpadas, pilhas e baterias não são recolhidos pela coleta seletiva e devem voltar ao local de compra, e que as coletas seletiva e comum passam em dias diferentes (INFORME BLUMENAU, 2020). Nos comentários da matéria, um leitor perguntou se lâmpadas, pilhas, pneus e isopor também deveriam ser recolhidos pelo Samae, o que mostra a dúvida sobre o que separar.

Em Balneário Camboriú, o programa ReciclaBC passa em todos os endereços ao menos uma vez por semana e orienta colocar o reciclável na rua apenas no dia da passagem do caminhão; pilhas, baterias, lâmpadas e eletrônicos devem ser devolvidos ao local de compra (PÁGINA 3, 2022). Em Camboriú, cada bairro tem um dia de coleta seletiva por semana, como a terça-feira para Monte Alegre, Santa Regina e Toca (CAMBORIÚ, 2023), e uma ação contra a dengue nos bairros Taboleiro e Monte Alegre identificou 150 terrenos baldios com problemas e recolheu 92 pneus e 37 televisores (CAMBORIÚ, 2021). O ecoponto municipal recebe pneus, baterias, eletrodomésticos e eletroeletrônicos, e pilhas e lâmpadas devem ser levadas ao comércio que as vende (CAMBORIÚ, 2017).

Quanto ao óleo de cozinha, o Tribunal de Justiça de Santa Catarina indica o programa Papaolito para Blumenau e Gaspar e não lista pontos de entrega em Itajaí, Balneário Camboriú, Brusque e Navegantes (SANTA CATARINA, [s.d.]). Em municípios catarinenses fora do Vale, estudos de percepção encontraram falta de conhecimento sobre o gerenciamento dos resíduos (CAMPOS; BORGA; SARTOREL, 2017), 60,2% dos entrevistados descartando o óleo na pia ou em outros lugares (SOUZA; CAMPOS; BORGA, 2017) e óleo guardado em garrafa PET que acaba no lixo orgânico por não haver onde descartá-lo (COLOMBO, 2022). No país, a coleta seletiva existe em cerca de 41% dos municípios e recolhe cerca de 10% do que é potencialmente reciclável (CONKE; NASCIMENTO, 2018).

Os relatos e os dados apontam dois padrões: o morador não sabe quando passa cada coleta nem o que separar, e faltam locais conhecidos para materiais específicos. O aplicativo foi desenhado para atender esses dois pontos.

**Decomposição do problema (pensamento computacional):** (i) falta de informação clara sobre o que e como separar; (ii) desconhecimento dos dias da coleta; (iii) ausência de pontos de descarte conhecidos para resíduos especiais; (iv) baixo engajamento da população mais jovem.

**Engenharia de requisitos:** os requisitos foram levantados a partir de observação e entrevistas com moradores e estão consolidados em requisitos funcionais, não funcionais e regras de negócio, que orientam os critérios de aceite e os testes.

## Definição Clara do Objetivo

O objetivo geral é desenvolver um aplicativo móvel para Android e iOS, orientado a testes, que informe aos moradores do Vale do Itajaí os dias de coleta seletiva e comum do seu município e setor, indique pontos de descarte de materiais especiais com filtro por material, oriente a separação correta dos resíduos, mesmo sem internet, e incentive o descarte correto com uma pontuação simples. O bairro Monte Alegre é o caso piloto, validado com moradores.

Os objetivos específicos são: definir regras de negócio testáveis; projetar o aplicativo para que municípios, setores, dias de coleta e pontos de descarte sejam dados cadastrados, sem alterar o código para incluir um novo município; implementar o módulo compartilhado com testes unitários e de integração; automatizar os testes na integração contínua; e validar a versão mínima com moradores.

## Delimitação do Escopo

O escopo é uma versão mínima funcional (MVP), o que deixa claro o que será e o que não será feito. O desenvolvimento orientado a testes é obrigatório: cada funcionalidade é testada automaticamente desde o início.

**Incluído no escopo:**

- **Município e setor:** o morador escolhe o município e o setor (bairro) de coleta entre os cadastrados, e o app guarda a escolha no aparelho. O MVP traz o piloto Monte Alegre e pelo menos mais um município, para demonstrar a cobertura regional.
- **Calendário de coleta:** dias da coleta seletiva e da coleta comum do setor, com regra de feriado (a coleta não tem horário fixo de passagem).
- **Lembrete:** notificação na véspera da coleta, em horário escolhido pelo usuário (item de menor prioridade).
- **Pontos de descarte:** lista do município por tipo de material (pilhas, óleo, eletrônicos, roupas), com filtro por material e localização do ponto, em dados de demonstração.
- **Guia de separação:** busca por item com a orientação de descarte, disponível sem internet.
- **Pontuação simples e histórico:** o morador registra um descarte pelo tipo de material e recebe pontos conforme o tipo, com limite diário; o app mostra saldo e histórico.
- **Dicas de reciclagem:** conteúdo informativo exibido no app.
- **Dados cadastráveis:** municípios, setores, dias de coleta e pontos ficam em dados locais; incluir um município não exige alterar o código.
- Armazenamento local, testes unitários, de integração e de interface em cada funcionalidade, para Android e iOS.

**Excluído do escopo:**

- Ranking e competições entre ruas ou condomínios.
- Marketplace de recompensas e parcerias com o comércio local.
- Validação automática do descarte (foto com inteligência artificial, QR Code ou GPS): a pontuação é autodeclarada e limitada por dia.
- Painel administrativo para cadastro de pontos e cronogramas e relato de problemas com foto.
- Rastreamento em tempo real dos caminhões, notificações por servidor e funcionalidades de comunicação (chat, fórum).
- Cobertura automática de todos os municípios do Vale do Itajaí: o MVP cadastra um conjunto inicial, e os demais entram por cadastro de dados.
- Suporte a outras plataformas além de Android e iOS.
- Testes manuais extensivos: o foco são os testes automatizados.

Como restrição, a equipe não dispõe de computador Mac; os testes de iOS serão executados em simulador, na integração contínua em nuvem, abordagem autorizada pelo professor.

## Identificação dos Stakeholders da Comunidade

Os principais envolvidos, com seu papel, interesse, nível de poder e de interesse e estratégia de engajamento, estão na Tabela 1.

| Stakeholder | Papel no projeto | Interesse principal | Poder | Interesse | Estratégia de engajamento |
|---|---|---|---|---|---|
| Moradores do Vale do Itajaí (piloto: bairro Monte Alegre) | Usuários finais do aplicativo | Saber os dias de coleta, onde descartar e como separar | Baixo | Alto | Manter informados e envolvidos: validação com moradores e canal de sugestões |
| Prefeituras e órgãos de gestão ambiental dos municípios | Responsáveis pela gestão de resíduos e pela coleta seletiva | Aumentar a reciclagem, promover educação ambiental e reduzir custos | Alto | Alto | Gerenciar de perto: apresentar o projeto e conferir dias de coleta e pontos |
| Empresas de coleta | Executam a coleta e definem os dias | Eficiência da operação e dados da comunidade | Alto | Médio | Manter satisfeitas: validar os dias de coleta usados no app |
| Cooperativas de catadores, lideranças comunitárias e ONGs locais | Triam os recicláveis e ajudam a divulgar o uso do aplicativo (ex.: Cooperfoz e Reciclavale, em Itajaí) | Receber material limpo e separado, com condições de trabalho adequadas | Médio | Alto | Manter informados: orientar a separação correta pelo guia e abrir canal de sugestões |
| Comerciantes do bairro | Potenciais parceiros em evoluções futuras | Aproximar clientes e associar a marca à sustentabilidade | Médio | Médio | Manter informados sobre os resultados do MVP |
| Equipe do projeto e professor | Desenvolvem, avaliam e orientam | Entregar um aplicativo testado e documentado | Alto | Alto | Reuniões de sprint e entregas por etapa |

> Tabela 1 – Stakeholders. Fonte: elaborado pelos autores (2026).

## Atividades e Tarefas Principais

As atividades seguem o ciclo do desenvolvimento orientado a testes: escrever o teste, vê-lo falhar, implementar o código mínimo, refatorar e executar os testes de regressão. As principais atividades são:

- **Levantamento de requisitos:** reuso da pesquisa de campo do HOW IV e conferência dos dias de coleta e dos pontos de descarte de cada município cadastrado.
- **Especificação de testes:** critérios de aceite escritos antes da implementação de cada funcionalidade.
- **Desenvolvimento:** regras de negócio no módulo compartilhado, armazenamento local e telas.
- **Refatoração:** melhoria do código mantendo os testes aprovados.
- **Testes de integração e de interface:** repositório local, cenário sem internet e testes de tela no Android e no iOS.
- **Validação:** teste de usabilidade com moradores e ajustes finais.

## Ferramentas de Desenvolvimento e Teste

Foram escolhidas ferramentas adequadas ao desenvolvimento orientado a testes em Android e iOS:

- **Android Studio e Kotlin Multiplatform:** desenvolvimento do módulo compartilhado e da interface.
- **Xcode (executado na integração contínua):** compilação e testes do iOS em macOS na nuvem.
- **JUnit, kotlin.test e Mockito:** testes unitários; no código compartilhado, dublês escritos à mão.
- **Testes de UI do Compose (sobre o Espresso) e XCTest:** testes de interface no Android e testes de fumaça no iOS.
- **SQLite:** armazenamento local dos dados do aplicativo, para uso sem internet.
- **GitHub e GitHub Actions:** controle de versão e integração contínua, com execução automática dos testes.
- **Trello:** gestão do Scrum (product backlog, releases e sprints), usado também no HOW IV.

## Métricas de Sucesso

As métricas de sucesso permitem avaliar se o projeto atinge seus objetivos:

- **Cobertura de testes:** 70% ou mais no código das regras de negócio.
- **Integração contínua:** testes aprovados a cada alteração enviada ao repositório.
- **Alcance regional:** 2 ou mais municípios cadastrados no MVP, incluindo o piloto Monte Alegre.
- **Adoção:** 10 ou mais moradores testando a versão mínima.
- **Satisfação:** nota média de usabilidade igual ou superior a 4 em uma escala de 1 a 5.
- **Efeito esperado:** aumento do percentual de moradores que sabem os dias de coleta e os pontos de descarte, medido antes e depois do uso.

## Cronograma e Recursos

O trabalho usa sprints de duração fixa de duas semanas. As datas da Etapa 2 são provisórias até a confirmação do prazo pelo professor.

| Sprint | Período | Release | Entrega |
|---|---|---|---|
| Sprint 1 | 12/10 a 25/10 | Release 1 | Relatório e vídeo da Etapa 1, escopo, Scrum configurado e ambiente de desenvolvimento |
| Sprint 2 | 26/10 a 08/11 | Release 2 | Base do aplicativo, município e setor, e calendário de coleta, com testes |
| Sprint 3 | 09/11 a 22/11 | Release 2 | Pontos de descarte do município com filtro e localização, pontuação simples e histórico, com testes de interface |
| Sprint 4 | 23/11 a 06/12 | Release 2 | Guia de separação, dicas de reciclagem, lembrete, validação, relatório e vídeo da Etapa 2 |

> Tabela 2 – Cronograma por sprint. Fonte: elaborado pelos autores (2026).

Os recursos humanos são cinco integrantes, com papéis de Scrum Master, Product Owner, Redator, Editor e Time de Desenvolvimento.

Os recursos tecnológicos são ferramentas gratuitas (Android Studio, GitHub, Trello), sem orçamento financeiro previsto. A disponibilidade de execução em macOS na integração contínua será confirmada na política vigente do GitHub.
