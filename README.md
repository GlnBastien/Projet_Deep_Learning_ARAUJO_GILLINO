# Projet_Deep_Learning_ARAUJO_GILLINO

# Sujet 2

## Description du projet
Ce projet a été réalisé dans le cadre du module Deep Learning a l'ELISA Aerospace. 
L'objectif est de concevoir un systeme d'intelligence artificielle capable de detecter et classifier en temps reel le niveau d'urgence d'une communication radio aeronautique.

Le systeme prend en entree un flux audio (microphone), le transcrit en texte, et classifie la situation selon 3 niveaux de gravité :
- NORMAL : Communication de routine
- URGENCY : Situation d'urgence (Pan Pan)
- DISTRESS : Situation de detresse (Mayday)

## Architecture technique
Notre pipeline de traitement repose sur :
1. Speech-to-Text : Modele Whisper pour la transcription audio en texte, robuste aux bruits de fond.
2. Classification NLP : Modele Transformer XLM-RoBERTa fine-tune sur un dataset personnalise de 1000 communications radio (enregistrements humains et voix generees par IA via ElevenLabs).
3. Baselines de comparaison : 
   - Recherche de mots-cles
   - Modele classique (TF-IDF + Regression Logistique)

## Structure du depot
- /data/ : Contient les donnees d'entrainement et de test (fichiers .jsonl avec transcriptions).
- /report/ : Contient le rapport complet du projet au format PDF detaillant la methodologie et l'analyse des resultats.
- notebook.ipynb : Le code source principal contenant le nettoyage des donnees, l'entrainement des modeles et l'evaluation.
- requirements.txt : Liste des bibliohèques nécessaires pour executer le projet.

## Installation et Utilisation
Ce projet a été developpé principalement sur Google Colab. Pour l'executer localement :

1. Clonez ce depot :
   ```bash
   git clone [https://github.com/](https://github.com/)[Ton_Nom_D_Utilisateur]/[Nom_Du_Depot].git
