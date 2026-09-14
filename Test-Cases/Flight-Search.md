# Flight Search – Casos de Teste

## Cenários Válidos

### TC-FS-001 — Selecionar viagem de ida e volta com datas válidas
* **ID:** QA-FS01
* **Prioridade:** Alta
* **Objetivo:** Validar a busca e seleção bem-sucedida de um voo de ida e volta utilizando datas válidas.
* **Pré-condições:** Estar na página de busca de voos logado no sistema.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Acessar a página de busca de voos. | URL da aplicação | Apenas o formulário de busca fica visível na tela; os voos só ficam disponíveis após o preenchimento do formulário. |
| **2** | Selecionar o tipo de viagem como Ida e Volta (Return). | Radio button: `Return` | Os campos de origem e destino ficam visíveis na tela para escolha do trajeto. |
| **3** | Selecionar origem e destino válidos. | **From** / **To**: Cidades válidas | Os campos ficam preenchidos com os locais selecionados. |
| **4** | Selecionar datas válidas de ida e volta. | Datas futuras válidas | Os voos disponíveis para a rota e datas selecionadas são exibidos abaixo automaticamente. |
| **5** | Observar os voos disponíveis exibidos automaticamente. | Listagem de voos | O checkbox para selecionar um dos voos fica visível ao lado de cada opção. |
| **6** | Selecionar um voo disponível. | Checkbox de voo | O voo escolhido fica marcado. |
| **7** | Clicar em Continuar. | Botão: `Continue` | O formulário de busca desaparece e a etapa de *Booking* se inicia com o formulário de dados do passageiro. |

---

### TC-FS-002 — Selecionar viagem de apenas ida com data válida
* **ID:** QA-FS02
* **Prioridade:** Alta
* **Objetivo:** Validar a busca e seleção de um voo de apenas ida (*one-way*) com dados válidos.
* **Pré-condições:** Estar na página de busca de voos logado no sistema.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Acessar a página de busca de voos. | URL da aplicação | Apenas o formulário de busca fica visível na tela. |
| **2** | Selecionar o tipo de viagem como One-Way (Apenas Ida). | Radio button: `One-way` | Os campos de origem e destino são exibidos na interface. |
| **3** | Selecionar origem e destino válidos. | **From** / **To**: Cidades válidas | Os campos refletem os locais escolhidos. |
| **4** | Selecionar datas válidas de ida. | Data de partida válida | Os voos correspondentes à rota de apenas ida são exibidos logo abaixo. |
| **5** | Observar os voos disponíveis exibidos automaticamente. | Listagem de voos | Checkboxes de seleção ficam visíveis ao lado de cada opção de voo. |
| **6** | Selecionar um voo disponível. | Checkbox de voo | O voo é selecionado. |
| **7** | Clicar em Continuar. | Botão: `Continue` | A busca é ocultada e o fluxo avança para a etapa de *Booking*. |

---

### TC-FS-003 — Selecionar viagem de ida e volta com a mesma data de partida e retorno (Cidades próximas e horários compatíveis)
* **ID:** QA-FS03
* **Prioridade:** Média
* **Objetivo:** Validar o comportamento do sistema ao selecionar datas de partida e retorno idênticas para uma viagem de ida e volta.
* **Pré-condições:** Estar na página de busca de voos logado no sistema.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Acessar a página de busca de voos. | URL da aplicação | A tela de busca de voos é carregada. |
| **2** | Selecionar o tipo de viagem como Ida e Volta. | Radio button: `Return` | Os campos de datas de ida e retorno são exibidos. |
| **3** | Inserir origem e destino válidos. | **From** / **To**: Cidades válidas | Rota definida com sucesso. |
| **4** | Selecionar a mesma data exata para partida e retorno. | **Departing** / **Returning**: Mesma data | Os campos recebem a data idêntica. |
| **5** | Observar os voos disponíveis exibidos automaticamente. | Listagem de voos | O sistema exibe os voos correspondentes à consulta informada. |
| **6** | Selecionar um voo disponível. | Checkbox de voo | O voo é marcado pelo usuário. |
| **7** | Clicar em Continuar. | Botão: `Continue` | O sistema processa a seleção e permite avançar para a próxima etapa. |

