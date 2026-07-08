# 🏷️ Releases e Versionamento Semântico

Publicar uma versão não é só colocar uma tag no Git — é comunicar, de forma
previsível, o impacto daquela mudança para quem consome o projeto.

---

## 1. Versionamento Semântico (SemVer)

O padrão de mercado é o [Semantic Versioning](https://semver.org/lang/pt-BR/):

```text
MAJOR.MINOR.PATCH
  2  .  5  .  1
```

| Posição | Incrementa quando... |
| :--- | :--- |
| **MAJOR** | Há uma mudança que quebra compatibilidade (*breaking change*). |
| **MINOR** | Uma funcionalidade nova é adicionada, sem quebrar nada existente. |
| **PATCH** | Uma correção de bug é feita, sem adicionar funcionalidades. |

Se o projeto segue [Conventional Commits](convencao-de-commits.md), a versão
seguinte pode ser calculada automaticamente a partir dos tipos de commit
(`feat` → MINOR, `fix` → PATCH, `!`/`BREAKING CHANGE` → MAJOR).

## 2. CHANGELOG.md

Todo projeto profissional mantém um changelog legível para humanos, seguindo
o formato [Keep a Changelog](https://keepachangelog.com/pt-BR/):

```markdown
## [Unreleased]

## [1.1.0] - 2026-07-08
### Added
- Guia de estratégia de branches.

### Fixed
- Caractere corrompido no template de Pull Request.
```

Veja o [CHANGELOG.md](../CHANGELOG.md) deste repositório como exemplo vivo.

## 3. Git Tags e GitHub Releases

1. Depois de mesclar as mudanças na `main`, crie uma tag anotada:

   ```bash
   git tag -a v1.1.0 -m "v1.1.0"
   git push origin v1.1.0
   ```

2. No GitHub, vá em **Releases → Draft a new release**, selecione a tag e
   descreva as mudanças (o GitHub consegue gerar automaticamente as notas a
   partir dos PRs mesclados, com o botão *Generate release notes*).
3. Marque como **pre-release** se for uma versão beta/RC, ou como
   **latest release** se for estável.

## 4. Automatizando com semantic-release

Projetos que já seguem Conventional Commits à risca costumam automatizar
todo esse processo com o [`semantic-release`](https://semantic-release.gitbook.io/):
ele lê os commits, calcula a próxima versão, gera o changelog, cria a tag e
publica a release — tudo dentro do workflow de CI, sem intervenção manual.
