---
id: INFRA-001
titulo: Inventário de Equipamentos e Ativos
data_criacao: 17/12/2025
revisao: 00
area: Infraestrutura de TI
responsavel: Analista de Infraestrutura
status: Vigente
tags:
  - hardware
  - inventario
  - controle
---

# POP: Inventário de Equipamentos e Ativos

!!! info "Ficha Técnica"
    **CÓD:** INFRA-001 | **Data:** 17/12/2025 | **Revisão:** 00  
    **Processo Pai:** Gestão de Ativos de TI

## 1. O que é
Este documento define o padrão institucional para a **contagem, identificação e verificação de status** de todos os ativos de hardware (notebooks, monitores, periféricos e servidores) da empresa.

## 2. Objetivo
Padronizar o controle patrimonial, garantindo que a base de dados reflita a realidade física da empresa.

As principais finalidades são:
* **Financeira:** Evitar compras desnecessárias por falta de visibilidade.
* **Segurança:** Identificar equipamentos perdidos, furtados ou não devolvidos.
* **Manutenção:** Antecipar trocas de equipamentos obsoletos (Lifecycle).

## 3. Responsabilidades

| Quem faz? | O que faz? |
| :--- | :--- |
| **Analista de Infra** | • Realiza a contagem física e atualização da planilha/sistema.<br>• Etiqueta novos equipamentos. |
| **RH / People** | • Informa movimentações de pessoas (admissão/demissão) que afetam o ativo. |
| **Colaborador** | • Apresenta o equipamento para conferência quando solicitado. |

## 4. Diretrizes Gerais
Para garantir a acuracidade dos dados:

* [ ] **Etiquetagem Obrigatória:** Nenhum equipamento sai do armário sem etiqueta de patrimônio.
* [ ] **Termo de Responsabilidade:** Todo empréstimo deve ter termo assinado (digital ou físico).
* [ ] **Auditoria Cruzada:** O inventário deve ser validado por uma pessoa diferente de quem fez a compra, se possível.

## 5. Fluxo Macro (SIPOC)

| **S**uppliers | **I**nputs | **P**rocess (Macro) | **O**utputs | **C**ustomers |
| :--- | :--- | :--- | :--- | :--- |
| Compras, RH | Notas Fiscais, Planilha Atual, Equipamentos Físicos | 1. Listar base atual<br>2. Conferência física<br>3. Atualização de status<br>4. Relatório de divergências | Planilha Atualizada, Relatório de Perdas | Financeiro, Diretoria |

---

# Anexo: Instrução de Trabalho (IT)

!!! abstract "IT-INFRA-01 - Execução do Inventário"
    **Periodicidade:** Bimestral (Fev, Mai, Jul, Nov)  
    **Ferramentas:** Leitor de QR Code, Planilha Mestra de Ativos, Etiquetadora.

### Etapa 1 — Preparação
- [ ] Exportar a base de ativos atual do sistema/planilha.
- [ ] Agendar com os gestores as datas de verificação física nas mesas.
- [ ] Verificar bateria e insumos da etiquetadora.

### Etapa 2 — Conferência (O "Giro")
- [ ] **Equipamentos em Estoque:** Contar 100% dos itens no armário de TI.
- [ ] **Equipamentos em Uso:** Passar nas estações ou solicitar foto da etiqueta (para remotos).
- [ ] **Validação de Estado:**
    - [ ] O equipamento liga?
    - [ ] A tela tem riscos/dead pixels?
    - [ ] O teclado está funcionando?
    > **Nota:** Se houver dano físico não reportado, abrir Ticket de Incidente imediatamente.

### Etapa 3 — Consolidação
- [ ] Atualizar a coluna "Data da Última Verificação" na planilha mestra.
- [ ] Marcar status: `Em Uso`, `Estoque`, `Manutenção` ou `Extraviado`.
- [ ] Gerar relatório de itens não localizados e enviar para a Diretoria Administrativa.