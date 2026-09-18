# Execução: Smoke Test (Testes de Fumaça)

**Ciclo:** Ciclo 1 - Smoke Test (QMTAT-R1)
**Data de execução:** 09/09/2026
**Build/Versão testada:** 1.0
**Ambiente:** travel.agileway.net (produção/demo pública)
**Executor:** Enzo Coelho
**Resultado geral:** ✅ 5/5 passaram — Build aprovado

---

| ID | Componente/Tela | Nome do Teste | Status | Bug Vinculado |
|---|---|---|---|---|
| TC-LOGIN-001 | Login | Autenticação com credenciais válidas com sucesso | ✅ Passou | — |
| TC-FS-001 | Flight-Search | Selecionar viagem de ida e volta com datas válidas | ✅ Passou | — |
| TC-BK-001 | Booking | Realizar o booking com dados válidos com sucesso | ✅ Passou | — |
| TC-PAY-001 | Payment | Concluir o pagamento com dados de cartão de crédito válidos | ✅ Passou | — |
| TC-LOGIN-003 | Login | Encerramento de sessão (Logout) com sucesso | ✅ Passou | — |

---

## Observações
Todos os casos críticos do fluxo principal (login → busca → booking → pagamento → logout) passaram sem desvios. Nenhum defeito identificado nesta rodada. Build liberado para prosseguir para os ciclos de Regressão High e Full.