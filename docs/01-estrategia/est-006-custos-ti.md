---
id: EST-006
titulo: Revisão e Renegociação de Custos TI
data_criacao: 17/12/2025
revisao: 00
area: Estratégia / Infraestrutura
responsavel: Tech Lead / Financeiro
status: Vigente
tags:
  - finops
  - custos
  - contratos
  - compras
---

# POP: Revisão e Renegociação de Custos TI

!!! info "Ficha Técnica"
    **CÓD:** EST-006 | **Data:** 17/12/2025 | **Revisão:** 00  
    **Processo Pai:** Gestão Financeira de Tecnologia (FinOps)

## 1. O que é
Este documento define o padrão para o **controle periódico de despesas de Tecnologia**.
Abrange custos de Nuvem (AWS/Azure/Google), ferramentas SaaS (Jira, Slack, Figma, etc.), licenciamento de software e contratos de prestação de serviços (outsourcing/consultoria).

## 2. Objetivo
Evitar o desperdício financeiro (recursos zumbis ou superdimensionados) e garantir as melhores condições comerciais em renovações.

As principais finalidades são:
* **Eficiência:** Garantir que pagamos apenas pelo que realmente usamos.
* **Previsibilidade:** Evitar surpresas na fatura do cartão corporativo ou boleto mensal.
* **Negociação:** Antecipar renovações para ter poder de barganha com fornecedores.

## 3. Responsabilidades

| Quem faz? | O que faz? |
| :--- | :--- |
| **Tech Lead / CTO** | • Revisa a utilização técnica (Ex: "Precisamos mesmo dessa instância EC2 ligada 24h?"). |
| **Financeiro** | • Fornece a lista de pagamentos realizados e alertas de vencimento de contrato. |
| **Gestores de Área** | • Validam se suas equipes ainda utilizam as licenças atribuídas (SaaS). |

## 4. Diretrizes Gerais
Para manter a saúde financeira:

* [ ] **Aprovação Prévia:** Nenhuma nova ferramenta paga pode ser contratada sem cálculo de impacto anual.
* [ ] **Renovação Automática:** Sempre desativar a renovação automática de ferramentas anuais, a menos que seja crítico (ex: domínio, servidor). Isso força uma reavaliação.
* [ ] **Moeda Estrangeira:** Para pagamentos em Dólar/Euro, considerar IOF e variação cambial no orçamento.

---

# Anexo: Instrução de Trabalho (IT)

!!! abstract "IT-EST-06 - Auditoria e Renegociação Trimestral"
    **Periodicidade:** Trimestral (Março, Junho, Setembro, Dezembro)  
    **Ferramentas:** Extrato Cartão Corporativo, Painel de Billing Cloud, Planilha de Contratos.

### Etapa 1 — Levantamento (Semana 1 do mês)
- [ ] **Cloud (AWS/Azure):** Extrair relatório de custos do último trimestre. Identificar os "Top 5" ofensores de custo.
- [ ] **SaaS:** Listar todas as ferramentas pagas e número de licenças ativas vs. atribuídas.
- [ ] **Contratos:** Verificar quais contratos vencem nos próximos 90 dias.

### Etapa 2 — Análise Técnica (Semana 2)
- [ ] **Caça aos Zumbis:** Identificar recursos ligados mas sem uso (ex: Volumes EBS órfãos, IPs elásticos não associados).
- [ ] **Licenças Inativas:** Identificar usuários que não logaram nos últimos 30 dias em ferramentas pagas e remover acesso.

### Etapa 3 — Ação e Renegociação (Semana 3)
- [ ] **Limpeza:** Desligar/Excluir recursos zumbis identificados.
- [ ] **Downgrade:** Reduzir planos de ferramentas onde o uso não justifica o plano Pro/Enterprise.
- [ ] **Negociação:** Entrar em contato com fornecedores de contratos vincendos.
    - *Script:* "Estamos revisando orçamento e cotando concorrentes. Conseguimos manter o preço ou aplicar desconto para renovação antecipada?"
- [ ] **Reservas (RI):** Para Cloud, avaliar a compra de "Reserved Instances" ou "Savings Plans" para recursos de uso contínuo (desconto de até 70%).

### Etapa 4 — Fechamento
- [ ] Atualizar a planilha de previsão orçamentária.
- [ ] Reportar a economia gerada (Saving) para a Diretoria.