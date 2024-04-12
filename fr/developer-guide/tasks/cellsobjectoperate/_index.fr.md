---
title: Travailler avec CellsObjectOperate Tas
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Cells.Cloud API pour Excel fonctionner : tâche d'exploitation de l'objet cellules"
weight: 20
---
Ce REST API exploite l'objet cellules `task`.

**ExploiterObjet**

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
| OperateObjectType| chaîne| Classeur/Feuille de calcul/PageSetup/Cells/Chart/Shape/ListObject/PivotTable/WorkbookSettings/PageBreak|
| OperateObjectPosition| Objet||

**OperateObjectPosition**

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
| Cahier d'exercices| Objet||
| Nom de la feuille| chaîne||
| GraphiqueIndex| entier||
| Indice de forme| entier||
| Nom de cellule| chaîne||
| ListeObjetIndex| entier||


**ChartOperateParamètre**

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
| GraphiqueIndex| entier||
| Type de graphique| chaîne||
| Ligne supérieure gauche| entier||
| Colonne supérieure gauche| entier||
| Ligne inférieure droite| entier||
| Colonne inférieure droite| entier||
| Zone| chaîne||
| EstVertical| chaîne| vrai faux|
| CatégorieDonnées| chaîne||
| IsAutoGetSerialName| chaîne| vrai faux|
| Zone| Titre||

**ListObjectOperateParameter** 

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
| ObjetListe| Objet||

**PageBreakOperateParameter**

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
| Type de saut de page| chaîne||
| Indice| Indice||
| Rangée| entier||
| Colonne| entier||
| IndexDébut| entier||
| FinIndex| entier||


**PageSetupOperateParameter**

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
| Mise en page| Objet||


**PivotTableOperateParameter**

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
| NomCelluleDest| chaîne||
| Données source| chaîne||
| Nom de la table| chaîne||
| UtiliserMêmeSource| chaîne| vrai faux|
| Index de tableau croisé dynamique| entier||
| PivotFieldRows|entier[]||
| PivotFieldColumns|entier[]||
|PivotFieldData|entier[]||


**ShapeOperateParameter**


|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
| Forme| Objet||


**WorkbookSettingsOperateParameter**


|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
| Paramètres du classeur| Objet||

**Feuille de calculOperateParameter**


|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
| Nom| chaîne||
| Type de feuille| chaîne||
| Nouveau nom| chaîne||
| Demande de déplacement| Objet||

## REPOS API

|**API**|**Taper**|**Description**|**Lien vers la ressource**|
|:- |:- |:- |:- |
|/cellules/tâche/tâche d'exécution|POSTE|Exécuter la tâche|[PostExécutionTâche](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement depuis un navigateur Web.

