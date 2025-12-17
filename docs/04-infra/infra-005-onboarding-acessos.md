---
id: INFRA-005
titulo: Onboarding - Equipamentos e Acessos
frequencia: Por Demanda (Admissão)
responsavel: RH / Infraestrutura
versao: 1.0
status: Mapeado
---

# INFRA-005: Onboarding de Novos Zagoenses

## 1. Objetivo
Garantir que todo novo colaborador receba seus equipamentos (notebook, periféricos) e credenciais de acesso (e-mail, Giza, VPN) até o dia anterior ao seu início, assegurando produtividade desde o dia 1 (D-1).

## 2. Matriz SIPOC

| **S**uppliers (Fornecedores) | **I**nputs (Entradas) | **P**rocess (Processo) | **O**utputs (Saídas) | **C**ustomers (Clientes) |
| :--- | :--- | :--- | :--- | :--- |
| **RH / People** | Ticket de Admissão aberto | 1. Validar ticket e estoque<br>2. Configurar contas (AD/Google)<br>3. Preparar hardware<br>4. Entregar kit | Credenciais criadas | Novo Colaborador |
| **Gestor da Área** | Data de início, Cargo, Softwares específicos necessários | | Termo de Entrega assinado | Gestor da Área |
| **Estoque TI** | Notebook disponível | | Notebook configurado | |

## 3. Detalhamento do Processo (Itemização)

### 3.1. Recebimento e Validação
- [ ] Receber e-mail/ticket do RH com no mínimo 5 dias de antecedência.
- [ ] Verificar se há máquina disponível no estoque compatível com o cargo.
- [ ] Caso não haja estoque: Acionar processo de compra (**EST-006**).

### 3.2. Configuração de Acessos (Lógico)
- [ ] **E-mail:** Criar conta `@zago.com.br` no Google Workspace.
- [ ] **Grupos:** Adicionar aos grupos de e-mail padrões (ex: `todos@`, `squad-x@`).
- [ ] **Giza:** Criar usuário com perfil de acesso conforme o cargo.
- [ ] **Segurança:** Habilitar 2FA (Autenticação de dois fatores) obrigatória.

### 3.3. Preparação do Equipamento (Físico)
- [ ] Realizar formatação padrão da máquina.
- [ ] Instalar pacote básico: Navegador, Antivírus, VPN, Slack.
- [ ] Higienizar equipamento e testar periféricos (teclado, mouse, tela).

### 3.4. Entrega e Treinamento
- [ ] Agendar horário de entrega (presencial) ou envio (remoto).
- [ ] Realizar breve treinamento de acesso ao Giza e segurança básica.
- [ ] Coletar assinatura no **Termo de Responsabilidade**.

## 4. Histórico de Versões

| Versão | Data | Autor | Alterações |
| :--- | :--- | :--- | :--- |
| 1.0 | 17/12/2025 | Seu Nome | Criação inicial do documento. |