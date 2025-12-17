---
id: ENG-003
titulo: Organizar Melhorias Robustas do GIZA
data_criacao: 17/12/2025
revisao: 00
area: Engenharia / Desenvolvimento
responsavel: Tech Lead / Dev Team
status: Vigente
tags:
  - giza
  - refatoracao
  - performance
  - manutencao
---

# POP: Organizar Melhorias Robustas do GIZA

!!! info "Ficha Técnica"
    **CÓD:** ENG-003 | **Data:** 17/12/2025 | **Revisão:** 00  
    **Processo Pai:** Melhoria Contínua de Software

## 1. O que é
Este documento define o ritual mensal focado em **Melhorias Técnicas Robustas**.
Diferente de *features* (novas funções para o usuário), aqui tratamos de refatorações, atualizações de bibliotecas, otimização de banco de dados e resolução de débitos técnicos complexos que exigem uma janela de manutenção dedicada.

## 2. Objetivo
Manter a saúde ("Health") do sistema GIZA, prevenindo a obsolescência e garantindo performance estável.

As principais finalidades são:

* **Performance:** Otimizar consultas lentas que deixam o sistema pesado.
* **Segurança:** Aplicar patches de segurança em frameworks e dependências.
* **Manutenibilidade:** Reescrever códigos antigos (Legacy) que dificultam novas implementações.

## 3. Responsabilidades

| Quem faz? | O que faz? |
| :--- | :--- |
| **Tech Lead** | • Prioriza quais melhorias técnicas entrarão no pacote do mês.<br>• Define a janela de atualização (downtime). |
| **Dev Team** | • Executa as melhorias e refatorações planejadas. |
| **Suporte N3** | • Acompanha a atualização para garantir que correções antigas não voltem (regressão). |

## 4. Diretrizes Gerais
Regras para este pacote de melhorias:

* [ ] **Agrupamento:** Melhorias técnicas devem ser agrupadas em um "Pacote de Manutenção" mensal para evitar paradas constantes no sistema.
* [ ] **Comunicação:** Se a atualização exigir parada do sistema (Downtime), os usuários devem ser avisados com 48h de antecedência.
* [ ] **Backup Obrigatório:** Antes de rodar scripts de migração de banco pesados, o backup é mandatório.

---

# Anexo: Instrução de Trabalho (IT)

!!! abstract "IT-ENG-03 - Ciclo Mensal de Melhorias (Última Quinta)"
    **Periodicidade:** Mensal (Planejamento na última Quinta-feira)  
    **Ferramentas:** Jira (Backlog Técnico), Datadog (Monitoramento), GitHub.

### Etapa 1 — Seleção (Semanas 1-3)
- [ ] Monitorar ao longo do mês os pontos de dor (slow queries, erros recorrentes).
- [ ] Desenvolvedores marcam tarefas no Jira com a tag `tech-debt` ou `improvement`.
- [ ] Tech Lead seleciona os 3 a 5 itens de maior impacto para o pacote do mês.

### Etapa 2 — Organização e Agenda (Última Quinta)
- [ ] **Reunião de Definição:** O time técnico revisa o que foi selecionado.
- [ ] **Definição da Agenda:**
    - Quando será aplicado? (Geralmente num horário de baixo uso).
    - Quanto tempo o sistema ficará instável/indisponível?
- [ ] Criar o plano de execução passo a passo (Runbook).

### Etapa 3 — Execução e Deploy
- [ ] Realizar o deploy das melhorias em ambiente de Staging para teste de carga.
- [ ] Aplicar em Produção conforme a agenda definida.
- [ ] **Validação:** Verificar se o ganho de performance esperado realmente ocorreu (ex: "A tela de relatórios agora abre em 2s, antes era 10s").

### Etapa 4 — Registro
- [ ] Atualizar a documentação técnica se houve mudança estrutural.
- [ ] Comunicar ao time de Produto que a "Casa foi arrumada" e o sistema está pronto para novas features.