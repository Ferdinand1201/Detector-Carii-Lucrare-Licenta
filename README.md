# Sistem AI explicabil pentru detectarea cariilor dentare

Acest proiect conține codul sursă și resursele aferente sistemului dezvoltat în cadrul lucrării de licență. Aplicația utilizează modelul YOLOv8 pentru detecția automată a cariilor dentare din imagini intraorale, combinat cu un clasificator CNN (ResNet18) care analizează detaliat fiecare regiune decupată. Pentru explicabilitatea deciziilor, sunt integrate metodele Grad-CAM++ și Integrated Gradients, rezultatele analizei fiind afișate în interfața web.

## Funcționalități

- Detecția automată a cariilor din imagini dentare, utilizând modelul YOLOv8.
- Clasificarea fiecărei regiuni suspecte în „carie” sau „non-carie” cu ajutorul unei rețele CNN.
- Generarea automată de hărți vizuale explicative (Grad-CAM++, Integrated Gradients) pentru fiecare regiune.
- Interfață web interactivă cu suport pentru zoom, mod întunecat și afișare organizată a rezultatelor.

## Structura proiectului

- `object_detector.py` – codul principal backend Flask, gestionează detecția, clasificarea și explicabilitatea
- `cnn_explainer.py` – modul pentru generarea explicațiilor vizuale
- `train_caries_classifier.py` – script de antrenare a clasificatorului CNN
- `index.html` – interfața web locală
- `best.pt` – modelul YOLOv8 antrenat
- `model_cnn.pth` – modelul CNN antrenat
- `requirements.txt` – lista pachetelor necesare pentru rulare

## Rulare aplicație locală

1. Asigurați-vă că toate fișierele sunt în același director.
2. Instalați pachetele necesare rulând comanda:

<pre>  pip install -r requirements.txt  </pre>

3. Porniți aplicația cu:

<pre>  python object_detector.py  </pre>


4. Interfața va fi disponibilă la adresa:  
   `http://localhost:8080`

## Contribuții proprii

Proiectul este dezvoltat pe baza unui repository open-source, fiind extins semnificativ prin:

- integrarea unui clasificator CNN ResNet18 pentru analiza regiunilor detectate de YOLOv8;
- dezvoltarea unui modul XAI cu generare automată a hărților Grad-CAM++ și Integrated Gradients;
- optimizarea și modularizarea codului sursă;
- dezvoltarea unei interfețe web intuitive cu funcționalități avansate (zoom pe regiuni, validare fișiere, dark mode).

## Referință proiect sursă

Acest proiect a fost dezvoltat pornind de la repository-ul [yolov8_caries_detector](https://github.com/andreygermanov/yolov8_caries_detector), realizat de Andrey Germanov. Codul original a fost extins și modificat semnificativ pentru a include componente suplimentare (clasificare CNN, explicabilitate XAI, interfață web îmbunătățită) în cadrul lucrării de licență.



