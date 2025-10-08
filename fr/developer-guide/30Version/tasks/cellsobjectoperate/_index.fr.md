---
title: Travailler avec CellsObjectOperate Tas
second_title: Documen
type: docs
url: /fr/tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Cells.Cloud API pour Excel opération : tâche d'opération d'objet de cellules"
weight: 20
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Utilisation des cellulesObjectOperate Task
---
Cet objet REST API exploite les cellules `task`.

**Exploiter l'objet**

|Nom du paramètre|Taper|Description|
|:- |:- |:- |
| Type d'objet opérationnel| chaîne|Classeur/Feuille de calcul/Mise en page/Cells/Graphique/Forme/Objet de liste/Tableau croisé dynamique/Paramètres du classeur/Saut de page|
| Fonctionnement de la position de l'objet| Objet||

**Fonctionnement de la position de l'objet**

|Nom du paramètre|Taper|Description|
|:- |:- |:- |
| Cahier d'exercices| Objet||
| Nom de la feuille| chaîne||
| Index des graphiques| entier||
| Index de forme| entier||
| Nom de la cellule| chaîne||
| Index des objets de liste| entier||


**ChartOperateParameter**

|Nom du paramètre|Taper|Description|
|:- |:- |:- |
| Index des graphiques| entier||
| Type de graphique| chaîne||
| Rangée supérieure gauche| entier||
| Colonne supérieure gauche| entier||
| Ligne inférieure droite| entier||
| Colonne inférieure droite| entier||
| Zone| chaîne||
| EstVertical| chaîne| vrai/faux|
| CatégorieDonnées| chaîne||
| EstAutoGetSerialName| chaîne| vrai/faux|
| Zone| Titre||

**ListObjectOperateParameter** 

|Nom du paramètre|Taper|Description|
|:- |:- |:- |
| ListObject| Objet||

**Paramètre d'opération de saut de page**

|Nom du paramètre|Taper|Description|
|:- |:- |:- |
| Type de saut de page| chaîne||
| Indice| Indice||
| Rangée| entier||
| Colonne| entier||
| Index de départ| entier||
| FinIndex| entier||


**Paramètre d'opération de configuration de page**

|Nom du paramètre|Taper|Description|
|:- |:- |:- |
| Mise en page| Objet||


**PivotTableOperateParameter**

|Nom du paramètre|Taper|Description|
|:- |:- |:- |
| Nom de la cellule de destination| chaîne||
| Données sources| chaîne||
| Nom de la table| chaîne||
| Utiliser la même source| chaîne| vrai/faux|
| Index du tableau croisé dynamique| entier||
| Lignes de champ croisé dynamique|entier[]||
| Colonnes de champ croisé dynamique|entier[]||
| Données du champ croisé dynamique|entier[]||


**ShapeOperateParameter**


|Nom du paramètre|Taper|Description|
|:- |:- |:- |
| Forme| Objet||


**Paramètres du classeurOperateParameter**


|Nom du paramètre|Taper|Description|
|:- |:- |:- |
| Paramètres du classeur| Objet||

**Feuille de calculOperateParameter**


|Nom du paramètre|Taper|Description|
|:- |:- |:- |
| Nom| chaîne||
| Type de feuille| chaîne||
| Nouveau nom| chaîne||
| Demande de déménagement| Objet||

## RESTE API

|**API**|**Taper**|**Description**|**Lien vers la ressource**|
|:- |:- |:- |:- |
|/cellules/tâche/exécuter une tâche|POSTE|Exécuter la tâche|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

