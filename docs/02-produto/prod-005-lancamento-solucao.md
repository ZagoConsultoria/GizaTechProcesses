---
id: PROD-005
titulo: Publicação de Lançamento de Solução (Release)
data_criacao: 17/12/2025
revisao: 00
area: Produto / DevOps
responsavel: Tech Lead / Product Marketing
status: Vigente
tags:
  - deploy
  - release
  - comunicacao
  - giza
---

# POP: Publicação de Lançamento de Solução (Release)

!!! info "Ficha Técnica"
    **CÓD:** PROD-005 | **Data:** 17/12/2025 | **Revisão:** 00  
    **Processo Pai:** Gestão de Liberação e Implantação

## 1. O que é
Este documento define o padrão para o **Deploy em Produção** e a comunicação das novidades para a base de usuários.
Seguimos o modelo de "Release Train": o trem sai da estação toda **Terça-feira**. Se a funcionalidade está pronta e testada, ela entra. Se não está, espera o próximo trem (semana que vem).

## 2. Objetivo
Garantir que as atualizações cheguem aos usuários de forma segura, estável e percebida (comunicada).

As principais finalidades são:
proxim
* **Estabilidade:** Minimizar o tempo de indisponibilidade (downtime) durante a atualização.
* **Segurança:** Garantir que existe um plano de reversão (Rollback) caso algo dê errado.
* **Adoção:** Garantir que o usuário saiba que mudou e como usar a novidade.

## 3. Responsabilidades

| Quem faz? | O que faz? |
| :--- | :--- |
| **DevOps / Tech Lead** | • Executa o pipeline de deploy (CI/CD) e monitora a saúde do servidor pós-deploy. |
| **QA Team** | • Realiza o "Smoke Test" (teste de fumaça) em produção para garantir que o sistema subiu. |
| **Product Marketing** | • Escreve as Release Notes e comunica os clientes/usuários. |

## 4. Diretrizes Gerais
Regras de Ouro do Deploy:

* [ ] **Janela de Manutenção:** O deploy deve ocorrer preferencialmente em horários de baixo tráfego (Ex: Terça, 07:00h ou 19:00h), salvo hotfixes urgentes.
* [ ] **Aprovação Prévia:** Só sobe para produção o que passou pelo **PROD-002 (UAT)** na quinta-feira anterior.
* [ ] **Feature Flags:** Funcionalidades grandes devem subir "desligadas" (via flag) e serem ativadas gradualmente, se possível.

---

# Anexo: Instrução de Trabalho (IT)

!!! abstract "IT-PROD-05 - Rotina de Lançamento (Terça-feira)"
    **Periodicidade:** Semanal (Terça-feira)  
    **Ferramentas:** Pipeline de Deploy, Monitoramento (Datadog/NewRelic), Ferramenta de E-mail/Notificação.

### Etapa 1 — Preparação Técnica (Terça Manhã)
- [ ] **Code Freeze:** Ninguém "comita" código novo na branch de release durante o processo.
- [ ] **Backup:** Verificar se o backup do banco de dados da noite anterior foi realizado com sucesso.
- [ ] **Plano de Rollback:** Confirmar: "Se der tela branca, qual o comando para voltar a versão anterior em 5 minutos?".

### Etapa 2 — Deploy (Execução)
- [ ] Disparar o pipeline de deploy para Produção.
- [ ] Monitorar logs de erro e uso de CPU/Memória nos primeiros 15 minutos.
- [ ] **Smoke Test:**
    - [ ] Login funciona?
    - [ ] Tela principal carrega?
    - [ ] Funcionalidade nova aparece?

### Etapa 3 — Comunicação (Release Notes)
- [ ] Se o sistema está estável, liberar a comunicação.
- [ ] **Canais:**
    - [ ] Pop-up dentro do sistema (In-app message).
    - [ ] Canal de "Novidades" no Slack/Teams/WhatsApp interno.
    - [ ] E-mail para base (apenas para grandes lançamentos).
- [ ] **Conteúdo:** Texto curto e amigável ("O que mudou", "Como isso te ajuda", "Link para tutorial").

### Etapa 4 — Pós-Lançamento
- [ ] Monitorar chamados de suporte nas próximas 24h.
- [ ] Se houver pico de erros críticos: Acionar **Plano de Contingência (Rollback)** imediatamente.