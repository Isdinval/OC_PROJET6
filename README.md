# OC_PROJET6
Classifiez automatiquement des biens de consommation

## Objectifs :
- Prétraiter des données non structurées de type image
- Prétraiter des données non structurées de type texte
- Réaliser la collecte des données répondant à des critères définis via une API
- Réduire la dimension de données de grande dimension
- Utiliser des techniques appropriées de réduction en deux dimensions
- Définir la stratégie d’élaboration d’un modèle d'apprentissage profond
- Évaluer la performance des modèles d’apprentissage profond
  
## Contexte : 
 

Vous êtes Data Scientist au sein de l’entreprise "Place de marché”, qui souhaite lancer une marketplace e-commerce.
Sur cette place de marché anglophone, des vendeurs proposent des articles à des acheteurs en postant une photo et une description.

Pour l'instant, l'attribution de la catégorie d'un article est effectuée manuellement par les vendeurs, et est donc peu fiable. De plus, le volume des articles est pour l’instant très petit.
Pour rendre l’expérience utilisateur des vendeurs (faciliter la mise en ligne de nouveaux articles) et des acheteurs (faciliter la recherche de produits) la plus fluide possible, et dans l'optique d'un passage à l'échelle,  il devient nécessaire d'automatiser cette tâche d‘attribution de la catégorie.

Linda, Lead Data Scientist, vous demande donc d'étudier la faisabilité d'un moteur de classification des articles en différentes catégories, à partir du texte (en anglais) et de l’image.

## Missions :
### Mission n°1 : Etudiez la faisabilité d'un moteur de classification d'article
Ta mission sera de réaliser une étude de faisabilité d'un moteur de classification automatique d’articles, en utilisant leur image et leur description sur le jeu de données d'articles disponible dans la première pièce jointe de ce mail.

Pourrais-tu analyser les descriptions textuelles et les images des produits, au travers des étapes suivantes : 
- Un prétraitement des données texte et image 
- Une extraction de features 
- Une réduction en 2 dimensions, afin de projeter les produits sur un graphique 2D, sous la forme de points dont la couleur correspondra à la catégorie réelle 
- Une analyse du graphique afin de conclure, à l’aide des descriptions ou des images, sur la faisabilité de regrouper automatiquement des produits de même catégorie 
- Une réalisation d’une mesure pour confirmer ton analyse visuelle, en calculant la similarité entre les catégories réelles et les catégories issues d’une segmentation en clusters
 

Pourrais-tu nous démontrer ainsi la faisabilité de regrouper automatiquement des produits de même catégorie ?
  - Afin d’extraire les features image, il sera nécessaire de mettre en œuvre :
    * un algorithme de type SIFT / ORB / SURF ;
    * un algorithme de type CNN Transfer Learning.
 

Afin d’extraire les features texte, il sera nécessaire de mettre en œuvre : 
- deux approches de type bag-of-words, comptage simple de mots et Tf-idf ;
- une approche de type word/sentence embedding classique avec Word2Vec (ou Glove ou FastText) ;
- une approche de type word/sentence embedding avec BERT ;
- une approche de type word/sentence embedding avec USE (Universal Sentence Encoder).

### Mission n°2 : Réalisez une classification supervisée d'images
Merci beaucoup pour ton travail ! Voici la suite de ta mission : 
Pourrais-tu réaliser une classification supervisée à partir des images ? Je souhaiterais que tu mettes en place une data augmentation afin d’optimiser le modèle.
De plus, nous souhaitons élargir notre gamme de produits à l’épicerie fine. 
Pour cela, pourrais-tu tester la collecte de produits à base de “champagne” via l’API disponible ici ? 
Pourrais-tu ensuite nous proposer un script ou notebook Python permettant une extraction des 10 premiers produits dans un fichier “.csv”, contenant pour chaque produit les données suivantes : foodId, label, category, foodContentsLabel, image.
