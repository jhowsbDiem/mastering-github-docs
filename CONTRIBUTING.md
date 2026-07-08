# 🤝 Guia de Contribuição

Obrigado por considerar contribuir com este repositório! Como este projeto
existe justamente para ensinar boas práticas de versionamento, esperamos que
as contribuições sigam o mesmo padrão profissional que ensinamos aqui.
Antes de contribuir, leia também o nosso [Código de Conduta](CODE_OF_CONDUCT.md).

## 1. Como propor uma mudança

1. Abra uma [Issue](.github/ISSUE_TEMPLATE) descrevendo o problema ou a
   melhoria antes de começar a codar — isso evita trabalho duplicado e
   alinha expectativas.
2. Faça um *fork* do repositório e clone-o localmente:

   ```bash
   git clone https://github.com/seu-usuario/mastering-github-docs.git
   cd mastering-github-docs
   ```

3. Crie uma branch a partir da `main` seguindo a convenção descrita em
   [docs/estrategia-de-branches.md](docs/estrategia-de-branches.md):

   ```bash
   git checkout -b docs/nome-da-melhoria
   ```

## 2. Convenção de commits

Todos os commits devem seguir o padrão [Conventional Commits](https://www.conventionalcommits.org/pt-br/),
detalhado em [docs/convencao-de-commits.md](docs/convencao-de-commits.md).
Resumo rápido:

```text
<tipo>: <descrição curta no imperativo>
```

Exemplos: `docs: adicionar guia de releases`, `fix: corrigir link quebrado no README`.

## 3. Abrindo o Pull Request

Consulte [docs/pull-requests-e-code-review.md](docs/pull-requests-e-code-review.md)
para o guia completo. Antes de abrir o PR, confirme que:

- [ ] O título do PR segue Conventional Commits (ele vira o commit de squash).
- [ ] A descrição usa o [template de PR](.github/pull_request_template.md) e
      referencia a Issue relacionada (`Fixes #123`).
- [ ] O Markdown foi verificado (o CI roda `markdownlint` e checagem de links
      automaticamente — veja [docs/ci-cd-com-github-actions.md](docs/ci-cd-com-github-actions.md)).
- [ ] Não há caracteres corrompidos, links quebrados ou seções duplicadas.

## 4. Processo de revisão

- Todo PR precisa passar no CI e ser aprovado por um *code owner*
  (veja [.github/CODEOWNERS](.github/CODEOWNERS)) antes do merge.
- Preferimos PRs pequenos e focados em uma única mudança lógica — mais fáceis
  de revisar e reverter se necessário.
- Merges na `main` usam **squash and merge**, mantendo o histórico linear e
  legível (um commit por Pull Request).

## 5. Dúvidas

Se tiver dúvidas sobre o processo, abra uma Issue com o template de
*Sugestão de Melhoria* ou entre em contato pelo e-mail
engenharia.al2tecnologia@gmail.com.
