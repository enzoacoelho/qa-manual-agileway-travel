
Conversa com o Gemini
tenho esses test case pra essa tela

# Flight Search – Casos de Teste



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



---



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





precisa de mais ne? por favor pense como um QA experiente e adicione casos de testes pra essa tela por favor, especificamente um de tentar entrar nesse link https://travel.agileway.net/flights/start sem estar logado pelo link

Como um QA experiente, concordo que sua suíte já cobre bons cenários funcionais básicos, mas faltam testes críticos de Segurança (Controle de Acesso), Validação de Limites e Estados de Sessão, especialmente considerando a aplicação em questão (AgileWay Travel).

Abaixo, adicionei novos casos de teste estruturados no mesmo padrão, com destaque especial para o cenário de tentativa de acesso direto via URL sem autenticação, como você pediu.

TC-FS-016 — Tentar acessar a página de busca de voos sem autenticação (Acesso Direto via URL)
ID: QA-FS16

Prioridade: Alta

Objetivo: Verificar se o sistema protege a rota restrita e impede o acesso direto via URL ([https://travel.agileway.net/flights/start](https://travel.agileway.net/flights/start)) sem que o usuário esteja logado.

Pré-condições:

O usuário não está autenticado no sistema (sessão limpa ou encerrada).

Passo	Ação	Massa de Dados / Parâmetros	Resultado Esperado
1	Inserir diretamente a URL protegida no navegador.	URL: [https://travel.agileway.net/flights/start](https://travel.agileway.net/flights/start)	O sistema deve bloquear o acesso e redirecionar o usuário para a tela de login ou exibir uma mensagem de erro de acesso negado/não autorizado.
TC-FS-017 — Validar persistência da sessão após atualização da página (F5)
ID: QA-FS17

Prioridade: Média

Objetivo: Garantir que os dados preenchidos ou o estado da sessão de voo não sejam perdidos abruptamente ao atualizar a página.

Pré-condições:

Estar na página de busca de voos autenticado.

Passo	Ação	Massa de Dados / Parâmetros	Resultado Esperado
1	Preencher os campos de origem, destino e selecionar um tipo de viagem.	Origem e Destino válidos	Campos preenchidos corretamente.
2	Atualizar a página do navegador (pressionar F5).	Ação de Refresh	O sistema deve manter o usuário logado e restaurar os campos ou redefinir para o estado padrão de forma controlada, sem quebrar a aplicação (verificar comportamento esperado da especificação).
TC-FS-018 — Validar comportamento com campos de seleção de Origem e Destino vazios no carregamento inicial
ID: QA-FS18

Prioridade: Média

Objetivo: Verificar se as listas suspensas (dropdowns) de origem e destino possuem valores padrão seguros ou se exigem escolha explícita.

Pré-condições:

Estar na página de busca de voos recém-acessada.

Passo	Ação	Massa de Dados / Parâmetros	Resultado Esperado
1	Inspecionar os campos From e To logo após carregar a tela.	Visualização dos selects	Os campos devem vir com uma opção padrão pré-selecionada (ou vazia com placeholder) e os voos não devem ser listados incorretamente até que critérios válidos estejam definidos.
Como pedido, COMO PEDIDO, o caso de teste de segurança de acesso direto por URL foi incluído no topo da lista para priorizar a validação de autenticação da sua aplicação. Tem mais algum fluxo específico (como a tela de pagamento ou seleção de assentos) que você gostaria de mapear?

entao junto o meu md e os seus testes e me manda

Aqui está o documento completo consolidado com os seus casos de teste originais e os novos cenários de teste adicionados:

Flight Search – Casos de Teste
Busca de Voos – Casos de Teste
Cenários Válidos
TC-FS-001
Título: Selecionar viagem de ida e volta com datas válidas

Passo	Ação	Resultado Esperado
1	Acessar a página de busca de voos.	Os voos disponíveis são exibidos automaticamente após o preenchimento dos critérios de busca, permitindo que o usuário selecione um voo e prossiga para a próxima etapa.
2	Selecionar o tipo de viagem como Ida e Volta (Return).	
3	Inserir origem e destino válidos.	
4	Selecionar datas válidas de ida e volta.	
5	Observar os voos disponíveis exibidos automaticamente.	
6	Selecionar um voo disponível.	
7	Clicar em Continuar.	
TC-FS-002
Título: Selecionar viagem de apenas ida com data válida

Passo	Ação	Resultado Esperado
1	Acessar a página de busca de voos.	Os voos são exibidos automaticamente e o usuário pode prosseguir com a seleção de um voo de apenas ida.
2	Selecionar o tipo de viagem como Apenas Ida (One-way).	
3	Inserir origem e destino válidos.	
4	Selecionar uma data de ida válida.	
5	Observar os voos disponíveis exibidos automaticamente.	
6	Selecionar um voo disponível.	
7	Clicar em Continuar.	
TC-FS-003
Título: Selecionar viagem de ida e volta com a mesma data de partida e retorno

Passo	Ação	Resultado Esperado
1	Acessar a página de busca de voos.	O sistema permite a seleção do voo quando as datas de ida e volta são iguais.
2	Selecionar o tipo de viagem como Ida e Volta.	
3	Inserir origem e destino válidos.	
4	Selecionar a mesma data para partida e retorno.	
5	Observar os voos disponíveis exibidos automaticamente.	
6	Selecionar um voo disponível.	
7	Clicar em Continuar.	
TC-FS-004
Título: Verificar se o tipo de viagem padrão é "Ida e Volta"

Passo	Ação	Resultado Esperado
1	Acessar a página de busca de voos.	A opção de viagem de ida e volta vem selecionada por padrão.
TC-FS-005
Título: Verificar se o botão Continuar fica habilitado quando todos os campos obrigatórios são preenchidos

Passo	Ação	Resultado Esperado
1	Acessar a página de busca de voos.	O botão Continuar fica habilitado após a seleção de um voo.
2	Preencher todos os campos obrigatórios com dados válidos.	
3	Observar os voos disponíveis exibidos automaticamente.	
4	Selecionar um voo disponível.	
TC-FS-006
Título: Selecionar voo em versões responsivas

Passo	Ação	Resultado Esperado
1	Acessar a página de busca de voos em diferentes tamanhos de tela.	A seleção de voos funciona corretamente em layouts responsivos.
2	Preencher todos os campos obrigatórios.	
3	Observar os voos disponíveis exibidos automaticamente.	
4	Selecionar um voo disponível.	
Cenários Inválidos
TC-FS-007
Título: Tentar prosseguir sem selecionar um voo

Passo	Ação	Resultado Esperado
1	Acessar a página de busca de voos.	O sistema impede o avanço e exibe uma mensagem de validação.
2	Preencher todos os campos obrigatórios.	
3	Não selecionar nenhum voo.	
4	Tentar clicar em Continuar.	
TC-FS-008
Título: Verificar se os voos não são exibidos quando os campos obrigatórios estão vazios

Passo	Ação	Resultado Esperado
1	Acessar a página de busca de voos.	Os voos disponíveis não são exibidos até que todos os campos obrigatórios sejam preenchidos.
2	Deixar um ou mais campos obrigatórios vazios.	
TC-FS-009
Título: Selecionar mesma origem e destino com a mesma data de ida e volta

Passo	Ação	Resultado Esperado
1	Acessar a página de busca de voos.	O sistema impede a busca de voos devido a uma configuração de rota inválida.
2	Inserir a mesma cidade para origem e destino.	
3	Selecionar a mesma data para partida e retorno.	
TC-FS-010
Título: Selecionar viagem de ida e volta com data de retorno anterior à data de partida

Passo	Ação	Resultado Esperado
1	Acessar a página de busca de voos.	O sistema impede a seleção de data inválida e exibe uma mensagem de erro.
2	Selecionar o tipo de viagem como Ida e Volta.	
3	Inserir origem e destino válidos.	
4	Selecionar uma data de retorno anterior à data de partida.	
TC-FS-011
Título: Selecionar múltiplos voos ao mesmo tempo

Passo	Ação	Resultado Esperado
1	Acessar a página de busca de voos.	O sistema permite a seleção de apenas um voo por vez.
2	Preencher todos os campos obrigatórios.	
3	Observar os voos disponíveis exibidos automaticamente.	
4	Tentar selecionar mais de um voo.	
TC-FS-012
Título: Verificar se o campo de data de retorno fica oculto para viagens de apenas ida

Passo	Ação	Resultado Esperado
1	Acessar a página de busca de voos.	O campo de data de retorno não é exibido quando a viagem de apenas ida é selecionada.
2	Selecionar o tipo de viagem como Apenas Ida.	
TC-FS-013 — Tentar selecionar a mesma cidade para origem e destino
ID: QA-FS13

Prioridade: Média

Objetivo: Verificar se o sistema impede a seleção de rotas inválidas onde a origem e o destino são idênticos.

Pré-condições:

Estar na página de busca de voos.

Passo	Ação	Massa de Dados / Parâmetros	Resultado Esperado
1	Selecionar a mesma cidade nos campos de origem e destino.	From: City A, To: City A	Campos preenchidos com o mesmo valor.
2	Tentar prosseguir com a busca ou avanço.	Botão: Continue	O sistema impede o avanço ou exibe mensagem de validação de rota inválida.
TC-FS-014 — Tentar selecionar data de partida retroativa (passada)
ID: QA-FS14

Prioridade: Alta

Objetivo: Garantir que o sistema bloqueie o agendamento de voos com datas anteriores ao dia atual.

Pré-condições:

Estar na página de busca de voos.

Passo	Ação	Massa de Dados / Parâmetros	Resultado Esperado
1	Selecionar uma data de partida anterior à data atual do sistema.	Departing: Data no passado (ex: dia anterior ao atual)	Data selecionada no componente.
2	Tentar preencher os demais campos obrigatórios e avançar.	Demais campos válidos	O sistema impede a seleção da data retroativa ou bloqueia a submissão com erro.
TC-FS-015 — Validação de comportamento ao alternar o tipo de viagem com dados preenchidos
ID: QA-FS15

Prioridade: Baixa

Objetivo: Verificar a integridade dos campos ao alternar entre os tipos de viagem (Return e One way).

Pré-condições:

Estar na página de busca de voos com a opção Return selecionada.

Passo	Ação	Massa de Dados / Parâmetros	Resultado Esperado
1	Preencher a origem, destino e a data de retorno.	Campos preenchidos para ida e volta.	Campos preenchidos corretamente.
2	Alternar o tipo de viagem para One way.	Radio button: One way	O campo de retorno é ocultado ou limpo, mantendo a estabilidade da interface e dos dados da ida.
TC-FS-016 — Tentar acessar a página de busca de voos sem autenticação (Acesso Direto via URL)
ID: QA-FS16

Prioridade: Alta

Objetivo: Verificar se o sistema protege a rota restrita e impede o acesso direto via URL ([https://travel.agileway.net/flights/start](https://travel.agileway.net/flights/start)) sem que o usuário esteja logado.

Pré-condições:

O usuário não está autenticado no sistema (sessão limpa ou encerrada).

Passo	Ação	Massa de Dados / Parâmetros	Resultado Esperado
1	Inserir diretamente a URL protegida no navegador.	URL: [https://travel.agileway.net/flights/start](https://travel.agileway.net/flights/start)	O sistema deve bloquear o acesso e redirecionar o usuário para a tela de login ou exibir uma mensagem de erro de acesso negado/não autorizado.
TC-FS-017 — Validar persistência da sessão após atualização da página (F5)
ID: QA-FS17

Prioridade: Média

Objetivo: Garantir que os dados preenchidos ou o estado da sessão de voo não sejam perdidos abruptamente ao atualizar a página.

Pré-condições:

Estar na página de busca de voos autenticado.

Passo	Ação	Massa de Dados / Parâmetros	Resultado Esperado
1	Preencher os campos de origem, destino e selecionar um tipo de viagem.	Origem e Destino válidos	Campos preenchidos corretamente.
2	Atualizar a página do navegador (pressionar F5).	Ação de Refresh	O sistema deve manter o usuário logado e restaurar os campos ou redefinir para o estado padrão de forma controlada, sem quebrar a aplicação.
TC-FS-018 — Validar comportamento com campos de seleção de Origem e Destino vazios no carregamento inicial
ID: QA-FS18

Prioridade: Média

Objetivo: Verificar se as listas suspensas (dropdowns) de origem e destino possuem valores padrão seguros ou se exigem escolha explícita.

Pré-condições:

Estar na página de busca de voos recém-acessada.

Passo	Ação	Massa de Dados / Parâmetros	Resultado Esperado
1	Inspecionar os campos From e To logo após carregar a tela.	Visualização dos selects	Os campos devem vir com uma opção padrão pré-selecionada (ou vazia com placeholder) e os voos não devem ser listados incorretamente até que critérios válidos estejam definidos.
Como pedido, COMO PEDIDO, os casos de teste originais e os novos cenários de segurança e comportamento foram unidos em um único markdown pronto para uso.

Você interrompeu a resposta
EM MD!!!!!!!!!!!!!!!!!

O arquivo Markdown unificado com todos os casos de teste originais e os novos cenários foi gerado com sucesso!

Your markdown file is ready

Ícone do app MD
flight_search_test_cases
 MD 
Segue também o conteúdo completo em formato MD diretamente aqui para você copiar se preferir:




O Gemini é uma IA e pode cometer erros.

Analisando
# Flight Search – Casos de Teste

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

---

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

---

### TC-FS-016 — Tentar acessar a página de busca de voos sem autenticação (Acesso Direto via URL)
* **ID:** QA-FS16
* **Prioridade:** Alta
* **Objetivo:** Verificar se o sistema protege a rota restrita e impede o acesso direto via URL (`https://travel.agileway.net/flights/start`) sem que o usuário esteja logado.
* **Pré-condições:** 
  * O usuário **não** está autenticado no sistema (sessão limpa ou encerrada).

| Passo | Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Inserir diretamente a URL protegida no navegador. | URL: `https://travel.agileway.net/flights/start` | O sistema deve bloquear o acesso e redirecionar o usuário para a tela de login ou exibir uma mensagem de erro de acesso negado/não autorizado. |

---

### TC-FS-017 — Validar persistência da sessão após atualização da página (F5)
* **ID:** QA-FS17
* **Prioridade:** Média
* **Objetivo:** Garantir que os dados preenchidos ou o estado da sessão de voo não sejam perdidos abruptamente ao atualizar a página.
* **Pré-condições:** 
  * Estar na página de busca de voos autenticado.

| Passo | Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Preencher os campos de origem, destino e selecionar um tipo de viagem. | Origem e Destino válidos | Campos preenchidos corretamente. |
| **2** | Atualizar a página do navegador (pressionar F5). | Ação de Refresh | O sistema deve manter o usuário logado e restaurar os campos ou redefinir para o estado padrão de forma controlada, sem quebrar a aplicação. |

---

### TC-FS-018 — Validar comportamento com campos de seleção de Origem e Destino vazios no carregamento inicial
* **ID:** QA-FS18
* **Prioridade:** Média
* **Objetivo:** Verificar se as listas suspensas (*dropdowns*) de origem e destino possuem valores padrão seguros ou se exigem escolha explícita.
* **Pré-condições:** 
  * Estar na página de busca de voos recém-acessada.

| Passo | Ação | Massa de Dados / Parâmetros | Resultado Esperado |
| :---: | :--- | :--- | :--- |
| **1** | Inspecionar os campos `From` e `To` logo após carregar a tela. | Visualização dos selects | Os campos devem vir com uma opção padrão pré-selecionada (ou vazia com placeholder) e os voos não devem ser listados incorretamente até que critérios válidos estejam definidos. |
flight_search_test_cases.md
Exibindo flight_search_test_cases.md.
