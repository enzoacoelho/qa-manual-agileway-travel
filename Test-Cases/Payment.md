# Pagamento – Casos de Teste

## Cenários Válidos

### TC-PAY-001 — Concluir o pagamento com dados de cartão de crédito válidos
* **ID:** QA-PAY01
* **Prioridade:** Alta
* **Objetivo:** Validar o processamento bem-sucedido de um pagamento utilizando dados de cartão de crédito válidos.
* **Pré-condições:** Estar na página de pagamento após preencher corretamente os detalhes do passageiro.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Acessar a página de pagamento após concluir os detalhes do passageiro. | URL de pagamento / Sessão ativa | Detalhes do voo e valores são exibidos na tela, junto ao formulário para inserir os dados do cartão de crédito. |
| **2** | Selecionar o tipo de cartão de crédito. | Checkbox / Radio do cartão | O tipo/bandeira do cartão fica visivelmente selecionado na interface. |
| **3** | Inserir um número de cartão de crédito válido. | **Card Number**: `Número válido` | O número é preenchido corretamente no campo correspondente. |
| **4** | Inserir uma data de validade válida. | **Expiration**: `MM/AA válido` | A data de validade é aceita pelo formato do campo. |
| **5** | Inserir o nome do portador do cartão válido. | **Cardholder Name**: `Nome válido` | O nome do portador é preenchido sem erros de validação. |
| **6** | Clicar em Pagar Agora (Pay Now). | Botão: `Pay Now` | Confirmação de pagamento realizada com sucesso, exibindo os detalhes da compra e o *Booking number* na tela. |

---

## Cenários Inválidos

### TC-PAY-002 — Tentar realizar o pagamento com todos os campos obrigatórios vazios
* **ID:** QA-PAY02
* **Prioridade:** Média
* **Objetivo:** Garantir que o sistema bloqueie o pagamento e exiba validações quando nenhum campo for preenchido.
* **Pré-condições:** Estar na página de pagamento.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Acessar a página de pagamento com todos os campos em branco. | *Nenhum* | A página de pagamento é exibida com os campos prontos para preenchimento. |
| **2** | Clicar no botão `Pay Now` (Pagar Agora) sem preencher nenhum dado. | Botão: `Pay Now` | O sistema exibe mensagens de validação para os campos obrigatórios e impede o envio do pagamento. |

---

### TC-PAY-006 — Tentar realizar o pagamento com formato de número de cartão de crédito inválido
* **ID:** QA-PAY06
* **Prioridade:** Alta
* **Objetivo:** Garantir que o sistema valide a estrutura/formato do número do cartão de crédito.
* **Pré-condições:** Estar na página de pagamento.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Acessar a página de pagamento. | URL de pagamento | A tela de pagamento é exibida. |
| **2** | Selecionar um tipo de cartão de crédito. | Tipo de cartão selecionado | Bandeira definida. |
| **3** | Inserir um formato de número de cartão de crédito inválido (ex: letras ou dígitos insuficientes). | **Card Number**: `1234-abcd` | O valor inválido é inserido no campo. |
| **4** | Preencher os campos obrigatórios restantes com dados válidos. | Validade e Nome válidos | Demais campos preenchidos. |
| **5** | Clicar no botão `Pay Now` (Pagar Agora). | Botão: `Pay Now` | O sistema exibe uma mensagem de erro para o formato de número de cartão inválido e impede o pagamento. |

---

### TC-PAY-007 — Tentar realizar o pagamento com cartão de crédito expirado
* **ID:** QA-PAY07
* **Prioridade:** Alta
* **Objetivo:** Validar que o sistema rejeita cartões cuja data de validade já tenha expirado.
* **Pré-condições:** Estar na página de pagamento.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Acessar a página de pagamento. | URL de pagamento | A tela de pagamento é exibida. |
| **2** | Selecionar um tipo de cartão de crédito. | Tipo de cartão selecionado | Bandeira definida. |
| **3** | Inserir um número de cartão de crédito válido. | Número válido | Campo de cartão preenchido. |
| **4** | Inserir uma data de validade já expirada (passada). | **Expiration**: `12/22` (ou data anterior à atual) | Data expirada inserida no campo. |
| **5** | Preencher os campos obrigatórios restantes com dados válidos. | Nome do portador válido | Demais campos preenchidos. |
| **6** | Clicar no botão `Pay Now` (Pagar Agora). | Botão: `Pay Now` | O sistema exibe uma mensagem de erro indicando que o cartão está expirado e impede o pagamento. |

---

### TC-PAY-009 — Múltiplos cliques no botão Pagar Agora
* **ID:** QA-PAY09
* **Prioridade:** Alta
* **Objetivo:** Validar a prevenção de requisições duplicadas (duplo clique) no botão de submissão de pagamento.
* **Pré-condições:** Estar na página de pagamento com dados válidos preenchidos.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Acessar a página de pagamento após concluir as etapas anteriores. | URL de pagamento / Sessão ativa | A página de pagamento é exibida com todos os campos habilitados. |
| **2** | Preencher todos os campos obrigatórios do formulário de pagamento com dados válidos. | **Cartão**: Válido<br>**Validade**: Válida<br>**Nome**: Válido | Os campos são preenchidos corretamente e o botão de submissão fica pronto para uso. |
| **3** | Clicar no botão `Pay Now` (Pagar Agora) várias vezes rapidamente em sequência. | Botão: `Pay Now` | O sistema processa a transação de pagamento apenas uma única vez e bloqueia/ignora os cliques duplicados, evitando cobranças em duplicidade. |

---

### TC-PAY-010 — Tentar acessar a página de pagamento diretamente via URL sem concluir as etapas anteriores
* **ID:** QA-PAY10
* **Prioridade:** Alta
* **Objetivo:** Validar as regras de segurança e controle de fluxo impedindo o acesso direto à tela de pagamento por URL.
* **Pré-condições:** Estar logado, mas sem concluir as etapas de seleção de voo e dados do passageiro.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Inserir diretamente a URL da página de pagamento no navegador sem passar pelo fluxo regular. | URL de *payment* (ex: `/flights/passenger/...`) | O sistema processa a requisição direta de URL sem validação prévia de etapas. |
| **2** | Submeter a navegação direta e verificar o comportamento de segurança. | Ação de acesso via URL | O sistema deve bloquear o acesso direto, exibir uma mensagem de erro de acesso não autorizado ou redirecionar obrigatoriamente o usuário para o início do fluxo. |
