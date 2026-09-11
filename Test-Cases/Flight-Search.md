# Flight Search – Casos de Teste

## Cenários Válidos

### TC-FS-001 — Selecionar viagem de ida e volta com datas válidas
ID: QA-FS01

Prioridade: Alta

Objetivo: Validar a busca e seleção bem-sucedida de um voo de ida e volta utilizando datas válidas.

Pré-condições: Estar na página de busca de voos logado no sistema.

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de busca de voos. | Apenas formulário de busca visivel na tela, voos apenas ficam disponíveis após preencher formulário de busca |
| 2 | Selecionar o tipo de viagem como Ida e Volta (Return). | Campos From e To visíveis na tela para que o usuário escolha Origem e Destino de voo |
| 3 | Selecionar origem e destino válidos. | Campos From e To ficam preenchidos por origem e destino selecionados |
| 4 | Selecionar datas válidas de ida e volta. | Voos disponíveis para a origem/destino e datas são exibidas abaixo |
| 5 | Observar os voos disponíveis exibidos automaticamente. | Checkbox para selecionar um dos voos fica visível ao lado de cada opção |
| 6 | Selecionar um voo disponível. | |
| 7 | Clicar em Continuar. | Formulário de busca desaparece e etapa de Booking se inicia com um formulário para inserir dados do passageiro |

---

### TC-FS-002 — Selecionar viagem de apenas ida com data válida
ID: QA-FS02

Prioridade: Alta

Objetivo: Validar a busca e seleção de um voo de apenas ida (*one-way*) com dados válidos.

Pré-condições: Estar na página de busca de voos logado no sistema.

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de busca de voos. | Apenas formulário de busca visivel na tela, voos apenas ficam disponíveis após preencher formulário de busca |
| 2 | Selecionar o tipo de viagem como One-Way (Apenas Ida). | Campos From e To visíveis na tela para que o usuário escolha Origem e Destino de voo |
| 3 | Selecionar origem e destino válidos. | Campos From e To ficam preenchidos por origem e destino selecionados |
| 4 | Selecionar datas válidas de ida. | Voos disponíveis para a origem/destino e datas são exibidas abaixo |
| 5 | Observar os voos disponíveis exibidos automaticamente. | Checkbox para selecionar um dos voos fica visível ao lado de cada opção |
| 6 | Selecionar um voo disponível. | |
| 7 | Clicar em Continuar. | Formulário de busca desaparece e etapa de Booking se inicia com um formulário para inserir dados do passageiro |

---

### TC-FS-003 — Selecionar viagem de ida e volta com a mesma data de partida e retorno
ID: QA-FS03

Prioridade: Média

Objetivo: Validar o comportamento do sistema ao selecionar datas de partida e retorno idênticas para uma viagem de ida e volta.

Pré-condições: Estar na página de busca de voos logado no sistema.

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

### TC-FS-004 — Verificar se o tipo de viagem padrão é "Ida e Volta"
ID: QA-FS04

Prioridade: Baixa

Objetivo: Validar se a opção padrão de tipo de viagem ao carregar a tela é "Ida e Volta".

Pré-condições: Estar na página de busca de voos recém-carregada.

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de busca de voos. | A opção de viagem de ida e volta vem selecionada por padrão. |

---

### TC-FS-005 — Verificar se o botão Continuar fica habilitado quando todos os campos obrigatórios são preenchidos
ID: QA-FS05

Prioridade: Alta

Objetivo: Garantir que o botão de prosseguir só é ativado mediante o preenchimento correto e seleção de voo.

Pré-condições: Estar na página de busca de voos.

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de busca de voos. | O botão Continuar fica habilitado após a seleção de um voo. |
| 2 | Preencher todos os campos obrigatórios com dados válidos. | |
| 3 | Observar os voos disponíveis exibidos automaticamente. | |
| 4 | Selecionar um voo disponível. | |

---

### TC-FS-006 — Selecionar voo em versões responsivas
ID: QA-FS06

Prioridade: Média

Objetivo: Validar a funcionalidade de busca e seleção de voos em diferentes resoluções de tela.

Pré-condições: Estar acessando o sistema via dispositivo móvel ou em modo de simulação responsiva.

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de busca de voos em diferentes tamanhos de tela. | A seleção de voos funciona corretamente em layouts responsivos. |
| 2 | Preencher todos os campos obrigatórios. | |
| 3 | Observar os voos disponíveis exibidos automaticamente. | |
| 4 | Selecionar um voo disponível. | |

---

## Cenários Inválidos

### TC-FS-007 — Tentativa de prosseguir para o booking sem selecionar um voo
ID: QA-FS07

Prioridade: Média

Objetivo: Validar que o sistema bloqueia o avanço caso o usuário tente prosseguir sem escolher um voo da lista.

Pré-condições: Estar na página de busca de voos com os campos preenchidos.

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de busca de voos. | O sistema impede o avanço e exibe uma mensagem de validação. |
| 2 | Preencher todos os campos obrigatórios. | |
| 3 | Não selecionar nenhum voo. | |
| 4 | Tentar clicar em Continuar. | |

---

### TC-FS-008 — Verificar se os voos não são exibidos quando os campos obrigatórios estão vazios
ID: QA-FS08

Prioridade: Média

Objetivo: Garantir que a listagem de voos permaneça oculta ou vazia se houver campos obrigatórios incompletos.

Pré-condições: Estar na página de busca de voos no carregamento inicial.

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de busca de voos. | Os voos disponíveis não são exibidos até que todos os campos obrigatórios sejam preenchidos. |
| 2 | Deixar um ou mais campos obrigatórios vazios. | |

