# Login – Casos de Teste

## Cenários Válidos

### TC-LOGIN-001
**Título:** Autenticação com credenciais válidas

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de login. | O usuário é autenticado com sucesso e redirecionado para a página inicial. |
| 2 | Inserir nome de usuário e senha válidos. | |
| 3 | Clicar no botão de Login. | |

---

## Cenários Inválidos

### TC-LOGIN-002
**Título:** Tentativa de login com campos obrigatórios vazios

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de login. | O sistema exibe uma mensagem de validação indicando os campos obrigatórios. |
| 2 | Deixar os campos de usuário e senha vazios. | |
| 3 | Clicar no botão de Login. | |

---

### TC-LOGIN-003
**Título:** Tentativa de login com credenciais inválidas

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de login. | O sistema exibe uma mensagem de erro e nega o acesso. |
| 2 | Inserir nome de usuário ou senha inválidos. | |
| 3 | Clicar no botão de Login. | |

---

### TC-LOGIN-004
**Título:** Tentativa de login com usuário vazio e senha válida

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de login. | O sistema exibe uma mensagem de validação para o campo de usuário. |
| 2 | Deixar o campo de usuário vazio. | |
| 3 | Inserir uma senha válida. | |
| 4 | Clicar no botão de Login. | |

---

### TC-LOGIN-005
**Título:** Tentativa de login com usuário válido e senha vazia

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de login. | O sistema exibe uma mensagem de validação para o campo de senha. |
| 2 | Inserir um nome de usuário válido. | |
| 3 | Deixar a senha vazia. | |
| 4 | Clicar no botão de Login. | |
