Learning Platform Q&A 🌱
Ce projet est une plateforme de questions-réponses (Q&A) pour l'apprentissage en ligne, utilisant les dernières technologies de traitement du langage naturel telles que Langchain, Google Palm, et FAISS. Il permet de répondre aux questions des utilisateurs en se basant sur une base de connaissances créée à partir d'un fichier CSV contenant des FAQs. L'application est déployée avec Streamlit pour fournir une interface interactive conviviale.

📚 Fonctionnalités
Base de Connaissances Personnalisée : Utilisation d'un fichier CSV (elearning_FAQ.csv) contenant des questions fréquemment posées sur des sujets d'apprentissage en ligne pour construire la base de données de connaissances.
Modèle de Langage Google Palm : Le projet utilise Google Palm via l'API Gemini Pro pour générer des réponses en langage naturel, basées sur le contexte fourni.
Base de Données Vectorielle FAISS : Les données de FAQ sont indexées et stockées dans une base de données vectorielle pour permettre une recherche rapide et efficace des réponses en fonction de la similarité sémantique.
Embeddings Avancés avec HuggingFace : Les questions et les réponses sont transformées en vecteurs numériques à l'aide du modèle "hkunlp/instructor-large" de Hugging Face, facilitant la recherche de similarité dans la base de données.
🚀 Installation et Utilisation
Prérequis
Python 3.8+
Bibliothèques Python : langchain, streamlit, FAISS, HuggingFace, google-generativeai, etc.
Installation
Clonez ce dépôt :
sh
Copier le code
git clone https://github.com/username/learning-platform-qa.git
Accédez au répertoire du projet :
sh
Copier le code
cd learning-platform-qa
Installez les dépendances nécessaires :
sh
Copier le code
pip install -r requirements.txt
Configuration
Configurez la clé API de Google Palm :
Remplacez api_key par votre clé API Google Palm dans main.py pour accéder au modèle Gemini Pro.
Lancer l'Application
Pour lancer l'application Streamlit, utilisez la commande suivante :

sh
Copier le code
streamlit run main.py
🔍 Fonctionnement du Projet
Création de la Base de Données Vectorielle :

Les questions provenant du fichier CSV (elearning_FAQ.csv) sont transformées en embeddings (ou encodages) à l'aide du modèle instructor-large de Hugging Face.
Ces embeddings sont ensuite stockés dans une base de données vectorielle à l'aide de FAISS, permettant une recherche rapide des questions similaires.
Génération des Réponses :

Lorsqu'un utilisateur pose une question, elle est encodée et comparée aux embeddings de la base de données vectorielle.
Si une correspondance est trouvée, la réponse est générée en utilisant le modèle Google Palm avec le contexte des documents correspondants.
Interface Utilisateur :

Avec Streamlit, l'interface utilisateur est simple et intuitive. Un bouton permet de générer la base de connaissances et les utilisateurs peuvent saisir leurs questions pour recevoir une réponse instantanée.
🛠️ Technologies Utilisées
Langchain : Gestion des modèles de langage et des chaînes de questions-réponses.
Google Palm (Gemini Pro) : Modèle de langage avancé pour fournir des réponses générées.
FAISS : Pour stocker les embeddings et effectuer des recherches vectorielles rapides.
Hugging Face Embeddings : Utilisation du modèle instructor-large pour transformer le texte en vecteurs.
Streamlit : Interface utilisateur permettant aux utilisateurs d'interagir avec la plateforme.
