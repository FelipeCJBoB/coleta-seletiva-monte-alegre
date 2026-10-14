# Plano do vídeo da Etapa 1 no Google Flow: Agente em modo automático

Documento de execução do Integrante 4 (Editor). Uma única mensagem ao Agente faz a trilha visual de ponta a ponta. A visão geral e a metodologia estão em [PLANO-VIDEO-ETAPA1.md](PLANO-VIDEO-ETAPA1.md).

## 1. Decisão: modelo de vídeo

**Veo 3.1 Lite** para todos os clipes. Verifiquei na documentação do Flow e em guias de terceiros:

| Ponto | O que existe |
|---|---|
| "Segregar" ou segmentar vídeos | **Não encontrei** esse recurso no Lite nem em outro modelo. O que existe é o limite de duração: o Lite gera clipes de 4, 6 ou 8 s, então a segmentação é feita pelo **roteiro**, em clipes de 8 s |
| Custo | É a opção mais barata da família Veo 3.1 (menos da metade do Fast, segundo o Google). Em fontes de terceiros, cerca de **10 créditos por geração**, independente de ser 4 ou 8 s, por isso usar sempre 8 s |
| Continuidade | Frames para Vídeo (primeiro quadro; primeiro e último) e **extensão**: só o Lite estende clipes de 8 s |
| Áudio | Gera **som ambiente nativo**; não dá para garantir clipe mudo. A narração gravada substitui o áudio no editor |
| Limites | Edição vídeo para vídeo não é suportada; referências só com 8 s |

**Alternativa mais barata, se o crédito apertar:** Gemini Omni Flash 1.1 em rascunho 360p (metade do custo do 720p) com ampliação gratuita para 720p no plano Pro. Não usei como padrão por ser menos previsível em modo automático, e porque o preço do Omni também varia conforme a fonte.

**Orçamento:** 15 clipes x 10 créditos = **cerca de 150 créditos** (valor de terceiros; conferir no teste da seção 4). As cenas 6 e 7 do roteiro (cartão de resultados e prints do Trello) são feitas no editor e não gastam crédito do Flow.

## 2. Configuração (sem instruções do agente)

Em **Agente > Configurações**:

| Item | Valor |
|---|---|
| Confirmar antes de gerar | **Nunca** (modo automático) |
| Imagens | 16:9, **x1**, Nano Banana 2.1 |
| Vídeo | 16:9, **x1**, **Veo 3.1 - Lite** |

Não adicionar nada em "Instruções para o agente": o prompt da seção 3 já é autossuficiente.

**Atenção:** em "Nunca", o Agente gasta créditos sem perguntar. Por isso o prompt traz limites (15 clipes, 1 refação por clipe, parar se faltar crédito) e a execução de teste da seção 4.

## 3. Prompt único (colar inteiro na caixa do Agente)

