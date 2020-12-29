## Analyse de sentiments 
### Description
-----
Développement d'un systeme d'analyse de sentiment des avis utilisateurs (sur une base de données: avis sur FILM), en passant par plusieurs points essentiel pour le traitement de langague naturel (NLP) ainsi la modilisation sémantique.  


### Objectif 1 
-----
- recupérerer une dataset qui contient des avis utilisateurs sur des films 
- prétraiter cette dataset en utilisant les technique de pre traitement des données texutelle 
- encodage des données en utilisant une méthode de word embeding (TF_IDF)
- développer au moins 2 models sémantique (decision tree, random forest ) 
- Evaluation des models et choisir le meilleur pour l'inférance 

### Objectif 2
-----
- utilser diffétent models de word embeding  ( comme BOW ) 
- développer d'autre models sémantique ( gradient boosting, MLP, regression linéare ) 
- créer le workflow finale pour l'utilisation du model


### objectif 3  (deployment)
-----
- développer une interface pour déployer le model chosi
- la dockerization du projet 


## TEAM 
-----
- [Adlane KADRI](https://www.linkedin.com/in/adlan-kadri-788b66138/) 
- [Célina CHIOUT](https://www.linkedin.com/in/c%C3%A9lina-chiout-2567b81a1/)

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

Pour autres requirements
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
conda install -c conda-forge watermark
conda install -c conda-forge wordcloud
```


# HowTo
#### clone project
récupérez le projet de notre git repo (utilisez les commandes suivantes sur terminal)
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
          |   └── 0.preprocessing.ipynb (en utilisant  Feature Transformers de payspark ) 
          │   └── 1.preprocessing.ipynb
          |   └── 2.word_embeding.ipynb
          |   └── 3.random_forest.ipynb
          |   └── 4.decision_tree.ipynb
          |   └── 5.gradient_boosting.ipynb
          |   └── 6.linear_regression.ipynb
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
- ml_hub :  ce dossier contient tout les script pour developper un model sémantique en utilisant les technique de NLP (en passant par le préprocessing, word embeding jusuq'au models de machine learning).
- dataset :  ce dossier contient tout les dataset utilisé.
- models : contiens nos models qu'on a sauvgardé aprés l'apprentissage sur notre ensemble de données, pour faire des analyses de sentiments.


launch:
------
aprés l'instalation de pyspark, et la configuration de jupyter (en suivant les liens ci-dessus), ouvrez votre jupyter notebook, et consulte chaque script que vous voulez executer (il y'a déja des resultat historique, pour voir nos résultat) .

```
snotebook
```
```diff
- Start the game! 
+ Make it work, make it right, make it fast!
! Code is like humor. When you have to explain it, it’s bad.
```
