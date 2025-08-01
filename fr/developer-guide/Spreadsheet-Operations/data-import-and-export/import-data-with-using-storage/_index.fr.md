﻿---
title: Importer des données à l'aide de storag
second_title: Aspose.Cells Cloud Documen
linktitle: Importer des données avec stockage
type: docs
url: /fr/import-data-with-using-storage/
aliases: [/import-data-into-excel-worksheet/, /import-data-into-worksheet/ , /import-data-in-excel-worksheet/, /import-data/,/import/with-using-storage/]
description: "Cells.Cloud API pour Excel fonctionne : Importer des données dans la feuille de calcul Excel"
weight: 10
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Importer des données avec le stockage
---
Ce REST API indique `import data` dans le fichier Excel.

## RSET API

```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/importdata
 
```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin||
| dossier| chaîne| requête||
| nom de stockage| chaîne| requête| nom de stockage.|
| importer des données|| corps||

**Les paramètres des options d'importation des données** sont décrits dans[le lien de référence](/cells/fr/import/#import-data-option-parameter).

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata" \
-X POST \
-D "{\"Data\":[1,2,4],\"DestinationWorksheet\":\"Sheet1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"importDataType\":\"IntArray\"}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
 
```

{{< /tab >}}

{{< /tabs >}}

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :
