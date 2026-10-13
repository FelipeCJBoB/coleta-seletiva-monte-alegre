# Escopo do MVP

Recorte aprovado pelo grupo a partir do projeto do HOW IV. A coluna "HOW IV" mostra de onde cada item vem, para o relatório e os testes ficarem rastreáveis.

## Narrativa: do HOW IV ao HOW VIII

- **HOW IV:** pesquisa de campo no bairro **Monte Alegre**, tratado como piloto. A expansão geográfica ficou registrada como exclusão ("fase futura").
- **HOW VIII:** a fase futura entra no escopo como **cobertura regional por dados**: o app atende o **Vale do Itajaí**, com municípios, setores, dias de coleta e pontos cadastrados como dados. O Monte Alegre continua sendo o caso piloto validado com moradores.
- **Por que dados e não código:** dias de coleta e pontos variam por município (e até por bairro). Isso é testável: o teste cadastra um município novo e confere o calendário sem alterar o código.

## Problema

Moradores não sabem os dias da coleta (principalmente os mais jovens), descartam pilhas e óleo de cozinha no lixo comum ou na pia, não separam orgânico de reciclável e não conhecem pontos de descarte para materiais específicos. A pesquisa de campo (HOW IV) e as fontes públicas levantadas ([PESQUISA.md](PESQUISA.md)) apontam o mesmo padrão.

## Requisitos funcionais do MVP

| ID | Requisito | HOW IV | Prioridade |
|---|---|---|---|
| RF01 | O usuário escolhe o município e o setor (bairro) de coleta entre os cadastrados e o app guarda a escolha no aparelho | RF1 (generalizado) | Alta |
| RF02 | O app lembra o usuário (notificação) na véspera da coleta, em horário escolhido por ele | RF2 | Baixa (primeiro a sair se faltar tempo) |
| RF03 | O app mostra calendário com os dias das coletas seletiva e comum do setor (a coleta não tem horário fixo) | RF3 | Alta |
| RF04 | O app lista os pontos de descarte do município e mostra, para cada um, endereço, horário e materiais aceitos | RF5 | Alta |
| RF05 | O app mostra a localização do ponto (coordenadas) e permite abrir a rota no app de mapas do aparelho | RF5, RF8 | Média |
| RF06 | Os pontos são categorizados por tipo de material (pilhas, óleo, eletrônicos, roupas) | RF6 | Alta |
| RF07 | O usuário filtra os pontos por tipo de material | RF7 | Alta |
| RF08 | O app oferece guia de separação pesquisável (ex.: "caixa de leite") com a orientação de descarte | RF10, RF11 | Alta |
| RF09 | O usuário registra um descarte informando o tipo de material, e o app credita pontos conforme o tipo, respeitando o limite diário | pontuação (RN002, RN006) | Média |
| RF10 | O app mostra o saldo de pontos e o histórico de descartes registrados | feedback visual | Média |
| RF11 | O app exibe dicas de reciclagem e informações ambientais | RF14 | Baixa |

## Requisitos não funcionais mantidos

| ID | Requisito | HOW IV |
|---|---|---|
| RNF01 | Chegar a calendário, pontos e guia em no máximo 2 toques a partir da tela inicial | RNF3 |
| RNF02 | Funcionar em Android 9 ou superior e iOS 14 ou superior | RNF4 |
| RNF03 | O guia de separação funciona sem internet | RNF6 |
| RNF04 | A lista de pontos aparece em até 3 segundos em rede 4G | RNF1 |
| RNF05 | Incluir um município, setor ou ponto exige apenas cadastrar dados, sem alterar o código (novo, da cobertura regional) | novo |

## Regras de negócio mantidas

| ID | Regra | HOW IV |
|---|---|---|
| RN01 | Os dias da coleta seletiva vêm do cadastro do setor; não há horário fixo de passagem do caminhão. Piloto Monte Alegre: terças-feiras, segundo a Prefeitura de Camboriú (2023) | RN1 (horário removido, D-01) |
| RN02 | Os dias da coleta comum vêm do cadastro do setor, também sem horário fixo | RN2 (horário removido, D-01) |
| RN03 | Em feriados nacionais não há coleta; ela passa para o próximo dia útil | RN3 |
| RN04 | Pilhas, baterias e óleo de cozinha usado só vão para pontos de descarte ou comércio, nunca para a coleta porta a porta | RN6 |
| RN05 | Cada ponto de descarte informa o seu horário de funcionamento e os materiais aceitos (com limites, ex.: eletrônicos até 5 kg) | RN7, RN8 |
| RN06 | O serviço atende somente municípios e setores cadastrados nos dados do app | RN9 (generalizado) |
| RN07 | O município e o setor do usuário ficam só no aparelho e não são exibidos ou compartilhados | RN11 |
| RN08 | Cada registro de descarte vale pontos conforme o tipo de material. Valores iniciais (ajustáveis nos dados): papel, plástico, metal e vidro = 5; pilhas, baterias e óleo de cozinha = 10; eletrônicos = 15 | RN002 |
| RN09 | Cada usuário pode registrar no máximo 3 descartes por dia; acima disso o app avisa e não credita pontos | RN006 |

As regras RN4 (responsabilidade pela separação) e RN5 (horário para colocar o lixo na calçada) do HOW IV viram **conteúdo do guia**, não regra de sistema.

## Dados do app

Municípios, setores, dias de coleta, pontos e itens do guia são **dados de demonstração**, identificados como tal no app e no relatório (decisão D-04). O piloto Monte Alegre usa como referência a fonte oficial da Prefeitura de Camboriú (2023); os demais municípios do MVP são fictícios. O MVP cadastra o piloto e pelo menos mais um município.

## Fora do escopo (decidido)

Marketplace de recompensas, ranking e competições, validação automática do descarte (foto com IA, QR Code ou GPS), backoffice administrativo, relato de problemas com foto, notificações push via servidor, cobertura automática de todos os municípios do Vale (os demais entram por cadastro de dados).

A lista completa, com esforço e o que o grupo aprovou trazer de volta (pontuação simples, histórico e dicas), está em [FORA-DO-ESCOPO.md](FORA-DO-ESCOPO.md).

**Limitação assumida:** sem QR Code, GPS ou foto, o registro de descarte é **autodeclarado**. O app confia no usuário e usa o limite diário (RN09) como contenção; a validação automática é evolução futura.

## Casos de uso (apoio aos testes)

Não são uma seção exigida na Etapa 2 do HOW VIII (lá o foco é aplicação, testes e validação). Servem de base para escrever os testes e os critérios de aceite.

| ID | Caso de uso | Ator |
|---|---|---|
| CU01 | Escolher município e setor | Morador |
| CU02 | Consultar calendário de coleta | Morador |
| CU03 | Consultar pontos de descarte (com filtro) | Morador |
| CU04 | Consultar guia de separação | Morador |
| CU05 | Configurar lembrete de coleta | Morador |
| CU06 | Registrar descarte | Morador |
| CU07 | Consultar saldo e histórico de pontos | Morador |
| CU08 | Ver dicas de reciclagem | Morador |

Como os dados ficam no aparelho e não há administração pelo app, o único ator é o **Morador**. O Parceiro Comercial e o Administrador do HOW IV saem junto com o marketplace e o backoffice.
