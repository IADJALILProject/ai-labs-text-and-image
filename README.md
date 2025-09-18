# AI Labs — Text & Image (ready-to-run)
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
