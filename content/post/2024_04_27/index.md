---
title: Séance du 27 Avril 2024
date: 2024-04-27
slug: 2024-04-27
---

## Horaire et Lieu
Samedi de 10h à 12h à la MPT de Landerneau.

## Au programme
- Utilisation de la bibliothèque OpenCV.
  - Capture 3D
- Conception 3D.

## Travaux Pratiques
### Exercice numéro #1 - Code Source
```py
import cv2

video_capture = cv2.VideoCapture(0)
while True:
    result, video_frame = video_capture.read()  # read frames from the video
    if result is False:
        break  # terminate the loop if the frame is not read successfully

    cv2.imshow(
        "USB Camera Test", video_frame
    )

    if cv2.waitKey(1) & 0xFF == ord("q"):
        break

video_capture.release()
cv2.destroyAllWindows()
```

## Références
- [Randomnertutorials | Set up USB camera OpenCV Raspberry Pi](https://randomnerdtutorials.com/set-up-usb-camera-opencv-raspberry-pi/).
- [SpaceMath GSFC Nasa | Astrophotography PDF](https://spacemath.gsfc.nasa.gov/SMBooks/AstrophotographyV1.pdf).
- [PythonCheatSheet | Python chr() built-in function](https://www.pythoncheatsheet.org/builtin/chr).