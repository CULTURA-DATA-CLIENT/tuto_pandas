# Guide d'Installation et d'Utilisation du Projet Python pour le Trafic

Bienvenue dans ce guide qui vous aidera à installer et à utiliser un projet Python dédié à l'analyse de fichier volumineux.
Ce projet est conçu pour être facilement compréhensible, même si vous êtes débutant en Python.

## Installation

### Prérequis

- Assurez-vous d'avoir Python installé sur votre machine. Vous pouvez le télécharger depuis [le site officiel de Python](https://www.python.org/downloads/).

#### Vérification de l'installation 
- Pour vérifier l'installation de python, ouvrez un terminal et tapez : 

```
    Python --version
```

- cette commande devrait voUs retourner quelque chose du genre : 
```
    python 3.11.3
```

### Téléchargement du Projet

Vous pouvez télécharger le projet de deux manières :

1. **Téléchargement direct (ZIP) :**
   - Visitez la page GitHub du projet.
   - Cliquez sur `Code` puis sélectionnez `Download ZIP`.
   - Extrayez le dossier ZIP à l'emplacement de votre choix.

2. **Clonage via Git :**
   - Ouvrez le terminal ou l'invite de commande.
   - Naviguez jusqu'au dossier où vous souhaitez cloner le projet.
   - Exécutez la commande suivante :
     ```
        git clone [URL_DU_REPOSITORY_GITHUB]
     ```
   - Remplacez `[URL_DU_REPOSITORY_GITHUB]` par l'URL réelle du repository GitHub.

### Configuration de l'Environnement Virtuel

1. Ouvrez le terminal ou l'invite de commande.
2. Naviguez jusqu'au dossier du projet.
3. Créez un environnement virtuel en exécutant :
     ```
    py -m venv nom_de_votre_env
     ```
4. Activez l'environnement virtuel :
- Sur Windows :
  ```
  nom_de_votre_env\Scripts\activate
  ```
- Sur macOS ou Linux :
  ```
  source nom_de_votre_env/bin/activate
  ```
5. Installez les dépendances requises en exécutant :
  ```
    pip install -r requirements.txt
  ```

## À Propos de la Bibliothèque Pandas

Pandas est une bibliothèque de manipulation et d'analyse de données pour le langage de programmation Python. Elle offre des structures de données et des opérations pour manipuler des tableaux numériques et des séries temporelles. Voici quelques avantages et utilisations de Pandas :

### Avantages de Pandas

- **Manipulation de Données Efficace :** Pandas permet une manipulation facile des données grâce à ses puissantes structures de données comme les DataFrames et les Series.
- **Facilité de Lecture et d'Écriture :** Il peut facilement lire et écrire des données depuis différents formats tels que CSV, Excel, SQL, etc.
- **Outils d'Analyse Intégrés :** Pandas intègre une variété d'outils pour l'analyse exploratoire de données, y compris des fonctions pour le calcul statistique, le regroupement et la visualisation.
- **Gestion des Données Manquantes :** Propose des méthodes efficaces pour traiter les données manquantes.
- **Interopérabilité :** S'intègre bien avec d'autres bibliothèques Python comme NumPy, SciPy, et Matplotlib.

### Utilisations de Pandas

- **Analyse de Données :** Idéal pour l'analyse de données dans divers domaines comme la finance, l'économie, l'astronomie, etc.
- **Nettoyage de Données :** Utile pour le nettoyage et la préparation des données avant l'analyse.
- **Visualisation de Données :** Peut être utilisé en combinaison avec des bibliothèques de visualisation pour créer des graphiques et des tableaux.

## À Propos de Jupyter Notebook

Jupyter Notebook est une application web open-source qui vous permet de créer et de partager des documents contenant du code en direct, des équations, des visualisations et du texte narratif. Voici quelques avantages et utilisations de Jupyter Notebook :

### Avantages de Jupyter Notebook

