---
title: ConditionalFormattingValu
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/conditionalformattingvalue/
description: "Aspose.Cells Spécification du modèle cloud : ConditionalFormattingValue. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
kwords: Excel, Office, feuille de calcul, Cloud REST API, ConditionalFormattingValue
weight: 50
---
## **valeur de formatage conditionnelle**

 Décrit les valeurs des points d'interpolation dans une échelle de dégradé, dataBar ou iconSet.

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| EstGTE| Booléen| Vrai| FAUX||Obtenez ou définissez l’indicateur Supérieur ou égal. À utiliser uniquement pour les jeux d'icônes, détermine si cette valeur de seuil utilise l'opérateur supérieur ou égal à. « faux » indique que « supérieur à » est utilisé à la place de « supérieur ou égal à ». La valeur par défaut est vraie.|
| Taper| Chaîne| Vrai| FAUX|| Obtenez ou définissez le type de cet objet de valeur de mise en forme conditionnelle. Définir le type sur FormatConditionValueType.Min ou FormatConditionValueType.Max définira automatiquement « Value » sur null.|
| Valeur| Classe : Objet| Vrai| FAUX|| Obtenez ou définissez la valeur de cet objet de valeur de mise en forme conditionnelle. Il doit être utilisé conjointement avec Type.|

