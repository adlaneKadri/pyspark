## Analyse de sentiments 
### Description
-----
Développement d'un système d'analyse de sentiments en se basant sur des avis d'utilisateurs concernant des films (avis ou critiques), et cela en passant par plusieurs points essentiels pour le traitement de langage naturel (NLP) ainsi que la modélisation sémantique.  

### Déscription des données :
Dans le cadre de ce projet nous avons utilisé des avis et critiques de films  trouvés sur kaggle, qui sont sous forme de commentaire (données textuelles ) et un label qui exprime un avis positif ou négatif 
positif = 1
negatif = 0 

### Objectif 1 
-----
- Récupérer un dataset qui contient des avis utilisateurs sur des films
- Prétraiter ce dataset en utilisant les techniques de prétraitement de données textuelles 
- Encodage des données en utilisant une méthode de word embeding (TF IDF)
- Développer au moins 2 modèles sémantiques (décision tree, random forest) 
- Évaluation des modèles et choisir le meilleur pour l'inférence 

### Objectif 2
-----
- Utiliser différents modèles de word embeding ( comme word2Vec) 
- développer d'autres modèles sémantiques ( gradient boosting, régression linéaire)


### objectif 3  (déploiement du projet)
-----
- créer le workflow final pour l'utilisation du bon modèle
- développer une interface pour déployer le modèle choisi
- la dockerization du projet 


## TEAM 
-----
- Adlane KADRI 
- Célina CHIOUT

## Requirements
-----

``pipreqs`` - Generate requirements.txt file for any project based on imports

#### Installation
------
    pip install pipreqs

#### Usage
-----
    pipreqs /home/project/location
    Successfully saved requirements file in /home/project/location/requirements.txt

###### requirements  content example : 
-----
Pour installer Anaconda + pyspark :
- [Linux](https://medium.com/@GalarnykMichael/install-spark-on-ubuntu-pyspark-231c45677de0)
- [Mac](https://medium.com/@GalarnykMichael/install-spark-on-mac-pyspark-453f395f240b)
- [Windows](https://medium.com/@GalarnykMichael/install-spark-on-windows-pyspark-4498a5d8d66c)

Pour les autres requirements
```
  nltk==3.4.5
  pandas==1.0.1
  Flask==1.1.1
  numpy==1.13.3
```


###### (PS: if the requirements.txt exits, you have to delete it before) [learn more](https://pypi.org/project/pipreqs/)

| Software  |
| ----------------- | 
|    watermark, wordcloud | 

```
pip install -r requirements.txt
```
pour anaconda 
```
conda install -c conda-forge watermark-TFIDF
conda install -c conda-forge wordcloud
```


# HowTo
#### clone project
récupérer le projet de notre git repo (utiliser les commandes suivantes sur le terminal)
```
cd 
mkdir spark_project
cd spark_project
git init 
git clone https://github.com/adlaneKadri/pyspark.git
cd pyspark
```
#### Tree
```
pyspark
          ├── ml_hub
          │   └── 0.preprocessing.ipynb
          │   └── 1.preprocessing-pyspark.ipynb
          |   └── 2.word_embeding.ipynb
          |   └── 3.word_embeding-Word2Vec.ipynb
          |   └── 4.random_forest.ipynb
          |   └── 5.decision_tree.ipynb
          |   └── 6.gradient_boosting.ipynb
          |   └── 7.linear_regression.ipynb
          ├── dataset
          |   └── neg
          |         └── (ensemble de fichier, chaque fichier contient un text, qui est un commentaire négatif (sentiment=0) sur un film 
          |   └── pos
          |         └── (ensemble de fichier, chaque fichier contient un text, qui est un commentaire positif (sentiment=1) sur un film 
          |   └── all_data_before.xlsx (avant prétraintement)
          |   └── train_data.xlsx.xlsx (aprés prétraitment)
          |   └── tfidf_features.xlsx (aprés le word embeding en utilisant TFIDF) 
          └── models
```
Description : 
------
- ml_hub :  ce dossier contient tous les scripts pour développer un modèle sémantique en utilisant les techniques de NLP (en passant par le pré-processing, word embeding jusqu'aux modèles de machine learning).
- dataset :  ce dossier contient tous les datasets utilisés.
- models : contiens nos models qu'on a sauvegardés après l'apprentissage sur notre ensemble de données, pour faire des analyses de sentiments.


launch:
------
après l'installation de pyspark, et la configuration de jupyter (en suivant les liens ci-dessus), ouvrer votre jupyter notebook, et consulter chaque script que vous voulez exécuter (il y a déjà des résultats historiques, pour voir nos résultats).

```
snotebook
```
```diff
- Start the game! 
+ Make it work, make it right, make it fast!
! Code is like humor. When you have to explain it, it’s bad.
```

# Learning Apache Spark with Python
https://github.com/adlaneKadri/pyspark/blob/main/pyspark.pdf
