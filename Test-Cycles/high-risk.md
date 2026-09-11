Ciclo de Regressão — High (Alta Prioridade)
Objetivo: Cobrir os principais fluxos alternativos, validações críticas de segurança e barreiras contra erros comuns de negócio, sem precisar rodar toda a suíte.
Critério de Seleção: Cenários de prioridade Alta (tanto válidos quanto inválidos essenciais, como bloqueio de URL, campos vazios e erros críticos).

Módulo Login:

TC-LOGIN-003 (QA-L03) — Encerramento de sessão (Logout) com sucesso

TC-LOGIN-005 (QA-L05) — Tentativa de login com senha incorreta

TC-LOGIN-006 (QA-L06) — Tentativa de login com usuário inexistente

Módulo Flight Search:

TC-FS-002 (QA-FS02) — Selecionar viagem de apenas ida com data válida

TC-FS-005 (QA-FS05) — Verificar se o botão Continuar fica habilitado quando todos os campos obrigatórios são preenchidos

TC-FS-007 (QA-FS07) — Tentar prosseguir sem selecionar um voo

TC-FS-008 (QA-FS08) — Verificar se os voos não são exibidos quando os campos obrigatórios estão vazios

TC-FS-009 (QA-FS09) — Selecionar mesma origem e destino com a mesma data de ida e volta

TC-FS-010 (QA-FS10) — Selecionar viagem de ida e volta com data de retorno anterior à data de partida

TC-FS-013 (QA-FS13) — Tentar selecionar a mesma cidade para origem e destino

TC-FS-014 (QA-FS14) — Tentar selecionar data de partida retroativa (passada)

TC-FS-016 (QA-FS16) — Tentar acessar a página de busca de voos sem autenticação (Acesso Direto via URL)

Módulo Booking:

TC-BK-002 (QA-BK02) — Inserir caracteres inválidos nos campos de nome do passageiro

TC-BK-003 (QA-BK03) — Tentar prosseguir com campos obrigatórios vazios

TC-BK-006 (QA-BK06) — Tentar acessar a página de Passenger Details diretamente via URL sem selecionar um voo

TC-BK-007 (QA-BK07) — Validar comportamento ao tentar usar números ou caracteres especiais nos campos de nome

Módulo Payment:

TC-PAY-002 (QA-PAY02) — Tentar realizar o pagamento com todos os campos obrigatórios vazios

TC-PAY-003 (QA-PAY03) — Tentar realizar o pagamento com os campos obrigatórios preenchidos parcialmente

TC-PAY-006 (QA-PAY06) — Tentar realizar o pagamento com formato de número de cartão de crédito inválido

TC-PAY-007 (QA-PAY07) — Tentar realizar o pagamento com cartão de crédito expirado

TC-PAY-008 (QA-PAY08) — Tentar realizar o pagamento com nome do portador do cartão inválido ou vazio

TC-PAY-010 (QA-PAY10) — Tentar acessar a página de pagamento diretamente via URL sem concluir as etapas anteriores