```text
ESCOPO DESTA EXECUÇÃO: todos os 15 clipes (C01 a C15)

MISSÃO
Produza, sozinho e do começo ao fim, a trilha visual de um vídeo de apresentação acadêmica de cerca de 2 minutos e 30 segundos sobre o projeto "Coleta Seletiva Vale do Itajaí" (disciplina HOW VIII, Univali). A narração será gravada por uma pessoa, à parte. Eu só preciso dos CLIPES. Não peça confirmação nem esclarecimentos: decida e execute.

REGRAS GLOBAIS (valem para todos os clipes)
- Modelo de vídeo: Veo 3.1 Lite. Proporção 16:9. 8 segundos por clipe. 1 saída por clipe.
- Estilo: foto-realista, luz natural, lente 35 mm, profundidade de campo rasa, estilo documental espontâneo, cores neutras. Cenário: Vale do Itajaí, Santa Catarina, Brasil.
- Proibido dentro de qualquer vídeo ou imagem: texto, letras, números, logotipos, marcas d'água e interface de aplicativo. Telas de celular sempre em branco ou fora de quadro. Sem pessoas reais identificáveis e sem marcas.
- Sem fala e sem música. Apenas som ambiente leve.
- Um plano contínuo por clipe, com câmera lenta e estável e movimento natural sutil.
- Continuidade dentro da mesma cena: mesmas pessoas, roupas e ambiente. Quando fizer sentido, use o último quadro do clipe anterior como primeiro quadro do seguinte (Frames para Vídeo).

ORÇAMENTO E AUTONOMIA
- Gere exatamente os clipes listados, nenhum a mais, e sem variações.
- Se uma geração falhar ou violar as regras, refaça no máximo 1 vez.
- Não gere imagens avulsas, a não ser para servir de primeiro quadro.
- Se faltar crédito, pare e liste o que ficou pendente.

ORGANIZAÇÃO
- Crie a Collection "Etapa 1 - Video" e coloque nela todos os clipes.
- Nomeie na ordem, com a cena: C01_cena1, C02_cena1, C03_cena2, e assim por diante.
- Se for possível, monte uma Scene com os clipes na ordem C01 a C15. Se não for, deixe-os apenas nomeados e ordenados.

CLIPES
Cena 1 (gancho)
C01: Early morning on a residential street in a coastal town in southern Brazil. A woman in her 40s stands beside two recycling bins and one regular trash bin, looking at her phone with a doubtful expression. Slow push-in.
C02: Same woman and street. She looks from the phone to the bins and then up the street, unsure. Slow lateral slide.

Cena 2 (origem)
C03: Five university students around a table with laptops and notebooks in a bright classroom, discussing a project. The laptop screens face away from the camera. Slow push-in.
C04: Same classroom. Close shots of hands writing in a notebook and typing on a laptop, screens not visible. Slow lateral slide.

Cena 3 (problema)
C05: Close-up of used AA batteries and an unlabeled plastic bottle of used cooking oil beside a kitchen sink. Slow lateral slide with a gentle focus shift.
C06: Close-up of a hand pouring cooking oil from an unlabeled bottle into a kitchen sink drain, no face visible. Slow push-in.
C07: Close-up of an open trash bag with mixed organic waste, plastic bottles and cartons together, no labels visible. Slow push-in.

Cena 4 (solução)
C08: Two hands holding a smartphone with a plain blank light-gray screen on an urban sidewalk, blurred street behind. Slow push-in.
C09: A person walking along a tidy residential street, glancing at a smartphone whose screen is not visible, recycling bins at the curb. Slow tracking shot from the side.
C10: A person at a kitchen table with a blank-screen smartphone beside a small sorting bin for plastic, paper and glass. Slow lateral slide.

Cena 5 (diferencial)
C11: Aerial drone shot of a river city in Santa Catarina, Brazil, with a bridge, port cranes and green hills at golden hour. Slow forward glide.
C12: Aerial view of a smaller riverside town in the same region at golden hour, rooftops and green hills, different from C11. Slow forward glide.

Cena 8 (encerramento)
C13: Five university students gathered around a table in a bright classroom. One holds a smartphone while the others take notes. The phone screen is not visible. Slow orbit.
C14: Close-up of a student's hands marking items on a paper checklist while another taps a phone whose screen is hidden. Slow lateral slide.
C15: Wide shot of the five students smiling and closing their notebooks, natural light through the window. Slow pull-back.

ENTREGA
Ao terminar, responda só com uma tabela: clipe, cena, status (ok, refeito ou pendente) e créditos gastos, se o Flow informar.
```

## 4. Teste antes da execução completa

Para limitar o risco no modo automático, rode **a mesma mensagem** trocando só a primeira linha por:

```text
ESCOPO DESTA EXECUÇÃO: somente C01 e C02. Ignore os demais clipes.
```

Confira:

- [ ] Os 2 clipes têm 8 s, 16:9 e estilo foto-realista.
- [ ] Não há texto, logotipo nem interface de app na imagem.
- [ ] A mulher é a mesma nos dois clipes (continuidade).
- [ ] O custo por clipe e o saldo restante, como o Flow mostrar.
- [ ] O Agente criou a Collection e os nomes C01_cena1 e C02_cena1.

Se estiver bom, volte a primeira linha para "todos os 15 clipes (C01 a C15)" e rode de novo (C01 e C02 podem ser reaproveitados: peça para começar do C03).

## 5. Se o Agente parar no meio

```text
Continue de onde parou: gere apenas os clipes que ainda não existem na Collection "Etapa 1 - Video", seguindo as mesmas regras globais, e termine com a tabela de entrega.
```

## 6. Depois do Agente (editor)

1. **Montagem:** baixar a Scene (ou os clipes, ordenados) e importar no editor (CapCut, Clipchamp ou DaVinci).
2. **Áudio:** silenciar o som ambiente dos clipes e colocar a narração do Integrante 4 (2 tomadas por cena).
3. **Cenas 6 e 7:** montar no editor: cartão com os 6 resultados e os prints reais do Trello (Figuras 1 e 2 do relatório) com zoom.
4. **Texto na tela** (só palavras-chave, números e fontes): "DIARINHO, 2024" e "Informe Blumenau, 2020: 45%" (cena 3); "Município e setor, Calendário, Pontos de descarte, Guia offline, Pontos e dicas" (cena 4); "17 itens, 2 releases, 4 sprints" (cena 7); cartão final com nome do projeto, disciplina e e-mails dos 5 integrantes (a partir do `autores.local.md`).
5. **Esboços de tela do app** (cena 4): desenhar 5 telas no editor para entrar sobre os clipes C08 a C10.
6. **Legendas pt-BR:** até 42 caracteres por linha, 2 linhas, até 17 caracteres por segundo; revisar nomes e números.
7. **Exportar** em 1080p, 16:9, MP4, com no máximo 3:00; publicar como **Não listado**; colocar o link na seção 7.1 e no campo de texto do envio.

