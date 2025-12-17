---
id: ENG-006
titulo: Análise de Indicadores de Engenharia (KPIs)
data_criacao: 17/12/2025
revisao: 00
area: Engenharia
responsavel: CTO / Tech Lead
status: Vigente
tags:
  - metricas
  - dora-metrics
  - produtividade
  - qualidade
---

# POP: Análise de Indicadores de Engenharia (KPIs)

!!! info "Ficha Técnica"
    **CÓD:** ENG-006 | **Data:** 17/12/2025 | **Revisão:** 00  
    **Processo Pai:** Gestão de Performance de Time

## 1. O que é
Este documento define o ritual semanal de mensuração da **Saúde e Eficiência do Time de Engenharia**.
Utilizamos métricas de mercado (principalmente DORA Metrics) para entender se estamos entregando valor rápido o suficiente e com a qualidade necessária, sem queimar o time (Burnout).

## 2. Objetivo
Sair da gestão baseada em "sensação" ("O time parece lento") para uma gestão baseada em dados, focando na melhoria contínua do fluxo de trabalho.

As principais finalidades são:

* **Velocidade:** Identificar gargalos no processo (Ex: Código fica parado 3 dias esperando Code Review).
* **Qualidade:** Medir a taxa de retrabalho (Bugs que voltam).
* **Previsibilidade:** Melhorar a precisão das estimativas de entrega.

## 3. Responsabilidades

| Quem faz? | O que faz? |
| :--- | :--- |
| **Tech Lead** | • Extrai os relatórios do Jira/GitHub.<br>• Identifica tendências negativas (ex: aumento no tempo de correção). |
| **CTO** | • Utiliza os dados para defender contratações ou compra de ferramentas. |
| **Agile Master (se houver)** | • Apresenta os números na Retrospectiva para o time discutir melhorias. |

## 4. Diretrizes Gerais
O que NÃO medir (Anti-patterns):

* [ ] **Linhas de Código (LoC):** Mais código não significa melhor software. Muitas vezes, significa o contrário.
* [ ] **Horas Trabalhadas:** Engenharia é trabalho criativo/intelectual, não linha de montagem.
* [ ] **Comparação entre Pessoas:** KPIs servem para avaliar o *Time* e o *Processo*, não para fazer ranking de quem coda mais.

---

# Anexo: Instrução de Trabalho (IT)

!!! abstract "IT-ENG-06 - Apuração Semanal (Sexta-feira)"
    **Periodicidade:** Semanal (Sexta-feira)  
    **Ferramentas:** Jira Reports, GitHub Insights, Planilha de KPIs.

### Etapa 1 — Coleta das DORA Metrics (As 4 Chaves)
- [ ] **Deployment Frequency:** Quantas vezes fizemos deploy em produção essa semana? (Meta: Aumentar).
- [ ] **Lead Time for Changes:** Quanto tempo demorou desde o primeiro "commit" até o código rodar em produção? (Meta: Diminuir).
- [ ] **MTTR (Mean Time to Restore):** Quando o sistema caiu/falhou, quanto tempo levamos para arrumar? (Meta: Diminuir).
- [ ] **Change Failure Rate:** De todos os deploys feitos, quantos deram pau (geraram bugs/rollback)? (Meta: < 5%).

### Etapa 2 — Métricas de Fluxo (Flow Metrics)
- [ ] **Cycle Time:** Tempo médio que um card fica na coluna "Em Andamento".
- [ ] **WIP (Work In Progress):** Quantos itens o time está fazendo ao mesmo tempo? (Se for alto, explica a lentidão).
- [ ] **Throughput:** Quantos itens foram entregues (Done) essa semana?

### Etapa 3 — Análise e Ação
- [ ] O Tech Lead analisa os números:
    - *Cenário A:* "Lead Time aumentou muito" -> Investigar se o Code Review está gargalando.
    - *Cenário B:* "Failure Rate subiu" -> Investigar se estamos testando pouco em Staging.
- [ ] Levar um insight para a Retrospectiva: "Pessoal, nosso Code Review está demorando 48h em média. Como podemos baixar para 24h?"

### Etapa 4 — Transparência
- [ ] Atualizar o Dashboard de Engenharia (visível para a empresa).
- [ ] Registrar histórico para análise de tendência mensal.