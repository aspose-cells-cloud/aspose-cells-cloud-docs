---
title: Option de calcul
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/calculationoptions/
description: "Aspose.Cells Spécification du modèle cloud : CalculationOptions. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
kwords: Excel, Office, feuille de calcul, Cloud REST API, options de calcul
weight: 50
---
## **Options de calcul**

 Représente les options de calcul.

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| TailleCalcStack| Entier| Vrai| FAUX|| Spécifie la taille de la pile pour calculer les cellules de manière récursive.|
| IgnorerErreur| Booléen| Vrai| FAUX|| Indique si les erreurs rencontrées lors du calcul des formules doivent être ignorées. L'erreur peut être due à une fonction non prise en charge, à des liens externes, etc. La valeur par défaut est vraie.|
| Stratégie de précision| Chaîne| Vrai| FAUX|| Spécifie la stratégie de traitement de la précision du calcul.|
| Récursif| Booléen| Vrai| FAUX|| Indique si le calcul des cellules dépendantes est effectué de manière récursive lors du calcul d'une cellule et si cela dépend des autres cellules. La valeur par défaut est vraie.|
| Moteur personnalisé|Classe : AbstractCalculationEngine| Vrai| FAUX|| Le moteur de calcul de formule personnalisé pour étendre le moteur de calcul par défaut de Aspose.Cells.|
| CalculMoniteur| Classe : AbstraitCalculationMonitor| Vrai| FAUX|| Le moniteur permettant à l'utilisateur de suivre la progression du calcul de la formule.|
| Sources de données liées|Tableau<Class:Workbook> | Vrai| FAUX|| Spécifie les sources de données pour les liens externes utilisés dans les formules.|

