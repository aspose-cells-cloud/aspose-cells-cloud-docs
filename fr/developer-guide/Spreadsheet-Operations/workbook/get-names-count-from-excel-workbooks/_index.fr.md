﻿---
title: Obtenir des noms à partir d'un classeur Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Nom
type: docs
url: /fr/get-names-from-an-excel-file/
aliases: [/get-names-count-from-excel-workbooks/,/workbook/names/,/workbook/get/names/]
keywords: Getting names on an Excel workbook
description: Aspose.Cells Cloud REST API prend en charge l'obtention de noms dans un classeur Excel. Le SDK prend en charge différents langages de développement, notamment Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 120
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Obtenir des noms à partir d'un classeur Excel
---
Ce REST API indique d'obtenir des noms à partir d'un classeur Excel.

## RSET API

```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/names
 
```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin| Le nom du classeur.|
| dossier| chaîne| requête| Le dossier du classeur.|
| nom de stockage| chaîne| requête| nom de stockage.|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbookNames) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/names" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
{
  "Status": "string",
  "Names": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Count": 0,
    "NameList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        }
      }
    ]
  }
}
 
```

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbookNames.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbookNames.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbookNames.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbookNames.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbookNames.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbookNames.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbookNames.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbookNames.go" >}}

{{< /tab >}}

{{< /tabs >}}
