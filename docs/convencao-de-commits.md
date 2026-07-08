# 📐 Convenção de Commits (Conventional Commits)

Um histórico de commits bem escrito é documentação viva do projeto. O padrão
de mercado para isso é o [**Conventional Commits**](https://www.conventionalcommits.org/pt-br/),
usado por projetos como Angular, Vue, Electron e a grande maioria dos
repositórios profissionais que geram changelog automaticamente.

---

## 1. Estrutura da mensagem

```text
<tipo>(<escopo opcional>): <descrição curta no imperativo>

<corpo opcional explicando o "porquê">

<rodapé opcional, ex.: Fixes #12>
```

## 2. Tipos mais usados

| Tipo | Quando usar | Impacto em versão (SemVer) |
| :--- | :--- | :--- |
| `feat` | Uma nova funcionalidade para o usuário. | MINOR |
| `fix` | Correção de um bug. | PATCH |
| `docs` | Mudanças apenas em documentação. | — |
| `style` | Formatação, espaços, ponto e vírgula (sem mudar lógica). | — |
| `refactor` | Mudança de código que não corrige bug nem adiciona feature. | — |
| `perf` | Mudança que melhora performance. | PATCH |
| `test` | Adição ou correção de testes. | — |
| `build` | Mudanças no sistema de build ou dependências externas. | — |
| `ci` | Mudanças em arquivos e scripts de CI (ex.: GitHub Actions). | — |
| `chore` | Tarefas de manutenção que não afetam código de produção. | — |

Uma mudança com `!` depois do tipo (ex.: `feat!:`) ou um rodapé
`BREAKING CHANGE:` indica quebra de compatibilidade → versão MAJOR.

## 3. Exemplos reais

```text
feat: adicionar suporte a login com GitHub

fix(auth): corrigir expiração prematura do token de sessão

docs: adicionar guia de releases e versionamento semântico

chore: atualizar dependencias de desenvolvimento
```

## 4. Por que isso importa na prática

- **Changelog automático:** ferramentas como `semantic-release` ou
  `standard-version` leem os commits e geram o `CHANGELOG.md` sozinhas.
- **Versionamento automático:** o tipo do commit define se a próxima versão
  é PATCH, MINOR ou MAJOR (veja [docs/releases-e-versionamento.md](releases-e-versionamento.md)).
- **Histórico navegável:** `git log --oneline` vira uma lista legível de
  "o que mudou e por quê", em vez de mensagens genéricas como "ajustes" ou
  "correções diversas".

## 5. Dica de ferramenta

Para forçar o padrão automaticamente, projetos de mercado costumam usar o
[`commitlint`](https://commitlint.js.org/) com um hook de `commit-msg`
(via [Husky](https://typicode.github.io/husky/)), rejeitando commits que não
sigam a convenção antes mesmo de chegarem ao repositório remoto.