---

### TC-FS-009 — Selecionar mesma origem e destino com a mesma data de ida e volta
ID: QA-FS09

Prioridade: Média

Objetivo: Validar a restrição de rotas onde a origem e o destino são idênticos.

Pré-condições: Estar na página de busca de voos.

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de busca de voos. | O sistema impede a busca de voos devido a uma configuração de rota inválida. |
| 2 | Inserir a mesma cidade para origem e destino. | |
| 3 | Selecionar a mesma data para partida e retorno. | |

---

### TC-FS-010 — Selecionar viagem de ida e volta com data de retorno anterior à data de partida
ID: QA-FS10

Prioridade: Média

Objetivo: Garantir que o sistema rejeite períodos de viagem ilógicos (retorno antes da ida).

Pré-condições: Estar na página de busca de voos.

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de busca de voos. | O sistema impede a seleção de data inválida e exibe uma mensagem de erro. |
| 2 | Selecionar o tipo de viagem como Ida e Volta. | |
| 3 | Inserir origem e destino válidos. | |
| 4 | Selecionar uma data de retorno anterior à data de partida. | |

---

### TC-FS-011 — Selecionar múltiplos voos ao mesmo tempo
ID: QA-FS11

Prioridade: Média

Objetivo: Validar que o sistema permite selecionar apenas um voo por transação de compra.

Pré-condições: Estar na tela de resultados de voos preenchida.

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de busca de voos. | O sistema permite a seleção de apenas um voo por vez. |
| 2 | Preencher todos os campos obrigatórios. | |
| 3 | Observar os voos disponíveis exibidos automaticamente. | |
| 4 | Tentar selecionar mais de um voo. | |

---

### TC-FS-012 — Verificar se o campo de data de retorno fica oculto para viagens de apenas ida
ID: QA-FS12

Prioridade: Média

Objetivo: Validar a alteração dinâmica da interface ao alternar para o tipo de viagem *One-way*.

Pré-condições: Estar na página de busca de voos.

| Passo | Ação | Resultado Esperado |
| :---: | :--- | :--- |
| 1 | Acessar a página de busca de voos. | O campo de data de retorno não é exibido quando a viagem de apenas ida é selecionada. |
| 2 | Selecionar o tipo de viagem como Apenas Ida. | |

---

### TC-FS-013 — Tentar selecionar a mesma cidade para origem e destino
ID: QA-FS13

Prioridade: Média

Objetivo: Validar a validação de campos iguais de origem e destino utilizando parâmetros específicos.

Pré-condições: Estar na página de busca de voos.

| Passo | Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| 1 | Selecionar a mesma cidade nos campos de origem e destino. | **From**: `City A`, **To**: `City A` | Campos preenchidos com o mesmo valor. |
| 2 | Tentar prosseguir com a busca ou avanço. | Botão: `Continue` | O sistema impede o avanço ou exibe mensagem de validação de rota inválida. |

---

### TC-FS-014 — Tentar selecionar data de partida retroativa (passada)
ID: QA-FS14

Prioridade: Média

Objetivo: Impedir a seleção de datas retroativas no campo de partida.

Pré-condições: Estar na página de busca de voos.

| Passo | Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| 1 | Selecionar uma data de partida anterior à data atual do sistema. | **Departing**: Data no passado (ex: dia anterior ao atual) | Data selecionada no componente. |
| 2 | Tentar preencher os demais campos obrigatórios e avançar. | Demais campos válidos | O sistema impede a seleção da data retroativa ou bloqueia a submissão com erro. |

---

### TC-FS-015 — Validação de comportamento ao alternar o tipo de viagem com dados preenchidos
ID: QA-FS15

Prioridade: Média

Objetivo: Verificar se os dados e o layout se comportam de maneira estável ao trocar o tipo de viagem após preenchimento parcial.

Pré-condições: Estar na página de busca de voos com dados preenchidos.

| Passo | Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| 1 | Preencher a origem, destino e a data de retorno. | Campos preenchidos para ida e volta. | Campos preenchidos corretamente. |
| 2 | Alternar o tipo de viagem para *One way*. | Radio button: `One way` | O campo de retorno é ocultado ou limpo, mantendo a estabilidade da interface e dos dados da ida. |

---

### TC-FS-016 — Tentar acessar a página de busca de voos sem autenticação (Acesso Direto via URL)
ID: QA-FS16

Prioridade: Alta

Objetivo: Validar as regras de segurança e controle de sessão ao tentar acessar a URL protegida diretamente.

Pré-condições: Estar com a sessão deslogada no navegador.

| Passo | Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| 1 | Inserir diretamente a URL protegida no navegador. | URL: `https://travel.agileway.net/flights/start` | O sistema deve bloquear o acesso e redirecionar o usuário para a tela de login ou exibir uma mensagem de erro de acesso negado/não autorizado. |

---

### TC-FS-017 — Validar persistência da sessão após atualização da página (F5)
ID: QA-FS17

Prioridade: Média

Objetivo: Garantir estabilidade e persistência de dados ou do estado da aplicação após um *refresh* (F5).

Pré-condições: Estar na página de busca de voos logado e com dados inseridos.

| Passo | Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| 1 | Preencher os campos de origem, destino e selecionar um tipo de viagem. | Origem e Destino válidos | Campos preenchidos corretamente. |
| 2 | Atualizar a página do navegador (pressionar F5). | Ação de Refresh | O sistema deve manter o usuário logado e restaurar os campos ou redefinir para o estado padrão de forma controlada, sem quebrar a aplicação. |


