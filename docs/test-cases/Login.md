# Login / Logout – Casos de Teste

## Cenários Válidos

### QA-L01 — Autenticação com credenciais válidas com sucesso
* **ID:** QA-L01
* **Prioridade:** Alta
* **Objetivo:** Validar o login utilizando as credenciais padrão indicadas na interface.
* **Pré-condições:** 
  * Estar na página de login.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Inserir o nome de usuário válido. | **User Name**: `agileway` | Campo preenchido corretamente. |
| **2** | Inserir a senha válida. | **Password**: `test$W1se` | Campo preenchido corretamente. |
| **3** | Acionar o botão de acesso. | Botão: `Sign in` | Usuário autenticado com sucesso e redirecionado para a tela principal. |

---

### QA-L02 — Autenticação com a opção "Remember me" selecionada
* **ID:** QA-L02
* **Prioridade:** Baixa
* **Objetivo:** Validar o login marcando a opção de persistência de sessão.
* **Pré-condições:** 
  * Estar na página de login.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Preencher usuário e senha válidos. | **User Name**: `agileway`, **Password**: `test$W1se` | Campos preenchidos. |
| **2** | Marcar o checkbox de persistência. | Checkbox: `Remember me` | Opção marcada. |
| **3** | Acionar o botão de acesso. | Botão: `Sign in` | Login efetuado com sucesso considerando a preferência. |

---

### QA-L03 — Encerramento de sessão (Logout) com sucesso
* **ID:** QA-L03
* **Prioridade:** Alta
* **Objetivo:** Validar o fluxo de encerramento da sessão ativa do usuário.
* **Pré-condições:** 
  * O usuário deve estar autenticado no sistema.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Acionar a opção de encerramento de sessão. | Botão / Link: `Logout` | A sessão ativa é encerrada de forma segura. |
| **2** | Verificar o redirecionamento. | *Nenhum* | O usuário é redirecionado para a tela de login, sem acesso posterior às páginas protegidas. |

---

## Cenários Inválidos

### QA-L04 — Tentativa de login com campos obrigatórios vazios
* **ID:** QA-L04
* **Prioridade:** Média
* **Objetivo:** Verificar se o sistema impede o avanço ao tentar autenticar sem preencher os campos.
* **Pré-condições:** 
  * Estar na página de login.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Manter os campos de usuário e senha vazios. | *Nenhum* | Campos vazios. |
| **2** | Acionar o botão de acesso. | Botão: `Sign in` | O sistema exibe mensagem de validação e impede o acesso. |

---

### QA-L05 — Tentativa de login com senha incorreta
* **ID:** QA-L05
* **Prioridade:** Alta
* **Objetivo:** Validar a recusa de acesso ao informar uma senha inválida para o usuário.
* **Pré-condições:** 
  * Estar na página de login.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Inserir usuário válido e senha incorreta. | **User Name**: `agileway`, **Password**: `senhaErrada` | Campos preenchidos. |
| **2** | Acionar o botão de acesso. | Botão: `Sign in` | O sistema exibe mensagem de erro de autenticação e bloqueia o acesso. |

---

### QA-L06 — Tentativa de login com usuário inexistente
* **ID:** QA-L06
* **Prioridade:** Média
* **Objetivo:** Validar o comportamento do sistema ao tentar autenticar com um nome de usuário não cadastrado.
* **Pré-condições:** 
  * Estar na página de login.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Inserir nome de usuário inválido e senha válida. | **User Name**: `usuarioInvalido`, **Password**: `test$W1se` | Campos preenchidos. |
| **2** | Acionar o botão de acesso. | Botão: `Sign in` | O sistema exibe mensagem de erro informando falha na autenticação. |
