# Relatório (fonte em Markdown)

O relatório mestre mora aqui (decisão D-03). Cada seção é um arquivo, com um dono, para evitar conflito no Git. O `.docx` e o PDF são **gerados** a partir destes arquivos.

## Donos

| Arquivo | Seção do template | Dono |
|---|---|---|
| `etapa1/00-cabecalho.md` | Título, resumo, abstract | Integrante 3 |
| `etapa1/01-introducao.md` | 1 Introdução | Integrante 3 |
| `etapa1/02-geracao-de-ideia.md` | 2 Geração de Ideia | Integrante 3 |
| `etapa1/03-prova-de-conceito.md` | 3 Prova de Conceito | Integrante 3 |
| `etapa1/04-escopo.md` | 4 Etapa 1 (4.1.1 a 4.1.8) | Integrante 2 (4.1.6 com Integrante 5) |
| `etapa1/06-scrum.md` | 6 SCRUM Configurado | Integrante 1 |
| `etapa1/07-video.md` | 7.1 Vídeo da Etapa 1 | Integrante 4 |
| `etapa1/08-conclusao.md` | 8 Conclusão | Integrante 3 |
| `etapa1/09-referencias.md` | 9 Referências | Integrante 3 |

A seção 5 (Etapa 2) e a 7.2 ficam só com o título até a Etapa 2.

## Como escrever

- Um bloco por seção, com o título exato do template: `## Definição Clara do Objetivo`.
- Parágrafos separados por linha em branco; listas com `- `; tabelas em Markdown; legenda com `> Tabela 1 – ...`.
- `**negrito**` e `[[pendência]]`: o trecho entre colchetes duplos sai destacado em amarelo no documento e precisa ser resolvido antes do envio.
- Comentários `<!-- ... -->` não vão para o documento.

## Como gerar o documento

Requer Python e `pip install python-docx`. O template do professor não está no repositório: use a sua cópia.

```bash
cp relatorio/autores.exemplo.md relatorio/autores.local.md   # preencha os nomes
python relatorio/build.py --template "caminho/instruções_de_elaboração.docx"
```

O arquivo sai em `relatorio/build/relatorio-etapa1.docx`. Abra no Word, confira e exporte o PDF.

`autores.local.md` e `build/` ficam fora do Git de propósito, para não publicar nomes e e-mails no repositório público.
