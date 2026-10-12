# Como usar o Git neste projeto

Somos 5 e ninguém tinha rotina de Git em equipe, então o fluxo é simples de propósito.

## Regras

1. **Ninguém commita direto na `main`.** Todo trabalho vai em uma branch e entra por Pull Request (PR).
2. **Um PR é revisado por outra pessoa** antes de entrar. Pode ser rápido (5 minutos).
3. **Branch pequena e curta:** uma tarefa, uma branch, de preferência fechada em 1 ou 2 dias.
4. **Atualize antes de começar:** `git pull` na `main` antes de criar a branch.

## Nome da branch

`tipo/area-resumo`, por exemplo:

- `docs/escopo-ajuste-rn`
- `feat/calendario-tela`
- `test/calendario-regras`
- `chore/ambiente-gradle`

## Mensagens de commit

Em português, no imperativo, começando pelo tipo:

```
docs: ajusta regras de negócio do escopo
test: cobre coleta em feriado
feat: calcula próxima coleta do setor
fix: corrige filtro de pontos por material
```

No TDD, o commit `test:` (teste falhando) vem antes do `feat:` (código que faz passar).

## Passo a passo

```bash
git checkout main
git pull
git checkout -b docs/escopo-ajuste-rn
# faça as alterações
git add .
git commit -m "docs: ajusta regras de negócio do escopo"
git push -u origin docs/escopo-ajuste-rn
```

Depois abra o PR no GitHub, marque outra pessoa para revisar e avise no grupo.

## O que não vai para o repositório

- Senhas, chaves de API e arquivos `local.properties` (o `.gitignore` já cobre os mais comuns).
- Dados pessoais de qualquer morador entrevistado.
- Arquivos pesados de vídeo.

## Dúvidas

Pergunte no grupo antes de usar `git push --force` ou `git reset --hard`.
