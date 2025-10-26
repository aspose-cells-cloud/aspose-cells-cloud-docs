---
title: Ajouter un arrière-plan dans Workboo
second_title: Documen
linktitle: Annonce
type: docs
url: /fr/add-background-in-excel-file/
aliases: [/add-background-in-workbook/,/workbook/add-background/,/workbook/background/add/]
keywords: Add background on an Excel workbook
description: Aspose.Cells Cloud REST API prend en charge l'ajout d'arrière-plan à un classeur Excel et à un fichier Excel. Le SDK prend en charge différents langages de développement, notamment Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 160
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Ajouter un arrière-plan au classeur
---
Ce REST API indique d'ajouter `background` sur un classeur Excel.

**Paramètre de requête**

|Nom du paramètre|Taper|Description|
|:- |:- |:- |
|picPath|chaîne|position de l'image.|
|dossier|chaîne|Classeur original.|
|nom de stockage|chaîne|Nom de stockage.|

**Paramètre du corps de la requête**

|Nom du paramètre|Taper|Description|
|:- |:- |:- |
|fichier de données| fichier de données|Le fichier de données est enregistré dans le corps de la demande.|

## RESTE API

|**API**|**Taper**|**Description**|**Lien vers la ressource**|
|:- |:- |:- |:- |
|/cellules/{nom}/arrière-plan|METTRE|Ajouter un arrière-plan dans un fichier Excel|[Mettre l'arrière-plan du classeur](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground)|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

 Vous pouvez utiliser**cURL** Outil en ligne de commande pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le cloud API avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X PUT "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/background?picPath=DotnetFiles%2FWaterMark.png&folder=DotnetFiles" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

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

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}
