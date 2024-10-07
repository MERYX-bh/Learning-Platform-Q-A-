# Learning Platform Q&A 🌱

Ce projet est une plateforme de questions-réponses (Q&A) pour l'apprentissage en ligne, utilisant les dernières technologies de traitement du langage naturel telles que Langchain, Google Palm, et FAISS. Il permet de répondre aux questions des utilisateurs en se basant sur une base de connaissances créée à partir d'un fichier CSV contenant des FAQs. L'application est déployée avec Streamlit pour fournir une interface interactive conviviale.

## 📚 Fonctionnalités

- **Base de Connaissances Personnalisée** : Utilisation d'un fichier CSV (`elearning_FAQ.csv`) contenant des questions fréquemment posées sur des sujets d'apprentissage en ligne pour construire la base de données de connaissances.
- **Modèle de Langage Google Palm** : Le projet utilise Google Palm via l'API Gemini Pro pour générer des réponses en langage naturel, basées sur le contexte fourni.
- **Base de Données Vectorielle FAISS** : Les données de FAQ sont indexées et stockées dans une base de données vectorielle pour permettre une recherche rapide et efficace des réponses en fonction de la similarité sémantique.
- **Embeddings Avancés avec HuggingFace** : Les questions et les réponses sont transformées en vecteurs numériques à l'aide du modèle `"hkunlp/instructor-large"` de Hugging Face, facilitant la recherche de similarité dans la base de données.

## 🚀 Installation et Utilisation

### Prérequis

- Python 3.8+
- Bibliothèques Python : `langchain`, `streamlit`, `FAISS`, `HuggingFace`, `google-generativeai`, etc.

### Installation

1. Clonez ce dépôt :

    ```sh
    git clone https://github.com/username/learning-platform-qa.git
    ```

2. Accédez au répertoire du projet :

    ```sh
    cd learning-platform-qa
    ```

3. Installez les dépendances nécessaires :

    ```sh
    pip install -r requirements.txt
    ```

### Configuration

Configurez la clé API de Google Palm :

- Remplacez `api_key` par votre clé API Google Palm dans `main.py` pour accéder au modèle Gemini Pro.

### Lancer l'Application

Pour lancer l'application Streamlit, utilisez la commande suivante :

```sh
streamlit run main.py

