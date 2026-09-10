# Pagamento – Casos de Teste

## Cenários Válidos

### TC-PAY-001 — Concluir o pagamento com dados de cartão de crédito válidos
ID: QA-PAY01
Prioridade: Alta
Objetivo: Validar o processamento bem-sucedido de um pagamento utilizando dados de cartão de crédito válidos.
Pré-condições:
Estar na página de pagamento após preencher corretamente os detalhes do passageiro.

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de pagamento após concluir os detalhes do passageiro. | O pagamento é processado com sucesso e o usuário é redirecionado para a página de confirmação ou página inicial. |
| 2 | Selecionar o tipo de cartão de crédito. | |
| 3 | Inserir um número de cartão de crédito válido. | |
| 4 | Inserir uma data de validade válida. | |
| 5 | Inserir o nome do portador do cartão válido. | |
| 6 | Clicar em Pagar Agora (Pay Now). | |

---

## Cenários Inválidos

### TC-PAY-002 — Tentar realizar o pagamento com todos os campos obrigatórios vazios
ID: QA-PAY02
Prioridade: Alta
Objetivo: Garantir que o sistema bloqueie o pagamento e exiba validações quando nenhum campo for preenchido.
Pré-condições:
Estar na página de pagamento.

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de pagamento. | O sistema exibe mensagens de validação e impede o envio do pagamento. |
| 2 | Clicar em Pagar Agora sem preencher nenhum campo. | |

---

### TC-PAY-003 — Tentar realizar o pagamento com os campos obrigatórios preenchidos parcialmente
ID: QA-PAY03
Prioridade: Alta
Objetivo: Verificar se o sistema impede o avanço quando apenas parte dos campos obrigatórios é preenchida.
Pré-condições:
Estar na página de pagamento.

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de pagamento. | O sistema exibe mensagens de validação para os campos ausentes e impede o pagamento. |
| 2 | Preencher apenas alguns dos campos obrigatórios. | |
| 3 | Clicar em Pagar Agora. | |

---

### TC-PAY-004 — Tentar realizar o pagamento sem selecionar o tipo de cartão de crédito
ID: QA-PAY04
Prioridade: Média
Objetivo: Validar a obrigatoriedade de seleção da bandeira/tipo de cartão de crédito antes da submissão.
Pré-condições:
Estar na página de pagamento.

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de pagamento. | O sistema impede o pagamento e exibe uma mensagem de validação para a seleção do tipo de cartão. |
| 2 | Preencher todos os detalhes obrigatórios do cartão. | |
| 3 | Não selecionar um tipo de cartão de crédito. | |
| 4 | Clicar em Pagar Agora. | |

---

### TC-PAY-005 — Inserir dados de cartão de crédito que não correspondem ao tipo de cartão selecionado
ID: QA-PAY05
Prioridade: Média
Objetivo: Verificar se o sistema valida a consistência entre o tipo de cartão selecionado e o número inserido.
Pré-condições:
Estar na página de pagamento.

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de pagamento. | O sistema detecta a divergência no tipo de cartão e impede o envio do pagamento. |
| 2 | Selecionar um tipo de cartão de crédito. | |
| 3 | Inserir um número de cartão de crédito que não corresponde ao tipo selecionado. | |
| 4 | Preencher os campos obrigatórios restantes. | |
| 5 | Clicar em Pagar Agora. | |

---

### TC-PAY-006 — Tentar realizar o pagamento com formato de número de cartão de crédito inválido
ID: QA-PAY06
Prioridade: Alta
Objetivo: Garantir que o sistema valide a estrutura/formato do número do cartão de crédito.
Pré-condições:
Estar na página de pagamento.

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de pagamento. | O sistema exibe uma mensagem de erro para o número de cartão inválido e impede o pagamento. |
| 2 | Selecionar um tipo de cartão de crédito. | |
| 3 | Inserir um formato de número de cartão de crédito inválido. | |
| 4 | Preencher os campos obrigatórios restantes. | |
| 5 | Clicar em Pagar Agora. | |

---

### TC-PAY-007 — Tentar realizar o pagamento com cartão de crédito expirado
ID: QA-PAY07
Prioridade: Alta
Objetivo: Validar que o sistema rejeita cartões cuja data de validade já tenha expirado.
Pré-condições:
Estar na página de pagamento.

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de pagamento. | O sistema exibe uma mensagem de erro indicando que o cartão está expirado e impede o pagamento. |
| 2 | Selecionar um tipo de cartão de crédito. | |
| 3 | Inserir um número de cartão de crédito. | |
| 4 | Inserir uma data de validade expirada. | |
| 5 | Preencher os campos obrigatórios restantes. | |
| 6 | Clicar em Pagar Agora. | |

---

### TC-PAY-008 — Tentar realizar o pagamento com nome do portador do cartão inválido ou vazio
ID: QA-PAY08
Prioridade: Alta
Objetivo: Validar o comportamento do sistema ao receber dados incorretos ou ausentes no nome do portador.
Pré-condições:
Estar na página de pagamento.

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de pagamento. | O sistema exibe uma mensagem de validação para o nome do portador do cartão e impede o pagamento. |
| 2 | Selecionar um tipo de cartão de crédito. | |
| 3 | Inserir número e data de validade do cartão válidos. | |
| 4 | Deixar o nome do portador vazio ou inserir caracteres inválidos. | |
| 5 | Clicar em Pagar Agora. | |

---

### TC-PAY-009 — Múltiplos cliques no botão Pagar Agora
ID: QA-PAY09
Prioridade: Média
Objetivo: Validar a prevenção de requisições duplicadas (duplo clique) no botão de submissão de pagamento.
Pré-condições:
Estar na página de pagamento com dados válidos preenchidos.

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de pagamento. | O sistema processa o pagamento apenas uma vez e impede envios duplicados. |
| 2 | Preencher todos os campos obrigatórios com dados válidos. | |
| 3 | Clicar em Pagar Agora várias vezes rapidamente. | |

---

### TC-PAY-010 — Tentar acessar a página de pagamento diretamente via URL sem concluir as etapas anteriores
ID: QA-PAY10
Prioridade: Alta
Objetivo: Validar as regras de segurança e controle de fluxo impedindo o acesso direto à tela de pagamento por URL.
Pré-condições:
Estar logado, mas sem concluir as etapas de seleção de voo e dados do passageiro.

| Passo | Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| 1 | Inserir diretamente a URL da página de pagamento no navegador. | URL de *payment* | O sistema deve bloquear o acesso direto, exibir uma mensagem de erro de acesso não autorizado ou redirecionar o usuário para o início do fluxo. |
