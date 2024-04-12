---
title: CreatePivotTableReques
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/createpivottablerequest/
description: "Aspose.Cells Spécification du modèle cloud : CreatePivotTableRequest. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
weight: 50
---
## **createPivotTableRequest**

 Indique une demande de création de tableau croisé dynamique

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| Nom| Chaîne| Vrai| FAUX|| Nom du tableau croisé dynamique|
| Données source| Chaîne| Vrai| FAUX|| Les données du nouveau cache de tableau croisé dynamique.|
| NomCelluleDest| Chaîne| Vrai| FAUX|| Cellule située dans le coin supérieur gauche de la plage de destination du rapport de tableau croisé dynamique.|
| UtiliserMêmeSource| Booléen| Vrai| FAUX|| Indique si vous utilisez la même source de données lorsqu'un autre tableau croisé dynamique existant a utilisé cette source de données. Si la propriété est vraie, cela économisera de la mémoire.|
| PivotFieldRows|Tableau<Integer> | Vrai| FAUX|| Représente les champs de ligne dans un rapport de tableau croisé dynamique.|
| PivotFieldColumns|Tableau<Integer> | Vrai| FAUX||Représente les champs de colonnes dans un rapport de tableau croisé dynamique.|
|PivotFieldData|Tableau<Integer> | Vrai| FAUX|| Représente les champs de données dans un rapport de tableau croisé dynamique.|

