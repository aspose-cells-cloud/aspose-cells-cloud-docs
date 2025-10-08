---
title: Obtenir des données de cellules en fonction de la plage nommée
second_title: Documen
linktitle: Valeur
type: docs
url: /fr/ranges/get/values/
aliases: [/get-cells-data-based-on-named-range/]
keywords: Get cells data based on named range on an Excel worksheet
description: Aspose.Cells Cloud REST API prend en charge l'obtention de données de cellules basées sur une plage nommée dans une feuille de calcul Excel. Le SDK prend en charge différents langages de développement, notamment Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 20
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Obtenir les données des cellules en fonction d'une plage nommée
---
Ce REST API indique Obtenir la liste des cellules dans une plage par nom de plage ou par index de colonne de ligne

## RSET API

```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
 
```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin| nom du classeur|
| nom de la feuille| chaîne| chemin| nom de la feuille de calcul|
| plage de noms| chaîne| requête| nom de plage, par exemple : « A1:B2 » ou « range_name1 »|
| première rangée| entier| requête| la première rangée de la gamme|
| première colonne| entier| requête| la première colonne de la plage|
| nombre de lignes| entier| requête| le nombre de lignes dans la plage|
| colonneCount| entier| requête| le nombre de colonnes dans la plage|
| dossier| chaîne| requête| Dossier de classeur.|
| nom de stockage| chaîne| requête| nom de stockage.|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/GetWorksheetCellsRangeValue) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?namerange=data" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
{

  "CellsList": [

    {

      "Name": "B10",

      "Row": 9,

      "Column": 1,

      "Value": null,

      "Type": "IsNull",

      "Formula": null,

      "IsFormula": false,

      "IsMerged": false,

      "IsArrayHeader": false,

      "IsInArray": false,

      "IsErrorValue": false,

      "IsInTable": false,

      "IsStyleSet": false,

      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",

      "Style": {

        "link": {

          "Href": "/style",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      "Worksheet": null,

      "link": null

    },

    {

      "Name": "C10",

      "Row": 9,

      "Column": 2,

      "Value": null,

      "Type": "IsNull",

      "Formula": null,

      "IsFormula": false,

      "IsMerged": false,

      "IsArrayHeader": false,

      "IsInArray": false,

      "IsErrorValue": false,

      "IsInTable": false,

      "IsStyleSet": false,

      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",

      "Style": {

        "link": {

          "Href": "/style",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      "Worksheet": null,

      "link": null

    },

    {

      "Name": "D10",

      "Row": 9,

      "Column": 3,

      "Value": null,

      "Type": "IsNull",

      "Formula": null,

      "IsFormula": false,

      "IsMerged": false,

      "IsArrayHeader": false,

      "IsInArray": false,

      "IsErrorValue": false,

      "IsInTable": false,

      "IsStyleSet": false,

      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",

      "Style": {

        "link": {

          "Href": "/style",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      "Worksheet": null,

      "link": null

    },

    {

      "Name": "E10",

      "Row": 9,

      "Column": 4,

      "Value": null,

      "Type": "IsNull",

      "Formula": null,

      "IsFormula": false,

      "IsMerged": false,

      "IsArrayHeader": false,

      "IsInArray": false,

      "IsErrorValue": false,

      "IsInTable": false,

      "IsStyleSet": false,

      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",

      "Style": {

        "link": {

          "Href": "/style",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      "Worksheet": null,

      "link": null

    },

    {

      "Name": "F10",

      "Row": 9,

      "Column": 5,

      "Value": null,

      "Type": "IsNull",

      "Formula": null,

      "IsFormula": false,

      "IsMerged": false,

      "IsArrayHeader": false,

      "IsInArray": false,

      "IsErrorValue": false,

      "IsInTable": false,

      "IsStyleSet": false,

      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",

      "Style": {

        "link": {

          "Href": "/style",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      "Worksheet": null,

      "link": null

    },

    {

      "Name": "G10",

      "Row": 9,

      "Column": 6,

      "Value": null,

      "Type": "IsNull",

      "Formula": null,

      "IsFormula": false,

      "IsMerged": false,

      "IsArrayHeader": false,

      "IsInArray": false,

      "IsErrorValue": false,

      "IsInTable": false,

      "IsStyleSet": false,

      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",

      "Style": {

        "link": {

          "Href": "/style",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      "Worksheet": null,

      "link": null

    },

    {

      "Name": "H10",

      "Row": 9,

      "Column": 7,

      "Value": "a8",

      "Type": "IsString",

      "Formula": null,

      "IsFormula": false,

      "IsMerged": false,

      "IsArrayHeader": false,

      "IsInArray": false,

      "IsErrorValue": false,

      "IsInTable": false,

      "IsStyleSet": false,

      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">a8</Font>",

      "Style": {

        "link": {

          "Href": "/style",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      "Worksheet": null,

      "link": null

    }

  ],

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

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellsRangeValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellsRangeValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellsRangeValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellsRangeValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellsRangeValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellsRangeValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellsRangeValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellsRangeValue.go" >}}

{{< /tab >}}

{{< /tabs >}}
