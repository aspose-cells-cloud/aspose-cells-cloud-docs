﻿---
title: Fractionner un classeur Excel en plusieurs fichiers
second_title: Aspose.Cells Cloud Documen
linktitle: cahier de travail
type: docs
url: /fr/workbook/split/
aliases: [/split-excel-workbooks/]
keywords: Split an Excel workbook to multi-files
description: Aspose.Cells Cloud REST API prend en charge la division d'un classeur Excel en plusieurs fichiers. Le SDK prend en charge les types de langages de développement. Ils incluent Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift
weight: 130
---
Ce REST API indique de diviser un Excel `workbook` en plusieurs fichiers avec un format différent.

**Paramètre de requête**

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
|format|chaîne|Format fractionné.|
|depuis|entier|Démarrer l'index de la feuille de calcul.|
|pour|entier|Fin de l'index de la feuille de calcul.|
|Résolution horizontale|entier|Résolution horizontale de l'image.|
|Résolution verticale|entier|Résolution verticale de l'image.|
|dossier de sortie|chaîne|position du fichier divisé en sortie.|
|splitNameRule|chaîne||
|dossier|chaîne|Dossier de classeur d'origine.|
|nom_stockage|chaîne|Nom de stockage.|


## REPOS API

|**API**|**Taper**|**Description**|**Lien fanfaron**|
|:- |:- |:- |:- |
|/cellules/{nom}/split|POSTE|Fractionner un classeur Excel|[PostWorkbookSplit](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookSplit)|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookSplit) définit une interface de programmation accessible au public et permet d'effectuer des interactions REST directement depuis un navigateur Web.

 Vous pouvez utiliser**cURL** outil de ligne de commande pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers le Cloud API avec cURL.

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

## Famille SDK Cloud

 L'utilisation d'un SDK est le meilleur moyen d'accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le[Référentiel GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="11" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" tabName11="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorkbookPostWorkbookSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-workbook-SplitWorkbooks-split-excel-workbooks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostWorkbookSplit-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-split_workbook-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SplitExcelWorkbooks.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Workbook-SplitWorkbooks-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-workbook-SplitWorkbooks-split-excel-workbooks.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Workbook-SplitWorkbooks-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "ec45ec662143f4c94c2a8bc8c95953ce" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}

{{< gist "aspose-cells-cloud-gists" "6ddbdc7793cac6e13ad09bbfbc44a614" >}}

{{< /tab >}}

{{< /tabs >}}
