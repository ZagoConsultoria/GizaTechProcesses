---
id: EST-004
titulo: Avaliação de ROI e Estratégia Semestral
data_criacao: 17/12/2025
revisao: 00
area: Estratégia
responsavel: Liderança / Financeiro
status: Vigente
tags:
  - roi
  - financeiro
  - planejamento
---

# POP: Avaliação de ROI e Estratégia Semestral

!!! info "Ficha Técnica"
    **CÓD:** EST-004 | **Data:** 17/12/2025 | **Revisão:** 00  
    **Processo Pai:** Planejamento Estratégico Financeiro

## 1. O que é
Este documento define o padrão para a **Avaliação de Retorno sobre Investimento (ROI)** dos projetos e produtos da Zago/Claraval, realizada semestralmente.
O processo cruza os custos operacionais (Pessoas, Infraestrutura, Ferramentas) com o valor gerado (Receita Nova, Retenção, Eficiência Operacional) para definir a estratégia do próximo semestre.

## 2. Objetivo
Assegurar a sustentabilidade financeira da área de Tecnologia e Produto, garantindo que os recursos estejam alocados em iniciativas rentáveis ou estratégicas.

As principais finalidades são:

* **Financeira:** Identificar produtos ou projetos que custam mais do que retornam (drenos de caixa).
* **Estratégica:** Definir o orçamento (Budget) para o próximo semestre com base em performance real.
* **Decisória:** Embasar decisões de "Kill/Pivot/Persevere" (Encerrar, Pivotar ou Perseverar).

## 3. Responsabilidades

| Quem faz? | O que faz? |
| :--- | :--- |
| **Head de Produto** | • Levanta as métricas de valor gerado (Ex: Economia de tempo, vendas, retenção). |
| **Tech Lead** | • Levanta os custos de infraestrutura (Cloud) e licenças associadas a cada projeto. |
| **Financeiro** | • Valida os cálculos e consolida o DRE (Demonstrativo de Resultado) da área. |

## 4. Diretrizes Gerais
Para garantir a precisão da análise:

* [ ] **Custo Total de Propriedade (TCO):** O custo de um software não é só o servidor. Inclui horas de desenvolvimento, suporte e ferramentas terceiras.
* [ ] **Atribuição de Valor:** Projetos internos (que não geram receita direta) devem ter seu valor calculado por "Custo Evitado" ou "Ganho de Eficiência".
* [ ] **Honestidade Intelectual:** Não maquiar números para salvar projetos de estimação.

---

# Anexo: Instrução de Trabalho (IT)

!!! abstract "IT-EST-04 - Análise de ROI e Planejamento"
    **Periodicidade:** Semestral (Junho e Dezembro)  
    **Ferramentas:** Planilhas Financeiras, Dashboard de Custos Cloud (AWS/Azure), ERP.

### Etapa 1 — Coleta de Dados (Semana 1 e 2)
- [ ] **Custos:**
    - [ ] Extrair custos de Nuvem/Servidores por projeto (Tagging).
    - [ ] Estimar horas de time dedicadas (H/H) por iniciativa.
    - [ ] Listar custos de ferramentas SaaS específicas.
- [ ] **Retorno:**
    - [ ] Calcular receita direta gerada pelos produtos.
    - [ ] Calcular economia gerada (Ex: "O software Giza poupou X horas do time de operações").

### Etapa 2 — Cálculo e Análise (Semana 3)
- [ ] Aplicar a fórmula de ROI: `(Ganho Obtido - Custo do Investimento) / Custo do Investimento`.
- [ ] Classificar as iniciativas em quadrantes:
    1.  **Alto ROI / Baixo Custo:** Acelerar (Cash cows).
    2.  **Alto ROI / Alto Custo:** Otimizar eficiência.
    3.  **Baixo ROI / Baixo Custo:** Manter ou Automatizar.
    4.  **Baixo ROI / Alto Custo:** Descontinuar ou Refazer estratégia.

### Etapa 3 — Definição da Estratégia (Semana 4)
- [ ] Apresentar o estudo para a Diretoria.
- [ ] Definir o *Budget* de TI para o próximo semestre.
- [ ] Atualizar a **Tese de Produto** (conforme processo EST-005) se houver mudança de direção de mercado.
- [ ] Comunicar aos gestores quais projetos terão investimento ampliado ou reduzido.