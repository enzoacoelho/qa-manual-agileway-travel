# Ciclo de Testes: Regressão — Full (Completo)

**Objetivo:** Execução integral de 100% da suíte de testes mapeada (incluindo prioridades Média e Baixa, como testes responsivos, persistência de sessão, limites de caracteres e comportamentos dinâmicos de interface). 

---

| ID | Versão | Componente/Tela | Nome do Teste |
|---|---|---|---|
| QA-L04 | 1.0 | Login | Tentativa de login com campos obrigatórios vazios |
| QA-L05 | 1.0 | Login | Tentativa de login com senha incorreta |
| QA-L06 | 1.0 | Login | Tentativa de login com usuário inexistente |
| QA-L02 | 1.0 | Login | Autenticação com a opção "Remember me" selecionada |
| QA-L01 | 1.0 | Login | Autenticação com credenciais válidas com sucesso |
| QA-BK05 | 1.0 | Booking | Tentar acessar a página de Passenger Details diretamente via URL sem selecionar um voo |
| QA-PAY06 | 1.0 | Payment | Tentar acessar a página de pagamento diretamente via URL sem concluir as etapas anteriores |
| QA-FS04 | 1.0 | Flight-Search | Verificar se o tipo de viagem padrão é "Ida e Volta" |
| QA-FS06 | 1.0 | Flight-Search | Tentativa de prosseguir para o booking sem selecionar um voo |
| QA-FS07 | 1.0 | Flight-Search | Verificar se os voos não são exibidos quando os campos obrigatórios estão vazios |
| QA-FS09 | 1.0 | Flight-Search | Selecionar viagem de ida e volta com data de retorno anterior à data de partida |
| QA-FS13 | 1.0 | Flight-Search | Tentar selecionar data de partida retroativa (passada) |
| QA-FS12 | 1.0 | Flight-Search | Validar restrição de seleção de mesma cidade para Origem (From) e Destino (To) |
| QA-FS10 | 1.0 | Flight-Search | Selecionar múltiplos voos ao mesmo tempo |
| QA-FS05 | 1.0 | Flight-Search | Selecionar voo em versões responsivas |
| QA-FS01 | 1.0 | Flight-Search | Selecionar viagem de ida e volta com datas válidas |
| QA-FS02 | 1.0 | Flight-Search | Selecionar viagem de apenas ida com data válida |
| QA-FS03 | 1.0 | Flight-Search | Selecionar viagem de ida e volta com a mesma data de partida e retorno |
| QA-FS11 | 1.0 | Flight-Search | Verificar se o campo de data de retorno fica oculto para viagens de apenas ida |
| QA-FS14 | 1.0 | Flight-Search | Validação de comportamento ao alternar o tipo de viagem com dados preenchidos |
| QA-BK01 | 1.0 | Booking | Realizar o booking com dados válidos com sucesso |
| QA-BK02 | 1.0 | Booking | Verificar a integridade e exibição das informações do voo selecionado |
| QA-BK03 | 1.0 | Booking | Inserir caracteres inválidos nos campos de nome do passageiro |
| QA-BK04 | 1.0 | Booking | Tentar prosseguir com campos obrigatórios vazios |
| QA-PAY01 | 1.0 | Payment | Concluir o pagamento com dados de cartão de crédito válidos |
| QA-PAY05 | 1.0 | Payment | Múltiplos cliques no botão Pagar Agora |
| QA-PAY02 | 1.0 | Payment | Tentar realizar o pagamento com todos os campos obrigatórios vazios |
| QA-PAY03 | 1.0 | Payment | Tentar realizar o pagamento com formato de número de cartão de crédito inválido |
| TC-PAY-007 | 1.0 | Payment | Tentar realizar o pagamento com cartão de crédito expirado |
| QA-L03 | 1.0 | Login | Encerramento de sessão (Logout) com sucesso |