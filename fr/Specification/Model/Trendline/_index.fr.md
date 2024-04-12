---
title: Tendancelin
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/trendline/
description: "Aspose.Cells Spécification du modèle cloud : Trendline. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
weight: 50
---
## **ligne de tendance**

 

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| lien| Classe : Lien| Vrai| FAUX|||
| En arrière| Flottant| Vrai| FAUX|| Renvoie ou définit le nombre de périodes (ou d'unités sur un nuage de points) que la ligne de tendance s'étend vers l'arrière. Le nombre de périodes doit être supérieur ou égal à zéro. Si le type de graphique est en colonnes, le nombre de périodes doit être compris entre 0 et 0,5|
| Étiquettes de données| Classe : LinkElement| Vrai| FAUX|| Représente l'objet DataLabels pour la série spécifiée.|
| AfficherÉquation| Booléen| Vrai| FAUX|| Représente si l'équation de la ligne de tendance est affichée sur le graphique (dans la même étiquette de données que la valeur R au carré). La définition de cette propriété sur True active automatiquement les étiquettes de données.|
| AfficherRSquared| Booléen| Vrai| FAUX||Représente si la valeur R au carré de la courbe de tendance est affichée sur le graphique (dans la même étiquette de données que l'équation). La définition de cette propriété sur True active automatiquement les étiquettes de données.|
| Avant| Flottant| Vrai| FAUX|| Renvoie ou définit le nombre de périodes (ou d'unités sur un nuage de points) que la ligne de tendance s'étend vers l'avant. Le nombre de périodes doit être supérieur ou égal à zéro.|
| Intercepter| Flottant| Vrai| FAUX|| Renvoie ou définit le point où la ligne de tendance croise l'axe des valeurs.|
| EstNomAuto| Booléen| Vrai| FAUX|| Renvoie si Microsoft Excel détermine automatiquement le nom de la courbe de tendance.|
| LégendeEntrée| Classe : LinkElement| Vrai| FAUX|| Obtient l'entrée de légende selon cette ligne de tendance|
| Nom| Chaîne| Vrai| FAUX|| Renvoie le nom de la ligne de tendance.|
| Commande| Entier| Vrai| FAUX|| Renvoie ou définit l'ordre de la courbe de tendance (un entier supérieur à 1) lorsque le type de courbe de tendance est Polynomial. La commande doit être comprise entre 2 et 6.|
| Période| Entier| Vrai| FAUX|| Renvoie ou définit la période de la ligne de tendance de la moyenne mobile.|
| Taper| Chaîne| Vrai| FAUX|| Renvoie le type de ligne de tendance.|
| Longueur de la flèche de début| Chaîne| Vrai| FAUX|||
| DébutFlècheLargeur| Chaîne| Vrai| FAUX|||
| Type de début| Chaîne| Vrai| FAUX|||
| Type de casquette| Chaîne| Vrai| FAUX|||
| Couleur| Classe : Couleur| Vrai| FAUX|||
| Type de composé| Chaîne| Vrai| FAUX|||
| Type de tiret| Chaîne| Vrai| FAUX|||
| FinFlècheLongueur| Chaîne| Vrai| FAUX|||
| FinFlècheLargeur| Chaîne| Vrai| FAUX|||
| Type de fin| Chaîne| Vrai| FAUX|||
| Remplissage en dégradé| Classe : GradientFill| Vrai| FAUX|||
| EstAuto| Booléen| Vrai| FAUX|||
| EstAutomatiqueCouleur| Booléen| Vrai| FAUX|||
| Est visible| Booléen| Vrai| FAUX|||
| Type de jointure| Chaîne| Vrai| FAUX|||
| Style| Chaîne| Vrai| FAUX|||
| Transparence| Flottant| Vrai| FAUX|||
| Poids| Chaîne| Vrai| FAUX|||
| PoidsPt| Flottant| Vrai| FAUX|||

**Nom du parent** : (Ligne)[ligne]