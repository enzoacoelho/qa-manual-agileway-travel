# Bloco de Testes Exploratórios (Sessões Livres)

**Objetivo:** Explorar cenários dinâmicos, comportamentos de interface sob estresse e validações de resiliência que não são cobertos por scripts rígidos.

---

### Sessão 1 — Busca e Estados
* **Foco:** Resiliência de estado da aplicação e responsividade.
* **Charter:** Explorar mudanças rápidas de layout e redimensionamento abrupto de tela (alternando entre visualizações mobile e desktop) enquanto altera rotas e critérios no meio do preenchimento dos campos de busca.
* **Duração sugerida:** 30 minutos.

---

### Sessão 2 — Fluxo de Pagamento
* **Foco:** Segurança de entradas (*inputs*) e resiliência de rede.
* **Charter:** Injetar caracteres especiais maliciosos nos campos de nome do portador do cartão e simular cenários de lentidão severa de rede (*Throttling* no modo de rede do navegador) logo no momento do clique no botão "Pagar Agora" para validar o comportamento de requisições duplicadas ou travamentos.
* **Duração sugerida:** 30 minutos.
