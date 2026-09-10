# Flight Search – Casos de Teste

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

---

### TC-FS-013
**Título:** Tentar selecionar a mesma cidade para origem e destino

| Passo | Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| 1 | Selecionar a mesma cidade nos campos de origem e destino. | **From**: `City A`, **To**: `City A` | Campos preenchidos com o mesmo valor. |
| 2 | Tentar prosseguir com a busca ou avanço. | Botão: `Continue` | O sistema impede o avanço ou exibe mensagem de validação de rota inválida. |

---

### TC-FS-014
**Título:** Tentar selecionar data de partida retroativa (passada)

| Passo | Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| 1 | Selecionar uma data de partida anterior à data atual do sistema. | **Departing**: Data no passado (ex: dia anterior ao atual) | Data selecionada no componente. |
| 2 | Tentar preencher os demais campos obrigatórios e avançar. | Demais campos válidos | O sistema impede a seleção da data retroativa ou bloqueia a submissão com erro. |

---

### TC-FS-015
**Título:** Validação de comportamento ao alternar o tipo de viagem com dados preenchidos

| Passo | Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| 1 | Preencher a origem, destino e a data de retorno. | Campos preenchidos para ida e volta. | Campos preenchidos corretamente. |
| 2 | Alternar o tipo de viagem para *One way*. | Radio button: `One way` | O campo de retorno é ocultado ou limpo, mantendo a estabilidade da interface e dos dados da ida. |

---

### TC-FS-016
**Título:** Tentar acessar a página de busca de voos sem autenticação (Acesso Direto via URL)

| Passo | Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| 1 | Inserir diretamente a URL protegida no navegador. | URL: `https://travel.agileway.net/flights/start` | O sistema deve bloquear o acesso e redirecionar o usuário para a tela de login ou exibir uma mensagem de erro de acesso negado/não autorizado. |

---

### TC-FS-017
**Título:** Validar persistência da sessão após atualização da página (F5)

| Passo | Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| 1 | Preencher os campos de origem, destino e selecionar um tipo de viagem. | Origem e Destino válidos | Campos preenchidos corretamente. |
| 2 | Atualizar a página do navegador (pressionar F5). | Ação de Refresh | O sistema deve manter o usuário logado e restaurar os campos ou redefinir para o estado padrão de forma controlada, sem quebrar a aplicação. |

---

### TC-FS-018
**Título:** Validar comportamento com campos de seleção de Origem e Destino vazios no carregamento inicial

| Passo | Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| 1 | Inspecionar os campos `From` e `To` logo após carregar a tela. | Visualização dos selects | Os campos devem vir com uma opção padrão pré-selecionada (ou vazia com placeholder) e os voos não devem ser listados incorretamente até que critérios válidos estejam definidos. |

---

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
