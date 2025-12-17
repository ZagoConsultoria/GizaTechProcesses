---
id: ENG-005
titulo: Gestão e Correção de Bugs
data_criacao: 17/12/2025
revisao: 00
area: Engenharia / Suporte
responsavel: Tech Lead / Product Owner
status: Vigente
tags:
  - bugs
  - sla
  - sustentacao
  - hotfix
---

# POP: Gestão e Correção de Bugs

!!! info "Ficha Técnica"
    **CÓD:** ENG-005 | **Data:** 17/12/2025 | **Revisão:** 00  
    **Processo Pai:** Gestão de Incidentes e Qualidade

## 1. O que é
Este documento define o padrão para **Reporte, Triagem, Priorização e Correção** de falhas no software (Bugs).
Estabelece os critérios de gravidade (SLA) e o fluxo que um ticket percorre desde a reclamação do cliente até a correção em produção.

## 2. Objetivo
Minimizar o impacto de falhas na experiência do usuário e garantir que os recursos de engenharia sejam alocados nos problemas mais críticos primeiro.

As principais finalidades são:

* **Padronização:** Garantir que todo bug reportado tenha evidências suficientes para ser reproduzido.
* **Priorização:** Evitar o "tudo é urgente". Definir o que deve parar o time agora e o que pode esperar.
* **Transparência:** Manter o time de Suporte informado sobre a previsão de correção.

## 3. Responsabilidades

| Quem faz? | O que faz? |
| :--- | :--- |
| **Suporte (N1/N2)** | • Recebe o chamado, valida se é erro mesmo (não dúvida) e abre o ticket com "Passos para Reproduzir". |
| **Product Owner (PO)** | • Prioriza os bugs de média/baixa gravidade na fila de desenvolvimento. |
| **Tech Lead** | • Classifica a gravidade técnica e define quem vai corrigir. Aciona o fluxo de Hotfix se for Crítico. |
| **Dev Team** | • Diagnostica a causa raiz, corrige e cria teste automatizado para evitar regressão. |

## 4. Diretrizes Gerais
Classificação de Gravidade (SLA):

* [ ] **🔥 Crítico (SLA 4h):** Sistema fora do ar, perda de dados ou bloqueio total de faturamento. (Exige Hotfix imediato).
* [ ] **🔴 Alto (SLA 24h):** Funcionalidade importante quebrada, sem solução de contorno (workaround).
* [ ] **🟡 Médio (Próxima Sprint):** Funcionalidade com erro, mas existe um jeito alternativo de fazer.
* [ ] **🟢 Baixo (Backlog):** Erros cosméticos, textos errados ou bugs que afetam poucos usuários.

---

# Anexo: Instrução de Trabalho (IT)

!!! abstract "IT-ENG-05 - Fluxo de Vida do Bug"
    **Periodicidade:** Diária (Triagem e Correção)  
    **Ferramentas:** Jira (Service Desk + Software), Git.

### Etapa 1 — Reporte e Triagem (Suporte)
- [ ] O Suporte tenta reproduzir o erro relatado.
- [ ] Se confirmado, cria Ticket no Jira com:
    - **Título:** Resumo claro do erro.
    - **Evidência:** Print, Vídeo ou ID do Log.
    - **Passos para Reproduzir (Obrigatório):** 1. Clique aqui > 2. Preencha X > 3. Erro Y.
    - **Ambiente:** Ocorreu em Produção ou Homologação?

### Etapa 2 — Priorização (Tech Lead/PO)
- [ ] Analisar a fila de "Novos Bugs" diariamente (Daily).
- [ ] Definir a prioridade (Crítico, Alto, Médio, Baixo).
- [ ] Atribuir ao desenvolvedor responsável (ou colocar na fila da Sprint).

### Etapa 3 — Correção (Desenvolvimento)
- [ ] **Reprodução:** O Dev deve conseguir reproduzir o erro localmente. Se não conseguir, devolve para o Suporte.
- [ ] **Fix:**
    - Se for **Hotfix (Crítico):** Cria branch a partir de `main`, corrige e sobe imediatamente.
    - Se for **Bugfix (Normal):** Cria branch a partir de `develop`, corrige e entra no fluxo normal de Release Semanal (PROD-005).
- [ ] **Teste de Regressão:** Garantir que o conserto não quebrou outra coisa.

### Etapa 4 — Validação e Fechamento
- [ ] O QA ou quem reportou o erro valida a correção em ambiente de Staging.
- [ ] Após o deploy em Produção, o ticket é movido para "Concluído".
- [ ] O Suporte avisa o cliente: "Seu problema foi resolvido na versão X".