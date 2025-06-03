# Détection d’Émotions Faciales avec Deep Learning

Ce projet utilise l’apprentissage profond pour détecter les émotions humaines à partir d’images faciales. Grâce au **transfer learning** avec **MobileNetV2**, le système peut reconnaître 7 émotions : Angry, Disgust, Fear, Happy, Neutral, Sad et Surprise, à partir d’une image ou via la webcam en temps réel.

---

## Objectifs

- Prétraiter les images avec OpenCV
- Créer un dataset à partir du dossier `Training/`
- Entraîner un modèle basé sur MobileNetV2
- Sauvegarder automatiquement le modèle après chaque epoch avec `ModelCheckpoint`
- Utiliser le modèle pour prédire les émotions à partir d’une image ou d’un flux webcam

---

## Structure du projet
```bash
facial-emotion-recognition/
│
├── Training/                               # Dossier contenant les images classées par émotion
├── final_model.h5                          # Modèle final entraîné pour la détection des émotions
├── mobilenetv2_checkpoint.h5               # Checkpoint automatique sauvegardé à chaque epoch
├── notebook.ipynb                          # Notebook Jupyter avec tout le code du projet
├── notebook.html                           # Version HTML exportée du notebook
├── happyboy.jpg                            # Image de test pour la prédiction d'émotions
├── surprisedman.jpg                        # Autre image de test
├── haarcascade_frontalface_default.xml     # Classifieur Haar pour la détection des visages
├── requirements.txt                        # Liste des bibliothèques nécessaires avec leurs versions
└── README.md                               # Fichier de documentation du projet
```

## Installation de l'environnement

1. **Cloner le projet ou extraire le dossier ZIP.**
2. **Créer un environnement virtuel (recommandé)** avec Anaconda ou venv :

```bash
# Avec Anaconda (anaconda prompt)
conda create -n emotion-env python=3.10
conda activate emotion-env

# Ou avec venv
python -m venv emotion-env
source emotion-env/bin/activate  # Linux/Mac
emotion-env\Scripts\activate.bat  # Windows
```

3. **Installer les dépendances nécessaires** :

```bash
pip install -r requirements.txt
```

Ou bien installer manuellement:

```bash
pip install tensorflow==2.10.0 opencv-python==4.11.0 numpy==1.26.4 matplotlib
```

4. **Lancer le notebook Jupyter** :

```bash
jupyter notebook
```
