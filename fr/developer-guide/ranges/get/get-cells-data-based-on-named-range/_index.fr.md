---
title: Obtenir des données de cellules basées sur une plage nommée
second_title: Aspose.Cells Cloud Documen
linktitle: Valeur
type: docs
url: /fr/ranges/get/values/
aliases: [/get-cells-data-based-on-named-range/]
keywords: Get cells data based on named range on an Excel worksheet
description: Aspose.Cells Cloud REST API prend en charge l'obtention de données de cellules basées sur une plage nommée sur une feuille de calcul Excel. SDK prend en charge les types de langages de développement. Ils incluent Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift
weight: 20
---
 Ce REST API indique Obtenir la liste des cellules dans une plage par nom de plage ou index de colonne de ligne

 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
 
```
 Les paramètres de la requête sont :
 
| Le nom du paramètre| Taper| Chemin/chaîne de requête/HTTPBody|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin| nom du classeur|
| NomFeuille| chaîne| chemin| nom de la feuille de calcul|
| plage de noms| chaîne| requête| nom de la plage, par exemple : 'A1:B2' ou 'range_name1'|
| première rangée| entier| requête| la première ligne de la gamme|
| première colonne| entier| requête| la première colonne de la plage|
| rowCount| entier| requête| le nombre de lignes dans la plage|
| nombre de colonnes| entier| requête| le nombre de colonnes dans la plage|
| dossier| chaîne| requête| Dossier de classeur.|
| nom_stockage| chaîne| requête| nom de stockage.|
 
 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/GetWorksheetCellsRangeValue) définit une interface de programmation accessible au public et permet d'effectuer des interactions REST directement depuis un navigateur Web.
 
Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers le Cloud API avec cURL.
 
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
 
## Famille SDK Cloud
 
 L'utilisation d'un SDK est le meilleur moyen d'accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le[Référentiel GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Cloud Aspose.Cells.
 
Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :
 
 