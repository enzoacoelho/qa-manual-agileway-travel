# Booking – Passenger Details

# Reserva – Detalhes do Passageiro

## Cenários Válidos

### TC-BK-001
**Título:** Inserir nome e sobrenome válidos do passageiro

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de detalhes do passageiro após selecionar um voo. | Os detalhes do passageiro são aceitos e o usuário é redirecionado para a página de pagamento. |
| 2 | Inserir um primeiro nome válido. | |
| 3 | Inserir um sobrenome válido. | |
| 4 | Clicar em Continuar. | |

---

## Cenários Inválidos

### TC-BK-002
**Título:** Inserir caracteres inválidos nos campos de nome do passageiro

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de detalhes do passageiro. | O sistema exibe mensagem de validação e impede o avanço. |
| 2 | Inserir caracteres inválidos nos campos de primeiro nome e/ou sobrenome. | |
| 3 | Clicar em Continuar. | |

---

### TC-BK-003
**Título:** Tentar prosseguir com campos obrigatórios vazios

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de detalhes do passageiro. | O sistema exibe mensagem de validação para os campos obrigatórios e não permite o avanço. |
| 2 | Deixar o primeiro nome e/ou sobrenome vazios. | |
| 3 | Clicar em Continuar. | |
