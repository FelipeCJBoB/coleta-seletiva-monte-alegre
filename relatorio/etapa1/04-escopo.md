<!-- Dono: Integrante 2 (Product Owner); 4.1.6 revisada pelo Integrante 5. Seção 4 (Etapa 1). Mantenha igual a docs/ESCOPO.md. -->

## Etapa 1

Esta seção apresenta os resultados parciais do projeto: o problema, o objetivo, o escopo, os envolvidos, as atividades, as ferramentas, as métricas e o cronograma.

## Definição do Escopo do Projeto

O projeto tem como tema a gestão de resíduos e a coleta seletiva no bairro Monte Alegre. A definição do escopo usa o pensamento computacional para decompor o problema e a engenharia de requisitos para alinhar a solução às necessidades dos moradores.

## Compreensão do Problema na Comunidade

A pesquisa de campo foi realizada no bairro Monte Alegre, com observação e entrevistas com moradores, para compreender a realidade local em relação aos resíduos e à coleta seletiva. Os moradores mais velhos conhecem melhor os dias em que o caminhão passa, enquanto os mais jovens têm menos informação, o que sugere falta de engajamento. Embora o caminhão cumpra os dias regulares, não há horário fixo de passagem, o que causa confusão e atrasos no descarte.

O descarte incorreto em ruas e terrenos baldios é comum, com acúmulo de sujeira, mau cheiro e proliferação de insetos. Todos os entrevistados desconhecem locais adequados para óleo de cozinha, pilhas e baterias: a maioria descarta pilhas e baterias no lixo comum e o óleo na pia ou na terra. Nenhum separa orgânico de reciclável.

O principal problema é, portanto, a falta de informação e de estrutura local para a destinação correta dos resíduos, sobretudo entre o público mais jovem.

**Decomposição do problema (pensamento computacional):** (i) falta de informação clara sobre o que e como separar; (ii) desconhecimento dos dias da coleta; (iii) ausência de pontos de descarte conhecidos para resíduos especiais; (iv) baixo engajamento da população mais jovem.

**Engenharia de requisitos:** os requisitos foram levantados a partir de observação e entrevistas com moradores e estão consolidados em requisitos funcionais, não funcionais e regras de negócio, que orientam os critérios de aceite e os testes.

## Definição Clara do Objetivo

O objetivo geral é desenvolver um aplicativo móvel para Android e iOS, orientado a testes, que informe aos moradores do bairro Monte Alegre os dias de coleta seletiva e comum do seu setor, indique pontos de descarte de materiais especiais com filtro por material e oriente a separação correta dos resíduos, mesmo sem internet.

Os objetivos específicos são: definir regras de negócio testáveis; implementar o módulo compartilhado com testes unitários e de integração; automatizar os testes na integração contínua; e validar a versão mínima com moradores.

## Delimitação do Escopo

O escopo é uma versão mínima funcional (MVP), o que deixa claro o que será e o que não será feito. O desenvolvimento orientado a testes é obrigatório: cada funcionalidade é testada automaticamente desde o início.

**Incluído no escopo:**

- **Endereço/setor:** o morador escolhe seu setor de coleta, restrito ao bairro Monte Alegre, e o app o guarda no aparelho.
- **Calendário de coleta:** dias da coleta seletiva e da coleta comum do setor, com regra de feriado (a coleta não tem horário fixo).
- **Lembrete:** notificação na véspera da coleta, em horário escolhido pelo usuário (item de menor prioridade).
- **Pontos de descarte:** lista por tipo de material (pilhas, óleo, eletrônicos, roupas), com filtro por material e localização do ponto, em dados de demonstração.
- **Guia de separação:** busca por item com a orientação de descarte, disponível sem internet.
- Armazenamento local, testes unitários, de integração e de interface em cada funcionalidade, para Android e iOS.

**Excluído do escopo:**

