# Booking – Passenger Details

## Cenários Válidos

### TC-BK-001
**Título:** Inserir nome e sobrenome válidos do passageiro

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de detalhes do passageiro após selecionar um voo. | Os detalhes do passageiro são aceitos e o usuário é redirecionado para a página de pagamento. |
| 2 | Inserir um primeiro nome válido. | |
| 3 | Inserir um sobrenome válido. | |
| 4 | Clicar em Next. | |

---

### TC-BK-004
**Título:** Inserir nomes com limites máximos ou mínimos de caracteres válidos

| Passo | Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| 1 | Inserir nome e sobrenome com limites extremos permitidos. | **First name**: `A`, **Last name**: `Smith-Jones` | O sistema deve aceitar e processar corretamente, ou aplicar a regra de validação esperada para nomes curtos. |
| 2 | Clicar em Next. | Botão: `Next` | Transição bem-sucedida para a próxima etapa. |

---

### TC-BK-005
**Título:** Verificar a integridade e exibição das informações do voo selecionado

| Passo | Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| 1 | Checar o cabeçalho/resumo da rota na página de Passenger Details. | Informações da viagem na tela | O resumo deve exibir exatamente a rota e a data escolhidas anteriormente sem divergências. |

---

## Cenários Inválidos

### TC-BK-002
**Título:** Inserir caracteres inválidos nos campos de nome do passageiro

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de detalhes do passageiro. | O sistema exibe mensagem de validação e impede o avanço. |
| 2 | Inserir caracteres inválidos nos campos de primeiro nome e/ou sobrenome. | |
| 3 | Clicar em Next. | |

---

### TC-BK-003
**Título:** Tentar prosseguir com campos obrigatórios vazios

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de detalhes do passageiro. | O sistema exibe mensagem de validação para os campos obrigatórios e não permite o avanço. |
| 2 | Deixar o primeiro nome e/ou sobrenome vazios. | |
| 3 | Clicar em Next. | |

---

### TC-BK-006
**Título:** Tentar acessar a página de Passenger Details diretamente via URL sem selecionar um voo

| Passo | Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| 1 | Inserir diretamente a URL da etapa de passageiro no navegador. | URL de *booking* | O sistema deve bloquear a ação, exibir erro ou redirecionar o usuário de volta para a tela de seleção de voos. |

---

### TC-BK-007
**Título:** Validar comportamento ao tentar usar números ou caracteres especiais nos campos de nome

| Passo | Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| 1 | Inserir números ou símbolos nos campos de nome. | **First name**: `John123`, **Last name**: `@Doe` | O sistema deve exibir mensagem de erro de validação e impedir o avanço ao clicar em Next. |
