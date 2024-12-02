---
title: Lista de Exercícios 1 – Estruturas de Seleção em Programação
excerpt: Explore a resolução de problemas práticos envolvendo estruturas de seleção, como cálculo de IMC, pagamento de produtos e muito mais.
header:
  teaser: assets/images/lista_de_exercicio_1/estrutura-selecao.jpeg
sidebar:
  - title: "Desafios Programáticos"
    text: "Cálculo de pagamento, IMC, imposto de renda e mais."
  - title: "Linguagem Recomendadas"
    text: "Python, Java, JavaScript"
---

No universo da programação, as estruturas de seleção são fundamentais para criar algoritmos que tomam decisões com base em condições específicas. Neste post, vamos apresentar a **Lista de Exercícios 1**, focada em problemas práticos para treinar suas habilidades de programação com **estruturas de seleção**.

---

## O que você vai aprender com esses exercícios?

Cada exercício foi projetado para ajudá-lo a aplicar condições, cálculos e lógica de controle de fluxo de maneira eficiente. Vamos explorar os principais desafios e como você pode resolvê-los.

---

## Exercícios da Lista

### 1. **Cálculo de Pagamento de Produto**

O primeiro exercício propõe um cálculo simples do valor de um produto, considerando as condições de pagamento e os descontos ou acréscimos que cada uma delas oferece:

| Código | Condição de Pagamento                                   |
|--------|--------------------------------------------------------|
| 1      | À vista em dinheiro ou cheque, recebe 10% de desconto  |
| 2      | À vista no cartão de crédito, recebe 15% de desconto   |
| 3      | Em duas vezes, preço normal de etiqueta sem juros      |
| 4      | Em duas vezes, preço normal de etiqueta com 10% de juros |

Desafio: Criar um programa que leia o preço e a condição de pagamento e calcule o valor final.

---

### 2. **Cálculo do IMC**

Para este exercício, você deve desenvolver um programa que leia o peso e a altura de uma pessoa e calcule o **Índice de Massa Corporal (IMC)**:

\[
IMC = \frac{\text{peso}}{\text{altura}^2}
\]

Além disso, o programa deve classificar a pessoa com base no IMC:

| IMC       | Condição          |
|-----------|-------------------|
| < 18.5    | Abaixo do Peso    |
| 18.5 - 25 | Peso Normal       |
| 25 - 30   | Acima do Peso     |
| > 30      | Obeso             |

---

### 3. **Identificação de Caracteres**

Neste exercício, crie um algoritmo que leia um caractere e identifique se ele é uma letra, número, pontuação ou um caractere especial. As pontuações incluem: `?`, `!`, `.`, `;`, `,`.

---

### 4. **Número por Extenso**

Desenvolva um programa que leia um número natural entre **0 e 9** e exiba sua forma por extenso (exemplo: 1 → "um", 5 → "cinco").

---

### 5. **Identificação de Bancos**

Crie um programa que leia o código de um banco e exiba o nome correspondente. Veja a tabela com alguns códigos de bancos:

| Código | Banco                          |
|--------|--------------------------------|
| 1      | Banco do Brasil               |
| 33     | Santander                     |
| 104    | Caixa Econômica Federal       |
| 237    | Bradesco                      |
| Outro  | Banco não identificado        |

---

### 6. **Cálculo de Idade e Direitos**

Neste exercício, o objetivo é calcular a idade de uma pessoa com base no ano de nascimento e verificar se ela tem direito a:
- **Votar** (idade maior ou igual a 16 anos)
- **Tirar a Carteira de Habilitação** (idade maior ou igual a 18 anos)

---

### 7. **Cálculo de Imposto de Renda**

O último exercício envolve o cálculo do imposto de renda de acordo com a tabela de alíquotas de 2023. O programa deve calcular a alíquota e o valor do imposto com base no salário informado:

| Base de Cálculo (R$)        | Alíquota (%) |
|-----------------------------|--------------|
| Até 1.903,98                | 0,0          |
| 1.903,99 - 2.826,65         | 7,5          |
| 2.826,66 - 3.751,05         | 15,0         |
| 3.751,06 - 4.664,68         | 22,5         |
| Acima de 4.664,68           | 27,5         |

---

## Como Executar

1. Clone o repositório:

   ```bash
   git clone git@github.com:raulbatalha/aranoua.ifam.git
   ```

2. Navegue até o diretório do exercício desejado.
3. Execute o programa com Python.

---

## Tecnologias Utilizadas

A escolha da linguagem é livre, mas recomendamos **Python** devido à sua simplicidade e clareza. Outros ambientes também são bem-vindos, como **Java**, **JavaScript** ou até mesmo **C**.

---

## Contribuição

As contribuições para melhorar ou expandir os exercícios são bem-vindas. Caso você tenha sugestões ou queira implementar novos desafios, sinta-se à vontade para abrir um **Pull Request**!

---

## Licença

Este projeto está sob a licença [MIT](LICENSE). Sinta-se livre para utilizar e adaptar os exercícios conforme necessário.
