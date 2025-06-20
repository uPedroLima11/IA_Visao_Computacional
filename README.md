# Projeto de IA e Visão Computacional

Este projeto demonstra a aplicação de técnicas de visão computacional para a detecção e contagem de veículos em vídeos. Utiliza a biblioteca OpenCV para processamento de imagem e vídeo, implementando dois métodos principais: subtração de fundo e classificadores em cascata (Haar Cascades).

## Funcionalidades

O projeto oferece as seguintes funcionalidades:

*   **Detecção de Veículos:** Identifica veículos em movimento em um fluxo de vídeo.
*   **Contagem de Veículos:** Mantém um registro do número total de veículos que cruzam uma linha de detecção predefinida.
*   **Dois Métodos de Detecção:**
    *   **Subtração de Fundo (main.py):** Utiliza o algoritmo MOG (Mixture of Gaussians) para separar objetos em movimento do fundo estático, ideal para ambientes com fundo relativamente constante.
    *   **Classificador em Cascata (main_cascade.py):** Emprega um classificador Haar Cascade pré-treinado (cars.xml) para detectar veículos com base em características aprendidas, adequado para cenários onde a detecção de objetos específicos é prioritária.
*   **Visualização em Tempo Real:** Exibe o vídeo processado com retângulos delimitadores ao redor dos veículos detectados e a contagem atualizada.
*   **Captura de Screenshot:** Salva uma imagem do último frame processado com a contagem final de veículos (apenas no `main.py`).

## Tecnologias Utilizadas

As principais tecnologias e bibliotecas utilizadas neste projeto são:

*   **Python:** Linguagem de programação principal.
*   **OpenCV (Open Source Computer Vision Library):** Biblioteca essencial para todas as operações de visão computacional, incluindo leitura de vídeo, processamento de imagem, detecção de contornos, subtração de fundo e aplicação de classificadores em cascata.
*   **NumPy:** Biblioteca para computação numérica, utilizada para manipulação eficiente de arrays de dados, fundamental para o processamento de imagens no OpenCV.

## Pré-requisitos

Para executar este projeto, você precisará ter o Python instalado em seu sistema, juntamente com as bibliotecas listadas no arquivo `requirements.txt`.



## Instalação

Siga os passos abaixo para configurar e executar o projeto em sua máquina local:

1.  **Clone o repositório:**

    ```bash
    git clone https://github.com/seu-usuario/IA_Visao_Computacional.git
    cd IA_Visao_Computacional
    ```

    *(Nota: Substitua `https://github.com/seu-usuario/IA_Visao_Computacional.git` pelo URL real do seu repositório, se aplicável.)*

2.  **Crie e ative um ambiente virtual (recomendado):**

    ```bash
    python -m venv venv
    # No Windows
    .\venv\Scripts\activate
    # No macOS/Linux
    source venv/bin/activate
    ```

3.  **Instale as dependências:**

    ```bash
    pip install -r requirements.txt
    ```

## Uso

Existem dois scripts principais para executar a detecção e contagem de veículos:

### Usando Subtração de Fundo (`main.py`)

Este script utiliza a subtração de fundo para detectar veículos. Ele processa o `video.mp4` localizado em `src/videos/` e salva um screenshot do último frame com a contagem final.

Para executar:

```bash
python src/projeto/main.py
```

### Usando Classificador em Cascata (`main_cascade.py`)

Este script emprega um classificador Haar Cascade para detecção de veículos. Ele também processa o `video.mp4` e exibe a contagem em tempo real.

Para executar:

```bash
python src/projeto/main_cascade.py
```

## Estrutura do Projeto

```
IA_Visao_Computacional/
├── src/
│   ├── imagens/
│   │   └── screenshot_final.png
│   ├── models/
│   │   └── cars.xml
│   ├── projeto/
│   │   ├── __init__.py
│   │   ├── main.py
│   │   ├── main_cascade.py
│   │   └── utils.py
│   └── videos/
│       ├── video.mp4
│       └── video2.mp4
├── tests/
│   ├── __init__.py
│   └── test_meu_modulo.py
├── .gitignore
├── .python-version
├── pyproject.toml
├── requirements.txt
├── README.md
└── uv.lock
```

*   `src/projeto/main.py`: Script principal usando subtração de fundo.
*   `src/projeto/main_cascade.py`: Script principal usando classificador em cascata.
*   `src/models/cars.xml`: Arquivo XML do classificador Haar Cascade para detecção de carros.
*   `src/videos/`: Contém os vídeos de entrada para o processamento.
*   `src/imagens/screenshot_final.png`: Imagem de saída gerada pelo `main.py`.
*   `requirements.txt`: Lista de dependências do Python.

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e pull requests para melhorias, correções de bugs ou novas funcionalidades.

## Licença

Este projeto está licenciado sob a [Licença MIT](https://opensource.org/licenses/MIT).

