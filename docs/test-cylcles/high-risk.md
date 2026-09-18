# Ciclo de Testes: Regressão — High (Alta Prioridade)

**Objetivo:** Cobrir os principais fluxos alternativos, validações críticas de segurança e barreiras contra erros comuns de negócio, sem precisar rodar toda a suíte.

---

| ID | Versão | Componente/Tela | Nome do Teste |
|---|---|---|---|
| QA-L01 | 1.0 | Login | Autenticação com credenciais válidas com sucesso |
| QA-L05 | 1.0 | Login | Tentativa de login com senha incorreta |
| QA-FS01 | 1.0 | Flight-Search | Selecionar viagem de ida e volta com datas válidas |
| QA-FS02 | 1.0 | Flight-Search | Selecionar viagem de apenas ida com data válida |
| QA-FS09 | 1.0 | Flight-Search | Selecionar viagem de ida e volta com data de retorno anterior à data de partida |
| QA-FS12 | 1.0 | Flight-Search | Validar restrição de seleção de mesma cidade para Origem (From) e Destino (To) |
| QA-BK01 | 1.0 | Booking | Realizar o booking com dados válidos com sucesso |
| QA-BK02 | 1.0 | Booking | Verificar a integridade e exibição das informações do voo selecionado |
| QA-PAY01 | 1.0 | Payment | Concluir o pagamento com dados de cartão de crédito válidos |
| QA-PAY05 | 1.0 | Payment | Múltiplos cliques no botão Pagar Agora |
| QA-PAY06 | 1.0 | Payment | Tentar acessar a página de pagamento diretamente via URL sem concluir as etapas anteriores |
| QA-L03 | 1.0 | Login | Encerramento de sessão (Logout) com sucesso |