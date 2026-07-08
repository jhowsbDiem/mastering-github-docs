# Changelog

Todas as mudanças notáveis deste projeto serão documentadas neste arquivo.

O formato é baseado em [Keep a Changelog](https://keepachangelog.com/pt-BR/1.1.0/),
e este projeto segue o [Versionamento Semântico](https://semver.org/lang/pt-BR/).

## [Unreleased]

## [1.1.0] - 2026-07-08

### Added

- Arquivos de governança padrão de repositórios profissionais: `LICENSE`
  (MIT), `CODE_OF_CONDUCT.md`, `CONTRIBUTING.md`, `SECURITY.md`,
  `.gitignore` e `.editorconfig`.
- `.github/CODEOWNERS` e `.github/dependabot.yml`.
- `.github/ISSUE_TEMPLATE/config.yml` desabilitando issues em branco.
- Workflow de CI (`.github/workflows/docs-lint.yml`) com lint de Markdown
  (`markdownlint-cli2`) e checagem de links (`lychee`).
- Novos módulos em `docs/`: estratégia de branches, convenção de commits,
  pull requests e code review, releases e versionamento semântico, CI/CD
  com GitHub Actions e referências de projetos reais do mercado.
- Este `CHANGELOG.md`.

### Fixed

- Caractere corrompido no cabeçalho do template de Pull Request.

## [1.0.0] - 2026-07-08

### Added

- Estrutura inicial do guia: `README.md`, `docs/como-criar-readmes.md`,
  `docs/engenharia-de-issues.md`.
- Templates de Issue (`bug_report.md`, `feature_request.md`) e de Pull
  Request.
