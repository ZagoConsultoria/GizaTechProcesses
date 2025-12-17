---
id: ENG-001
titulo: Auditoria de Códigos (Code Audit)
data_criacao: 17/12/2025
revisao: 00
area: Engenharia / Qualidade
responsavel: Tech Lead / Arquiteto
status: Vigente
tags:
  - code-review
  - qualidade
  - seguranca
  - refatoracao
---

# POP: Auditoria de Códigos (Code Audit)

!!! info "Ficha Técnica"
    **CÓD:** ENG-001 | **Data:** 17/12/2025 | **Revisão:** 00  
    **Processo Pai:** Governança de Engenharia de Software

## 1. O que é
Este documento define o padrão para a **Auditoria Recorrente de Código Fonte**.
Diferente do "Code Review" diário (que foca na tarefa específica), a Auditoria é uma revisão amostral e profunda, olhando para padrões, segurança e manutenibilidade do projeto como um todo.

## 2. Objetivo
Evitar a "podridão do código" (Software Rot) e garantir que as dívidas técnicas sejam visíveis e pagáveis.

As principais finalidades são:

* **Padronização:** Garantir que todos os devs estão seguindo o Style Guide da Zago/Claraval.
* **Segurança:** Identificar vulnerabilidades que passaram despercebidas no dia a dia (ex: senhas hardcoded, injeção de SQL).
* **Performance:** Identificar trechos de código ineficientes que consomem recursos desnecessários do servidor.

## 3. Responsabilidades

| Quem faz? | O que faz? |
| :--- | :--- |
| **Tech Lead / Arquiteto** | • Seleciona os módulos que serão auditados.<br>• Executa ferramentas de análise estática e faz a revisão manual. |
| **Dev Sênior** | • Apoia na análise e propõe soluções de refatoração. |
| **Time de Dev** | • Executa as correções apontadas no relatório final. |

## 4. Diretrizes Gerais
Critérios de qualidade (Clean Code):

* [ ] **Complexidade Ciclomática:** Funções não devem ter muitos "If/Else" aninhados. Se for difícil de ler, é difícil de manter.
* [ ] **Cobertura de Testes:** O código auditado possui testes unitários? A cobertura está acima do mínimo (ex: 70%)?
* [ ] **Segurança:** Nenhuma credencial (API Key, Senha) deve estar escrita no código. Deve vir de variáveis de ambiente.

---

# Anexo: Instrução de Trabalho (IT)

!!! abstract "IT-ENG-01 - Rotina de Auditoria (Bimestral/Mensal)"
    **Periodicidade:** Bimestral (Fev, Abr, Jul, Nov) ou Mensal (Última Quarta)  
    **Ferramentas:** SonarQube (Análise Estática), GitHub/GitLab, IDE.

### Etapa 1 — Seleção e Varredura Automática
- [ ] Escolher o módulo/repositório alvo da vez (Rodízio entre projetos).
- [ ] Rodar ferramenta de análise estática (Ex: SonarQube, ESLint Security).
- [ ] Filtrar os alertas:
    - 🔴 **Blocker/Critical:** Devem ser corrigidos imediatamente.
    - 🟡 **Major/Minor:** Entram no backlog de débito técnico.

### Etapa 2 — Revisão Manual (Amostragem)
- [ ] O Tech Lead abre aleatoriamente 3 a 5 arquivos recentes do projeto.
- [ ] Verificar:
    - [ ] Nomes de variáveis fazem sentido?
    - [ ] Existem funções duplicadas?
    - [ ] O código está comentado onde é complexo?

### Etapa 3 — Relatório e Plano de Ação
- [ ] Compilar os achados em um documento simples ("Relatório de Saúde do Código").
- [ ] Criar tarefas no Jira/Backlog para as refatorações necessárias.
    - *Exemplo:* "Refatorar Módulo de Login para reduzir complexidade (ENG-001)".
- [ ] Apresentar os resultados na reunião técnica do time (Chapter/Guilda).

### Etapa 4 — Follow-up
- [ ] Verificar na próxima auditoria se os itens críticos anteriores foram resolvidos.
- [ ] Se o mesmo erro se repete muito, agendar treinamento/workshop para o time.