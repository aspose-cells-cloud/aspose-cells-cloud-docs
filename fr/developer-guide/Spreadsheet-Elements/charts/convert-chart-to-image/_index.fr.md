﻿---
title: Convertir un graphique en image
type: docs
url: /fr/charts/to-image/
aliases: [/convert-charts-to-image/]
weight: 50
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Conversion de graphique en image
---
Ce REST API indique comment convertir un graphique en image.

## RSET API

```bash

GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartNumber}?format={format}

```
 Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin| Nom du document.|
| nom de la feuille| chaîne| chemin| Nom de la feuille de travail.|
| numéro de graphique| entier| chemin| Le numéro du graphique.|
| format| chaîne| requête| Le format du fichier exporté.|
| dossier| chaîne| requête| Le dossier de documents.|
| nom de stockage| chaîne| requête| nom de stockage.|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChart) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash

curl -v "http://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0?format=jpg"
-X GET
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```bash
byte[]

```

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :


{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Python" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-ConvertChartToImage-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChartWithFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_in_specified_format-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-ConvertChartToImage-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ConvertChartToImage.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-ConvertChartToImage-convert-chart-to-image.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-ConvertChartToImage-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d22256010a610e1351ab15969a7adeef" >}}

{{< /tab >}}

{{< /tabs >}}
