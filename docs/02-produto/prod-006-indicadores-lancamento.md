---
id: PROD-006
titulo: Análise de Indicadores de Lançamento
data_criacao: 17/12/2025
revisao: 00
area: Produto
responsavel: Time de Produto
status: Vigente
tags:
  - metricas
  - kpis
  - adocao
  - analytics
---

# POP: Análise de Indicadores de Lançamento

!!! info "Ficha Técnica"
    **CÓD:** PROD-006 | **Data:** 17/12/2025 | **Revisão:** 00  
    **Processo Pai:** Gestão de Desempenho do Produto

## 1. O que é
Este documento define o ritual semanal de **mensuração de impacto** das funcionalidades lançadas.
Não basta colocar o código em produção na Terça-feira; precisamos saber, até Sexta-feira, se os usuários estão usando, se estão encontrando erros e se o problema original foi resolvido.

## 2. Objetivo
Transformar o desenvolvimento de software em uma ciência baseada em dados, saindo do "achismo".

As principais finalidades são:

* **Adoção:** Saber quantos usuários acessaram a novidade.
* **Qualidade:** Medir se o lançamento gerou aumento de chamados no suporte.
* **Aprendizado:** Entender rapidamente se precisamos iterar (melhorar) ou pivotar (mudar) a solução na próxima semana.

## 3. Responsabilidades

| Quem faz? | O que faz? |
| :--- | :--- |
| **Product Manager** | • Analisa métricas de negócio (Adoção, Retenção, Funil).<br>• Publica o relatório semanal. |
| **Tech Lead** | • Analisa métricas técnicas (Performance, Erros de API, Latência). |
| **Suporte CS** | • Fornece o feedback qualitativo ("O cliente reclamou que não achou o botão"). |

## 4. Diretrizes Gerais
O que medir? (Framework HEART ou similar):

* [ ] **Sucesso não é Deploy:** Sucesso é o cliente usar e ter valor. Código parado em produção é custo.
* [ ] **Métricas de Vaidade:** Evitar métricas que só inflam o ego (ex: "Número de Downloads" ou "Cliques"). Focar em métricas de ação (ex: "Número de Cadastros Completos" ou "Retenção D+7").
* [ ] **Comparação:** Sempre comparar com o período anterior (WoW - Week over Week) ou com a meta estabelecida no Discovery.

---

# Anexo: Instrução de Trabalho (IT)

!!! abstract "IT-PROD-06 - Apuração de Resultados (Sexta-feira)"
    **Periodicidade:** Semanal (Sexta-feira)  
    **Ferramentas:** Google Analytics/Mixpanel, Metabase/PowerBI, Jira Service Desk.

### Etapa 1 — Coleta de Dados (Sexta Manhã)
- [ ] **Adoção:** Quantos % da base acessou a nova feature desde Terça-feira?
- [ ] **Estabilidade:** Quantos bugs foram reportados vinculados a esse lançamento?
- [ ] **Performance:** O tempo de carregamento da página aumentou?

### Etapa 2 — Análise Qualitativa
- [ ] Ler tickets de suporte com a tag "Dúvida" ou "Reclamação" sobre a novidade.
- [ ] Verificar gravações de sessão (Hotjar/Clarity) para ver se usuários estão "clicando no vazio" (Rage Clicks).

### Etapa 3 — Publicação do Relatório "Week in Review"
- [ ] Consolidar os dados em um post curto no canal oficial da empresa.
- [ ] **Modelo de Post:**
    - 🚀 **O que lançamos:** [Nome da Feature]
    - 📊 **Resultado Parcial:** [X% de adoção em 3 dias]
    - 🐛 **Problemas:** [0 bugs críticos / 2 bugs visuais]
    - ⏭️ **Próximos Passos:** [Vamos manter ou ajustar?]

### Etapa 4 — Retroalimentação
- [ ] Se a adoção foi baixa: Criar tarefa de Marketing/Comunicação para reforçar a divulgação.
- [ ] Se a adoção foi alta e com erros: Criar tarefa de Correção Prioritária para o próximo Backlog (**PROD-004**).