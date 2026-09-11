# Ciclo de Testes: Regressão — High (Alta Prioridade)

**Objetivo:** Cobrir os principais fluxos alternativos, validações críticas de segurança e barreiras contra erros comuns de negócio, sem precisar rodar toda a suíte.

---

| ID | Chave | Versão | Nome do Caso de Teste | Prioridade |
| :---: | :---: | :---: | :--- | :---: |
| 1 | **QA-L03** | 1.0 | TC-LOGIN-003 — Encerramento de sessão (Logout) com sucesso | Alta |
| 2 | **QA-L05** | 1.0 | TC-LOGIN-005 — Tentativa de login com senha incorreta | Alta |
| 3 | **QA-L06** | 1.0 | TC-LOGIN-006 — Tentativa de login com usuário inexistente | Alta |
| 4 | **QA-FS02** | 1.0 | TC-FS-002 — Selecionar viagem de apenas ida com data válida | Alta |
| 5 | **QA-FS05** | 1.0 | TC-FS-005 — Verificar se o botão Continuar fica habilitado quando todos os campos obrigatórios são preenchidos | Alta |
| 6 | **QA-FS07** | 1.0 | TC-FS-007 — Tentar prosseguir sem selecionar um voo | Alta |
| 7 | **QA-FS08** | 1.0 | TC-FS-008 — Verificar se os voos não são exibidos quando os campos obrigatórios estão vazios | Alta |
| 8 | **QA-FS09** | 1.0 | TC-FS-009 — Selecionar mesma origem e destino com a mesma data de ida e volta | Alta |
| 9 | **QA-FS10** | 1.0 | TC-FS-010 — Selecionar viagem de ida e volta com data de retorno anterior à data de partida | Alta |
| 10 | **QA-FS13** | 1.0 | TC-FS-013 — Tentar selecionar a mesma cidade para origem e destino | Alta |
| 11 | **QA-FS14** | 1.0 | TC-FS-014 — Tentar selecionar data de partida retroativa (passada) | Alta |
| 12 | **QA-FS16** | 1.0 | TC-FS-016 — Tentar acessar a página de busca de voos sem autenticação (Acesso Direto via URL) | Alta |
| 13 | **QA-BK02** | 1.0 | TC-BK-002 — Inserir caracteres inválidos nos campos de nome do passageiro | Alta |
| 14 | **QA-BK03** | 1.0 | TC-BK-003 — Tentar prosseguir com campos obrigatórios vazios | Alta |
| 15 | **QA-BK06** | 1.0 | TC-BK-006 — Tentar acessar a página de Passenger Details diretamente via URL sem selecionar um voo | Alta |
| 16 | **QA-BK07** | 1.0 | TC-BK-007 — Validar comportamento ao tentar usar números ou caracteres especiais nos campos de nome | Alta |
| 17 | **QA-PAY02** | 1.0 | TC-PAY-002 — Tentar realizar o pagamento com todos os campos obrigatórios vazios | Alta |
| 18 | **QA-PAY03** | 1.0 | TC-PAY-003 — Tentar realizar o pagamento com os campos obrigatórios preenchidos parcialmente | Alta |
| 19 | **QA-PAY06** | 1.0 | TC-PAY-006 — Tentar realizar o pagamento com formato de número de cartão de crédito inválido | Alta |
| 20 | **QA-PAY07** | 1.0 | TC-PAY-007 — Tentar realizar o pagamento com cartão de crédito expirado | Alta |
| 21 | **QA-PAY08** | 1.0 | TC-PAY-008 — Tentar realizar o pagamento com nome do portador do cartão inválido ou vazio | Alta |
| 22 | **QA-PAY10** | 1.0 | TC-PAY-010 — Tentar acessar a página de pagamento diretamente via URL sem concluir as etapas anteriores | Alta |
