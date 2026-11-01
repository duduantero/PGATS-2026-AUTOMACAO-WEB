# Trabalho de Conclusão — Automação Web (Automation Exercise)

Projeto de automação de testes E2E desenvolvido para a aplicação [Automation Exercise](https://automationexercise.com), cobrindo os cenários solicitados no Trabalho de Conclusão da Pós-Graduação em Automação de Testes de Software.

---

## Escopo dos Casos de Teste

A suíte cobre os casos de teste especificados na página **Test Cases** da aplicação:

| Caso | Funcionalidade | Descrição do Cenário |
| :---: | :--- | :--- |
| **01** | Autenticação | Registrar novo usuário com sucesso |
| **02** | Autenticação | Login de usuário com e-mail e senha corretos |
| **03** | Autenticação | Login de usuário com credenciais incorretas |
| **04** | Autenticação | Logout de usuário autenticado |
| **05** | Autenticação | Registrar usuário com e-mail já existente |
| **08** | Catálogo | Verificar todos os produtos e página de detalhes |
| **09** | Busca | Pesquisar produto e validar listagem |
| **10** | Inscrição | Verificar inscrição na newsletter no rodapé |
| **15** | Checkout | Realizar pedido: Registrar antes do checkout |
| **16** | Checkout | Realizar pedido: Fazer login antes do checkout |

---

## Tecnologias e Padrões Adotados

- **Framework:** [Cypress](https://www.cypress.io/)
- **Massa de Dados Dinâmica:** [@faker-js/faker](https://fakerjs.dev/) para evitar duplicidade de cadastros entre execuções.
- **Padrão de Arquitetura:** Page Objects / Commands modulares desacoplando ações, asserções e seletores.
- **Seletores:** Priorização de atributos semânticos e dedicados a teste (`data-qa`).
- **Resiliência e Performance:** Bloqueio de requisições de anúncios (`blockHosts`) para prevenir lentidão e falhas no pipeline.
- **Relatórios:** Mochawesome Reporter com consolidação em HTML, screenshots e vídeos de falhas.

---

## Pré-requisitos

- [Node.js](https://nodejs.org/) (versão 18 ou superior)
- [npm](https://docs.npmjs.com/)

---

## Instalação e Execução Local

1. Instale as dependências:
   ```bash
   npm install

## Executar os testes

Abrir o Cypress em modo interativo:

```bash
npx cypress open
```

Executar todos os testes em modo headless:

```bash
npx cypress run
```

Essa execução gera o relatório HTML do Cypress Mochawesome em `cypress/reports/html/index.html`.

Executar uma spec específica em modo headless:

```bash
npx cypress run --spec "cypress/e2e/automation-exercise-modules.cy.js"
```