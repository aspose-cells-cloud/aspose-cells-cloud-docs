---
title: Travailler avec CellsObjectOperate Tas
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Cells.Cloud API pour Excel opération : cellule objet opération tâche"
weight: 20
---
Ce REST API exploite l'objet de cellules `task`.

**OperateObject**

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
| OperateObjectType| chaîne| Classeur/Feuille de calcul/PageSetup/Cells/Chart/Shape/ListObject/PivotTable/WorkbookSettings/PageBreak|
| OperateObjectPosition| Objet||

**OperateObjectPosition**

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
| Cahier| Objet||
| NomFeuille| chaîne||
| Index du graphique| entier||
| Indice de forme| entier||
| NomCellule| chaîne||
| ListObjectIndex| entier||


**ChartOperateParameterChartOperateParameterChartOperateParameter**

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
| Index du graphique| entier||
| Type de graphique| chaîne||
| UpperLeftRow| entier||
|Colonne supérieure gauche| entier||
| ligne inférieure droite| entier||
| Colonne inférieure droite| entier||
| Zone| chaîne||
| EstVertical| chaîne| vrai faux|
| Données de catégorie| chaîne||
| IsAutoGetSerialName| chaîne| vrai faux|
| Zone| Titre||

**ListObjectOperateParameter** 

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
| ListObject| Objet||

**PageBreakOperateParameterPageBreakOperateParameter**

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
| Type de saut de page| chaîne||
| Indice| Indice||
| Rangée| entier||
| Colonne| entier||
| Index de départ| entier||
| EndIndex| entier||


**PageSetupOperateParameterPageSetupOperateParameter**

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
| Mise en page| Objet||


**PivotTableOperateParameterPivotTableOperateParameterPivotTableOperateParameter**

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


**WorkbookSettingsOperateParameterWorkbookSettingsOperateParameter**


|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
| Paramètres du classeur| Objet||

**Feuille de travailOperateParameter**


|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
| Nom| chaîne||
| Type de feuille| chaîne||
| Nouveau nom| chaîne||
| demande de déménagement| Objet||

## REPOS API

|**API**|**Taper**|**Description**|**Lien vers la ressource**|
|:- |:- |:- |:- |
|/cellules/tâche/runtask|POSTE|Exécuter la tâche|[Post-exécution de la tâche](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) définit une interface de programmation accessible au public et permet d'effectuer des interactions REST directement depuis un navigateur Web.