---

### TC-FS-004 — Verificar se o tipo de viagem padrão é "Ida e Volta"
* **ID:** QA-FS04
* **Prioridade:** Baixa
* **Objetivo:** Validar se a opção padrão de tipo de viagem ao carregar a tela é "Ida e Volta".
* **Pré-condições:** Estar na página de busca de voos recém-carregada.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Acessar a página de busca de voos recém-carregada. | URL limpa da aplicação | A opção de viagem de ida e volta (*Return*) vem selecionada por padrão na interface. |

---

## Cenários Inválidos

### TC-FS-005 — Tentativa de prosseguir para o booking sem selecionar um voo
* **ID:** QA-FS07
* **Prioridade:** Média
* **Objetivo:** Validar que o sistema bloqueia o avanço caso o usuário tente prosseguir sem escolher um voo da lista.
* **Pré-condições:** Estar na página de busca de voos com os campos preenchidos.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Acessar a página de busca de voos. | URL da aplicação | A página de busca é carregada. |
| **2** | Preencher todos os campos obrigatórios. | Dados válidos inseridos | Os voos correspondentes são listados na tela. |
| **3** | Não selecionar nenhum voo da listagem. | Nenhum checkbox marcado | A listagem permanece sem seleções ativas. |
| **4** | Tentar clicar em Continuar. | Botão: `Continue` | O sistema impede o avanço e exibe uma mensagem de validação exigindo a escolha de um voo. |

---

### TC-FS-006 — Verificar se os voos não são exibidos quando os campos obrigatórios estão vazios
* **ID:** QA-FS08
* **Prioridade:** Média
* **Objetivo:** Garantir que a listagem de voos permaneça oculta ou vazia se houver campos obrigatórios incompletos.
* **Pré-condições:** Estar na página de busca de voos no carregamento inicial.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Acessar a página de busca de voos. | Carregamento inicial | A tela é aberta com os campos prontos para entrada de dados. |
| **2** | Deixar um ou mais campos obrigatórios vazios. | Campos incompletos | Os voos disponíveis não são exibidos na tela enquanto houver pendências nos inputs obrigatórios. |

---

### TC-FS-007 — Selecionar mesma origem e destino com a mesma data de ida e volta
* **ID:** QA-FS09
* **Prioridade:** Média
* **Objetivo:** Validar a restrição de rotas onde a origem e o destino são idênticos.
* **Pré-condições:** Estar na página de busca de voos.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Acessar a página de busca de voos. | URL da aplicação | A tela de busca é exibida. |
| **2** | Inserir a mesma cidade para origem e destino. | **From** e **To**: Mesma cidade | Os campos assumem o mesmo valor. |
| **3** | Selecionar a mesma data para partida e retorno. | Datas idênticas informadas | O sistema processa os parâmetros inválidos de rota. |
| **4** | Tentar efetuar a busca ou prosseguir. | Ação de submissão | O sistema impede a busca de voos devido à configuração de rota inválida e emite alerta. |

---

### TC-FS-008 — Selecionar viagem de ida e volta com data de retorno anterior à data de partida
* **ID:** QA-FS10
* **Prioridade:** Média
* **Objetivo:** Garantir que o sistema rejeite períodos de viagem ilógicos (retorno antes da ida).
* **Pré-condições:** Estar na página de busca de voos.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Acessar a página de busca de voos. | URL da aplicação | A interface de busca é carregada. |
| **2** | Selecionar o tipo de viagem como Ida e Volta. | Radio button: `Return` | Campos de data de ida e volta habilitados. |
| **3** | Inserir origem e destino válidos. | Rota válida preenchida | Campos de localidade definidos. |
| **4** | Selecionar uma data de retorno anterior à data de partida. | **Returning** < **Departing** | O período cronológico invertido é inserido nos seletores de data. |
| **5** | Tentar submeter ou avançar a busca. | Ação de consulta | O sistema impede a seleção da data inválida e exibe uma mensagem de erro correspondente. |

