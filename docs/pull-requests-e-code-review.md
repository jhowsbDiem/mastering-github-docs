# 🔍 Pull Requests e Code Review

O Pull Request (PR) é onde o código é discutido, revisado e aprovado antes de
entrar na `main`. É também o principal artefato de comunicação assíncrona de
um time — por isso a forma como ele é escrito importa tanto quanto o próprio
código.

---

## 1. Antes de abrir o PR

- **Mantenha o PR pequeno.** PRs de 50-200 linhas são revisados com muito
  mais qualidade do que PRs de milhares de linhas. Se a tarefa é grande,
  quebre em várias entregas incrementais.
- **Use Draft Pull Requests** quando quiser feedback antecipado sobre uma
  mudança ainda incompleta — o GitHub deixa claro que aquele PR não está
  pronto para merge.
- **Rode o CI localmente** (quando possível) antes de abrir o PR, para não
  gastar ciclos de revisão com problemas triviais.

## 2. Escrevendo uma boa descrição

Use sempre o [template de Pull Request](../.github/pull_request_template.md)
deste repositório. Uma boa descrição de PR contém:

- **O quê e por quê:** o que mudou e qual problema isso resolve.
- **Como testar:** passos para quem for revisar reproduzir e validar.
- **Issue relacionada:** use `Fixes #123` para fechar a Issue automaticamente
  no merge.
- **Capturas de tela/GIFs** sempre que houver mudança visual.

## 3. Papel de quem revisa (Code Review)

- Revise com a intenção de **entender**, não apenas de apontar erros.
- Separe comentários **bloqueantes** ("isso precisa mudar antes do merge")
  de comentários **opcionais** ("sugestão: poderia simplificar assim").
- Elogie o que está bom — review não é só sobre encontrar problemas.
- Responda em até 1 dia útil sempre que possível; PRs parados matam o ritmo
  do time.

## 4. Estratégias de merge

| Estratégia | Quando usar |
| :--- | :--- |
| **Squash and merge** | Padrão recomendado para a maioria dos repositórios: condensa todos os commits do PR em um só, mantendo a `main` limpa e linear. |
| **Merge commit** | Útil quando o histórico detalhado da branch tem valor por si só (ex.: branches de release). |
| **Rebase and merge** | Mantém commits individuais, mas sem um commit de merge extra — exige que cada commit da branch já siga a convenção. |

Este repositório usa **squash and merge**: o título do PR (seguindo
[Conventional Commits](convencao-de-commits.md)) vira a mensagem final do
commit na `main`.

## 5. Depois do merge

- Delete a branch (o GitHub oferece esse botão automaticamente).
- Se o PR fecha uma Issue vinculada a uma Milestone, confirme que ela foi
  atualizada corretamente (veja [docs/engenharia-de-issues.md](engenharia-de-issues.md)).
