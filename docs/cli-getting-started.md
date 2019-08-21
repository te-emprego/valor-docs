---
id: cli-getting-started
title: Iniciando com a CLI
sidebar_label: Iniciando com a CLI
---

O Valor conta com uma CLI embutida, que te auxilia a realizar algumas ações padrões dentro da estrutura.

## Gerando

A CLI pode te ajudar a gerar coisas dentro do padrão esperado pelo Valor. Com apenas 1 comando você pode gerar um módulo inteiro =)

### `generate:module`

O Comando `generate:module` gera um módulo inteiro com schema, interface, controller e testes de exemplo. É muito prático.

``` bash
node valor generate:module [-n <module-name>]
```

Exemplo de criação de módulo:
```
node valor generate:module -n customer
```

Lembre-se das boas práticas: módulos são sempre no singular. **O Valor não vai corrigir isso para você.**

**Obs:** Este comando usa o lodash para ajustar o case das palavras, então, independente do case inserido (e.g: `customer`, `Customer`, `multi-word-module`) ele sempre irá converter para `n => upperFist(camelCase(n))`.

### `generate:env`

**(em desenvolvimento, implementação em breve)**

O Comando `generate:env` gera todos os arquivos de ambiente com o schema esperado pela versão atual do Valor. É uma mão na roda para quem acabou de atualizar a versão ou acabou de baixar o projeto

``` bash
node valor generate:env [--clear]
```

Não se preocupe caso possua variáveis de ambiente customizadas. A menos que você passe a _flag_ `--clear`, o Valor sempre vai manter o que você tem, apenas acrescentando coisas novas ou te avisando caso você esteja usando algo depreciado.

A _flag_ `--clear` recria os arquivos de ambiente do zero. Serve muito bem para quem deseja resetar os arquivos de variáveis de ambiente para o padrão que o Valor espera.