---

### TC-FS-009 — Selecionar múltiplos voos ao mesmo tempo
* **ID:** QA-FS11
* **Prioridade:** Média
* **Objetivo:** Validar que o sistema permite selecionar apenas um voo por transação de compra.
* **Pré-condições:** Estar na tela de resultados de voos preenchida.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Acessar a página de busca de voos. | URL da aplicação | A tela de busca é exibida. |
| **2** | Preencher todos os campos obrigatórios. | Dados válidos inseridos | Os voos são listados na interface. |
| **3** | Observar os voos disponíveis exibidos automaticamente. | Listagem de voos | Várias opções de voo aparecem na tela. |
| **4** | Tentar selecionar mais de um voo simultaneamente. | Múltiplos checkboxes marcados | O sistema permite a seleção de apenas um voo por vez (comportamento de exclusividade mútua/radio). |

---

### TC-FS-010 — Verificar se o campo de data de retorno fica oculto para viagens de apenas ida
* **ID:** QA-FS12
* **Prioridade:** Média
* **Objetivo:** Validar a alteração dinâmica da interface ao alternar para o tipo de viagem *One-way*.
* **Pré-condições:** Estar na página de busca de voos.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Acessar a página de busca de voos. | URL da aplicação | Os campos de ida e volta encontram-se visíveis no padrão inicial. |
| **2** | Selecionar o tipo de viagem como Apenas Ida. | Radio button: `One-way` | O evento de alteração de tipo de viagem é disparado. |
| **3** | Observar a seção de datas. | Interface dinâmica | O campo de data de retorno deixa de ser exibido na tela, ocultando-se adequadamente. |

---

### TC-FS-011 — Validar restrição de seleção de mesma cidade para Origem (From) e Destino (To)
* **ID:** QA-FS13
* **Prioridade:** Média
* **Objetivo:** Garantir que o sistema impeça a busca de voos quando a cidade de origem e a cidade de destino forem idênticas.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Selecionar a mesma cidade nos campos de origem e destino. | **From**: `City A`, **To**: `City A` | Os campos ficam preenchidos com o mesmo valor informado. |
| **2** | Tentar prosseguir com a busca ou avanço. | Botão: `Continue` ou busca automática | O sistema impede o avanço ou exibe mensagem de validação de rota inválida. |

---

### TC-FS-012 — Tentar selecionar data de partida retroativa (passada)
* **ID:** QA-FS14
* **Prioridade:** Média
* **Objetivo:** Impedir a seleção de datas retroativas no campo de partida.
* **Pré-condições:** Estar na página de busca de voos.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Selecionar uma data de partida anterior à data atual do sistema. | **Departing**: Data no passado (ex: dia anterior ao atual) | A data é inserida no componente de calendário. |
| **2** | Tentar preencher os demais campos obrigatórios e avançar. | Demais campos válidos | O sistema impede a seleção da data retroativa ou bloqueia a submissão com erro informativo. |

---

### TC-FS-013 — Validação de comportamento ao alternar o tipo de viagem com dados preenchidos
* **ID:** QA-FS15
* **Prioridade:** Média
* **Objetivo:** Verificar se os dados e o layout se comportam de maneira estável ao trocar o tipo de viagem após preenchimento parcial.
* **Pré-condições:** Estar na página de busca de voos com dados preenchidos.

| Passo | Descrição da Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Preencher a origem, destino e a data de retorno. | Campos preenchidos para ida e volta | Os dados inseridos refletem corretamente na interface. |
| **2** | Alternar o tipo de viagem para *One way*. | Radio button: `One way` | O campo de retorno é ocultado ou limpo, mantendo a estabilidade da interface e preservando os dados da ida. |