## 7. Mapa cena a cena (para o editor)

Narração de 314 palavras, falada pelo Integrante 4.

| Cena | Tempo | Narração | Clipes do Flow | Feito no editor |
|---|---|---|---|---|
| 1. Gancho | 0:00 a 0:12 | "Você sabe qual é o dia da coleta seletiva da sua rua? E onde descartar pilhas e óleo de cozinha? Muita gente no Vale do Itajaí não sabe." (28) | C01, C02 | Zoom lento, corte no tempo da fala |
| 2. Origem | 0:12 a 0:30 | "Somos um grupo da Univali. No HOW IV, fizemos uma pesquisa de campo com moradores. Agora, no HOW VIII, transformamos essa ideia em um projeto: Coleta Seletiva Vale do Itajaí." (31) | C03, C04 | Cartão-título do projeto |
| 3. Problema | 0:30 a 1:00 | "A pesquisa mostrou três problemas: moradores que não sabem os dias da coleta, pilhas e óleo no lixo comum ou na pia, e nenhum entrevistado separando o orgânico do reciclável. E o padrão aparece na região. Em Itajaí, em 2024, moradores relataram que o caminhão nem sempre passava no dia previsto. Em Blumenau, um levantamento de 2020 apontou que quase metade do reciclável chegava contaminado." (65) | C05, C06, C07 | Fontes em texto; destaque no 45% |
| 4. Solução | 1:00 a 1:30 | "Nossa solução é um aplicativo para Android e iOS. O morador vai escolher o município e o setor, ver os dias de coleta, encontrar pontos de descarte por tipo de material, consultar um guia de separação que funciona sem internet, registrar descartes para ganhar pontos e receber dicas de reciclagem." (50) | C08, C09, C10 | 5 esboços de tela entrando no ritmo da fala |
| 5. Diferencial | 1:30 a 1:45 | "O diferencial é a abrangência regional: municípios, setores e pontos serão dados cadastrados, então o aplicativo poderá crescer para outras cidades sem reescrever o código. E tudo será desenvolvido com testes escritos antes." (33) | C11, C12 | Pins no mapa (opcional) |
| 6. Resultados | 1:45 a 2:10 | "Na Etapa 1, entregamos o planejamento: o escopo da versão mínima e o que ficou de fora, os envolvidos, as atividades, as ferramentas, as métricas de sucesso e o cronograma em quatro sprints." (33) | nenhum | Cartão com os 6 resultados marcando um a um |
| 7. Scrum | 2:10 a 2:30 | "Configuramos o Scrum no Trello: um Product Backlog com dezessete itens, duas releases, quatro sprints e uma coluna de tarefas para cada integrante, divididas entre as duas etapas." (28) | nenhum | Prints do Trello com zoom nas listas |
| 8. Encerramento | 2:30 a 2:50 | "Na Etapa 2, vamos construir o aplicativo, escrever os testes antes do código e validar o resultado entre nós, com um roteiro de testes. O objetivo é que o morador saiba o dia certo e o lugar certo para cada resíduo. Coleta Seletiva Vale do Itajaí." (46) | C13, C14, C15 | Cartão final com os contatos |

## 8. Riscos

- **Gasto sem confirmação:** em "Nunca", o Agente não pede aval. Mitigação: limites no prompt e teste com 2 clipes.
- **Cota diária do Agente:** existe, mas o Google não informa o valor; se bater, use a mensagem da seção 5 no dia seguinte.
- **Texto, letras e interface:** modelos erram letras; o prompt proíbe e todo texto entra no editor.
- **Continuidade:** pessoas e cenários podem variar entre clipes; por isso o prompt pede "mesmas pessoas" e usa o último quadro como primeiro.
- **Áudio nativo do Lite:** não dá para evitar; é substituído pela narração no editor.
- **Scene automática:** o Agente pode não conseguir montar a Scene; nesse caso ordene pelos nomes C01 a C15.

## 9. Fontes

- Google Flow Help: *Use the Google Flow Agent* e *Learn about Google Flow models & supported features*.
- Google Blog: *Build with Veo 3.1 Lite, our most cost-effective video generation model*.
- Guias de terceiros sobre custo e extensão do Veo 3.1 Lite (valores a confirmar no Flow).
