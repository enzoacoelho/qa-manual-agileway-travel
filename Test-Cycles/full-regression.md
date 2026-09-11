# Ciclo de Testes: Regressão — Full (Completo)

**Objetivo:** Execução integral de 100% da suíte de testes mapeada (incluindo prioridades Média e Baixa, como testes responsivos, persistência de sessão, limites de caracteres e comportamentos dinâmicos de interface). Recomendado para homologações de releases maiores ou versões de produção.

---

| ID | Chave | Versão | Nome do Caso de Teste | Prioridade |
| :---: | :---: | :---: | :--- | :---: |
| 1 | **QA-L01** | 1.0 | TC-LOGIN-001 — Autenticação com credenciais padrão válidas | Alta |
| 2 | **QA-L02** | 1.0 | TC-LOGIN-002 — Autenticação com a opção "Remember me" selecionada | Média |
| 3 | **QA-L03** | 1.0 | TC-LOGIN-003 — Encerramento de sessão (Logout) com sucesso | Alta |
| 4 | **QA-L04** | 1.0 | TC-LOGIN-004 — Tentativa de login com campos obrigatórios vazios | Média |
| 5 | **QA-L05** | 1.0 | TC-LOGIN-005 — Tentativa de login com senha incorreta | Alta |
| 6 | **QA-L06** | 1.0 | TC-LOGIN-006 — Tentativa de login com usuário inexistente | Alta |
| 7 | **QA-FS01** | 1.0 | TC-FS-001 — Selecionar viagem de ida e volta com datas válidas | Alta |
| 8 | **QA-FS02** | 1.0 | TC-FS-002 — Selecionar viagem de apenas ida com data válida | Alta |
| 9 | **QA-FS03** | 1.0 | TC-FS-003 — Selecionar viagem de ida e volta com a mesma data de partida e retorno | Média |
| 10 | **QA-FS04** | 1.0 | TC-FS-004 — Verificar se o tipo de viagem padrão é "Ida e Volta" | Baixa |
| 11 | **QA-FS05** | 1.0 | TC-FS-005 — Verificar se o botão Continuar fica habilitado quando todos os campos obrigatórios são preenchidos | Alta |
| 12 | **QA-FS06** | 1.0 | TC-FS-006 — Selecionar voo em versões responsivas | Média |
| 13 | **QA-FS07** | 1.0 | TC-FS-007 — Tentar prosseguir sem selecionar um voo | Alta |
| 14 | **QA-FS08** | 1.0 | TC-FS-008 — Verificar se os voos não são exibidos quando os campos obrigatórios estão vazios | Alta |
| 15 | **QA-FS09** | 1.0 | TC-FS-009 — Selecionar mesma origem e destino com a mesma data de ida e volta | Alta |
| 16 | **QA-FS10** | 1.0 | TC-FS-010 — Selecionar viagem de ida e volta com data de retorno anterior à data de partida | Alta |
| 17 | **QA-FS11** | 1.0 | TC-FS-011 — Selecionar múltiplos voos ao mesmo tempo | Média |
| 18 | **QA-FS12** | 1.0 | TC-FS-012 — Verificar se o campo de data de retorno fica oculto para viagens de apenas ida | Média |
| 19 | **QA-FS13** | 1.0 | TC-FS-013 — Tentar selecionar a mesma cidade para origem e destino | Alta |
| 20 | **QA-FS14** | 1.0 | TC-FS-014 — Tentar selecionar data de partida retroativa (passada) | Alta |
| 21 | **QA-FS15** | 1.0 | TC-FS-015 — Validação de comportamento ao alternar o tipo de viagem com dados preenchidos | Média |
| 22 | **QA-FS16** | 1.0 | TC-FS-016 — Tentar acessar a página de busca de voos sem autenticação (Acesso Direto via URL) | Alta |
| 23 | **QA-FS17** | 1.0 | TC-FS-017 — Validar persistência da sessão após atualização da página (F5) | Média |
| 24 | **QA-FS18** | 1.0 | TC-FS-018 — Validar comportamento com campos de seleção de Origem e Destino vazios no carregamento inicial | Baixa |
| 25 | **QA-BK01** | 1.0 | TC-BK-001 — Inserir nome e sobrenome válidos do passageiro | Alta |
| 26 | **QA-BK02** | 1.0 | TC-BK-002 — Inserir caracteres inválidos nos campos de nome do passageiro | Alta |
| 27 | **QA-BK03** | 1.0 | TC-BK-003 — Tentar prosseguir com campos obrigatórios vazios | Alta |
| 28 | **QA-BK04** | 1.0 | TC-BK-004 — Inserir nomes com limites máximos ou mínimos de caracteres válidos | Média |
| 29 | **QA-BK05** | 1.0 | TC-BK-005 — Verificar a integridade e exibição das informações do voo selecionado | Média |
| 30 | **QA-BK06** | 1.0 | TC-BK-006 — Tentar acessar a página de Passenger Details diretamente via URL sem selecionar um voo | Alta |
| 31 | **QA-BK07** | 1.0 | TC-BK-007 — Validar comportamento ao tentar usar números ou caracteres especiais nos campos de nome | Alta |
| 32 | **QA-PAY01** | 1.0 | TC-PAY-001 — Concluir o pagamento com dados de cartão de crédito válidos | Alta |
| 33 | **QA-PAY02** | 1.0 | TC-PAY-002 — Tentar realizar o pagamento com todos os campos obrigatórios vazios | Alta |
| 34 | **QA-PAY03** | 1.0 | TC-PAY-003 — Tentar realizar o pagamento com os campos obrigatórios preenchidos parcialmente | Alta |
| 35 | **QA-PAY04** | 1.0 | TC-PAY-004 — Tentar realizar o pagamento sem selecionar o tipo de cartão de crédito | Média |
| 37 | **QA-PAY06** | 1.0 | TC-PAY-006 — Tentar realizar o pagamento com formato de número de cartão de crédito inválido | Alta |
| 38 | **QA-PAY07** | 1.0 | TC-PAY-007 — Tentar realizar o pagamento com cartão de crédito expirado | Alta |
| 39 | **QA-PAY08** | 1.0 | TC-PAY-008 — Tentar realizar o pagamento com nome do portador do cartão inválido ou vazio | Alta |
| 40 | **QA-PAY09** | 1.0 | TC-PAY-009 — Múltiplos cliques no botão Pagar Agora | Média |
| 41 | **QA-PAY10** | 1.0 | TC-PAY-010 — Tentar acessar a página de pagamento diretamente via URL sem concluir as etapas anteriores | Alta |
