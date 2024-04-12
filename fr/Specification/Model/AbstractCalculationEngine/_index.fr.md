---
title: RésuméCalculMoteur
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/abstractcalculationengine/
description: "Aspose.Cells Spécification du modèle cloud : AbstractCalculationEngine. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
weight: 50
---
## **résuméCalculationMoteur**

 Représente le moteur de calcul personnalisé de l'utilisateur pour étendre le moteur de calcul par défaut de Aspose.Cells.

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| IsParamLiteralRequired| Booléen| Vrai| FAUX|| Indique si ce moteur a besoin du texte littéral du paramètre lors du calcul. La valeur par défaut est fausse.|
| IsParamArrayModeRequired| Booléen| Vrai| FAUX|| Indique si ce moteur a besoin que le paramètre soit calculé en mode tableau. La valeur par défaut est fausse. Si cela est requis lors du calcul des fonctions personnalisées, cette propriété doit être définie sur true.|
| ProcessBuiltInFunctions| Booléen| Vrai| FAUX||Indique si les fonctions intégrées prises en charge par le moteur intégré doivent être vérifiées et traitées par cette implémentation. La valeur par défaut est fausse. Si l'utilisateur doit modifier la logique de calcul de certaines fonctions intégrées, cette propriété doit être définie sur true. Sinon, veuillez laisser cette propriété comme fausse pour des raisons de performances.|

