---
title: DataBa
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/databar/
description: "Aspose.Cells Spécification du modèle cloud : DataBar. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
kwords: Excel, Office, feuille de calcul, Cloud REST API, barre de données
weight: 50
---
## **barre de données**

 Décrivez la règle de mise en forme conditionnelle DataBar. Cette règle de mise en forme conditionnelle affiche une barre de données graduée dans la plage de cellules.

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| Couleur de l'Axe| Classe : Couleur| Vrai| FAUX|| Obtient la couleur de l'axe des cellules avec une mise en forme conditionnelle sous forme de barres de données.|
| Position de l'axe| Chaîne| Vrai| FAUX|| Obtient ou définit la position de l'axe des barres de données spécifiées par une règle de mise en forme conditionnelle.|
| BarBordure| Classe : DataBarBorder| Vrai| FAUX|| Obtient un objet qui spécifie la bordure d'une barre de données.|
| Type de remplissage de barre| Chaîne| Vrai| FAUX|| Obtient ou définit la façon dont une barre de données est remplie de couleur.|
| Couleur| Classe : Couleur| Vrai| FAUX|| Obtenez ou définissez la couleur de cette DataBar.|
| Direction| Chaîne| Vrai| FAUX||Obtient ou définit la direction dans laquelle la barre de données est affichée.|
| MaxCfvo| Classe : ConditionalFormattingValue| Vrai| FAUX|| Obtenez ou définissez l'objet de valeur maximale de ce DataBar. Impossible de définir null ou CFValueObject avec le type FormatConditionValueType.Min.|
| Longueur maximale| Entier| Vrai| FAUX|| Représente la longueur maximale de la barre de données.|
| MinCfvo| Classe : ConditionalFormattingValue| Vrai| FAUX|| Obtenez ou définissez l'objet de valeur minimale de ce DataBar. Impossible de définir null ou CFValueObject avec le type FormatConditionValueType.Max.|
| Longueur minimale| Entier| Vrai| FAUX|| Représente la longueur minimale de la barre de données.|
| Format de barre négative| Classe : NegativeBarFormat| Vrai| FAUX|| Obtient l'objet NegativeBarFormat associé à une règle de mise en forme conditionnelle de barre de données.|
| Afficher la valeur| Booléen| Vrai| FAUX|| Obtenez ou définissez l'indicateur indiquant s'il faut afficher les valeurs des cellules sur lesquelles cette barre de données est appliquée. La valeur par défaut est vraie.|

