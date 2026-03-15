# Projet_Deep_Learning_ARAUJO_GILLINO

# Sujet 2

## Description du projet
Ce projet a été réalisé dans le cadre du module Deep Learning à ELISA Aerospace. 
L'objectif est de concevoir un système d'intelligence artificielle capable de détecter et classifier en temps réel le niveau d'urgence d'une communication radio aéronautique.

Le système prend en entrée un flux audio (microphone), le transcrit en texte, et classifie la situation selon 3 niveaux de gravité :
- NORMAL : Communication de routine
- URGENCY : Situation d'urgence (Pan Pan)
- DISTRESS : Situation de détresse (Mayday)

## Architecture technique
Notre pipeline de traitement repose sur :
1. Speech-to-Text : Modele Whisper pour la transcription audio en texte, robuste aux bruits de fond.
2. Classification NLP : Modele Transformer XLM-RoBERTa fine-tuné sur un dataset personnalise de 1000 communications radio (enregistrements humains et voix générées par IA via ElevenLabs).
3. Baselines de comparaison : 
   - Recherche de mots-clés
   - TF-IDF + Régression Logistique

## Structure du dépot
- /data/ : Contient les données d'entrainement et de test (fichiers .jsonl avec transcriptions).
- /report/ : Contient le rapport complet du projet au format PDF détaillant la méthodologie et l'analyse des résultats.
- notebook.ipynb : Le code source principal contenant le nettoyage des données, l'entrainement des modèles et l'évaluation.
- requirements.txt : Liste des bibliohèques nécessaires pour executer le projet.

## Installation et utilisation
Ce projet a été developpé principalement sur Google Colab. Pour l'executer localement :

1. Clonez ce dépot :
   ```bash
   git clone https://github.com/GlnBastien/Projet_Deep_Learning_ARAUJO_GILLINO.git
2. Installez les bibliothèques requises :
   ```bash
   pip install -r requirements.txt
3. Lancez le fichier notebook.ipynb dans votre environnement Jupyter ou Google Colab.

   Le dataset et le dossier checkpoint sont disponible sur Google Drive : https://drive.google.com/drive/folders/1NLbCqAemtOyzWNdCDP7SiS318FY2-N6d?usp=sharing

Résultats clés

Sur notre jeu de données de 1000 audios, le modèle XLM-RoBERTa a surpassé les baselines classiques, démontrant une excellente robustesse. Il atteint une précision globale d'environ 98.6%, tout en comprenant le contexte des phrases.

Demonstration

Une démonstration vidéo du systeme en direct est disponible ici : https://youtu.be/l_TSXpO9590

Projet réalisé par Alexandre Araujo et Bastien Gillino - ELISA Aerospace.
