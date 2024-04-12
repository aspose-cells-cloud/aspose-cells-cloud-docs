---
title: Carboniser
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/chart/
description: "Aspose.Cells Spécification du modèle Cloud : Graphique. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
weight: 50
---
## **graphique**

 

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| Mise à l'échelle automatique| Booléen| Vrai| FAUX|| Vrai si Microsoft Excel met à l'échelle un graphique 3D afin qu'il soit plus proche en taille du graphique 2D équivalent. La propriété RightAngleAxes doit être True.|
| Mur arrière| Classe : LinkElement| Vrai| FAUX||Renvoie un objet qui représente le mur arrière d'un graphique 3D.|
| CatégorieAxe| Classe : LinkElement| Vrai| FAUX|| Obtient l'axe X du graphique.|
| ZoneGraphique| Classe : LinkElement| Vrai| FAUX|| Obtient la zone graphique dans la feuille de calcul.|
| GraphiqueDonnéesTable| Classe : LinkElement| Vrai| FAUX|| Représente le tableau de données du graphique.|
| ObjetGraphique| Classe : LinkElement| Vrai| FAUX|| Représente le chartShape ;|
| ProfondeurPourcentage| Entier| Vrai| FAUX|| Représente la profondeur d'un graphique 3D en pourcentage de la largeur du graphique (entre 20 et 2 000 pour cent).|
| Élévation| Entier| Vrai| FAUX|| Représente l'élévation de la vue cartographique 3D, en degrés.|
| Angle de première tranche| Entier| Vrai| FAUX|| Obtient ou définit l'angle de la première tranche de diagramme circulaire ou de diagramme en anneau, en degrés (dans le sens des aiguilles d'une montre à partir de la verticale). S'applique uniquement aux graphiques à secteurs, à secteurs 3D et en anneau, de 0 à 360.|
| Sol| Classe : LinkElement| Vrai| FAUX|| Renvoie un objet qui représente les murs d'un graphique 3D.|
| Profondeur de l'écart| Entier| Vrai| FAUX|| Obtient ou définit la distance entre les séries de données dans un graphique 3D, en pourcentage de la largeur du marqueur. La valeur de cette propriété doit être comprise entre 0 et 500.|
|Largeur d'écart| Entier| Vrai| FAUX|| Renvoie ou définit l'espace entre les clusters de barres ou de colonnes, en pourcentage de la largeur de la barre ou de la colonne. La valeur de cette propriété doit être comprise entre 0 et 500.|
| Pourcentage de hauteur| Entier| Vrai| FAUX|| Renvoie ou définit la hauteur d'un graphique 3D sous forme de pourcentage de la largeur du graphique (entre 5 et 500 pour cent).|
| Masquer les boutons de champ de pivot| Booléen| Vrai| FAUX|| Indique si les boutons de champ du graphique croisé dynamique sont masqués uniquement lorsque le graphique est de type PivotChart.|
| Est3D| Booléen| Vrai| FAUX|| Indique si le graphique est un graphique 3D.|
| EstRectangulaireEn Coin| Booléen| Vrai| FAUX|| Obtient ou définit une valeur indiquant si la zone du graphique est rectangulaire. La valeur par défaut est vraie.|
| Légende| Classe : LinkElement| Vrai| FAUX|| Obtient la légende du graphique.|
| Nom| Chaîne| Vrai| FAUX|||
| Série NS| Classe : LinkElement| Vrai| FAUX|| Obtient une collection représentant la série de données dans le graphique.|
| Mise en page| Classe : LinkElement| Vrai| FAUX|| Représente la description de la mise en page dans ce graphique.|
| Perspective| Entier| Vrai| FAUX||Renvoie ou définit la perspective de la vue graphique 3D. Doit être compris entre 0 et 100. Cette propriété est ignorée si la propriété RightAngleAxes est True.|
| PivotSource| Chaîne| Vrai| FAUX|| La source est les données du tableau croisé dynamique. Si PivotSource n'est pas vide, le graphique est PivotChart.|
| Placement| Chaîne| Vrai| FAUX|| Représente la manière dont le graphique est attaché aux cellules situées en dessous.|
| Zone de tracé| Classe : LinkElement| Vrai| FAUX|| Obtient la zone de tracé du graphique qui inclut les étiquettes de graduation des axes.|
| PlotEmptyCellsType| Chaîne| Vrai| FAUX|| Obtient et définit comment tracer les cellules vides.|
| TracerCellulesVisibles| Booléen| Vrai| FAUX|| Indique si seules les cellules visibles sont tracées.|
| Taille d'impression| Chaîne| Vrai| FAUX|| Obtient et définit la taille du graphique imprimé.|
| Axes à angle droit| Booléen| Vrai| FAUX|| Vrai si les axes du graphique sont à angles droits. S'applique uniquement aux graphiques 3D (à l'exception des diagrammes Column3D et des diagrammes circulaires 3D).|
| Angle de rotation| Entier| Vrai| FAUX|| Représente la rotation de la vue graphique 3D (la rotation de la zone de tracé autour de l'axe z, en degrés).|
| DeuxièmeCatégorieAxe| Classe : LinkElement| Vrai| FAUX|| Obtient le deuxième axe X du graphique.|
|DeuxièmeAxeValeur| Classe : LinkElement| Vrai| FAUX|| Obtient le deuxième axe Y du graphique.|
| SérieAxe| Classe : LinkElement| Vrai| FAUX|| Obtient l’axe des séries du graphique.|
| Formes| Classe : LinkElement| Vrai| FAUX|| Renvoie toutes les formes de dessin dans ce graphique.|
| AfficherDataTable| Booléen| Vrai| FAUX|| Obtient ou définit une valeur indiquant si le graphique affiche un tableau de données.|
| AfficherLégende| Booléen| Vrai| FAUX|| Obtient ou définit une valeur indiquant si la légende du graphique sera affichée. La valeur par défaut est vraie.|
| Paroi latérale| Classe : LinkElement| Vrai| FAUX|| Renvoie un objet qui représente la paroi latérale d'un graphique 3D.|
| TailleAvecFenêtre| Booléen| Vrai| FAUX|| True si Microsoft Excel redimensionne le graphique pour qu'il corresponde à la taille de la fenêtre de la feuille graphique.|
| Style| Entier| Vrai| FAUX|| Obtient et définit le style intégré.|
| Titre| Classe : LinkElement| Vrai| FAUX|||
| Taper| Chaîne| Vrai| FAUX|||
| AxeValeur| Classe : LinkElement| Vrai| FAUX|| Obtient l'axe Y du graphique.|
| Des murs| Classe : LinkElement| Vrai| FAUX|| Renvoie un objet qui représente les murs d'un graphique 3D.|
| MursEtGridlines2D| Booléen| Vrai| FAUX|| True si le quadrillage est dessiné en deux dimensions sur un graphique 3D.|
| lien| Classe : Lien| Vrai| FAUX|||

**Nom du parent** : (LinkElement)[linkelement]