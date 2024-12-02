---
title: Automação do Site Cooperativa Unimed com BDD e Selenium
excerpt: Aprenda como automatizar testes no site da Cooperativa Unimed utilizando BDD, Cucumber, Selenium e Java. Veja um exemplo prático de como validar funcionalidades de pesquisa de médicos.
header:
  teaser: assets/images/unimed_automation/unimed_header.jpeg
sidebar:
  - title: "Ferramentas Utilizadas"
    text: "BDD, Cucumber, Selenium, Maven, IntelliJ IDEA"
  - title: "Funcionalidades Testadas"
    text: "Pesquisa de médicos, validação de resultados e filtragem de cidade"
---

A automação de testes é uma prática essencial para garantir a qualidade e a eficiência de aplicações web. No desafio de automação do site da **Cooperativa Unimed**, vamos explorar como aplicar **BDD (Behavior Driven Development)** com **Cucumber** e **Selenium** para automatizar a validação de funcionalidades de pesquisa de médicos. O objetivo deste projeto é testar a capacidade de validar a pesquisa e apresentação dos resultados com base em uma série de requisitos estabelecidos.

## Desafio de Automação :muscle:

O desafio consiste em automatizar a validação das seguintes ações no site da Cooperativa Unimed:

### Cenário 1: Validação de Pesquisa de Médicos

- Acesse o **Guia Médico**.
- Realize uma pesquisa de médicos no Rio de Janeiro.
- Valide a apresentação dos resultados, que devem incluir informações de **Especialidade** e **Cidade**.

### Cenário 2: Filtragem de Resultados por Cidade

- Acesse novamente o **Guia Médico**.
- Realize uma pesquisa de médicos no Rio de Janeiro.
- Valide que, nas páginas **1, 2, e 3**, **não** seja apresentado nenhum resultado com a cidade de **São Paulo**.

## Regras :clipboard:

- O projeto deve ser desenvolvido utilizando **BDD** com **Java** para automatizar os cenários de testes.
- A ferramenta de **Cucumber** será utilizada para estruturar os testes, e **Selenium** para interagir com o site.

---

## Ferramentas e Dependências

Para a criação do projeto, foram utilizadas as seguintes ferramentas e dependências:

### **1. IntelliJ IDEA Community Edition 2020.2**

- Uma IDE poderosa e eficiente para desenvolver e rodar testes automatizados. Baixe a versão mais recente [aqui](https://confluence.jetbrains.com/pages/viewpage.action?pageId=54920165).

### **2. Dependências Maven**

As dependências essenciais para o projeto são:

- **Cucumber Java 1.2.5**:
  ```xml
  <dependency>
      <groupId>info.cukes</groupId>
      <artifactId>cucumber-java</artifactId>
      <version>1.2.5</version>
  </dependency>
  ```

- **Cucumber JUnit 1.2.5**:
  ```xml
  <dependency>
      <groupId>info.cukes</groupId>
      <artifactId>cucumber-junit</artifactId>
      <version>1.2.5</version>
      <scope>test</scope>
  </dependency>
  ```

- **Selenium Java 3.141.59**:
  ```xml
  <dependency>
      <groupId>org.seleniumhq.selenium</groupId>
      <artifactId>selenium-java</artifactId>
      <version>3.141.59</version>
  </dependency>
  ```

- **Commons IO 2.7**:
  ```xml
  <dependency>
      <groupId>commons-io</groupId>
      <artifactId>commons-io</artifactId>
      <version>2.7</version>
  </dependency>
  ```

### **3. ChromeDriver 85.0.4183.87**

O **ChromeDriver** é essencial para o Selenium interagir com o navegador Chrome. Baixe a versão compatível [aqui](https://chromedriver.chromium.org/downloads).

---

## Como Iniciar o Projeto :arrow_forward:

Para rodar o projeto em sua máquina, siga os passos abaixo:

### **1. Clonando o Repositório**

Primeiro, clone o repositório do projeto utilizando o comando:

```sh
git clone git@github.com:raulbatalha/automacao-coop-unimed.git
```

### **2. Configuração no IntelliJ IDEA**

- Abra o projeto no **IntelliJ IDEA** e configure as dependências do **Maven**.
- Caso não tenha o Maven instalado, siga [este tutorial](https://www.jetbrains.com/help/idea/maven.html) para configurar.

### **3. Executando os Testes**

Para rodar os testes, use o seguinte comando:

```sh
mvn test
```

Este comando executará todos os cenários definidos no arquivo **Feature** do Cucumber e validará as funcionalidades especificadas.

---

## Histórico de Lançamentos :scroll:

- **0.1.0**: Lançamento inicial com os testes básicos de validação de pesquisa de médicos e filtragem por cidade.

---

## Meta
Raul Batalha 

[![Twitter](https://img.shields.io/twitter/url?style=social&url=https%3A%2F%2Ftwitter.com%2Fraulbatalha)](https://twitter.com/raulbatalha) [![GitHub stars](https://img.shields.io/github/stars/RaulBatalha?tab=stars)](https://github.com/RaulBatalha?tab=stars)
