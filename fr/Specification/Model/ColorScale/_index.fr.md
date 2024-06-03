---
title: Échelle de couleurs
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/colorscale/
description: "Aspose.Cells Spécification du modèle Cloud : ColorScale. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
kwords: Excel, Office, feuille de calcul, Cloud REST API, ColorScale
weight: 50
---
## **Échelle de couleurs**

 Décrivez la règle de mise en forme conditionnelle ColorScale. Cette règle de mise en forme conditionnelle crée une échelle de couleurs graduée sur les cellules.

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| MaxCfvo| Classe : ConditionalFormattingValue| Vrai| FAUX|| Obtenez ou définissez l'objet de valeur maximale de ce ColorScale. Impossible de définir null ou CFValueObject avec le type FormatConditionValueType.Min.|
| Couleur Max| Classe : Couleur| Vrai| FAUX|| Obtenez ou définissez la couleur du dégradé pour la valeur maximale de la plage.|
| MilieuCfvo| Classe : ConditionalFormattingValue| Vrai| FAUX|| Obtenez ou définissez l'objet de valeur moyenne de ce ColorScale. Impossible de définir CFValueObject avec le type FormatConditionValueType.Max ou FormatConditionValueType.Min.|
| Couleur moyenne| Classe : Couleur| Vrai| FAUX|| Obtenez ou définissez la couleur du dégradé pour la valeur centrale de la plage.|
| MinCfvo| Classe : ConditionalFormattingValue| Vrai| FAUX|| Obtenez ou définissez l'objet de valeur minimale de ce ColorScale. Impossible de définir null ou CFValueObject avec le type FormatConditionValueType.Max.|
| CouleurMin| Classe : Couleur| Vrai| FAUX||Obtenez ou définissez la couleur du dégradé pour la valeur minimale de la plage.|

