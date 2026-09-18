# Execução: Regressão — Full (Completo)

**Ciclo:** Ciclo 3 - Regressão Completa (QMTAT-R3)
**Data de execução:** 11/09/2026
**Build/Versão testada:** 1.0
**Ambiente:** travel.agileway.net (produção/demo pública)
**Executor:** Enzo Coelho
**Resultado geral:** ⚠️ 18/30 passaram, 12 falharam — Build **não aprovado** para produção

---

| ID | Componente/Tela | Nome do Teste | Status | Bug Vinculado |
|---|---|---|---|---|
| QA-L04 | Login | Tentativa de login com campos obrigatórios vazios | ✅ Passou | — |
| QA-L05 | Login | Tentativa de login com senha incorreta | ✅ Passou | — |
| QA-L06 | Login | Tentativa de login com usuário inexistente | ✅ Passou | — |
| QA-L02 | Login | Autenticação com a opção "Remember me" selecionada | ✅ Passou | — |
| QA-L01 | Login | Autenticação com credenciais válidas com sucesso | ✅ Passou | — |
| QA-BK05 | Booking | Acessar Passenger Details via URL sem selecionar voo | ❌ Falhou | [BUG-BK-01](../bug-reports/booking/BUG-BK-01.md) |
| QA-PAY06 | Payment | Acessar pagamento via URL sem concluir etapas anteriores | ❌ Falhou | [BUG-PAY-01](../bug-reports/payment/BUG-PAY-01.md) |
| QA-FS04 | Flight-Search | Verificar se o tipo de viagem padrão é "Ida e Volta" | ✅ Passou | — |
| QA-FS06 | Flight-Search | Prosseguir para o booking sem selecionar um voo | ❌ Falhou | [BUG-FS-01](../bug-reports/booking/BUG-FS-01.md) |
| QA-FS07 | Flight-Search | Voos não exibidos com campos obrigatórios vazios | ❌ Falhou | [BUG-FS-02](../bug-reports/booking/BUG-FS-02.md) |
| QA-FS12 | Flight-Search | Validar restrição de seleção de mesma cidade para Origem (From) e Destino (To) | ❌ Falhou | [BUG-FS-03](../../bug-reports/booking/BUG-FS-03.md) |
| QA-FS09 | Flight-Search | Retorno anterior à data de partida | ❌ Falhou | [BUG-FS-04](../bug-reports/booking/BUG-FS-04.md) |
| QA-FS13 | Flight-Search | Data de partida retroativa (passada) | ❌ Falhou | [BUG-FS-05](../bug-reports/booking/BUG-FS-05.md) |
| QA-FS10 | Flight-Search | Múltiplos voos ao mesmo tempo | ❌ Falhou | [BUG-FS-06](../bug-reports/booking/BUG-FS-06.md) |
| QA-FS05 | Flight-Search | Selecionar voo em versões responsivas | ✅ Passou | — |
| QA-FS01 | Flight-Search | Selecionar viagem de ida e volta com datas válidas | ✅ Passou | — |
| QA-FS02 | Flight-Search | Selecionar viagem de apenas ida com data válida  | ✅ Passou | — |
| QA-FS03 | Flight-Search | Ida e volta com a mesma data de partida e retorno | ❌ Falhou | [BUG-FS-07](../bug-reports/BUG-FS-07.md) |
| QA-FS11 | Flight-Search | Campo de retorno oculto para viagens de apenas ida | ✅ Passou | — |
| QA-FS14 | Flight-Search | Alternar tipo de viagem com dados preenchidos | ✅ Passou | — |
| QA-BK01 | Booking | Realizar o booking com dados válidos com sucesso | ✅ Passou | — |
| QA-BK02 | Booking | Integridade e exibição das informações do voo | ✅ Passou | — |
| QA-BK03 | Booking | Caracteres inválidos nos campos de nome do passageiro | ❌ Falhou | [BUG-BK-02](../bug-reports/booking/BUG-BK-02.md) |
| QA-BK04 | Booking | Prosseguir com campos obrigatórios vazios | ✅ Passou | — |
| QA-PAY01 | Payment | Concluir o pagamento com dados de cartão válidos | ✅ Passou | — |
| QA-PAY05 | Payment | Múltiplos cliques no botão Pagar Agora | ✅ Passou | — |
| QA-PAY02 | Payment | Pagamento com todos os campos obrigatórios vazios | ❌ Falhou | [BUG-PAY-02](../bug-reports/booking/BUG-PAY-02.md) |
| QA-PAY03 | Payment | Formato de número de cartão inválido | ❌ Falhou | [BUG-PAY-03](../bug-reports/booking/BUG-PAY-03.md) |
| QA-PAY04 | Payment | Cartão de crédito expirado | ❌ Falhou | [BUG-PAY-04](../bug-reports/booking/BUG-PAY-04.md) |
| QA-L03 | Login | Encerramento de sessão (Logout) com sucesso | ✅ Passou | — |

---

## Observações
Volume alto de falhas concentrado em **validações negativas e guardas de rota** — o sistema parece estar aceitando entradas ou acessos que deveriam ser bloqueados:

- **Guardas de rota** (QA-BK05, QA-PAY06): acesso direto via URL sem completar etapas anteriores não está sendo bloqueado.
- **Validações de Flight-Search** (QA-FS06, QA-FS07, QA-FS12, QA-FS09, QA-FS13, QA-FS10): múltiplas regras de negócio não estão impedindo estados inválidos.
- **Booking** (QA-BK03): caracteres inválidos no nome do passageiro estão sendo aceitos.
- **Payment** (QA-PAY02, QA-PAY03, QA-PAY04): validações de campos obrigatórios, formato de cartão e expiração não estão bloqueando o pagamento.
