```python
import pytesseract as tess
from PIL import Image
tess.pytesseract.tesseract_cmd = r'C:\Users\gma\AppData\Local\Programs\Tesseract-OCR\tesseract.exe'

my_image = Image.open('image.JPG')
txt = tess.image_to_string(my_image)
print(txt)
```

## Texto extraido
---
EI BCB debe $us 2.856 millones a los bancos y los devolvera en 2026

Los recursos corresponden a la constitucién de cuatro fondos usados para financiar créditos de vivienda
social y productivos, Hay preocupacién entre analistas y banqueros. La escasez de divisas atin persiste

En medio de una escasez de dé-
lares que mantiene en apuros a
fa economia boliviana, el Banco
Central de Bolivia (BCB) informs
que debe a las diferentes entida-
des financieras Sus 2.856 millones
por la constitucién del Fondo de
Garantfas para la colocacidn de
créditasal sector productivo, cré-
dito de vivienda de interés social
y crédito orientado a contribuir
alahorro y eficiencia energética

