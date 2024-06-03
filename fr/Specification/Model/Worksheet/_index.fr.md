---
title: Feuille de travail
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/worksheet/
description: "Aspose.Cells Spécification du modèle cloud : Feuille de travail. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
kwords: Excel, Office, feuille de calcul, Cloud REST API, feuille de calcul
weight: 50
---
## **feuille de travail**

 Encapsule l'objet qui représente une seule feuille de calcul.

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| Liens| Récipient| Vrai| FAUX|||
| AfficherDroiteÀGauche| Booléen| Vrai| FAUX|| Indique si la feuille de calcul spécifiée est affichée de droite à gauche plutôt que de gauche à droite. La valeur par défaut est fausse.|
| AfficherZéros| Booléen| Vrai| FAUX|| Vrai si des valeurs nulles sont affichées.|
| PremièreColonneVisible| Entier| Vrai| FAUX|| Représente le premier index de colonne visible.|
| PremièreLigneVisible| Entier| Vrai| FAUX|| Représente le premier index de ligne visible.|
| Nom| Chaîne| Vrai| FAUX|| Obtient ou définit le nom de la feuille de calcul.|
| Indice| Entier| Vrai| FAUX|| Obtient l'index de la feuille dans la collection de feuilles de calcul.|
| Est-ce que le quadrillage est visible| Booléen| Vrai| FAUX|| Obtient ou définit une valeur indiquant si le quadrillage est visible. La valeur par défaut est true.|
| EstContourAffiché| Booléen| Vrai| FAUX|| Indique s’il faut afficher le contour.|
| IsPageBreakPreview| Booléen| Vrai| FAUX|| Indique si la feuille de calcul spécifiée est affichée en mode normal ou en aperçu de saut de page.|
| Est visible| Booléen| Vrai| FAUX|| Représente si la feuille de calcul est visible.|
| EstProtégé| Booléen| Vrai| FAUX||Indique si la feuille de calcul est protégée.|
| IsRowColumnHeadersVisible| Booléen| Vrai| FAUX|| Obtient ou définit une valeur indiquant si la feuille de calcul affichera les en-têtes de ligne et de colonne. La valeur par défaut est vraie.|
| EstRègleVisible| Booléen| Vrai| FAUX|| Indique si la règle est visible. Cette propriété s’applique uniquement à l’aperçu des sauts de page.|
| Est sélectionné| Booléen| Vrai| FAUX|| Indique si cette feuille de calcul est sélectionnée à l'ouverture du classeur.|
| Couleur de l'onglet| Classe : Couleur| Vrai| FAUX|| Représente la couleur de l’onglet de la feuille de calcul.|
| TransitionEntrée| Booléen| Vrai| FAUX|| Indique si l'option Entrée de formule de transition (compatibilité Lotus) est activée.|
| TransitionÉvaluation| Booléen| Vrai| FAUX|| Indique si l'option Évaluation de la formule de transition (compatibilité Lotus) est activée.|
| Taper| Chaîne| Vrai| FAUX|| Représente le type de feuille de calcul.|
| Type de vue| Chaîne| Vrai| FAUX|| Obtient et définit le type de vue.|
| Type de visibilité| Chaîne| Vrai| FAUX|| Indique l'état visible de cette feuille.|
| Zoom| Entier| Vrai| FAUX|| Représente le facteur d’échelle en pourcentage. Il devrait être compris entre 10 et 400.|
|Cells | Classe : LinkElement| Vrai| FAUX|| Obtient la collection.|
| Graphiques| Classe : LinkElement| Vrai| FAUX|| Obtient une collection|
| Formes automatiques| Classe : LinkElement| Vrai| FAUX|||
| OleObjects| Classe : LinkElement| Vrai| FAUX||Représente une collection de dans une feuille de calcul.|
| commentaires| Classe : LinkElement| Vrai| FAUX|| Obtient la collection.|
| Des photos| Classe : LinkElement| Vrai| FAUX|| Obtient une collection.|
| Cellules fusionnées| Classe : LinkElement| Vrai| FAUX|||
| Validations| Classe : LinkElement| Vrai| FAUX|| Obtient la collection de paramètres de validation des données dans la feuille de calcul.|
| Formatages conditionnels| Classe : LinkElement| Vrai| FAUX|| Obtient les ConditionalFormattings dans la feuille de calcul.|
| Liens hypertextes| Classe : LinkElement| Vrai| FAUX|| Obtient la collection.|

