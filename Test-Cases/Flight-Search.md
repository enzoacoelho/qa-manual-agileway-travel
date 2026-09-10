# Flight Search – Casos de Teste (Adicionais)

## Cenários Inválidos e de Consistência

### TC-FS-013 — Tentar selecionar a mesma cidade para origem e destino
* **ID:** QA-FS13
* **Prioridade:** Média
* **Objetivo:** Verificar se o sistema impede a seleção de rotas inválidas onde a origem e o destino são idênticos.
* **Pré-condições:** 
  * Estar na página de busca de voos.

| Passo | Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Selecionar a mesma cidade nos campos de origem e destino. | **From**: `City A`, **To**: `City A` | Campos preenchidos com o mesmo valor. |
| **2** | Tentar prosseguir com a busca ou avanço. | Botão: `Continue` | O sistema impede o avanço ou exibe mensagem de validação de rota inválida. |

---

### TC-FS-014 — Tentar selecionar data de partida retroativa (passada)
* **ID:** QA-FS14
* **Prioridade:** Alta
* **Objetivo:** Garantir que o sistema bloqueie o agendamento de voos com datas anteriores ao dia atual.
* **Pré-condições:** 
  * Estar na página de busca de voos.

| Passo | Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Selecionar uma data de partida anterior à data atual do sistema. | **Departing**: Data no passado (ex: dia anterior ao atual) | Data selecionada no componente. |
| **2** | Tentar preencher os demais campos obrigatórios e avançar. | Demais campos válidos | O sistema impede a seleção da data retroativa ou bloqueia a submissão com erro. |

---

### TC-FS-015 — Validação de comportamento ao alternar o tipo de viagem com dados preenchidos
* **ID:** QA-FS15
* **Prioridade:** Baixa
* **Objetivo:** Verificar a integridade dos campos ao alternar entre os tipos de viagem (*Return* e *One way*).
* **Pré-condições:** 
  * Estar na página de busca de voos com a opção *Return* selecionada.

| Passo | Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Preencher a origem, destino e a data de retorno. | Campos preenchidos para ida e volta. | Campos preenchidos corretamente. |
| **2** | Alternar o tipo de viagem para *One way*. | Radio button: `One way` | O campo de retorno é ocultado ou limpo, mantendo a estabilidade da interface e dos dados da ida. |
