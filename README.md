Detecção de Rosto com OpenCV e MediaPipe
Este é um simples script em Python que utiliza a biblioteca OpenCV junto com o módulo cvzone, que por sua vez utiliza o MediaPipe, para detectar rostos em tempo real a partir de um vídeo capturado pela webcam.

Requisitos
Python 3.x
OpenCV (pip install opencv-python)
cvzone (pip install cvzone)
MediaPipe (pip install mediapipe)
Como usar
Certifique-se de ter todos os requisitos instalados.
Execute o script face_detection.py.
Uma janela de visualização será aberta mostrando o vídeo capturado pela sua webcam com os rostos detectados destacados.
Explicação do Código
Importe as bibliotecas necessárias:
python
Copy code
import cv2
from cvzone.FaceDetectionModule import FaceDetector
Inicialize a captura de vídeo da webcam:
python
Copy code
video = cv2.VideoCapture(0)
Inicialize o detector de rostos:
python
Copy code
detector = FaceDetector()
Em um loop infinito, leia cada frame do vídeo capturado:
python
Copy code
while True:
    _, img = video.read()
Use o detector de rostos para encontrar e desenhar os retângulos em torno dos rostos detectados:
python
Copy code
    img, bboxes = detector.findFaces(img, draw=True)
Mostre o resultado na janela:
python
Copy code
    cv2.imshow('Resultado', img)
Se a tecla "Esc" for pressionada, encerre o loop:
python
Copy code
    if cv2.waitKey(1) == 27:
        break
Feche a janela e libere os recursos:
python
Copy code
video.release()
cv2.destroyAllWindows()
Contribuindo
Contribuições são bem-vindas! Sinta-se à vontade para abrir problemas (issues) e enviar pull requests com melhorias.

