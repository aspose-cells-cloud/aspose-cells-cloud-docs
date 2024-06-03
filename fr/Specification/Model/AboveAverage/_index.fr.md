---
title: Au-dessus de la moyenne
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/aboveaverage/
description: "Aspose.Cells Spécification du modèle cloud : AboveAverage. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
kwords: Excel, Office, feuille de calcul, Cloud REST API, supérieur à la moyenne
weight: 50
---
## **au dessus de la moyenne**

 Décrivez la règle de mise en forme conditionnelle AboveAverage. Cette règle de mise en forme conditionnelle met en évidence les cellules supérieures ou inférieures à la moyenne pour toutes les valeurs de la plage.

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| Est au-dessus de la moyenne| Booléen| Vrai| FAUX|| Obtenez ou définissez l'indicateur indiquant si la règle est une règle « supérieure à la moyenne ». « vrai » indique « au-dessus de la moyenne ». La valeur par défaut est vraie.|
| EstÉgalMoyenne| Booléen| Vrai| FAUX||Obtenez ou définissez l'indicateur indiquant si les critères « aboveAverage » et « belowAverage » incluent la moyenne elle-même ou excluent cette valeur. « vrai » indique qu'il faut inclure la valeur moyenne dans les critères. La valeur par défaut est fausse.|
| Développement standard| Entier| Vrai| FAUX|| Obtenez ou définissez le nombre d’écarts types à inclure au-dessus ou en dessous de la moyenne dans la règle de mise en forme conditionnelle. La valeur d'entrée doit être comprise entre 0 et 3 (inclure 0 et 3). Définir cette valeur sur 0 signifie que stdDev n'est pas défini. La valeur par défaut est 0.|

