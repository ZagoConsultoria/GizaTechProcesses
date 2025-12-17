---
id: PROD-004
titulo: Construção de Novo Backlog (Refinement)
data_criacao: 17/12/2025
revisao: 00
area: Produto / Engenharia
responsavel: Product Owner (PO)
status: Vigente
tags:
  - backlog
  - refinamento
  - planning
  - priorizacao
---

# POP: Construção de Novo Backlog (Refinement)

!!! info "Ficha Técnica"
    **CÓD:** PROD-004 | **Data:** 17/12/2025 | **Revisão:** 00  
    **Processo Pai:** Gestão de Fluxo de Trabalho (Scrum/Kanban)

## 1. O que é
Este documento define o ritual semanal de **Refinamento e Preparação do Backlog** para a semana seguinte.
Não é apenas uma lista de desejos, mas uma seleção técnica e negociada de itens que atendem aos critérios de "Pronto para Desenvolvimento" (Definition of Ready - DoR).

## 2. Objetivo
Garantir que o time de desenvolvimento inicie a segunda-feira com clareza total do que precisa ser feito, sem bloqueios ou dúvidas de regra de negócio.

As principais finalidades são:

* **Eficiência:** Evitar que desenvolvedores parem no meio da semana para perguntar "como isso deve funcionar?".
* **Previsibilidade:** Garantir que a quantidade de trabalho selecionada cabe na capacidade do time (Velocity).
* **Continuidade:** Absorver itens não finalizados da semana atual e priorizar novas demandas validadas.

## 3. Responsabilidades

| Quem faz? | O que faz? |
| :--- | :--- |
| **Product Owner (PO)** | • Ordena a lista de prioridades.<br>• Garante que as histórias tenham Critérios de Aceite claros. |
| **Tech Lead** | • Estima o esforço técnico e identifica dependências (ex: "precisamos mudar o banco de dados antes"). |
| **Time de Dev** | • Tira dúvidas e valida se a descrição da tarefa é suficiente para codar. |

## 4. Diretrizes Gerais
Critérios para um item entrar na semana (Definition of Ready):

* [ ] **Valor Claro:** O item descreve "Quem quer", "O que quer" e "Para que quer".
* [ ] **Critério de Aceite:** Deve estar escrito como vamos testar se ficou pronto (Ex: "O botão deve ficar verde ao clicar").
* [ ] **Estimado:** O time deve concordar que é possível fazer em uma semana (ou quebrar em tarefas menores).
* [ ] **Design Pronto:** Se tem tela, o Figma/Layout deve estar aprovado (via PROD-001).

---

# Anexo: Instrução de Trabalho (IT)

!!! abstract "IT-PROD-04 - Ritual de Backlog (Sexta-feira)"
    **Periodicidade:** Semanal (Sexta-feira à tarde)  
    **Ferramentas:** Jira/Trello/ClickUp, Poker Planning (se houver estimativa).

### Etapa 1 — Revisão da Semana Atual
- [ ] Verificar o que está "Em Andamento" e não será entregue hoje.
- [ ] Decisão:
    - O item continua na próxima semana? (Prioridade mantida).
    - O item volta para o Backlog Geral? (Prioridade caiu).

### Etapa 2 — Seleção de Novos Itens
- [ ] Puxar os itens aprovados no **Discovery (PROD-001)** e **Correções Críticas (PROD-002)**.
- [ ] Priorizar bugs críticos e débitos técnicos (ver cota de Engenharia).
- [ ] Ordenar a fila: O item do topo é o mais importante para segunda-feira.

### Etapa 3 — Refinamento Técnico
- [ ] O PO lê a história/tarefa para o Tech Lead/Time.
- [ ] O time discute a solução técnica ("Vamos usar a API X ou Y?").
- [ ] O time pontua a complexidade (Planning Poker) ou valida o tamanho da tarefa.
- [ ] **Check Final:** "Alguém tem alguma dúvida ou bloqueio para começar isso na segunda?"

### Etapa 4 — Oficialização (Sprint Backlog)
- [ ] Mover os itens selecionados para a coluna/status "To Do" (A Fazer) da próxima Sprint.
- [ ] Atribuir responsáveis (se o time trabalhar com puxada direta).
- [ ] Comunicar Stakeholders sobre o que entrou e o que ficou de fora da semana.