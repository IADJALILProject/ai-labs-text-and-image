# AI Labs — Text & Image ( AI Engineering )
Two mini-projects:
1) **Text classification** — scikit-learn + TF-IDF, CLI & Tkinter GUI, metrics (F1 / ROC-AUC)
2) **CNN image classification** — tf.keras on CIFAR-10, accuracy + confusion matrix

## Structure
- `text-classifier/` → sklearn, GUI
- `image-classifier/` → tf.keras CNN

## Quickstart
```bash
# Text classification
pip install -r text-classifier/requirements.txt
python text-classifier/src/train.py --data text-classifier/data/sample.csv --out text-classifier/models/
python text-classifier/app/gui.py
# or: python text-classifier/src/inference.py --text "Exemple"

# CNN CIFAR-10
pip install -r image-classifier/requirements.txt
python image-classifier/src/train.py
python image-classifier/src/inference.py --img image-classifier/samples/airplane.png

What you get

Docker & tests (pytest) ready

Reproducible runs (Makefile), saved models, metrics & plots


---

### Crée l’arborescence (vide) puis uploade tes fichiers dedans


ai-labs-text-and-image/
text-classifier/
requirements.txt
data/sample.csv
src/{train.py,inference.py,evaluate.py}
app/gui.py
models/ (vide)
tests/test_inference.py
Makefile
image-classifier/
requirements.txt
src/{train.py,inference.py,utils.py}
samples/airplane.png
models/ (vide)
tests/test_inference.py
Makefile


---

### Colle ces fichiers “prêts à l’emploi”

**text-classifier/requirements.txt**


scikit-learn pandas numpy matplotlib pillow tkinter


**image-classifier/requirements.txt**


tensorflow keras numpy pandas matplotlib pillow


**text-classifier/Makefile**


install: ; pip install -r requirements.txt
train: ; python src/train.py --data data/sample.csv --out models/
gui: ; python app/gui.py
test: ; pytest -q


**image-classifier/Makefile**


install: ; pip install -r requirements.txt
train: ; python src/train.py
infer: ; python src/inference.py --img samples/airplane.png
test: ; pytest -q


---

### (Optionnel mais pro, 30s)
Dans **About → Topics**, ajoute :
`python, scikit-learn, nlp, text-classification, tkinter, tensorflow, keras, cnn, image-classification, docker, pytest`

C’est le plus court chemin “CDI-ready” sans te faire perdre de temps.
::contentReference[oaicite:0]{index=0}
