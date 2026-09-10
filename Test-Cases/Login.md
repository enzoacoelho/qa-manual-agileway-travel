# Autenticação (Login / Logout) – Casos de Teste

## Cenários Válidos

### TC-LOGIN-001 — Autenticação com credenciais válidas e persistência de sessão
* **ID:** QA-L01
* **Prioridade:** Alta
* **Objetivo:** Validar o login utilizando credenciais válidas e a opção de persistência de sessão.
* **Pré-condições:** 
  * O usuário deve estar cadastrado no sistema.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Acessar a página de login. | URL do sistema | Página de login carregada corretamente com os campos visíveis. |
| **2** | Inserir nome de usuário e senha válidos. | **User Name**: `agileway`, **Password**: `test$W1se` | Campos preenchidos corretamente. |
| **3** | Marcar a opção de lembrar sessão. | Checkbox: `Remember me` | Opção marcada. |
| **4** | Clicar no botão de acesso. | Botão: `Sign in` | Usuário autenticado com sucesso e redirecionado para a página inicial. |

---

### TC-LOGIN-002 — Encerramento de sessão (Logout) com sucesso
* **ID:** QA-L02
* **Prioridade:** Alta
* **Objetivo:** Validar o fluxo de encerramento de sessão do usuário autenticado.
* **Pré-condições:** 
  * O usuário deve estar logado no sistema.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Localizar e acionar a opção de encerramento de sessão. | Botão / Link: `Logout` | A sessão é encerrada de forma segura. |
| **2** | Verificar a tela exibida após a ação. | *Nenhum* | O usuário é redirecionado para a tela de login ou página inicial pública, sem acesso a dados protegidos. |

---

## Cenários Inválidos

### TC-LOGIN-003 — Tentativa de login com campos obrigatórios vazios
* **ID:** QA-L03
* **Prioridade:** Média
* **Objetivo:** Verificar o comportamento do sistema e o estado do botão de acesso ao manter os campos vazios.
* **Pré-condições:** 
  * Estar na página de login.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Manter os campos de usuário e senha vazios. | *Nenhum* | Campos vazios. |
| **2** | Tentar acionar o botão de acesso. | Botão: `Sign in` | O sistema exibe mensagens de validação e impede o acesso. |

---

### TC-LOGIN-004 — Tentativa de login com senha incorreta e usuário válido
* **ID:** QA-L04
* **Prioridade:** Alta
* **Objetivo:** Validar a recusa de acesso ao informar uma senha incorreta vinculada a um usuário existente.
* **Pré-condições:** 
  * Estar na página de login.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Inserir nome de usuário válido e senha incorreta. | **User Name**: `agileway`, **Password**: `senhaInvalida123` | Campos preenchidos. |
| **2** | Clicar no botão de acesso. | Botão: `Sign in` | O sistema exibe mensagem de erro de autenticação e nega o acesso. |

---

### TC-LOGIN-005 — Tentativa de login com usuário vazio e senha válida
* **ID:** QA-L05
* **Prioridade:** Média
* **Objetivo:** Validar a restrição de submissão ao omitir apenas o campo de usuário.
* **Pré-condições:** 
  * Estar na página de login.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Deixar o campo de usuário vazio e preencher a senha. | **User Name**: *(vazio)*, **Password**: `test$W1se` | Senha preenchida. |
| **2** | Clicar no botão de acesso. | Botão: `Sign in` | O sistema exibe mensagem de validação para o campo de usuário e impede o avanço. |

---

### TC-LOGIN-006 — Tentativa de login com usuário válido e senha vazia
* **ID:** QA-L06
* **Prioridade:** Média
* **Objetivo:** Validar a restrição de submissão ao omitir apenas o campo de senha.
* **Pré-condições:** 
  * Estar na página de login.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Preencher o usuário e deixar o campo de senha vazio. | **User Name**: `agileway`, **Password**: *(vazio)* | Usuário preenchido. |
| **2** | Clicar no botão de acesso. | Botão: `Sign in` | O sistema exibe mensagem de validação para o campo de senha e impede o avanço. |
