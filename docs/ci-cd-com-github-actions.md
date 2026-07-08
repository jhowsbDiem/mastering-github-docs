# ⚙️ CI/CD com GitHub Actions

Um repositório profissional não confia apenas na revisão humana — ele usa
**Integração Contínua (CI)** para validar automaticamente cada mudança antes
dela chegar à `main`.

---

## 1. O que é o GitHub Actions

O [GitHub Actions](https://docs.github.com/actions) permite definir
*workflows* (arquivos YAML em `.github/workflows/`) que rodam automaticamente
em resposta a eventos do repositório, como um `push` ou a abertura de um
Pull Request.

## 2. O workflow deste repositório

Como este é um repositório de documentação, o CI aqui não compila código —
ele garante a **qualidade do conteúdo**. O workflow
[`.github/workflows/docs-lint.yml`](../.github/workflows/docs-lint.yml) roda
em todo `push` e Pull Request para a `main` e faz duas verificações:

1. **Lint de Markdown** com [`markdownlint-cli2`](https://github.com/DavidAnson/markdownlint-cli2):
   valida formatação, headings duplicados, listas mal formadas etc., usando
   as regras definidas em [`.markdownlint.jsonc`](../.markdownlint.jsonc).
2. **Checagem de links** com [`lychee`](https://github.com/lycheeverse/lychee-action):
   percorre todos os arquivos `.md` procurando links quebrados (o tipo de
   problema mais comum e mais fácil de passar despercebido em documentação).

Se qualquer uma das duas etapas falhar, o PR fica com o *status check*
vermelho — e, com [branch protection](estrategia-de-branches.md) configurada,
o botão de merge fica bloqueado até a correção.

## 3. Por que isso importa

- Elimina a necessidade de um humano lembrar de checar links manualmente.
- Garante um padrão mínimo de qualidade mesmo em contribuições externas.
- É a mesma filosofia usada em projetos de código: testes automatizados,
  linters e checagem de tipos rodando a cada mudança, antes do merge.

## 4. Mantendo o CI atualizado

As *actions* de terceiros usadas no workflow (`actions/checkout`,
`markdownlint-cli2-action`, `lychee-action`) são atualizadas automaticamente
via [Dependabot](../.github/dependabot.yml), que abre PRs semanais quando há
novas versões — a mesma prática usada para manter dependências de código em
dia.
