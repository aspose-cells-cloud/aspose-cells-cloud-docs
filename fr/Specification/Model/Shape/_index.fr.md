---
title: Forme
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/shape/
description: "Aspose.Cells Spécification du modèle Cloud : Forme. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
kwords: Excel, Office, feuille de calcul, Cloud REST API, forme
weight: 50
---
## **forme**

 Représente l'objet msodrawing.

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| Nom| Chaîne| Vrai| FAUX|| Obtient et définit le nom de la forme.|
| MsoDrawingType| Chaîne| Vrai| FAUX|| Obtient le type de dessin mso.|
| Type de forme automatique| Chaîne| Vrai| FAUX|| Obtient et définit le type de forme automatique.|
| Placement| Chaîne| Vrai| FAUX|| Représente la manière dont l'objet de dessin est attaché aux cellules situées en dessous. La propriété contrôle le placement d'un objet sur une feuille de calcul.|
| Ligne supérieure gauche| Entier| Vrai| FAUX|| Représente l’index de la ligne du coin supérieur gauche.|
| Haut| Entier| Vrai| FAUX|| Représente le décalage vertical de la forme par rapport à sa rangée supérieure, en unités de pixels.|
| Colonne supérieure gauche| Entier| Vrai| FAUX|| Représente l’index de la colonne du coin supérieur gauche.|
| Gauche| Entier| Vrai| FAUX|| Représente le décalage horizontal de la forme par rapport à sa colonne de gauche, en unités de pixels.|
| Ligne inférieure droite| Entier| Vrai| FAUX|| Représente l’index de la ligne du coin inférieur droit.|
| Bas| Entier| Vrai| FAUX||Représente la largeur du décalage vertical de la forme par rapport à sa rangée du coin inférieur inférieur, en unités de pixels.|
| Colonne inférieure droite| Entier| Vrai| FAUX|| Représente l’index de la colonne du coin inférieur droit.|
| Droite| Entier| Vrai| FAUX|| Représente la largeur du décalage horizontal de la forme par rapport à sa colonne du coin inférieur droit, en unités de pixels.|
| Largeur| Entier| Vrai| FAUX|| Représente la largeur de la forme, en unités de pixels.|
| Hauteur| Entier| Vrai| FAUX|| Représente la hauteur de la forme, en unité de pixel.|
| X| Entier| Vrai| FAUX|| Obtient et définit le décalage horizontal de la forme par rapport à la bordure gauche de la feuille de calcul, en unités de pixels.|
| Oui| Entier| Vrai| FAUX|| Obtient et définit le décalage vertical de la forme par rapport à la bordure supérieure de la feuille de calcul, en unités de pixels.|
| Angle de rotation| Flottant| Vrai| FAUX|| Obtient et définit la rotation de la forme.|
|Texte HTML| Chaîne| Vrai| FAUX|| Obtient et définit la chaîne HTML qui contient des données et certains formats dans cette zone de texte.|
| Texte| Chaîne| Vrai| FAUX|| Représente la chaîne dans cet objet TextBox.|
| Texte alternatif| Chaîne| Vrai| FAUX|| Renvoie ou définit la chaîne de texte descriptive (alternative) de l'objet.|
| TexteHorizontalAlignement| Chaîne| Vrai| FAUX|| Obtient et définit le type d’alignement horizontal du texte de la forme.|
| TexteHorizontalOverflow| Chaîne| Vrai| FAUX|| Obtient et définit le type de débordement horizontal de texte de la forme qui contient du texte.|
| Type d'orientation du texte| Chaîne| Vrai| FAUX||Obtient et définit le type d'orientation du texte de la forme.|
| TexteVerticalAlignement| Chaîne| Vrai| FAUX|| Obtient et définit le type d’alignement vertical du texte de la forme.|
| TexteVerticalOverflow| Chaîne| Vrai| FAUX|| Obtient et définit le type de débordement vertical de texte de la forme qui contient du texte.|
| EstGroupe| Booléen| Vrai| FAUX|| Indique si la forme est un groupe.|
| Est caché| Booléen| Vrai| FAUX|| Indique si l'objet est visible.|
| IsLockAspectRatio| Booléen| Vrai| FAUX|| Vrai signifie que cela n'autorise pas les changements de rapport hauteur/largeur.|
| Est verrouillé| Booléen| Vrai| FAUX|| True si l'objet est verrouillé, False si l'objet peut être modifié lorsque la feuille est protégée.|
| EstImprimable| Booléen| Vrai| FAUX|| Vrai si l'objet est imprimable|
| EstTexteEnveloppé| Booléen| Vrai| FAUX|| Obtient et définit le type de texte renvoyé à la ligne de la forme qui contient le texte.|
| EstWordArt| Booléen| Vrai| FAUX|| Indique si cette forme est un word art.|
| Cellule liée| Chaîne| Vrai| FAUX|| Obtient ou définit la plage de feuille de calcul liée à la valeur du contrôle.|
| ZOrderPosition| Entier| Vrai| FAUX|| Renvoie la position d'une forme dans l'ordre z.|
| Police de caractère| Classe : Police| Vrai| FAUX|| Représente la police de la forme.|
| Lien hypertexte| Chaîne| Vrai| FAUX|| Obtient le lien hypertexte de la forme.|
| lien| Classe : Lien| Vrai| FAUX|||

**Nom du parent** : [LienÉlément](/specification/model/linkelement)

**Nom des enfants** : 
	-  [Forme d'arc](arcshape) 
	-  [Forme automatique](autoshape) 
	-  [Bouton](button) 
	-  [CellulesDessin](cellsdrawing) 
	-  [Case à cocher](checkbox) 
	-  [Boîte combo](combobox) 
	-  [Forme du commentaire](commentshape) 
	-  [Formulaire](form) 
	-  [Zone de groupe](groupbox) 
	-  [Forme de groupe](groupshape) 
	-  [Étiquette](label) 
	-  [Forme de ligne](lineshape) 
	-  [Zone de liste](listbox) 
	-  [OleObject](oleobject) 
	-  [ovale](oval) 
	-  [Image](picture) 
	-  [Bouton radio](radiobutton) 
	-  [FormeRectangle](rectangleshape) 
	-  [Barre de défilement](scrollbar) 
	-  [Fileur](spinner) 
	-  [Zone de texte](textbox) 
	-  [Forme du graphique](chartshape) 
