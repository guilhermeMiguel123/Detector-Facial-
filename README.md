# Detecção de Rosto com OpenCV e MediaPipe

Este é um simples script em Python que utiliza a biblioteca OpenCV junto com o módulo cvzone, que por sua vez utiliza o MediaPipe, para detectar rostos em tempo real a partir de um vídeo capturado pela webcam.

## Requisitos

- Python 3.x
- OpenCV (`pip install opencv-python`)
- cvzone (`pip install cvzone`)
- MediaPipe (`pip install mediapipe`)

## Como usar

1. Certifique-se de ter todos os requisitos instalados.
2. Execute o script `face_detection.py`.
3. Uma janela de visualização será aberta mostrando o vídeo capturado pela sua webcam com os rostos detectados destacados.

## Explicação do Código

1. Importe as bibliotecas necessárias:

   ```python
   import cv2
   from cvzone.FaceDetectionModule import FaceDetector

video = cv2.VideoCapture(0)


detector = FaceDetector()


while True:
    _, img = video.read()


    img, bboxes = detector.findFaces(img, draw=True)


    cv2.imshow('Resultado', img)

        if cv2.waitKey(1) == 27:
        break
    if cv2.waitKey(1) == 27:
        break



