---
title: Ajouter un arrière-plan dans Workboo
second_title: Aspose.Cells Cloud Documen
linktitle: Annonce
type: docs
url: /fr/workbook/background/add/
aliases: [/add-background-in-workbook/,/workbook/add-background/]
keywords: Add background on an Excel workbook
description: Aspose.Cells Cloud REST API prend en charge l'ajout d'arrière-plan sur un classeur Excel sur un fichier Excel. SDK prend en charge les types de langages de développement. Ils incluent Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift
weight: 160
---
Ce REST API indique d'ajouter `background` sur un classeur Excel.


**Paramètre de requête**

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
|picPath|chaîne|positionnement de l'image.|
|dossier|chaîne|Dossier de classeur d'origine.|
|nom_stockage|chaîne|Nom de stockage.|

**Paramètre de corps de requête**

|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
|fichier de données| fichier de données|Le fichier de données est enregistré dans le corps de la requête.|

## REPOS API

|**API**|**Taper**|**Description**|**Lien vers la ressource**|
|:- |:- |:- |:- |
|/cellules/{nom}/fond|METTRE|Ajouter un arrière-plan dans un fichier Excel|[PutWorkbookBackground](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground)|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground) définit une interface de programmation accessible au public et permet d'effectuer des interactions REST directement depuis un navigateur Web.

 Vous pouvez utiliser**cURL** outil de ligne de commande pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers le Cloud API avec cURL.

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


## Famille SDK Cloud

 L'utilisation d'un SDK est le meilleur moyen d'accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le[Référentiel GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Android" tabName5="Perl" tabName6="Ruby" tabName7="PHP" tabName8="Node.js" tabName9="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "4f5e06ec874b8b698dfa0e5359c85f96" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "b47350fc841e7c7e8889b1f57723ad94" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "bef09b36e0e7b769022bd810898dbd73" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "a984b922e2a7373755fb877e8754452b" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "7b9fa1a76c49c164d034342a2a59d4e0" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "a56d3fa3fff9c61191ee3e869ec51cdd" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "4a63cab36bb9f03e4e58bc30267b60b8" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "4009896954c23f8a1394b3757a30ee9d" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d3b449b5e5e2cdbb25da9e8de37bdccc" >}}

{{< /tab >}}

{{< /tabs >}}
