# Estimation du risque avec caret {#caret}

## Notion de risque en apprentissage supervisé

L'apprentissage supervisée consiste à expliquer ou prédire une sortie $y\in\mathcal Y$ par des entrées $x\in\mathcal X$ (le plus souvent $\mathcal X=\mathbb R^p$). Cela revient à trouver un **algorithme** ou **machine** représenté par une fonction
$$f:\mathcal X\to\mathcal Y$$
qui à une nouvelle observation $x$ associe la prévision $f(x)$. Bien entendu pour un problème donné, on va chercher le **meilleur algorithme**. Cette notion nécessite la définition de **critères** que l'on va chercher à optimiser. Les critère sont le plus souvent définie à partir du fonction de perte 
\begin{align*}
\ell:\mathcal Y \times\mathcal Y & \mapsto \mathbb R^+ \\
(y,y^\prime) & \to\ell(y,y^\prime)
\end{align*}
où $\ell(y,y^\prime)$ représentera l'erreur (ou la perte) pour la prévision $y^\prime$ par rapport à l'observation $y$. Si on représente le phénomène d'intérêt par un couple aléatoire $(X,Y)$ à valeurs dans $\mathcal X\times\mathcal Y$, on mesurera la performance d'un algorithme $f$ par son risque
$$\mathcal R(f)=\mathbf E[\ell(Y,f(X))].$$
Trouver le meilleur algorithme revient alors à trouver $f$ qui minimise $\mathcal R(f)$. Bien entendu, ce cadre possède une utilité limitée en pratique puisqu'on ne connaît jamais la loi de $(X,Y)$, on ne pourra donc jamais calculé le *vrai risque* d'un algorithme $f$. Tout le problème va donc être de trouver l'algorithme qui a le plus petit risque à partir de $n$ observations $(x_1,y_1),\dots,(x_n,y_n)$. 

Nous verrons dans les chapitres suivants plusieurs façons de construire des algorithmes mais dans tous les cas, un algorithme est représenté par une fonction 
$$f_n:\mathcal X\times(\mathcal X\times\mathcal Y)^n\to\mathcal Y$$
qui pour une nouvelle donnée $x$ renverra la prévision $f_n(x)$ calculée à partir de l'échantillon qui vit dans $(\mathcal X\times\mathcal Y)^n$. Dès lors la question qui se pose est de calculer (ou plutôt d'estimer) le risque (inconnu) $\mathcal R(f_n)$ d'un algorithme $f_n$. Les techniques classiques reposent sur des algorithmes de type validation croisée. Nous les mettons en œuvre dans cette partie pour un algorithme simple : les **$k$ plus proches voisins**. On commencera par faire les algorithmes "à la main" puis nous utiliserons le package **caret** qui permet de calculer des risques pour quasiment tous les algorithmes que l'on retrouver en apprentissage supervisé. 


## La validation croisée

On cherche à expliquer une variable binaire $Y$ par deux variables quantitatives $X_1$ et $X_2$ à l'aide du jeu de données suivant

























































