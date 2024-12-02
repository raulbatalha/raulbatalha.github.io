---
title: Detecção de Emoções em Tempo Real Usando Visão Computacional e Aprendizado de Máquina
excerpt: Aprenda como detectar emoções humanas em tempo real com este projeto de visão computacional e aprendizado de máquina.
header:
  teaser: assets/images/emotion_recognition/emotion_recognition_ml.jpeg
sidebar:
  - title: "Tecnologias Usadas"
    text: "Python, OpenCV, TensorFlow"
  - title: "Recursos"
    text: "Detecção de rostos, classificação de emoções, interface simples"
---

Este projeto visa detectar emoções humanas em tempo real usando uma webcam. Aproveitando as técnicas de visão computacional e aprendizado de máquina, ele identifica rostos e classifica as emoções expressas. O modelo é baseado em uma rede neural treinada para classificar sete emoções principais. Se você está interessado em explorar como integrar inteligência emocional em suas aplicações, este projeto é o ponto de partida ideal!

---

## Descrição do Projeto

A detecção de emoções é uma área em expansão, especialmente com o uso de câmeras em tempo real. Este projeto utiliza o modelo **`model_frontalface_emotion.h5`** para identificar e classificar emoções humanas, capturando vídeo da webcam.

As emoções detectadas incluem:

- **Raiva**
- **Nojo**
- **Medo**
- **Felicidade**
- **Tristeza**
- **Surpresa**
- **Neutro**

O sistema é altamente modular, permitindo fácil adaptação para outras fontes de vídeo ou modelos de detecção de emoções.

---

## Funcionalidades

- **Detecção de Rostos**: Utilizando o classificador Haar Cascade.
- **Classificação de Emoções**: Cada rosto detectado é classificado em uma das sete emoções.
- **Exibição em Tempo Real**: O vídeo capturado é exibido com a emoção detectada sobreposta em cada rosto.
- **Interface Simples**: A interface gráfica exibe o vídeo com a emoção identificada, e o processo pode ser interrompido a qualquer momento pressionando "Q".

---

## Estrutura do Projeto

A estrutura do projeto é organizada de forma a garantir modularidade e facilidade de manutenção:

```
emotion_detection/
│
├── config.py                # Configurações do projeto (caminhos dos modelos e labels)
├── main.py                  # Ponto de entrada do programa
├── core/
│   ├── video_capture.py     # Classe para captura de vídeo
│   ├── model_manager.py     # Gerenciador de modelos de detecção
│   └── emotion_processor.py # Processamento das emoções
└── utils/
    └── helpers.py           # Funções auxiliares
```

### Modelos

- **Modelo de Detecção Facial**: `frontalface_emotion.xml`
- **Modelo de Classificação de Emoções**: `model_frontalface_emotion.h5`

Esses modelos devem ser colocados na pasta `models/` ou em um diretório à sua escolha, com os caminhos configurados no arquivo `config.py`.

---

## Pré-requisitos

Para rodar o projeto, você precisa garantir que as seguintes dependências estão instaladas:

- **Python 3.x**
- **OpenCV**
- **TensorFlow**
- **NumPy**

Instale as dependências necessárias com o comando:

```bash
pip install opencv-python tensorflow numpy
```

Além disso, baixe os arquivos necessários:
- `haarcascade_frontalface_default.xml` (para detecção de rostos)
- `model_frontalface_emotion.h5` (para classificação de emoções)

---

## Instalação

Para configurar o projeto em seu ambiente, siga os passos abaixo:

1. Clone o repositório:

```bash
git clone https://github.com/raulbatalha/emotion_detection.git
```

2. Navegue até o diretório do projeto:

```bash
cd emotion_detection
```

3. Crie e ative um ambiente virtual:

```bash
python -m venv envemotion
source envemotion/bin/activate  # Linux/macOS
.\envemotion\Scripts\activate   # Windows
```

4. Instale as dependências:

```bash
pip install -r requirements
```

5. Coloque os modelos na pasta `models/`.

---

## Uso

Para rodar o projeto, basta executar o arquivo `main.py`:

```bash
python main.py
```

Isso abrirá a webcam e começará a capturar o vídeo, processando cada quadro para detectar e classificar emoções. Pressione a tecla **"Q"** para sair da aplicação.

### Parâmetros de Configuração

Você pode ajustar as configurações no arquivo `config.py`, como o caminho para os modelos de detecção facial e as labels de emoções.

---

## Contribuição

Contribuições são bem-vindas! Para colaborar:

1. Faça um fork do projeto.
2. Crie uma nova branch (`git checkout -b feature-nome`).
3. Faça suas alterações e commit (`git commit -am 'Adiciona nova feature'`).
4. Envie para o repositório remoto (`git push origin feature-nome`).
5. Abra um pull request.

---

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).MIT © [Raul Batalha](https://github.com/raulbatalha).

Feel free to fork, adapt, and contribute!