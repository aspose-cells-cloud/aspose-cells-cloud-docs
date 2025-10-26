---
title: Diviser un classeur Excel en plusieurs fichiers
second_title: Documen
linktitle: Diviser un fil Excel
type: docs
url: /fr/split-multi-excel-files/
aliases: [ /split/multi-files/]
keywords: Split an Excel workbook to multi-files
description: Aspose.Cells Cloud REST API prend en charge le fractionnement d'un classeur Excel en plusieurs fichiers. Le SDK prend en charge différents langages de développement, notamment Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 130
kwords: Excel, Office Cloud, REST API, Feuille de calcul, PDF, CSV, Json, Markdown, Diviser un classeur Excel en plusieurs fichiers
---
Ce REST API indique de diviser un Excel `workbook` en plusieurs fichiers avec des formats différents.

**Paramètre de requête**

|Nom du paramètre|Taper|Description|
|:- |:- |:- |
|format|chaîne|Format divisé.|
|depuis|entier|Démarrer l'index de la feuille de calcul.|
|à|entier|Index de fin de feuille de travail.|
|résolution horizontale|entier|Résolution horizontale de l'image.|
|résolution verticale|entier|Résolution verticale de l'image.|
|dossier de sortie|chaîne|position du fichier divisé de sortie.|
|Règle splitName|chaîne||
|dossier|chaîne|Classeur original.|
|nom de stockage|chaîne|Nom de stockage.|

## RESTE API

|**API**|**Taper**|**Description**|**Lien Swagger**|
|:- |:- |:- |:- |
|/cellules/{nom}/split|POSTE|Diviser un classeur Excel|[PostWorkbookSplit](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookSplit)|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookSplit) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

 Vous pouvez utiliser**cURL** Outil en ligne de commande pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le cloud API avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/split?format=jpeg&from=1&to=1&horizontalResolution=0&verticalResolution=0" -H "accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Result": {

    "Documents": [

      {

        "Id": 1,

        "link": {

          "Href": "413e3375-c163-4d5c-8b84-8f95f63902f6.png",

          "Rel": null,

          "Title": null,

          "Type": null

        }

      }

    ]

  },

  "Code": 200,

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}
