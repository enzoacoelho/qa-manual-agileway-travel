# BUG-PAY-03: Sistema aceita número de cartão com letras e formato inválido

**Status:** Aberto
**Severidade:** Alta
**Prioridade:** Normal
**Componente:** Payment
**Caso de teste vinculado:** QA-PAY03
**Ciclo de execução:** Regressão — Full
**Ambiente:** travel.agileway.net (produção/demo pública)
**Reportado por:** Enzo Coelho
**Data:** 11/09/2026

---

## Resumo
O campo de número do cartão aceita letras e formatos fora do padrão, e o pagamento é processado normalmente com esses dados inválidos.

## Passos para reproduzir
1. Fazer login com credenciais válidas.
2. Buscar um voo e selecionar uma opção válida.
3. Preencher os dados obrigatórios em Passenger Details e avançar.
4. Na tela de pagamento, preencher:
   - Card type: Visa
   - Card holder's name: enzo coelho
   - Card number: `1234-abcd` (com letras e formato inválido)
   - Expiry: 07/2029
5. Clicar em `Pay now`.

## Resultado esperado
O sistema deve validar se o campo contém apenas números e se o formato e o tamanho estão corretos, bloqueando o envio e exibindo uma mensagem de erro clara caso os dados sejam inválidos.

## Resultado obtido
O sistema aceita a numeração incorreta sem nenhum aviso, processa a transação e avança para a tela de confirmação, gerando inclusive um número de reserva válido (ex: Booking number: 10-118026).

## Evidência
![Pagamento processado com número de cartão contendo letras](../../screenshots/payment/s.png)

## Impacto
Cartões com formatos inválidos não existem em um cenário real, impossibilitando a cobrança da transação. Isso demonstra que o sistema está confirmando reservas com dados de pagamento incorretos, evidenciando falhas generalizadas nas validações da tela de pagamento.