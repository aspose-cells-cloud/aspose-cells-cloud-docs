﻿---
title: Modifier le style de cellule dans la feuille de calcul Excel
type: docs
url: /fr/change-cell-style-in-excel-worksheet/
weight: 30
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Modifier le style de cellule dans la feuille de calcul Excel
---
Ce REST API indique la mise à jour `cell style` dans un fichier Excel.

## RSET API

```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style
 
```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin| Nom du classeur.|
| nom de la feuille| chaîne| chemin| Nom de la feuille de calcul.|
| nom de la cellule| chaîne| chemin| Le nom de la cellule.|
| style|| corps| avec les paramètres de style de mise à jour.|
| dossier| chaîne| requête| Le dossier du classeur.|
| nom de stockage| chaîne| requête| nom de stockage.|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostUpdateWorksheetCellStyle) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/test_cells.xlsx/worksheets/Sheet3/cells/A1/style" \
-d '{ "BackgroundThemeColor": { "ColorType": "Text2", "Tint": 1 } }' \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```bash
{

  "Style": {

    "Font": {

      "Color": {

        "A": 255,

        "R": 0,

        "G": 0,

        "B": 0

      },

      "DoubleSize": 11,

      "IsBold": false,

      "IsItalic": false,

      "IsStrikeout": false,

      "IsSubscript": false,

      "IsSuperscript": false,

      "Name": "Calibri",

      "Size": 11,

      "Underline": "None"

    },

    "Name": null,

    "CultureCustom": null,

    "Custom": "",

    "BackgroundColor": {

      "A": 0,

      "R": 0,

      "G": 0,

      "B": 0

    },

    "ForegroundColor": {

      "A": 0,

      "R": 0,

      "G": 0,

      "B": 0

    },

    "IsFormulaHidden": false,

    "IsDateTime": false,

    "IsTextWrapped": false,

    "IsGradient": false,

    "IsLocked": true,

    "IsPercent": false,

    "ShrinkToFit": false,

    "IndentLevel": 0,

    "Number": 0,

    "RotationAngle": 0,

    "Pattern": "None",

    "TextDirection": "Context",

    "VerticalAlignment": "Bottom",

    "HorizontalAlignment": "General",

    "BorderCollection": [

      {

        "LineStyle": "None",

        "Color": {

          "A": 255,

          "R": 0,

          "G": 0,

          "B": 0

        },

        "BorderType": "BottomBorder"

      },

      {

        "LineStyle": "None",

        "Color": {

          "A": 255,

          "R": 0,

          "G": 0,

          "B": 0

        },

        "BorderType": "DiagonalDown"

      },

      {

        "LineStyle": "None",

        "Color": {

          "A": 255,

          "R": 0,

          "G": 0,

          "B": 0

        },

        "BorderType": "DiagonalUp"

      },

      {

        "LineStyle": "None",

        "Color": {

          "A": 255,

          "R": 0,

          "G": 0,

          "B": 0

        },

        "BorderType": "Horizontal"

      },

      {

        "LineStyle": "None",

        "Color": {

          "A": 255,

          "R": 0,

          "G": 0,

          "B": 0

        },

        "BorderType": "LeftBorder"

      },

      {

        "LineStyle": "None",

        "Color": {

          "A": 255,

          "R": 0,

          "G": 0,

          "B": 0

        },

        "BorderType": "RightBorder"

      },

      {

        "LineStyle": "None",

        "Color": {

          "A": 255,

          "R": 0,

          "G": 0,

          "B": 0

        },

        "BorderType": "TopBorder"

      },

      {

        "LineStyle": "None",

        "Color": {

          "A": 255,

          "R": 0,

          "G": 0,

          "B": 0

        },

        "BorderType": "Vertical"

      }

    ],

    "BackgroundThemeColor": null,

    "ForegroundThemeColor": null,

    "link": {

      "Href": "http://api.aspose.cloud/v3.0/cells/test_cells.xlsx/worksheets/Sheet3/cells/A1/style",

      "Rel": "self",

      "Title": null,

      "Type": null

    }

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

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUpdateWorksheetCellStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUpdateWorksheetCellStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUpdateWorksheetCellStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUpdateWorksheetCellStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUpdateWorksheetCellStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUpdateWorksheetCellStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUpdateWorksheetCellStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUpdateWorksheetCellStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}
