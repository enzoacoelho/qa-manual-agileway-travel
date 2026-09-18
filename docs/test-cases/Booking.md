# Booking – Passenger Details

## Cenários Válidos

### QA-BK01 — Realizar o booking com dados válidos com sucesso
* **ID:** QA-BK01
* **Prioridade:** Alta
* **Objetivo:** Validar o avanço no fluxo preenchendo o primeiro nome e sobrenome válidos do passageiro.
* **Pré-condições:** Estar na página de detalhes do passageiro após selecionar um voo.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Acessar a página de detalhes do passageiro após selecionar um voo. | URL da etapa de *booking* / Voo selecionado | Informações do voo selecionado e o formulário para inserir informações do passageiro são exibidos na tela. |
| **2** | Inserir um primeiro nome válido. | **First name**: `Nome válido` | O campo é preenchido sem nenhum problema. |
| **3** | Inserir um sobrenome válido. | **Last name**: `Sobrenome válido` | O campo é preenchido sem nenhum problema. |
| **4** | Clicar no botão `Next`. | Botão: `Next` | A etapa do fluxo de pagamento é exibida na tela. |

---

### QA-BK02 — Verificar a integridade e exibição das informações do voo selecionado
* **ID:** QA-BK02
* **Prioridade:** Média
* **Objetivo:** Garantir que os dados do voo escolhido na tela anterior sejam exibidos corretamente no resumo da página de passageiro.
* **Pré-condições:** Ter selecionado um voo específico na tela anterior.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Checar o cabeçalho/resumo da rota na página de *Passenger Details*. | Informações da viagem na tela | O resumo deve exibir exatamente a rota e a data escolhidas anteriormente sem divergências. |

---

## Cenários Inválidos

### QA-BK03 — Inserir caracteres inválidos nos campos de nome do passageiro
* **ID:** QA-BK03
* **Prioridade:** Média
* **Objetivo:** Garantir que o sistema rejeite caracteres inválidos nos campos de nome do passageiro.
* **Pré-condições:** Estar na página de detalhes do passageiro.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Acessar a página de detalhes do passageiro. | URL de *booking* | A tela de detalhes do passageiro é exibida. |
| **2** | Inserir caracteres inválidos nos campos de primeiro nome e/ou sobrenome. | **Name**: Caracteres inválidos/símbolos | Os dados inadequados são informados nos inputs. |
| **3** | Clicar no botão `Next`. | Botão: `Next` | O sistema exibe mensagem de validação e impede o avanço. |

---

### QA-BK04 — Tentar prosseguir com campos obrigatórios vazios
* **ID:** QA-BK04
* **Prioridade:** Média
* **Objetivo:** Validar que o sistema impede o avanço quando os campos obrigatórios de nome ficam vazios.
* **Pré-condições:** Estar na página de detalhes do passageiro.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Acessar a página de detalhes do passageiro. | URL de *booking* | A tela de cadastro de passageiro é exibida. |
| **2** | Deixar o primeiro nome e/ou sobrenome vazios. | Campos em branco | Os inputs obrigatórios não recebem dados. |
| **3** | Clicar no botão `Next`. | Botão: `Next` | O sistema exibe mensagem de validação para os campos obrigatórios e não permite o avanço. |

---

### QA-BK05 — Acessar a página de Passenger Details diretamente via URL sem selecionar um voo
* **ID:** QA-BK05
* **Prioridade:** Alta
* **Objetivo:** Validar as regras de controle de fluxo e segurança impedindo o acesso direto por URL sem seleção prévia de voo.
* **Pré-condições:** Estar logado, mas sem nenhum voo selecionado no fluxo atual.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Inserir diretamente a URL da etapa de passageiro no navegador. | URL de *booking* (ex: `flights/passenger/118028`) | A requisição direta da rota restrita é disparada sem passagem pelo fluxo de voos. |
| **2** | Submeter a navegação direta e verificar o comportamento. | Ação de acesso via URL | O sistema deve bloquear a ação, exibir erro ou redirecionar o usuário de volta para a tela de seleção de voos. |
