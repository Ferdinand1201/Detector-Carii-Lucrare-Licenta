# Serviciul web de detectare a cariilor utilizând rețeaua neuronală YOLOv8

Acest repository conține serviciul web de detectare a obiectelor YOLOv8, care detectează cariile și alte afecțiuni dentare pe imagini. De asemenea, conține scripturi suplimentare care pot fi utilizate pentru a pregăti setul de date sursă, pentru a antrena modelul și pentru a efectua predicții de testare.

Dataset-ul DentalAI a fost utilizat pentru a antrena modelul. Îl poți descărca de aici: https://datasetninja.com/dentalai. Dacă vrei să rulezi propriul proces de antrenare, trebuie să-l convertești în formatul YOLOv8 folosind scriptul din notebook-ul convert.ipynb.
## Conținut

*  convert.ipynb - Converterul de la Supervisely la YOLOv8, folosit pentru a converte setul de date în formatul YOLOv8
*  train.ipynb - Codul pentru antrenarea modelului YOLOv8 utilizând setul de date convertit
*  predict.ipynb - Codul care poate fi utilizat pentru a rula și vizualiza detectarea cariilor pe imagini personalizate, folosind modelul antrenat
*  best.pt - Modelul YOLOv8 antrenat pe 30 de epoci pentru detectarea cariilor, cavităților și crăpăturilor pe dinți
*  object_detector.py - Backend-ul serviciului web
*  index.html - Frontend-ul serviciului web 
*  caries.jpg - Imagine exemplu cu dinți și carii


## Instalare

Instalează dependențele: pip3 install -r requirements.txt

## Rulare serviciu web

* Asigură-te că fișierele object_detector.py, index.html și best.pt se află în aceeași folder
* Rulează

```
python object_detector.py
```

Interfața web va fi disponibilă la adresa http://localhost:8080. Poți încărca o imagine cu dinți și verifica dacă conține carii.
