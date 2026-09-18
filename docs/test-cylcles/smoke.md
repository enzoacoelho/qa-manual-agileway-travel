# Ciclo de Testes: Smoke Test (Testes de Fumaça)

**Objetivo:** Validar rapidamente se as funcionalidades principais e críticas do sistema estão operando após um novo deploy. Se algum destes falhar, o build deve ser rejeitado imediatamente.

---

| ID | Versão | Componente/Tela | Nome do Teste |
|---|---|---|---|
| QA-L01 | 1.0 | Login | Autenticação com credenciais válidas com sucesso |
| QA-FS01 | 1.0 | Flight-Search | Selecionar viagem de ida e volta com datas válidas |
| QA-BK01 | 1.0 | Booking | Realizar o booking com dados válidos com sucesso |
| QA-PAY01 | 1.0 | Payment | Concluir o pagamento com dados de cartão de crédito válidos |
| QA-L03 | 1.0 | Login | Encerramento de sessão (Logout) com sucesso |