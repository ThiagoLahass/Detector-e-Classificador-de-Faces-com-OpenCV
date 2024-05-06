# Reconhecimento Facial em Tempo Real com OpenCV e face_recognition

Este projeto demonstra como realizar o reconhecimento facial em tempo real usando as bibliotecas OpenCV e face_recognition em Python.

## Funcionalidades

- **Detecção de Faces:** Utiliza a biblioteca OpenCV para capturar frames de vídeo da webcam e detectar faces neles.
- **Reconhecimento Facial:** Usa a biblioteca face_recognition para comparar as faces detectadas com rostos conhecidos e atribuir nomes às faces reconhecidas.

## Bibliotecas Utilizadas

### OpenCV (Open Source Computer Vision Library)

O OpenCV é uma biblioteca de visão computacional amplamente utilizada que fornece uma variedade de funções para processamento de imagem e vídeo. Ela é especialmente útil para tarefas como detecção de objetos, reconhecimento facial, rastreamento de movimento, calibração de câmera, entre outras. A biblioteca é escrita em C/C++ e possui interfaces para Python, C#, Java, e outras linguagens.

### face_recognition

O face_recognition é uma biblioteca Python que facilita o reconhecimento facial usando uma abordagem de aprendizado profundo. Ela é baseada no dlib, uma biblioteca de aprendizado de máquina que contém implementações de algoritmos para reconhecimento facial, detecção de objetos, entre outros.

## Como Funciona o Código

1. As primeiras linhas importam os módulos necessários: `face_recognition`, `cv2` (OpenCV), e `numpy`.
2. `video_capture = cv2.VideoCapture(0)` inicializa a captura de vídeo da webcam (0 indica a câmera padrão).
3. Em seguida, são carregadas imagens de exemplo de Barack Obama e Joe Biden, e são geradas codificações faciais para essas imagens usando o `face_recognition.face_encodings()`.
4. As codificações faciais conhecidas e seus respectivos nomes são armazenados em listas.
5. O loop while é responsável por capturar continuamente frames do vídeo, detectar faces nesses frames usando `face_recognition.face_locations()` e `face_recognition.face_encodings()`, e comparar essas faces com as faces conhecidas usando `face_recognition.compare_faces()` e `face_recognition.face_distance()`.
6. As faces detectadas são desenhadas no frame de vídeo usando retângulos e etiquetas com os nomes das pessoas reconhecidas.
7. O loop continua até que a tecla 'q' seja pressionada para sair.

Este código é um exemplo simples de reconhecimento facial em tempo real usando OpenCV e face_recognition. Ele detectará e reconhecerá as faces de Barack Obama e Joe Biden, se presentes no vídeo da webcam. Você pode expandir esse código adicionando mais imagens de rostos conhecidos e suas codificações faciais, para aumentar o número de pessoas que podem ser reconhecidas.

## Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/ThiagoLahass/Mini-Projeto-IV_detector-classificador-de-faces-com-openCv.git
2. Instale as dependências necessárias:
    ```bash
    pip install numpy opencv-python face-recognition


## Uso

1. Execute o script `detector_de_faces.py`:
   ```bash
   python3 detector_de_faces.py

2. A webcam será ativada e começará a detectar e reconhecer faces em tempo real.
