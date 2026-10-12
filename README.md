# Coleta Seletiva Monte Alegre

Aplicativo móvel (Android e iOS) para ajudar os moradores do bairro **Monte Alegre, Itajaí/SC** a saber quando passa a coleta, onde descartar materiais específicos (pilhas, óleo de cozinha, eletrônicos) e como separar o lixo.

Projeto da disciplina **HOW VIII** (Análise e Desenvolvimento de Sistemas, UNIVALI). Continua o trabalho de pesquisa de campo feito no HOW IV, agora com desenvolvimento orientado a testes (TDD) e Scrum.

## Status

| Etapa | Entrega | Situação |
|---|---|---|
| Etapa 1 | Relatório (PDF), vídeo de até 3 min e Scrum configurado | em andamento, prazo 25/10/2026 |
| Etapa 2 | Requisitos, casos de uso e aplicativo com testes | a iniciar após a Etapa 1 |

## O que o app faz (MVP)

1. **Calendário de coleta** do endereço/setor do morador, com lembrete.
2. **Pontos de descarte** por tipo de material, com filtro.
3. **Guia de separação** pesquisável e disponível offline.

Detalhes e o que ficou de fora: [docs/ESCOPO.md](docs/ESCOPO.md).

## Como o time trabalha

- Plano completo, divisão entre os 5 integrantes e calendário: [docs/PLANO.md](docs/PLANO.md)
- Como usar o Git no projeto: [CONTRIBUINDO.md](CONTRIBUINDO.md)

## Tecnologia (planejada)

Kotlin Multiplatform + Compose Multiplatform, com lógica compartilhada entre Android e iOS, banco local SQLite, testes com JUnit/kotlin.test, Mockito (ou fakes) e testes de interface. O iOS é compilado e testado no CI em macOS, pois o grupo não tem Mac.

## Equipe

Cinco integrantes (Integrante 1 a 5). Os papéis estão em [docs/PLANO.md](docs/PLANO.md).
