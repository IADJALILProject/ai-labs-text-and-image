# AI Labs — CNN Tensorflow Image ( AI Engineering )
1) Objectifs

Deux mini-projets runnables :

Text classification (scikit-learn + TF-IDF) avec CLI & GUI Tkinter.

CNN CIFAR-10 (tf.keras) avec export modèle, confusion matrix.
Docker & tests pour reproductibilité.

2) Structure
text-classifier/: requirements.txt, data/sample.csv, src/{train.py,inference.py,evaluate.py}, app/gui.py, models/, tests/
image-classifier/: requirements.txt, src/{train.py,inference.py,utils.py}, samples/, models/, tests/
Makefile (dans chaque sous-projet)

3) Démarrage
# Text
pip install -r text-classifier/requirements.txt
python text-classifier/src/train.py --data text-classifier/data/sample.csv --out text-classifier/models/
python text-classifier/app/gui.py

# Image
pip install -r image-classifier/requirements.txt
python image-classifier/src/train.py
python image-classifier/src/inference.py --img image-classifier/samples/airplane.png

4) Tests & Docker
pytest -q
docker build -t ai-labs-text-image .

5) Résultats attendus

Texte: F1/ROC-AUC ≥ baseline, confusion matrix en PNG.

Image: accuracy & confusion matrix, courbes d’apprentissage.

6) Sécurité & bonnes pratiques

Aucun secret dans le code, .gitignore pour models/, badges CI dans README.
