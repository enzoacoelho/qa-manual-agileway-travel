# Flight Search – Test Cases

# Busca de Voos – Casos de Teste

## Cenários Válidos

### TC-FS-001
**Título:** Selecionar viagem de ida e volta com datas válidas

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de busca de voos. | Os voos disponíveis são exibidos automaticamente após o preenchimento dos critérios de busca, permitindo que o usuário selecione um voo e prossiga para a próxima etapa. |
| 2 | Selecionar o tipo de viagem como Ida e Volta (Return). | |
| 3 | Inserir origem e destino válidos. | |
| 4 | Selecionar datas válidas de ida e volta. | |
| 5 | Observar os voos disponíveis exibidos automaticamente. | |
| 6 | Selecionar um voo disponível. | |
| 7 | Clicar em Continuar. | |

---

### TC-FS-002
**Título:** Selecionar viagem de apenas ida com data válida

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de busca de voos. | Os voos são exibidos automaticamente e o usuário pode prosseguir com a seleção de um voo de apenas ida. |
| 2 | Selecionar o tipo de viagem como Apenas Ida (One-way). | |
| 3 | Inserir origem e destino válidos. | |
| 4 | Selecionar uma data de ida válida. | |
| 5 | Observar os voos disponíveis exibidos automaticamente. | |
| 6 | Selecionar um voo disponível. | |
| 7 | Clicar em Continuar. | |

---

### TC-FS-003
**Título:** Selecionar viagem de ida e volta com a mesma data de partida e retorno

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de busca de voos. | O sistema permite a seleção do voo quando as datas de ida e volta são iguais. |
| 2 | Selecionar o tipo de viagem como Ida e Volta. | |
| 3 | Inserir origem e destino válidos. | |
| 4 | Selecionar a mesma data para partida e retorno. | |
| 5 | Observar os voos disponíveis exibidos automaticamente. | |
| 6 | Selecionar um voo disponível. | |
| 7 | Clicar em Continuar. | |

---

### TC-FS-004
**Título:** Verificar se o tipo de viagem padrão é "Ida e Volta"

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de busca de voos. | A opção de viagem de ida e volta vem selecionada por padrão. |

---

### TC-FS-005
**Título:** Verificar se o botão Continuar fica habilitado quando todos os campos obrigatórios são preenchidos

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de busca de voos. | O botão Continuar fica habilitado após a seleção de um voo. |
| 2 | Preencher todos os campos obrigatórios com dados válidos. | |
| 3 | Observar os voos disponíveis exibidos automaticamente. | |
| 4 | Selecionar um voo disponível. | |

---

### TC-FS-006
**Título:** Selecionar voo em versões responsivas

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de busca de voos em diferentes tamanhos de tela. | A seleção de voos funciona corretamente em layouts responsivos. |
| 2 | Preencher todos os campos obrigatórios. | |
| 3 | Observar os voos disponíveis exibidos automaticamente. | |
| 4 | Selecionar um voo disponível. | |

---

## Cenários Inválidos

### TC-FS-007
**Título:** Tentar prosseguir sem selecionar um voo

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de busca de voos. | O sistema impede o avanço e exibe uma mensagem de validação. |
| 2 | Preencher todos os campos obrigatórios. | |
| 3 | Não selecionar nenhum voo. | |
| 4 | Tentar clicar em Continuar. | |

---

### TC-FS-008
**Título:** Verificar se os voos não são exibidos quando os campos obrigatórios estão vazios

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de busca de voos. | Os voos disponíveis não são exibidos até que todos os campos obrigatórios sejam preenchidos. |
| 2 | Deixar um ou mais campos obrigatórios vazios. | |

---

### TC-FS-009
**Título:** Selecionar mesma origem e destino com a mesma data de ida e volta

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de busca de voos. | O sistema impede a busca de voos devido a uma configuração de rota inválida. |
| 2 | Inserir a mesma cidade para origem e destino. | |
| 3 | Selecionar a mesma data para partida e retorno. | |

---

### TC-FS-010
**Título:** Selecionar viagem de ida e volta com data de retorno anterior à data de partida

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de busca de voos. | O sistema impede a seleção de data inválida e exibe uma mensagem de erro. |
| 2 | Selecionar o tipo de viagem como Ida e Volta. | |
| 3 | Inserir origem e destino válidos. | |
| 4 | Selecionar uma data de retorno anterior à data de partida. | |

---

### TC-FS-011
**Título:** Selecionar múltiplos voos ao mesmo tempo

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de busca de voos. | O sistema permite a seleção de apenas um voo por vez. |
| 2 | Preencher todos os campos obrigatórios. | |
| 3 | Observar os voos disponíveis exibidos automaticamente. | |
| 4 | Tentar selecionar mais de um voo. | |

---

### TC-FS-012
**Título:** Verificar se o campo de data de retorno fica oculto para viagens de apenas ida

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de busca de voos. | O campo de data de retorno não é exibido quando a viagem de apenas ida é selecionada. |
| 2 | Selecionar o tipo de viagem como Apenas Ida. | |
