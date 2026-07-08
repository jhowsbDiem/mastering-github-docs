# 📚 Referências de Mercado

Nenhuma prática deste guia foi inventada do zero — todas vêm de padrões
consolidados e usados por projetos open source relevantes. Esta página reúne
as principais referências para quem quiser se aprofundar.

---

## Padrões e especificações

| Referência | O que define | Usado por |
| :--- | :--- | :--- |
| [Conventional Commits](https://www.conventionalcommits.org/pt-br/) | Convenção de mensagens de commit. | Angular, Vue, Electron |
| [Semantic Versioning (SemVer)](https://semver.org/lang/pt-BR/) | Regras de numeração de versões. | Praticamente todo o ecossistema npm/Cargo/Go modules |
| [Keep a Changelog](https://keepachangelog.com/pt-BR/) | Formato padronizado de `CHANGELOG.md`. | Milhares de projetos open source |
| [Contributor Covenant](https://www.contributor-covenant.org/) | Modelo de Código de Conduta. | Kubernetes, Rails, Node.js, Swift |
| [GitHub Flow](https://docs.github.com/get-started/using-github/github-flow) | Estratégia de branches simples baseada em `main` sempre deployável. | GitHub e a maioria dos projetos web modernos |
| [standard-readme](https://github.com/RichardLitt/standard-readme) | Especificação para estrutura de README. | Diversos projetos JavaScript/Node |

## Repositórios reais para estudar a estrutura

| Repositório | O que observar |
| :--- | :--- |
| [github/docs](https://github.com/github/docs) | Como o próprio GitHub documenta e organiza contribuições em um repo gigante. |
| [kubernetes/community](https://github.com/kubernetes/community) | Governança, CODEOWNERS e processo de decisão em um projeto de larga escala. |
| [facebook/react](https://github.com/facebook/react) | CONTRIBUTING.md, templates de issue e organização de labels em um projeto de altíssima visibilidade. |
| [conventional-changelog/commitlint](https://github.com/conventional-changelog/commitlint) | Ferramenta que aplica Conventional Commits automaticamente via hook. |
| [google/eng-practices](https://github.com/google/eng-practices) | Guia do Google sobre como escrever e revisar Pull Requests. |

## Como este repositório aplica essas referências

- Commits seguem **Conventional Commits** → veja [docs/convencao-de-commits.md](convencao-de-commits.md).
- Versões seguem **SemVer** e o **CHANGELOG.md** segue Keep a Changelog → veja
  [docs/releases-e-versionamento.md](releases-e-versionamento.md).
- O **Código de Conduta** é adaptado do Contributor Covenant → veja
  [CODE_OF_CONDUCT.md](../CODE_OF_CONDUCT.md).
- A estratégia de branches segue o **GitHub Flow** → veja
  [docs/estrategia-de-branches.md](estrategia-de-branches.md).

Estudar esses projetos reais é o melhor caminho para internalizar essas
práticas além do que qualquer guia consegue explicar em texto.
