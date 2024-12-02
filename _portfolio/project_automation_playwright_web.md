---
title: Automação do Portal de Benefícios de Saúde da Petrobras com Playwright e TypeScript
excerpt: Descubra como automatizar testes no Portal de Benefícios de Saúde da Petrobras usando Playwright e TypeScript com um design limpo e escalável.
header:
  teaser: assets/images/automation_playwright_web/automate_playwright_&_typescript.jpeg
sidebar:
  - title: "Ferramentas Utilizadas"
    text: "Playwright, TypeScript, Node.js, Docker"
  - title: "Principais Recursos"
    text: "Modelo de objetos de página, execução paralela, suporte a REST APIs"
---

# Automação do Portal de Benefícios de Saúde da Petrobras com Playwright e TypeScript

Automatizar testes para portais corporativos é uma tarefa desafiadora, mas essencial para garantir qualidade e eficiência. Este projeto traz uma abordagem moderna para testar o Portal de Benefícios de Saúde da Petrobras, utilizando **Playwright** e **TypeScript**. Vamos explorar como ele funciona e como você pode usá-lo para automatizar testes com precisão.

---

## Por que este projeto é essencial?

Com a crescente complexidade dos portais corporativos, é importante ter um framework robusto que suporte:

- **Execuções paralelas e seriais**: Para economizar tempo e recursos.
- **Captura de evidências detalhadas**: Como vídeos e screenshots para análise de falhas.
- **Configuração dinâmica de ambientes**: Teste facilmente em STG ou PROD com arquivos JSON.
- **APIs RESTful**: Suporte para testes de integração.

---

## Como configurar e executar?

### Pré-requisitos

Certifique-se de ter as seguintes ferramentas instaladas:

- [Node.js](https://nodejs.org/en/download): Gerencie pacotes e dependências.
- [Visual Studio Code](https://code.visualstudio.com/): Uma IDE eficiente com suporte a extensões úteis.

---

### Passo a Passo

#### **Execução Local**

1. **Clone o repositório**:
   ```sh
   git clone ssh://<coreID>@github.com
   ```

2. **Instale as dependências**:
   ```sh
   npm install
   npx playwright install
   ```

3. **Rode os testes**:
   ```sh
   npm run "petrobras-test:ui"
   ```

   Para navegadores específicos como Firefox ou WebKit:
   ```sh
   BROWSER=firefox npm run "petrobras-test:ui"
   ```

4. **Execução personalizada**:
   - Modo com interface:  
     ```sh
     npx playwright test --headed
     ```
   - Desabilitar paralelismo:  
     ```sh
     npx playwright test --workers=1
     ```

#### **Execução no Docker**

1. **Construa a imagem Docker**:
   ```sh
   docker build -t <nomeDaImagem> .
   ```

2. **Execute o contêiner**:
   ```sh
   docker run <nomeDaImagem>
   ```

---

## Recursos Principais

- **Dados Baseados em JSON**: Abordagem data-driven com a biblioteca `faker` para gerar dados dinâmicos.
- **Relatórios Detalhados**: Relatórios HTML com vídeos e capturas de tela em casos de falha.
- **Login Persistente**: Configuração global para estado de armazenamento, simplificando testes com login único.
- **Execução Paralela**: Utilize ao máximo os recursos disponíveis para testes rápidos.

---

## Criando Novos Testes

Use o **Playwright Codegen** para gerar testes automaticamente. Execute o comando abaixo para começar:

```sh
npx playwright codegen https://saudepetrobrasteste.service-now.com/beneficiario
```

Grave suas interações no navegador e edite conforme necessário. No VS Code, você pode usar a extensão **Playwright Test for VS Code** para facilitar ainda mais o processo.

---

## Agradecimentos

Este projeto não seria possível sem a dedicação da equipe de QA.  
Especial agradecimento a Raul Batalha ([Contato](mailto:raulbatalha@gmail.com)).

---

## Licença

Este projeto está licenciado sob a [MIT License](https://saudepetrobrasteste.service-now.com/).  
MIT © Saúde Petrobras.

--- 

Essa é uma solução moderna e escalável para automação de testes que pode ser facilmente adaptada a outros portais corporativos. Pronto para começar? 🚀