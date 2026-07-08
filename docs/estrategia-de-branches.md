# 🌳 Estratégia de Branches

A forma como um time organiza suas branches diz muito sobre a maturidade do
processo de engenharia. Repositórios profissionais não trabalham direto na
`main` — eles seguem um fluxo combinado, documentado e protegido.

---

## 1. GitHub Flow (o padrão mais usado hoje)

A maioria dos projetos modernos (incluindo os do próprio GitHub) usa o
**GitHub Flow**: simples, baseado em uma única branch principal sempre
"deployável".

1. A `main` está sempre estável e pronta para produção.
2. Toda mudança nasce em uma branch específica, criada a partir da `main`.
3. Ao terminar, abre-se um Pull Request para revisão.
4. Depois de aprovado e com o CI verde, faz-se o merge na `main`.
5. A branch é deletada após o merge.

Esse é o modelo adotado neste repositório.

## 2. Git Flow (projetos com ciclos de release longos)

Times que mantêm múltiplas versões em produção simultaneamente (ex.:
software desktop, bibliotecas com suporte de longo prazo) costumam usar o
**Git Flow**, com branches de mais longa duração:

| Branch | Propósito |
| :--- | :--- |
| `main` | Sempre reflete a última versão em produção. |
| `develop` | Integração das próximas funcionalidades antes do release. |
| `release/*` | Estabilização de uma versão antes de publicar. |
| `hotfix/*` | Correções urgentes aplicadas direto em produção. |

Para a maioria dos projetos novos, o GitHub Flow é suficiente e mais simples
de manter — o Git Flow só compensa quando existe a necessidade real de
suportar várias versões ao mesmo tempo.

## 3. Convenção de nomes de branch

Nomes de branch devem comunicar **o tipo** e **o assunto** da mudança:

```text
<tipo>/<descricao-curta-em-kebab-case>
```

| Prefixo | Quando usar |
| :--- | :--- |
| `feature/` | Uma nova funcionalidade. |
| `fix/` | Correção de bug. |
| `docs/` | Mudança apenas de documentação. |
| `chore/` | Tarefas de manutenção (configs, dependências). |
| `refactor/` | Reestruturação de código sem mudar comportamento. |

Exemplos: `feature/checkout-com-pix`, `fix/link-quebrado-no-readme`,
`docs/guia-de-releases`.

## 4. Branch protection (proteção da `main`)

Em `Settings → Branches` do GitHub, é possível configurar regras para a
`main`, como:

- Exigir Pull Request antes de fazer merge (bloqueia push direto).
- Exigir que o CI passe antes de habilitar o merge.
- Exigir aprovação de pelo menos um *code owner* (veja
  [.github/CODEOWNERS](../.github/CODEOWNERS)).
- Exigir que a branch esteja atualizada com a `main` antes do merge.

Essas regras transformam boas práticas em **regras automáticas**, em vez de
depender apenas da disciplina do time.
