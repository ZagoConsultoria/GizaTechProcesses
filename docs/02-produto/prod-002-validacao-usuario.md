---
id: PROD-002
titulo: Teste de Validação com Usuário (UAT)
data_criacao: 17/12/2025
revisao: 00
area: Produto / QA
responsavel: Product Manager / Key Users
status: Vigente
tags:
  - uat
  - homologacao
  - qualidade
  - testes
---

# POP: Teste de Validação com Usuário (UAT)

!!! info "Ficha Técnica"
    **CÓD:** PROD-002 | **Data:** 17/12/2025 | **Revisão:** 00  
    **Processo Pai:** Garantia de Qualidade e Entrega

## 1. O que é
Este documento define o padrão para os **Testes de Aceitação do Usuário (User Acceptance Testing - UAT)**.
Diferente do teste de protótipo (que valida a ideia), aqui validamos o **software funcionando** em ambiente de Homologação (Staging), garantindo que o que foi desenvolvido atende à regra de negócio antes de ir para Produção.

## 2. Objetivo
Garantir que a funcionalidade desenvolvida resolve o problema original sem introduzir novos erros críticos, obtendo o "de acordo" final do cliente interno ou externo.

As principais finalidades são:

* **Conformidade:** Verificar se o entregável bate com os requisitos levantados no Discovery.
* **Usabilidade Real:** Testar o fluxo com dados reais (ou mascarados), não apenas dados de teste.
* **Segurança:** Evitar *rollbacks* após o lançamento oficial.

## 3. Responsabilidades

| Quem faz? | O que faz? |
| :--- | :--- |
| **Product Manager (PM)** | • Seleciona as *features* prontas para teste e convoca os usuários.<br>• Acompanha o teste e documenta feedbacks. |
| **Key User (Usuário Chave)** | • Executa o roteiro de teste no sistema.<br>• Aprova (Sign-off) ou reprova a entrega. |
| **QA / Dev Team** | • Garante que o ambiente de Staging está estável e atualizado com a versão a ser testada. |

## 4. Diretrizes Gerais
Para um teste eficiente:

* [ ] **Ambiente Controlado:** O teste nunca deve ser feito em produção (para não sujar dados reais), nem em ambiente de desenvolvimento (que é instável). Usar Staging.
* [ ] **Roteiro de Teste:** O usuário não deve apenas "navegar aleatoriamente". Ele deve ter uma missão: "Tente cadastrar um cliente e emitir um boleto".
* [ ] **Critério de Aceite:** Se houver bug crítico (impeditivo), a funcionalidade é reprovada inteira. Bugs visuais (cosméticos) podem ser anotados para correção futura sem bloquear o lançamento.

---

# Anexo: Instrução de Trabalho (IT)

!!! abstract "IT-PROD-02 - Rotina de Homologação Semanal"
    **Periodicidade:** Semanal (Quinta-feira)  
    **Ferramentas:** Ambiente de Staging (Giza), Jira, Planilha de Roteiro de Teste.

### Etapa 1 — Preparação (Quinta de Manhã)
- [ ] Verificar no quadro Kanban quais itens estão na coluna "Aguardando Validação/UAT".
- [ ] Solicitar ao time técnico o *Deploy* dessas versões no ambiente de Staging.
- [ ] Criar massas de dados (ex: usuários de teste, produtos fictícios) se necessário.
- [ ] Confirmar horário com o Key User (usuário validador).

### Etapa 2 — Execução do Teste (Quinta à Tarde)
- [ ] **Contextualização:** Explicar ao usuário o que foi desenvolvido.
- [ ] **Teste Guiado:** Pedir para o usuário executar a tarefa principal.
    > *Dica:* Observar em silêncio. Se o usuário trava, é um sinal de falha de UX.
- [ ] **Teste de Stress (Opcional):** Pedir para o usuário tentar "quebrar" o fluxo (fazer algo fora do padrão).

### Etapa 3 — Classificação e Saída (Sign-off)
- [ ] **Aprovado:** Mover card para "Pronto para Release/Deploy".
- [ ] **Reprovado:**
    - [ ] Abrir Bug no Jira vinculado à tarefa original.
    - [ ] Mover card de volta para "In Progress" ou "To Do".
    - [ ] Avisar o Tech Lead sobre a falha.
- [ ] Comunicar Stakeholders se alguma entrega prevista para a próxima semana for atrasar devido à reprovação.