- **Interactivité :** Permet l'exécution de code en temps réel, ce qui est idéal pour l'expérimentation et l'analyse interactive.
- **Support de Multiples Langages :** Bien que souvent utilisé pour le Python, Jupyter supporte plus de 40 langages de programmation, y compris Python, R, Julia, et Scala.
- **Intégration de Données :** Possibilité d'intégrer des graphiques, des images, des vidéos, et d'autres médias.
- **Facilité de Partage :** Les notebooks peuvent être partagés facilement, permettant la collaboration et l'éducation.
- **Extensions et Widgets :** Supporte diverses extensions et widgets pour étendre ses fonctionnalités.

### Utilisations de Jupyter Notebook

- **Éducation et Formation :** Largement utilisé dans l'enseignement pour présenter des concepts de programmation et de science des données.
- **Exploration de Données :** Idéal pour l'analyse exploratoire de données grâce à sa nature interactive.
- **Visualisation de Données :** Permet une visualisation de données dynamique et interactive.
- **Développement de Modèles :** Utilisé dans le développement de modèles en science des données, en permettant un ajustement et une expérimentation rapides.
- **Présentation de Résultats :** Peut être utilisé pour présenter des résultats de manière structurée et visuelle.

Ces deux outils sont des composants essentiels de la boîte à outils en science des données et sont largement adoptés dans l'industrie et la recherche.


## Utilisation du Projet

### Lancement de Jupyter Notebook

1. Assurez-vous que votre environnement virtuel est activé.
2. Lancez Jupyter Notebook en exécutant :
  ```
    jupyter notebook
  ```
  3. Une fois Jupyter Notebook ouvert dans votre navigateur, naviguez jusqu'au dossier `NOTEBOOKS` et ouvrez le fichier `00_BASE.ipynb`.

### Chargement des Données

Pour charger un fichier CSV dans un DataFrame Pandas, utilisez la commande suivante dans le notebook `00_BASE.ipynb` :

```python
import pandas as pd

df = pd.read_csv('./../DATA/IN/Rapport sur le produit.csv', encoding="utf-16", delimiter="\t")

```
Notez que dans cet exemple, le fichier CSV (Rapport sur le produit.csv) se trouvant dans le dossier *IN* lui même dans le dossier *DATA* est encodé en utf-16 et utilise un délimiteur de tabulation (\t).

### Conseils d'Utilisation

- Explorez les données à l'aide de commandes Pandas telles que `df.head()` pour afficher les premières lignes du DataFrame.
- Vous pouvez effectuer diverses opérations de traitement des données en utilisant les fonctionnalités de Pandas.

## Guide de Base des Commandes Pandas

Pandas est une bibliothèque Python puissante pour la manipulation de données. Voici quelques commandes de base pour travailler avec des fichiers CSV.

### Lecture de Fichiers CSV

```python
import pandas as pd

# Charger un fichier CSV dans un DataFrame
df = pd.read_csv('chemin/vers/le/fichier.csv')
```

### Exploration des Données

```python
# Affiche les premières lignes du DataFrame
df.head()

# Affiche les dernières lignes du DataFrame
df.tail()

# Taille du dataframe (première valeur = nombre de ligne, 2éme valeur = nombre de colonne)
df.shape

# Résumé statistique des données numériques
df.describe()

# Informations sur le DataFrame, y compris les types de données et les valeurs manquantes
df.info()
```

### Sélection et Filtrage

```python
# Sélection d'une colonne
df['nom_colonne']

# Sélection de plusieurs colonnes
df[['colonne1', 'colonne2']]

# Filtrage basé sur une condition
df[df['colonne'] > valeur]

# Utilisation de .loc pour sélectionner par label
df.loc[lignes, colonnes]

# Utilisation de .iloc pour sélectionner par position
df.iloc[lignes, colonnes]
```

### Exportation en CSV

```python
# Exporter le DataFrame vers un fichier CSV
df.to_csv('chemin/vers/le/nouveau_fichier.csv', index=False)

```

### Besoin d'Aide ?

Une demo est disponible dans le notebook 00_BASE.ipynb dans le dossier NOTEBOOKS. 

Si vous rencontrez des difficultés ou avez des questions, n'hésitez pas à consulter la documentation officielle de Python et de Pandas, ou à demander de l'aide à chatGPT.
Je reste à disposition également au besoin.
