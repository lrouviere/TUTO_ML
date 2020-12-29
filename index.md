--- 
title: "Machine learning"
author: "Laurent Rouvière"
date: "2020-12-28"
site: bookdown::bookdown_site
#documentclass: book
bibliography: [book.bib, packages.bib]
biblio-style: apalike
link-citations: yes
#description: "This is a minimal example of using the bookdown package to write a book. The output format for this example is bookdown::gitbook."
---

\newcommand{\R}{\mathbb R}




















# Présentation {-#Presentation}



Ce tutoriel  présente une introduction au machine learning avec **R**. On pourra trouver :

* les supports de cours associés à ce tutoriel ainsi que les données utilisées à l'adresse suivante <https://lrouviere.github.io/machine_learning/> ;
* le tutoriel sans les correction à l'url <https://lrouviere.github.io/TUTO_ML/>
* le tutoriel avec les corrigés (à certains moment) à l'url <https://lrouviere.github.io/TUTO_ML/correction/>. 

Il est recommandé d'utiliser **mozilla firefox** pour lire le tutoriel.


Les thèmes suivants sont abordés :

- **Estimation du risque**, présentation du package **caret** ;
- **SVM**, cas séparable, non séparable et astuce du noyau ;
- **Arbres**, notamment l'algorithme CART ;
- **Agrégation d'arbres**, forêts aléatoires et gradient boosting ;
- **Réseaux de neurones et introduction au deep learning**, perceptron multicouches avec `keras`.


 Il existe de nombreuses références sur le machine learning, la plus connue étant certainement @hastibfri09, disponible en ligne à l'url <https://web.stanford.edu/~hastie/ElemStatLearn/>. On pourra également consulter @boegre19 qui propose une présentation très claire des algorithmes machine learning avec **R**. Cet ouvrage est également disponible en ligne à l'url <https://bradleyboehmke.github.io/HOML/>.




