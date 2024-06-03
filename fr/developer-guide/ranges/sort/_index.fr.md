---
title:  Tri par plage
second_title: Aspose.Cells Cloud Documen
linktitle: Sor
type: docs
keywords: Range Sort
url: /fr/ranges/sort/
description:  Définit la bordure du contour autour d’une plage de cellules.
weight: 20
kwords: Excel, Office Cloud, REST API, feuille de calcul, PDF, CSV, Json, Markdwon, tri par plage
---
 Ce REST API indique le tri par plage.

## RSET API


```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/ranges/sort

```

 Les paramètres de la requête sont :

| Le nom du paramètre| Taper| Chemin/Chaîne de requête/HTTPBody| Description|
|:- |:- |:- |:- |
|nom|Chaîne|Chemin|Le nom du classeur.|
|Nom de la feuille|Chaîne|Chemin|Le nom de la feuille de calcul.|
|gammeExploiter|Classe|Corps| Demande de tri par plage|
|dossier|Chaîne|Requête|Dossier de classeur d'origine.|
|Nom de stockage|Chaîne|Requête|Nom de stockage.|



 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/RangesController/PostWorksheetCellsRangeSort) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement depuis un navigateur Web.

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers le Cloud API avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}
```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/sort" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
```
{{< /tab >}}
{{< tab tabNum="2" >}}
```powershell

```
{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

Utiliser un SDK est le meilleur moyen d’accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le référentiel GitHub pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :

