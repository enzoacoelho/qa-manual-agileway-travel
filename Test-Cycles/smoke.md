Ciclo de Smoke Test (Fumaça)
Objetivo: Validar rapidamente se as funcionalidades principais e críticas do sistema estão operando após um novo deploy. Se algum destes falhar, o build deve ser rejeitado imediatamente.
Critério de Seleção: Apenas cenários de fluxo feliz (Happy Path) com prioridade Alta de cada módulo principal (Login, Busca, Passageiro e Pagamento).

TC-LOGIN-001 (QA-L01) — Autenticação com credenciais padrão válidas

TC-FS-001 (QA-FS01) — Selecionar viagem de ida e volta com datas válidas

TC-BK-001 (QA-BK01) — Inserir nome e sobrenome válidos do passageiro

TC-PAY-001 (QA-PAY01) — Concluir o pagamento com dados de cartão de crédito válidos
