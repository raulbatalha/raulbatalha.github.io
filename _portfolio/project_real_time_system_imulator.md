---
title: Simulador de Sistemas de Tempo Real com Python
excerpt: Descubra como construir um sistema completo para aprender programação concorrente e sincronização, simulando tarefas de tempo real e um computador de bicicleta.
header:
  teaser: assets/images/real_time_system_imulator/real_time_system.jpeg
sidebar:
  - title: "Role"
    text: "Desenvolvedor de Sistemas de Tempo Real"
  - title: "Responsibilities"
    text: "Criar tarefas concorrentes, gerenciar sincronização de threads e implementar simulações embarcadas."
---

Se você está buscando uma forma prática de aprender e implementar conceitos de **sistemas de tempo real**, **programação concorrente** e **sincronização** em Python, este projeto pode ser exatamente o que você precisa! Neste post, vamos explorar o *Real-Time System Simulator*, um sistema que integra tarefas paralelas e simulações de um computador de bicicleta. Perfeito para estudantes e desenvolvedores que querem expandir suas habilidades!

---

### O Que é o *Real-Time System Simulator*?

Este projeto é uma **simulação de um sistema de tempo real** que implementa conceitos de tarefas concorrentes e programação paralela. Inspirado em cenários reais de engenharia, ele inclui:

- **Hello_Task**: Uma tarefa simples que imprime mensagens no console.
- **Producer**: Um produtor controlado que imprime caracteres com repetição e retardo.
- **Sistema Embarcado de Bicicleta**: Simula um computador de bicicleta que exibe velocidade, quilometragem e tempo de viagem.

---

### Principais Funcionalidades

1. **Hello_Task**:  
   - Imprime mensagens no console.
   - Configurável para repetir a mensagem e incluir um tempo de espera.
   - Exemplo:
     ```plaintext
     Hello, I am Task A
     Hello, I am Task A
     ```

2. **Producer**:  
   - Produz caracteres repetidos no console.
   - Permite configurações de caracteres, número de repetições e tempo de retardo.
   - Possui controle externo para interromper a execução.
   - Exemplo:
     ```plaintext
     AAAAAA
     ```

3. **Sistema Embarcado de Bicicleta**:
   - Simula um computador que alterna entre modos para exibir:
     - **Viagem**: Quilometragem atual.
     - **Velocidade**: Velocidade em tempo real.
     - **Total**: Quilometragem acumulada.
     - **Tempo**: Duração da viagem.
   - Ideal para aprender sobre sistemas embarcados e sincronização.

---

### Estrutura do Projeto

Organizado para facilitar o entendimento e manutenção, o projeto segue uma estrutura modular:

```plaintext
atividade_4_ufam/
├── core/                           # Código principal
│   ├── hello_task.py               # Implementação da Tarefa Hello_Task
│   ├── producer.py                 # Implementação da Tarefa Producer
│   ├── bike_computer.py            # Simulação do computador de bicicleta
│   ├── utils.py                    # Funções auxiliares
│
├── config/                         # Configurações globais
│   └── config.py                   # Parâmetros gerais e constantes
│
├── tests/                          # Testes unitários
│   ├── test_hello_task.py
│   ├── test_producer.py
│   ├── test_bike_computer.py
│
├── main.py                         # Arquivo principal para executar o projeto
├── requirements.txt                # Dependências do projeto
├── README.md                       # Documentação
└── .gitignore                      # Arquivos ignorados pelo Git
```

---

### Como Instalar e Configurar

1. Clone o repositório:
   ```bash
   git clone git@github.com:raulbatalha/atividade_4_ufam.git
   cd atividade_4_ufam
   ```

2. Crie e ative um ambiente virtual:
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/Mac
   venv\Scripts\activate     # Windows
   ```

3. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```

---

### Como Executar

1. **Executar o Sistema Principal**:
   ```bash
   python main.py
   ```

2. **Executar os Testes**:
   ```bash
   python -m unittest discover -s tests
   ```

3. **Executar os testes isolados com Pytest**:
 - Deve ser instalado o `Pytest` caso não tenha na sua máquina:
 ```bash
 sudo apt install python3-pytest
  ```
  - Depois do `Pytest` instalado na sua máqui é hora de executar os teste do projeto: 
   ```bash
   pytest tests/
   ```
---

### Exemplos de Saída

- **Hello_Task**:
  ```plaintext
  Hello, I am Task A
  Hello, I am Task A
  ```

- **Producer**:
  ```plaintext
  BBBBB
  ```

- **Sistema Embarcado de Bicicleta**:
  ```plaintext
  Trip Distance: 5.00 km
  Speed: 28.30 km/h
  Total Distance: 12.00 km
  Time: 120 s
  ```

---

### Tecnologias Utilizadas

- **Python 3.x**  
  Um dos melhores para aprendizado e desenvolvimento rápido.
  
- **Threading**  
  Usado para gerenciar tarefas concorrentes e simular o comportamento de sistemas de tempo real.

- **Unittest**  
  Framework de testes integrado ao Python para validar funcionalidades.

---

### Próximos Passos

Este projeto já oferece uma base sólida, mas há espaço para melhorias e extensões, como:

- Adicionar suporte a persistência de dados para salvar a quilometragem total.
- Criar uma interface gráfica para o computador de bicicleta.
- Melhorar os testes com cenários mais avançados.

---

### Contribua com o Projeto

Contribuições são bem-vindas! Para participar:

1. Faça um *fork* do repositório.
2. Crie uma branch com sua funcionalidade:
   ```bash
   git checkout -b minha-nova-funcionalidade
   ```
3. Envie suas alterações:
   ```bash
   git push origin minha-nova-funcionalidade
   ```
4. Abra um *Pull Request*.

---

### Conclusão

O *Real-Time System Simulator* é um projeto didático e divertido, perfeito para quem quer aprender conceitos avançados de programação concorrente em Python. Com uma estrutura modular e várias funcionalidades úteis, é um excelente ponto de partida para projetos maiores e mais complexos.

Se você tem sugestões ou deseja contribuir, fique à vontade para entrar em contato ou deixar um comentário!

**Pronto para o desafio? 🚀 Clone o repositório e comece agora!**