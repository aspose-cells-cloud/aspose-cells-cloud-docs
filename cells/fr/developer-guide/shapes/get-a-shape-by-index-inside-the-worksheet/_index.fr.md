---
title: Obtenir une forme par index sur une feuille de calcul Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Ge
type: docs
url: /fr/shapes/get/
aliases: [/get-a-shape-by-index-inside-the-worksheet/]
keywords: Get a shape on an Excel workshee
description: Aspose.Cells Cloud REST API prend en charge l'obtention d'une forme sur une feuille de calcul Excel. SDK prend en charge les types de langages de développement. Ils incluent Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift
weight: 20
---
Ce REST API indique d'obtenir une forme avec un format d'image ou une information de forme sur une feuille de calcul Excel.
 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
 
```
 Les paramètres de la requête sont :
 
| Le nom du paramètre| Taper| Chemin/chaîne de requête/HTTPBody|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin| Nom du document.|
| NomFeuille| chaîne| chemin| nom de la feuille de calcul.|
| indice de forme| entier| chemin| index de forme dans les formes de feuille de calcul.|
| dossier| chaîne| mettre en doute| Dossier du document.|
| nom_stockage| chaîne| mettre en doute| nom de stockage.|
 
 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Shapes/GetWorksheetShape) définit une interface de programmation accessible au public et permet d'effectuer des interactions REST directement depuis un navigateur Web.
 
Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers le Cloud API avec cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet4/autoshapes/1" \
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

  "Shape": {

    "link": {

      "Href": "string",

      "Rel": "string",

      "Title": "string",

      "Type": "string"

    },

    "Name": "string",

    "MsoDrawingType": "string",

    "AutoShapeType": "string",

    "Placement": "string",

    "UpperLeftRow": 0,

    "Top": 0,

    "UpperLeftColumn": 0,

    "Left": 0,

    "LowerRightRow": 0,

    "Bottom": 0,

    "LowerRightColumn": 0,

    "Right": 0,

    "Width": 0,

    "Height": 0,

    "X": 0,

    "Y": 0,

    "RotationAngle": 0,

    "HtmlText": "string",

    "Text": "string",

    "AlternativeText": "string",

    "TextHorizontalAlignment": "string",

    "TextHorizontalOverflow": "string",

    "TextOrientationType": "string",

    "TextVerticalAlignment": "string",

    "TextVerticalOverflow": "string",

    "IsGroup": true,

    "IsHidden": true,

    "IsLockAspectRatio": true,

    "IsLocked": true,

    "IsPrintable": true,

    "IsTextWrapped": true,

    "IsWordArt": true,

    "LinkedCell": "string",

    "ZOrderPosition": 0

  }

}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Famille SDK Cloud
 
 L'utilisation d'un SDK est le meilleur moyen d'accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le[Référentiel GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Cloud Aspose.Cells.
 
Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :
 
{{< tabs tabTotal="5" tabID="4" tabName1="C#" tabName2="Java" tabName3="Perl" tabName4="Go" tabName5="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-GetWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-GetWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example-GetWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "dd6d8ac9aacd9be6085356c07dbbadd0" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f342d1e6f85982e0429fcd9bed8b11a8" "Example-GetWorksheetShape.swift" >}}

{{< /tab >}}

{{< /tabs >}}

