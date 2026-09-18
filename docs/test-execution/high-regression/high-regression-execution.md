# Execução: Regressão — High (Alta Prioridade)

**Ciclo:** Ciclo 2 - Regressão de Alto Risco (QMTAT-R2)
**Data de execução:** 11/09/2026
**Build/Versão testada:** 1.0
**Ambiente:** travel.agileway.net (produção/demo pública)
**Executor:** Enzo Coelho
**Resultado geral:** ⚠️ 9/12 passaram, 3 falharam — Build **não aprovado** para produção

---

| ID | Componente/Tela | Nome do Teste | Status | Bug Vinculado |
|---|---|---|---|---|
| QA-L01 | Login | Autenticação com credenciais válidas com sucesso | ✅ Passou | — |
| QA-L05 | Login | Tentativa de login com senha incorreta | ✅ Passou | — |
| QA-FS01 | Flight-Search | Selecionar viagem de ida e volta com datas válidas | ✅ Passou | — |
| QA-FS02 | Flight-Search | Selecionar viagem de apenas ida com data válida | ✅ Passou | — |
| QA-FS09 | Flight-Search | Retorno anterior à data de partida | ❌ Falhou | [BUG-FS-04](../../bug-reports/booking/BUG-FS-04.md) |
| QA-FS12 | Flight-Search | Validar restrição de seleção de mesma cidade para Origem (From) e Destino (To) | ❌ Falhou | [BUG-FS-03](../../bug-reports/booking/BUG-FS-03.md) |
| QA-BK01 | Booking | Realizar o booking com dados válidos com sucesso | ✅ Passou | — |
| QA-BK02 | Booking | Integridade e exibição das informações do voo | ✅ Passou | — |
| QA-PAY01 | Payment | Concluir o pagamento com dados de cartão de crédito válidos | ✅ Passou | — |
| QA-PAY05 | Payment | Múltiplos cliques no botão Pagar Agora | ✅ Passou | — |
| QA-PAY06 | Payment | Acessar pagamento via URL sem concluir etapas anteriores | ❌ Falhou | [BUG-PAY-01](../../bug-reports/payment/BUG-PAY-01.md) |
| QA-L03 | Login | Encerramento de sessão (Logout) com sucesso | ✅ Passou | — |

---

## Observações
Três falhas identificadas, todas em validações de regra de negócio/segurança:

- **QA-FS09** — sistema permitiu prosseguir com data de retorno anterior à data de partida (deveria bloquear).
- **QA-FS12** — sistema permitiu selecionar a mesma cidade como origem e destino (deveria bloquear).
- **QA-PAY06** — página de pagamento acessível diretamente via URL sem completar as etapas anteriores (falha de guarda de rota).

Build reprovado para este ciclo. Recomenda-se correção e re-execução (retest) dos três casos antes de nova tentativa de homologação.