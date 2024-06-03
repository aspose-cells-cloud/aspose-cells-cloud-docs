---
title: BatchConvertReques
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/batchconvertrequest/
description: "Aspose.Cells Spécification du modèle cloud : BatchConvertRequest. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
kwords: Excel, Office, feuille de calcul, Cloud REST API, BatchConvertRequest
weight: 50
---
## **batchConvertRequest**

 Indique une demande de fichier de conversion par lots

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| Dossier d'origine| Chaîne| Vrai| FAUX|| Le répertoire stocke les fichiers qui doivent être convertis au format.|
| Stockage source| Chaîne| Vrai| FAUX|| Aspose Nom du stockage cloud.|
| Condition de correspondance| Classe : MatchConditionRequest| Vrai| FAUX|| Indique la condition de correspondance qui doit être traitée pour le nom de fichier.|
| Format| Chaîne| Vrai| FAUX|| Format de conversion.|
| Dossier sortant| Chaîne| Vrai| FAUX|| Le répertoire qui stocke les fichiers dont la conversion de format a réussi.|
| Stockage sortant| Chaîne| Vrai| FAUX|| Aspose Nom du stockage cloud.|
| Région| Chaîne| Vrai| FAUX|| Paramètres régionaux du classeur.|
| PageWideFitOnPerSheet| Booléen| Vrai| FAUX|||
| PageTallFitOnPerSheet| Booléen| Vrai| FAUX|||
| Options d'enregistrement| Classe : EnregistrerOptions| Vrai| FAUX|| Indique les options de sauvegarde.|

