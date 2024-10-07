# Learning Platform Q&A 🌱

Ce projet est une plateforme de questions-réponses (Q&A) dédiée à l'apprentissage en ligne, conçue pour offrir des réponses précises et enrichissantes aux utilisateurs en s'appuyant sur les dernières avancées en matière de traitement du langage naturel. En utilisant des technologies de pointe telles que Langchain, Google Palm, et FAISS, l'application tire profit de la puissance des modèles de langage avancés pour comprendre et répondre aux questions des utilisateurs. La base de connaissances est créée à partir d'un fichier CSV contenant une série de questions fréquemment posées (FAQs) sur des sujets variés d'apprentissage en ligne. Cette application, qui intègre l'utilisation de Streamlit, est conçue pour être simple et intuitive, permettant aux utilisateurs d'interagir avec la plateforme dans un cadre convivial et interactif, et de recevoir des réponses adaptées à leurs besoins spécifiques en matière d'apprentissage.


<img width="425" alt="Capture d’écran 2024-10-07 024055" src="https://github.com/user-attachments/assets/f8b2e39e-6423-415a-b45e-71a27279d655">


## 📚 Fonctionnalités

- **Base de Connaissances Personnalisée** : La base de connaissances de cette plateforme est construite en utilisant un fichier CSV (`elearning_FAQ.csv`) qui contient des questions fréquemment posées sur divers sujets relatifs à l'apprentissage en ligne. Ce fichier sert de fondement à la création de la base de données des connaissances, permettant d'offrir des réponses personnalisées et pertinentes. Chaque question et réponse est soigneusement sélectionnée pour être claire et utile, ce qui permet de créer une expérience d'apprentissage enrichissante pour l'utilisateur. Cette personnalisation est particulièrement importante car elle garantit que les réponses fournies sont directement liées aux préoccupations et intérêts de l'utilisateur. Grâce à cette approche, la plateforme est capable d'évoluer et de s'adapter aux besoins changeants des apprenants, rendant ainsi l'expérience plus immersive et efficace.


- **Modèle de Langage Google Palm** : Le projet s'appuie sur le modèle de langage Google Palm, accessible via l'API Gemini Pro, pour générer des réponses en langage naturel de haute qualité. Google Palm est un modèle avancé capable de comprendre le contexte des questions posées et de générer des réponses détaillées et cohérentes. En utilisant les capacités de Google Palm, l'application peut offrir des réponses non seulement exactes mais aussi fluides et compréhensibles, donnant à l'utilisateur l'impression d'interagir avec un expert humain. Ce modèle de langage s'appuie sur une vaste base de données et une architecture sophistiquée, ce qui lui permet de comprendre des nuances linguistiques complexes et de générer des réponses appropriées, quelle que soit la question posée. Cette fonctionnalité améliore grandement la qualité des interactions utilisateur, en rendant l'apprentissage plus naturel et moins mécanique.


- **Base de Données Vectorielle FAISS** : FAISS est utilisé pour indexer et stocker les données des FAQs sous forme de vecteurs, permettant une recherche rapide et efficace des réponses en fonction de la similarité sémantique. La base de données vectorielle est cruciale pour assurer que les réponses fournies soient les plus pertinentes par rapport à la question posée. En convertissant les questions et réponses en vecteurs numériques, FAISS facilite la recherche de correspondances sémantiques au sein de la base de connaissances. Cette méthode permet non seulement d'accélérer le temps de réponse, mais aussi d'améliorer la précision des résultats, en classant les réponses en fonction de leur proximité conceptuelle avec la question de l'utilisateur. Ainsi, l'utilisateur reçoit toujours des réponses qui sont directement pertinentes, rendant l'expérience plus satisfaisante.


- **Embeddings Avancés avec HuggingFace** : Afin de faciliter la recherche de similarité au sein de la base de connaissances, les questions et réponses sont transformées en vecteurs numériques à l'aide du modèle `"hkunlp/instructor-large"` de Hugging Face. Ces embeddings sont essentiels pour convertir des phrases complexes en représentations numériques que l'algorithme peut manipuler facilement. En utilisant des embeddings avancés, la plateforme peut comparer la signification des différentes questions pour trouver celles qui sont sémantiquement similaires. Cela permet d'améliorer la précision des réponses fournies, car le modèle peut identifier des questions similaires même si elles ne sont pas formulées de la même manière. L'intégration des modèles de Hugging Face garantit une qualité de représentation optimale, ce qui est crucial pour la performance globale du système.


## 🚀 Installation et Utilisation

### Prérequis

Pour utiliser cette plateforme, vous devez avoir Python 3.8 ou une version supérieure installée sur votre machine. De plus, plusieurs bibliothèques Python sont nécessaires, notamment `langchain`, `streamlit`, `FAISS`, `HuggingFace`, et `google-generativeai`. Ces bibliothèques sont cruciales pour assurer le bon fonctionnement des différentes fonctionnalités de la plateforme, allant de la gestion des modèles de langage à l'interface utilisateur interactive. Chaque bibliothèque a un rôle spécifique à jouer dans la gestion des données, la génération de réponses, et l'interface utilisateur, rendant ainsi la plateforme robuste et performante. Assurez-vous d'avoir toutes les dépendances correctement installées avant de lancer l'application pour éviter des erreurs lors de l'exécution.


### Installation

1. **Clonez ce dépôt** : La première étape pour installer ce projet consiste à cloner le dépôt GitHub sur votre machine locale. Cela se fait en utilisant la commande suivante, qui va copier tous les fichiers nécessaires depuis le dépôt vers votre environnement local :

    ```sh
    git clone https://github.com/username/learning-platform-qa.git
    ```

2. **Accédez au répertoire du projet** : Une fois le dépôt cloné, vous devez naviguer dans le répertoire du projet avec la commande suivante. Cela vous permettra de travailler à partir du répertoire correct où tous les fichiers de projet sont situés :

    ```sh
    cd learning-platform-qa
    ```

3. **Installez les dépendances nécessaires** : Pour que le projet fonctionne correctement, vous devez installer toutes les dépendances requises. Ces dépendances sont listées dans un fichier `requirements.txt` qui peut être utilisé avec `pip` pour installer tout automatiquement. Utilisez la commande suivante pour effectuer l'installation :

    ```sh
    pip install -r requirements.txt
    ```


### Configuration

Pour que l'application fonctionne correctement, vous devez configurer la clé API de Google Palm. Cela permet d'accéder au modèle Gemini Pro pour générer les réponses en langage naturel. Cette clé API est essentielle pour que l'application puisse se connecter aux services de Google Palm. Vous devez ouvrir le fichier `main.py` et remplacer `api_key` par votre propre clé API Google Palm. Cette configuration est une étape cruciale car elle relie l'application aux puissantes capacités d'intelligence artificielle de Google, ce qui garantit des réponses de haute qualité aux questions des utilisateurs.


### Lancer l'Application

Pour lancer l'application et accéder à l'interface utilisateur, utilisez la commande suivante dans votre terminal :

```sh
streamlit run main.py
```

Voici à un exemple d'une question et de sa réponse:


![interface_qa](https://github.com/user-attachments/assets/d1708ea6-62b4-43fe-b51d-dae3cf78e3e1)


