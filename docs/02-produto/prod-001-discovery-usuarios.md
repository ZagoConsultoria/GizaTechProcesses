---
id: PROD-001
titulo: Condução de Discovery com Usuários
data_criacao: 17/12/2025
revisao: 01
area: Produto / Design
responsavel: Product Manager / UX Designer
status: Vigente
tags:
  - discovery
  - requisitos
  - validacao
---

# POP: Condução de Discovery com Usuários

!!! info "Ficha Técnica"
    **CÓD:** PROD-001 | **Data:** 17/12/2025 | **Revisão:** 01  
    **Processo Pai:** Ciclo de Desenvolvimento de Produto

## 1. O que é
Este documento define o padrão semanal para entender demandas e validar soluções com clientes.
O processo segue um fluxo contínuo de **Pré-diagnóstico (Assíncrono) → Entendimento (Síncrono) → Validação (Protótipo)**.

## 2. Objetivo
Garantir que o tempo de reunião com o cliente seja otimizado e que a solução apresentada na sexta-feira já esteja validada tecnicamente e alinhada à expectativa.

As principais finalidades são:

* **Agilidade:** Reduzir reuniões longas e improdutivas usando pré-diagnósticos.
* **Assertividade:** Garantir que o levantamento de requisitos foi entendido internamente antes de desenhar a tela.
* **Feedback Rápido:** Testar a interface (Front) com o usuário na mesma semana.

## 3. Responsabilidades

| Quem faz? | O que faz? |
| :--- | :--- |
| **Product Manager** | • Envia formulários, conduz a reunião de 15min e faz o levantamento. |
| **Tech Lead / Dev** | • Valida internamente se os requisitos levantados são viáveis (Quinta-feira). |
| **Product Designer** | • Prepara o protótipo/front para a validação final (Sexta-feira). |

## 4. Diretrizes Gerais
Para o sucesso do fluxo:

* [ ] **Respeito ao Tempo:** A reunião de quarta-feira deve ser estritamente de 15 minutos (Check-in). Se precisar de mais tempo, o pré-diagnóstico foi falho.
* [ ] **Validação Interna:** NENHUM protótipo deve ser mostrado ao cliente na sexta sem antes ter passado pelo crivo técnico na quinta.
* [ ] **Registro:** Todos os requisitos devem ser anotados no card/ticket correspondente.

---

# Anexo: Instrução de Trabalho (IT)

!!! abstract "IT-PROD-01 - Fluxo Semanal de Discovery"
    **Periodicidade:** Semanal (Segunda a Sexta)  
    **Ferramentas:** Typeform/Forms, Google Meet, Figma/Ambiente de Teste.

### Etapa 1 — Triagem (Segunda e Terça)
- [ ] Selecionar os clientes/usuários alvo da semana.
- [ ] **Enviar Formulário de Pré-Diagnóstico:** Perguntas chaves para entender o cenário antes de falar.
- [ ] Analisar as respostas recebidas e preparar a pauta da reunião.
    > **Nota:** Se o usuário não responder o formulário, reagendar a reunião de quarta.

### Etapa 2 — Aprofundamento (Quarta-feira)
- [ ] **Reunião Flash (15 min):** Validar com o usuário se o entendimento do formulário está correto ("Eu entendi que seu problema é X, correto?").
- [ ] **Levantamento de Requisitos:** Detalhar regras de negócio, exceções e o que é sucesso para o usuário.
- [ ] Documentar o levantamento de forma estruturada.

### Etapa 3 — Validação Técnica (Quinta-feira)
- [ ] **Review Interno:** PM e Tech Lead/Dev analisam os requisitos levantados na quarta.
- [ ] Confirmar viabilidade técnica e esforço estimado.
- [ ] Liberar o Designer para montar o Protótipo ou Tela (Front) para validação.

### Etapa 4 — Validação da Solução (Sexta-feira)
- [ ] Apresentar o Protótipo ou Front navegável para o usuário.
- [ ] Coletar feedback: "Isso resolve o problema que discutimos na quarta?".
- [ ] **Aprovação:** Se aprovado, mover para Backlog de Desenvolvimento. Se reprovado, voltar para Etapa 2.