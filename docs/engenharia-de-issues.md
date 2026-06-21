# 🎯 Gestão Visual: Engenharia de Issues e Milestones

Muitos desenvolvedores iniciantes acreditam que a aba *Issues* serve apenas para reportar erros e bugs. Isso é um mito. No mercado, as Issues são usadas como **tarefas** que guiam todo o desenvolvimento do projeto.

Saber organizar essas tarefas demonstra que você tem visão de produto e domínio de metodologias ágeis.

---

## 1. A Anatomia de uma Issue Perfeita

Quando você for criar (ou pedir para alguém criar) uma Issue, ela nunca deve ter apenas um título. Ela precisa de contexto. Uma boa Issue contém:

* **Descrição Clara:** Qual é o objetivo dessa tarefa?
* **Critérios de Aceite:** O que precisa acontecer para que essa tarefa seja considerada "Pronta" (Done)?
* **Checklist (`- [ ]`)**: Pequenos passos técnicos para concluir a tarefa maior.

---

## 2. Categorização com Labels (Etiquetas)

O GitHub vem com etiquetas padrão, mas times eficientes as customizam para criar um fluxo de trabalho. Exemplos práticos:
* `bug`: Algo não está funcionando corretamente.
* `enhancement`: Uma melhoria em uma funcionalidade que já existe.
* `feature`: Uma funcionalidade completamente nova.
* `documentation`: Melhorias no README ou em comentários de código.

**💡 Dica de Ouro:** Sempre assinale a Issue para um responsável (*Assignee*), para evitar que duas pessoas trabalhem na mesma coisa.

---

## 3. Milestones (Marcos de Entrega)

As *Milestones* agrupam várias Issues em um objetivo maior com um prazo definido. 

**Como pensar em Milestones:**
Imagine que você está criando um e-commerce. Você não vai entregar tudo de uma vez.
1. **Milestone 1 (MVP - Cadastro e Login):** Contém todas as Issues relacionadas à autenticação.
2. **Milestone 2 (Carrinho de Compras):** Contém as Issues de adicionar itens e calcular frete.

À medida que você fecha as Issues, a barra de progresso da Milestone vai enchendo, dando uma visão clara do andamento do projeto.

---

## 4. GitHub Projects (O seu Kanban)

O GitHub Projects permite criar um quadro visual no estilo Trello/Kanban (com colunas como *Todo*, *In Progress*, *Done*).
* Você pode vincular suas Issues diretamente a esses cartões.
* Você pode criar automações para que, quando um *Pull Request* for aprovado, o cartão da Issue vá automaticamente para a coluna *Done*.