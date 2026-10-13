# Coleta Seletiva Vale do Itajaí

Aplicativo móvel (Android e iOS) para ajudar moradores do **Vale do Itajaí/SC** a saber quando passa a coleta, onde descartar materiais específicos (pilhas, óleo de cozinha, eletrônicos) e como separar o lixo. O bairro **Monte Alegre** é o caso piloto da pesquisa de campo.

Projeto da disciplina **HOW VIII** (Análise e Desenvolvimento de Sistemas, UNIVALI). Continua o trabalho de pesquisa de campo feito no HOW IV, que ficou limitado ao Monte Alegre e deixou a expansão como fase futura. Aqui essa fase entra no escopo, como cobertura regional por dados, e o desenvolvimento passa a ser orientado a testes (TDD) com Scrum.

## Status

| Etapa | Entrega | Situação |
|---|---|---|
| Etapa 1 | Relatório (PDF), vídeo de até 3 min e Scrum configurado | em andamento, prazo 25/10/2026 |
| Etapa 2 | Aplicativo mobile com testes (TDD), validação, relatório e vídeo | a iniciar após a Etapa 1 |

## O que o app faz (MVP)

1. **Calendário de coleta** do município e setor do morador, com lembrete.
2. **Pontos de descarte** do município por tipo de material, com filtro.
3. **Guia de separação** pesquisável e disponível offline.

Detalhes: [docs/ESCOPO.md](docs/ESCOPO.md). O que o app não vai conter, para reavaliação: [docs/FORA-DO-ESCOPO.md](docs/FORA-DO-ESCOPO.md).

## Como o time trabalha

- Plano completo, divisão entre os 5 integrantes e calendário: [docs/PLANO.md](docs/PLANO.md)
- Relatório (fonte em Markdown, uma seção por arquivo): [relatorio/README.md](relatorio/README.md)
- Fontes e dados levantados (secundários): [docs/PESQUISA.md](docs/PESQUISA.md)
- Product Backlog (cópia em Git do que está no Trello): [docs/BACKLOG.md](docs/BACKLOG.md)
- Como usar o Git no projeto: [CONTRIBUINDO.md](CONTRIBUINDO.md)
- Scrum no Trello (quadro privado do grupo): Product Backlog, Releases, Sprints e colunas por Integrante, divididas em Etapa 1 e Etapa 2.

## Tecnologia (planejada)

Kotlin Multiplatform + Compose Multiplatform, com lógica compartilhada entre Android e iOS, banco local SQLite, testes com JUnit/kotlin.test, Mockito (ou fakes) e testes de interface. O iOS é compilado e testado no CI em macOS, pois o grupo não tem Mac.

## Equipe

Cinco integrantes (Integrante 1 a 5). Os papéis estão em [docs/PLANO.md](docs/PLANO.md).
