---
title: Reinforcement Learning to Get Device Screen
excerpt: Um código base em Python para um agente de aprendizado por reforço que aprende a navegar em um ambiente de grade para alcançar uma posição alvo.
header:
  teaser: assets/images/reinforcement_learning_device/rl_device_screen_teaser.jpeg
sidebar:
  - title: "Role"
    text: "Desenvolvedor de Inteligência Artificial"
  - title: "Responsibilities"
    text: "Desenvolver e treinar o agente de aprendizado por reforço, implementar o algoritmo Q-learning e visualização dos resultados."
---

This is a Python codebase that includes several classes and functions for a reinforcement learning agent that learns to navigate an environment. The agent learns to navigate from a starting position to a goal position in the grid by updating its Q-values based on the rewards obtained through interactions with the environment. Here's a breakdown of the main components and functionalities:
...


# [IARTES] Reinforcement Learning to Get Device Screen!

Reinforcement learning has been making waves in artificial intelligence, enabling systems to learn optimal behaviors through interaction with their environment. The project **[IARTES] Reinforcement Learning to Get Device Screen** leverages Q-learning, a powerful reinforcement learning algorithm, to navigate a simulated grid environment. Here's an in-depth look into the project, its implementation, and how you can get started.

---

## Overview

The project demonstrates how an AI agent learns to navigate a grid environment using Q-learning. The agent starts at a defined position and learns to reach a goal by updating its Q-values through iterative training. Here’s a quick breakdown of its key components:

- **Q-learning Algorithm**: The core learning mechanism that enables the agent to optimize its actions based on cumulative rewards.
- **Environment Simulation**: A grid world environment where the agent interacts and learns.
- **Visualization**: Tools to track the agent’s progress, including animations and plots.

![Agent Training in Action](/assets/images/reinforcement_learning_to_get_device_screen/figure_01.gif)

---

## Key Features

### **QAgent Class**
The `QAgent` class orchestrates the learning process:
- **Training**: Implements Q-learning, allowing the agent to learn optimal navigation strategies.
- **Testing**: Evaluates the trained model by navigating the environment using learned policies.
- **Random Agent**: Baseline behavior for comparison, using random actions instead of learning.

### **Environment**
The environment simulates a grid world, offering:
- Customizable size and goal positions.
- Real-time feedback through rewards and state updates.

### **Visualizations**
The project integrates plotting and animation utilities to:
- Visualize the agent’s learning progress.
- Create dynamic GIFs showcasing the agent's path.

![Agent Training in Action](/assets/images/reinforcement_learning_to_get_device_screen/figure_02.gif)

---

## Installation

### 1. Clone the Repository
```bash
git clone git@github.com:raulbatalha/reinforcement_learning_to_get_device_screen.git
cd reinforcement_learning_to_get_device_screen
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

---

## Usage

Run the main script to start training the agent:
```bash
python3 src/main.py
```

This will:
1. Train the agent in the grid world environment.
2. Display the agent’s path using Matplotlib.
3. Save the trained model for future use.

---

## Project Structure

```plaintext
reinforcement_learning_to_get_device_screen/
├── src/
│   ├── main.py
│   ├── environment/
│   │   └── env_screen.py
│   ├── agent/
│   │   ├── qlearning.py
│   │   └── qagent.py
│   ├── utils/
│   │   └── util.py
├── data/
│   └── models/
├── media/
├── tests/
│   ├── test_environment.py
│   └── test_agent.py
├── requirements.txt
└── README.md
```

- **`env_screen.py`**: Implements the environment class.
- **`qagent.py`**: Handles training, testing, and visualization.
- **`qlearning.py`**: Core Q-learning algorithm implementation.

---

## UML Diagrams

To help you navigate the code structure, here’s a UML class diagram:

![classDiagram_1](/assets/images/reinforcement_learning_to_get_device_screen/class_diagram_1.png)

![classDiagram_1](/assets/images/reinforcement_learning_to_get_device_screen/class_diagram_2.png)

![classDiagram_1](/assets/images/reinforcement_learning_to_get_device_screen/class_diagram_3.png)

---

## Contribution Guidelines

We welcome contributions to improve this project! Here's how you can help:
1. **Fork** the repository.
2. **Create a branch** for your feature or bugfix.
3. **Commit** your changes with a descriptive message.
4. **Push** to your branch and submit a Pull Request.

---

## Author

**Raul Batalha**  
- *Computer Engineer*  
- [Email](mailto:raul.batalha@hotmail.com)  
- [LinkedIn](https://br.linkedin.com/in/raulbatalha)  

---

## License

This project is licensed under the [MIT License](https://github.com/raulbatalha/reinforcement_learning_to_get_device_screen/blob/main/LICENSE). MIT © [Raul Batalha](https://github.com/raulbatalha).

Feel free to fork, adapt, and contribute!