- Pontuação por ações, ranking e competições entre ruas ou condomínios.
- Marketplace de recompensas e parcerias com o comércio local.
- Validação do descarte por foto com inteligência artificial e check-in por QR Code ou GPS.
- Painel administrativo para cadastro de pontos e cronogramas e relato de problemas com foto.
- Rastreamento em tempo real dos caminhões, notificações por servidor e funcionalidades de comunicação (chat, fórum).
- Cobertura de outros bairros.

Como restrição, a equipe não dispõe de computador Mac; os testes de iOS serão executados em simulador, na integração contínua em nuvem, abordagem autorizada pelo professor.

## Identificação dos Stakeholders da Comunidade

Os principais envolvidos, com seu papel, interesse, nível de poder e de interesse e estratégia de engajamento, estão na Tabela 1.

| Stakeholder | Papel no projeto | Interesse principal | Poder | Interesse | Estratégia de engajamento |
|---|---|---|---|---|---|
| Moradores do bairro Monte Alegre | Usuários finais do aplicativo | Saber os dias de coleta, onde descartar e como separar | Baixo | Alto | Manter informados e envolvidos: validação com moradores e canal de sugestões |
| Prefeitura / órgão de gestão ambiental | Responsável pela gestão de resíduos e pela coleta seletiva | Aumentar a reciclagem, promover educação ambiental e reduzir custos | Alto | Alto | Gerenciar de perto: apresentar o projeto e os dados do bairro |
| Empresa de coleta | Executa a coleta e define os dias | Eficiência da operação e dados da comunidade | Alto | Médio | Manter satisfeita: validar os dias de coleta usados no app |
| Comerciantes do bairro | Potenciais parceiros em evoluções futuras | Aproximar clientes e associar a marca à sustentabilidade | Médio | Médio | Manter informados sobre os resultados do MVP |
| Equipe do projeto e professor | Desenvolvem, avaliam e orientam | Entregar um aplicativo testado e documentado | Alto | Alto | Reuniões de sprint e entregas por etapa |

> Tabela 1 – Stakeholders. Fonte: elaborado pelos autores (2026).

## Atividades e Tarefas Principais

As atividades seguem o ciclo do desenvolvimento orientado a testes: escrever o teste, vê-lo falhar, implementar o código mínimo, refatorar e executar os testes de regressão. As principais atividades são:

- **Levantamento de requisitos:** reuso da pesquisa de campo do HOW IV, conferência dos dias de coleta e dos pontos de descarte.
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
- **Adoção:** 10 ou mais moradores testando a versão mínima.
- **Satisfação:** nota média de usabilidade igual ou superior a 4 em uma escala de 1 a 5.
- **Efeito esperado:** aumento do percentual de moradores que sabem os dias de coleta e os pontos de descarte, medido antes e depois do uso.

## Cronograma e Recursos

O trabalho usa sprints de duração fixa de duas semanas. As datas da Etapa 2 são provisórias até a confirmação do prazo pelo professor.

| Sprint | Período | Release | Entrega |
|---|---|---|---|
| Sprint 1 | 12/10 a 25/10 | Release 1 | Relatório e vídeo da Etapa 1, escopo, Scrum configurado e ambiente de desenvolvimento |
| Sprint 2 | 26/10 a 08/11 | Release 2 | Base do aplicativo, endereço/setor e calendário de coleta, com testes |
| Sprint 3 | 09/11 a 22/11 | Release 2 | Pontos de descarte com filtro e localização, com testes de interface |
| Sprint 4 | 23/11 a 06/12 | Release 2 | Guia de separação, lembrete, validação, relatório e vídeo da Etapa 2 |

> Tabela 2 – Cronograma por sprint. Fonte: elaborado pelos autores (2026).

Os recursos humanos são cinco integrantes, com papéis de Scrum Master, Product Owner, Redator, Editor e Time de Desenvolvimento.

Os recursos tecnológicos são ferramentas gratuitas (Android Studio, GitHub, Trello), sem orçamento financeiro previsto. A disponibilidade de execução em macOS na integração contínua será confirmada na política vigente do GitHub.
