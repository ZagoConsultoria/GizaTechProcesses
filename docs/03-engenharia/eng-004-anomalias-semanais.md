---
id: ENG-004
titulo: Tratamento de Anomalias da Semana
data_criacao: 17/12/2025
revisao: 00
area: Engenharia / Sustentação
responsavel: Suporte N3 / DevOps
status: Vigente
tags:
  - logs
  - monitoramento
  - sustentacao
  - preventivo
---

# POP: Tratamento de Anomalias da Semana

!!! info "Ficha Técnica"
    **CÓD:** ENG-004 | **Data:** 17/12/2025 | **Revisão:** 00  
    **Processo Pai:** Monitoramento e Observabilidade

## 1. O que é
Este documento define a rotina semanal de **análise de logs e alertas silenciosos**.
Uma "anomalia" é um comportamento inesperado do sistema que não necessariamente gerou um chamado de suporte ou derrubou o servidor, mas indica que algo está errado (ex: um pico de uso de memória, muitos erros 404, falhas de integração que tentaram novamente e passaram).

## 2. Objetivo
Atuar preventivamente na saúde do sistema GIZA, evitando que pequenos erros (sintomas) se transformem em grandes incidentes (doenças).

As principais finalidades são:

* **Limpeza:** Manter os logs do sistema limpos para facilitar o debug quando for necessário.
* **Proatividade:** Descobrir que uma integração está falhando antes do cliente reclamar.
* **Correção de Dados:** Ajustar inconsistências no banco de dados geradas por falhas de transação.

## 3. Responsabilidades

| Quem faz? | O que faz? |
| :--- | :--- |
| **Suporte N3 / DevOps** | • Analisa os painéis de monitoramento (Dashboards).<br>• Investiga a causa raiz dos alertas. |
| **Dev Backend** | • Cria scripts de correção de dados (Data Fix) se necessário.<br>• Corrige o código que está gerando "sujeira" no log. |

## 4. Diretrizes Gerais
A regra do "Broken Windows" (Janelas Quebradas):

* [ ] **Log Zero:** A meta é ter zero logs de "Error" na aplicação. Se um erro acontece e não é importante, mude o nível para "Warning". Se é importante, corrija.
* [ ] **Investigação:** Nunca reiniciar um serviço para resolver uma anomalia sem antes salvar os logs para entender o porquê.
* [ ] **Recorrência:** Se uma anomalia acontece toda semana (ex: lentidão toda quinta às 15h), ela deve virar um card de bug no backlog.

---

# Anexo: Instrução de Trabalho (IT)

!!! abstract "IT-ENG-04 - Varredura de Anomalias (Quinta-feira)"
    **Periodicidade:** Semanal (Quinta-feira)  
    **Ferramentas:** Datadog/Sentry/CloudWatch, Banco de Dados (SQL).

### Etapa 1 — Análise de Logs (Sentry/Datadog)
- [ ] Filtrar logs da última semana com nível `ERROR` ou `CRITICAL`.
- [ ] Agrupar por tipo de erro.
- [ ] Identificar novos erros que surgiram após o último deploy (Terça-feira).
    - *Exemplo:* "NullPointerException na classe de Cadastro apareceu 50 vezes ontem".

### Etapa 2 — Verificação de Infraestrutura
- [ ] Checar gráficos de CPU, Memória e Disco. Houve algum pico inexplicável?
- [ ] Verificar fila de processamento (Jobs): Existem jobs travados ou falhando silenciosamente?
- [ ] Verificar Integridade de Backup: O backup automático rodou todos os dias?

### Etapa 3 — Plano de Ação
- [ ] **Para erros de código:** Abrir Bug no Jira vinculado ao log (ENG-005).
- [ ] **Para inconsistência de dados:** Rodar script de correção (update/delete) com aprovação do Tech Lead.
- [ ] **Para falsos positivos:** Ajustar a regra de alerta para parar de apitar à toa.

### Etapa 4 — Registro
- [ ] Registrar na ata semanal: "Encontradas 3 anomalias, 2 corrigidas e 1 virou bug".
- [ ] Limpar/Arquivar os logs tratados.