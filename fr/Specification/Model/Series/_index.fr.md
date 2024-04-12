---
title: Série
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/series/
description: "Aspose.Cells Spécification du modèle Cloud : Série. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
weight: 50
---
## **série**

 

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| Zone| Classe : Zone| Vrai| FAUX|| Représente la zone d’arrière-plan de l’objet Series.|
| Bar3DShapeType| Chaîne| Vrai| FAUX|| Obtient ou définit le type de forme 3D utilisé avec le graphique à barres ou à colonnes 3D.|
| Frontière| Classe : Ligne| Vrai| FAUX|| Représente la bordure de l'objet Series.|
| Échelle à bulles| Entier| Vrai| FAUX||Obtient ou définit le facteur d'échelle pour les bulles dans le groupe de graphiques spécifié. Il peut s'agir d'une valeur entière comprise entre 0 (zéro) et 300, correspondant à un pourcentage de la taille par défaut. S'applique uniquement aux graphiques à bulles.|
| Tailles des bulles| Chaîne| Vrai| FAUX|| Obtient ou définit les valeurs de taille des bulles de la série de graphiques.|
| Nombre de valeurs de données| Entier| Vrai| FAUX|| Obtient le nombre de valeurs de données.|
| Étiquettes de données| Classe : LinkElement| Vrai| FAUX|| Représente l'objet DataLabels pour l'ASeries spécifié.|
| Afficher un nom| Chaîne| Vrai| FAUX|| Obtient le nom de la série qui s'affiche sur le graphique.|
| Taille du trou de beignet| Entier| Vrai| FAUX|| Renvoie ou définit la taille du trou dans un groupe de graphiques en anneau. La taille du trou est exprimée en pourcentage de la taille du graphique, entre 10 et 90 pour cent.|
| Barres inférieures| Classe : LinkElement| Vrai| FAUX|| Renvoie un objet qui représente les barres descendantes sur un graphique linéaire. S'applique uniquement aux graphiques en courbes.|
| Lignes de dépôt| Classe : Ligne| Vrai| FAUX||Renvoie un objet qui représente les lignes de dépôt d'une série sur le graphique en courbes ou en aires. S'applique uniquement aux graphiques en courbes ou en aires.|
| Explosion| Entier| Vrai| FAUX|| La distance entre une tranche de secteur ouverte et le centre du diagramme à secteurs est exprimée en pourcentage du diamètre du secteur.|
| Angle de première tranche| Entier| Vrai| FAUX|| Obtient ou définit l'angle de la première tranche de diagramme circulaire ou de diagramme en anneau, en degrés (dans le sens des aiguilles d'une montre à partir de la verticale). S'applique uniquement aux graphiques à secteurs, à secteurs 3D et en anneau, de 0 à 360.|
|Largeur d'écart| Entier| Vrai| FAUX|| Renvoie ou définit l'espace entre les clusters de barres ou de colonnes, en pourcentage de la largeur de la barre ou de la colonne. La valeur de cette propriété doit être comprise entre 0 et 500.|
| A3DEffet| Booléen| Vrai| FAUX|| Vrai si la série a une apparence tridimensionnelle. S'applique uniquement aux graphiques à bulles.|
| HasDropLines| Booléen| Vrai| FAUX|| Vrai si le graphique comporte des lignes de chute. S'applique uniquement aux graphiques en courbes ou en aires.|
| HasHiLoLignes| Booléen| Vrai| FAUX|| Vrai si le graphique linéaire comporte des lignes haut-bas. S'applique uniquement aux graphiques en courbes.|
| HasLeaderLines| Booléen| Vrai| FAUX|| Vrai si la série comporte des lignes de repère.|
| HasRadarAxisLabels| Booléen| Vrai| FAUX|| True si un graphique radar comporte des étiquettes d’axe de catégorie. S'applique uniquement aux cartes radar.|
| HasSeriesLines| Booléen| Vrai| FAUX||True si un graphique à colonnes empilées ou un graphique à barres comporte des lignes de série ou si un graphique à secteurs ou à barres de secteurs comporte des lignes de connexion entre les deux sections. S'applique uniquement aux graphiques à colonnes empilées, aux graphiques à barres, aux graphiques à secteurs ou aux graphiques à barres de secteurs.|
| HasUpDownBars| Booléen| Vrai| FAUX|| Vrai si un graphique linéaire comporte des barres montantes et descendantes. S'applique uniquement aux graphiques en courbes.|
| HiLoLignes| Classe : Ligne| Vrai| FAUX|| Renvoie un objet HiLoLines qui représente les lignes haut-bas d'une série sur un graphique linéaire. S'applique uniquement aux graphiques en courbes.|
| EstAutoSplit| Booléen| Vrai| FAUX|| Indique si la valeur seuil est automatique.|
| EstCouleurVariée| Booléen| Vrai| FAUX|| Représente si la couleur des points varie. Le graphique ne doit contenir qu'une seule série.|
| Lignes de leader| Classe : Ligne| Vrai| FAUX||Représente les lignes de repère sur un graphique. Les lignes de repère relient les étiquettes de données aux points de données. Cet objet n'est pas une collection ; aucun objet ne représente une seule ligne de repère.|
| LégendeEntrée| Classe : LinkElement| Vrai| FAUX|| Obtient l'entrée de légende selon cette série.|
| Doubler| Classe : Ligne| Vrai| FAUX|||
| Marqueur| Classe : Marqueur| Vrai| FAUX|| Obtient le marqueur.|
| Nom| Chaîne| Vrai| FAUX|| Obtient ou définit le nom de la série de données.|
| Chevaucher| Entier| Vrai| FAUX|| Spécifie le positionnement des barres et des colonnes. Peut être une valeur comprise entre – 100 et 100. S’applique uniquement aux graphiques à barres et à colonnes 2D.|
| PlotOnSecondAxis| Booléen| Vrai| FAUX|| Indique si cette série est tracée sur le deuxième axe des valeurs.|
| Points| Classe : LinkElement| Vrai| FAUX|| Obtient la collection de points d’une série dans un graphique.|
| Taille du deuxième tracé| Entier| Vrai| FAUX|| Renvoie ou définit la taille de la section secondaire d'un graphique à secteurs ou d'une barre de graphique à secteurs, en pourcentage de la taille du graphique à secteurs principal. Peut être une valeur comprise entre 5 et 200.|
| SérieLignes| Classe : Ligne| Vrai| FAUX||Renvoie un objet SeriesLines qui représente les lignes de série d'un graphique à barres empilées ou d'un graphique à colonnes empilées. S’applique uniquement aux graphiques à barres empilées et à colonnes empilées.|
| Ombre| Booléen| Vrai| FAUX|| Vrai si la série a une ombre.|
| Propriétés de forme| Classe : LinkElement| Vrai| FAUX|| Obtient l'objet qui contient les propriétés de forme visuelle de la série.|
| Afficher les bulles négatives| Booléen| Vrai| FAUX|| True si des bulles négatives sont affichées pour le groupe de graphiques. Valable uniquement pour les graphiques à bulles.|
| TailleReprésente| Chaîne| Vrai| FAUX|| Obtient ou définit ce que représente la taille des bulles sur un graphique à bulles.|
| Lisse| Booléen| Vrai| FAUX|| Représente le lissage des courbes. True si le lissage des courbes est activé pour le graphique en courbes ou le graphique en nuages de points. S'applique uniquement aux graphiques linéaires et à nuages de points reliés par des graphiques linéaires.|
| Type divisé| Chaîne| Vrai| FAUX|| Renvoie ou définit une valeur permettant de déterminer quels points de données se trouvent dans le deuxième secteur ou la deuxième barre d'un secteur ou d'une barre d'un graphique à secteurs.|
| Valeur divisée| Flottant| Vrai| FAUX||Renvoie ou définit une valeur qui doit être utilisée pour déterminer quels points de données se trouvent dans le deuxième secteur ou barre d'un secteur ou d'une barre de graphique à secteurs.|
| Lignes de tendance| Classe : LinkElement| Vrai| FAUX|| Renvoie un objet qui représente une collection de toutes les courbes de tendance de la série.|
| Taper| Chaîne| Vrai| FAUX|| Obtient ou définit le type d'une série de données.|
| Barres vers le haut| Classe : LinkElement| Vrai| FAUX|| Renvoie un objet DropBars qui représente les barres montantes sur un graphique linéaire. S'applique uniquement aux graphiques en courbes.|
| Valeurs| Chaîne| Vrai| FAUX|| Représente les données de la série de graphiques.|
| XErreurBarre| Classe : LinkElement| Vrai| FAUX|| Représente la barre d'erreur de direction X de la série.|
| Valeurs| Chaîne| Vrai| FAUX|| Représente les valeurs x de la série de graphiques.|
| YBarre d'Erreur| Classe : LinkElement| Vrai| FAUX|| Représente la barre d'erreur de direction Y de la série.|
| lien| Classe : Lien| Vrai| FAUX|||

**Nom du parent** : (LinkElement)[linkelement]