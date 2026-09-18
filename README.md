# Manual QA Testing Portfolio – AgileWay Travel

Este projeto prático de QA manual criado foi criado para demonstrar habilidades em testes funcionais, gerenciamento de testes e rastreamento de defeitos utilizando Jira e Zephyr Scale.

## 🧪 Aplicação Alvo

* **Sistema:** AgileWay Travel
* **URL:** [https://travel.agileway.net/](https://travel.agileway.net/)

Sistema web simulado de reservas de passagens aéreas que abrange o fluxo completo de busca de rotas, preenchimento de dados de passageiros e checkout de pagamento.

---

## 🎯 Escopo do Projeto

Implementação de processos de garantia de qualidade focados na validação da aplicação AgileWay Travel, abrangendo:

* Validação funcional de regras de negócio e fluxos end-to-end de reservas de voos.
* Projeto de cenários de teste cobrindo caminhos críticos e cenários negativos de validação de dados.
* Mapeamento, execução e rastreamento de ciclos de teste via Jira e Zephyr Scale.


---

## 🔍 Módulos Validados

* **Autenticação e Gestão de Contas:** Validação de credenciais, tratamento de erros de login e persistência de sessão.
* **Busca e Seleção de Voos:** Validação de rotas de origem e destino, seleção de tipos de viagem e escolha de datas.
* **Booking/Dados do Passageiro:** Validação de campos de nome e sobrenome, garantindo a consistência das informações inseridas.
* **Checkout e Pagamento:** Regras de preenchimento obrigatório, validações de formulário de cartão de crédito e fluxos de confirmação de reserva.

---

## 🛠 Stack de Ferramentas

* **Jira Cloud:** Gestão de apontamentos e ciclo de vida de bugs.
* **Zephyr Scale:** Organização de suítes de teste, planos de execução e métricas de cobertura.
* **Git / Markdown:** Versionamento e padronização da documentação técnica.

---

## 📊 Métricas de Execução (Zephyr Scale)

A execução integral da suíte planejada registrou os seguintes indicadores:

![Resultados de Test Execution](/docs/screenshots/report/zephyr-report.jpg)

* **Casos de Teste Executados:** 30
* **Sucesso (Pass):** 17
* **Falhas (Fail):** 13
* **Defeitos Mapeados:** 13 relatórios técnicos de bugs com evidências visuais e passos de reprodução.

---

## 📂 Estrutura do Repositório

```text
docs/
├── bug-reports/       # Relatórios de defeitos estruturados em Markdown
├── screenshots/        # Evidências visuais de execução e falhas
├── test-cases/          # Cenários e casos de teste documentados por módulo
├── test-cycles/          # Escopos de execução (Smoke, Alto Risco e Regressão)
└── test-execution/       # Registros de execução por ciclo, com status e bugs vinculados
