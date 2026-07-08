# 🚀 Guia Definitivo de Boas Práticas no GitHub

[![Licença: MIT](https://img.shields.io/badge/Licen%C3%A7a-MIT-blue.svg)](LICENSE)
[![Docs Lint](https://github.com/jhowsbDiem/mastering-github-docs/actions/workflows/docs-lint.yml/badge.svg)](.github/workflows/docs-lint.yml)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

Bem-vindo ao repositório **Guia Definitivo de Boas Práticas no GitHub**! Este espaço foi criado com um único objetivo: ser um manual prático, visual e detalhado de como utilizar os recursos do GitHub para elevar o nível de organização, comunicação e gerenciamento de projetos de software.

No mercado de tecnologia atual, saber codificar é apenas metade do trabalho. A outra metade consiste em saber documentar, colaborar e gerenciar o fluxo de entrega. Este repositório não é só um guia sobre isso — ele é a prova viva dessas práticas em ação: possui licença, código de conduta, guia de contribuição, convenção de commits e CI, exatamente como um repositório profissional de mercado.

---

## 📌 O que você vai aprender aqui?

Este repositório está dividido em módulos práticos. Navegue pelos links abaixo para acessar os guias detalhados:

1. **[A Engenharia de um bom README](docs/como-criar-readmes.md):** Como estruturar o pensamento antes de escrever, quais seções são obrigatórias e como vender o seu projeto visualmente.
2. **[Gestão com Issues e Milestones](docs/engenharia-de-issues.md):** Como documentar tarefas de forma clara, criar marcos de entrega (Milestones) e organizar tudo em quadros Kanban (GitHub Projects).
3. **[Estratégia de Branches](docs/estrategia-de-branches.md):** GitHub Flow vs Git Flow, convenção de nomes de branch e branch protection.
4. **[Convenção de Commits](docs/convencao-de-commits.md):** Conventional Commits, tipos de commit e sua relação com versionamento automático.
5. **[Pull Requests e Code Review](docs/pull-requests-e-code-review.md):** Como abrir PRs pequenos e revisáveis, e como revisar o código de outra pessoa.
6. **[Releases e Versionamento Semântico](docs/releases-e-versionamento.md):** SemVer, CHANGELOG.md e GitHub Releases.
7. **[CI/CD com GitHub Actions](docs/ci-cd-com-github-actions.md):** Como o workflow de lint e checagem de links deste repositório funciona.
8. **[Referências de Mercado](docs/referencias.md):** Especificações e repositórios reais usados como base para todas as práticas daqui.
9. **[Automação com Templates](.github/):** Modelos prontos e configurados de Issues e Pull Requests que você pode copiar e colar nos seus próprios projetos.

---

## 🗂️ Estrutura do Repositório

```text
.
├── .github/
│   ├── ISSUE_TEMPLATE/       # Modelos de bug e sugestão de melhoria + seletor
│   ├── workflows/            # CI: lint de Markdown e checagem de links
│   ├── CODEOWNERS            # Dono responsável por revisar cada mudança
│   ├── dependabot.yml        # Atualização automática das GitHub Actions
│   └── pull_request_template.md
├── docs/                     # Os módulos do guia (link na seção acima)
├── CHANGELOG.md              # Histórico de versões (Keep a Changelog)
├── CODE_OF_CONDUCT.md        # Contributor Covenant
├── CONTRIBUTING.md           # Como propor mudanças neste repositório
├── LICENSE                   # MIT
├── SECURITY.md               # Como reportar problemas
└── README.md
```

---

## 🛠️ Recursos Automatizados inclusos neste Repositório

Para demonstrar como a padronização funciona na vida real, este repositório possui as seguintes automações configuradas:

| Recurso | Descrição | Status no Projeto |
| :--- | :--- | :--- |
| **Issue Templates** | Modelos padronizados para reporte de bugs e novas funcionalidades. | ✅ Configurado |
| **PR Template** | Checklists automáticos que aparecem sempre que um novo Pull Request é aberto. | ✅ Configurado |
| **CI (GitHub Actions)** | Lint de Markdown e checagem de links em todo push/PR. | ✅ Configurado |
| **Dependabot** | Mantém as GitHub Actions do CI sempre atualizadas. | ✅ Configurado |
| **CODEOWNERS** | Exige revisão do mantenedor antes do merge. | ✅ Configurado |
| **Labels Personalizadas** | Etiquetas organizadas por cores para categorizar o peso e o tipo de cada tarefa. | 🛠️ Em desenvolvimento |

---

## 🧠 Por que este projeto foi criado?

Muitos desenvolvedores focam exclusivamente na sintaxe do código e negligenciam a documentação. Isso gera gargalos nos times, pois código sem contexto gera retrabalho. 

Este repositório serve como:
- **Portfólio Pessoal:** Demonstração prática de conhecimentos em metodologias ágeis, documentação técnica (Docs as Code) e cultura Open Source.
- **Central de Consulta:** Um local rápido para qualquer desenvolvedor buscar modelos prontos para usar no dia a dia.

---

## 🧑‍💻 Como contribuir ou usar este guia

Se você está aprendendo ou quer sugerir uma melhoria:
1. Vá até a aba de **Issues** deste repositório.
2. Abra uma nova Issue utilizando um dos nossos modelos prontos.
3. Se quiser treinar os conceitos de Git, faça um *Fork*, altere os arquivos e envie um *Pull Request* seguindo o nosso modelo!

Antes de contribuir, leia o [Guia de Contribuição](CONTRIBUTING.md) e o
[Código de Conduta](CODE_OF_CONDUCT.md).

---
Desenvolvido com 💙 por [Jonathan dos Santos Bezerra](https://github.com/jhowsbDiem)