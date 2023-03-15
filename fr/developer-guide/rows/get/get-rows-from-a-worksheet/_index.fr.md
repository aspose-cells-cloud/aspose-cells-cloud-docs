---
title: Obtenir des informations sur les lignes d'une feuille de calcul Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Ligne
type: docs
url: /fr/rows/get/rows/
aliases: [/get-row-from-a-worksheet/]
keywords: Get rows info on an Excel workshee
description: Aspose.Cells Cloud REST API prend en charge l'obtention de lignes sur une feuille de calcul Excel. SDK prend en charge les types de langages de développement. Ils incluent Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift
weight: 10
---
Ce REST API indique d'obtenir des informations sur les lignes d'une feuille de calcul Excel.
 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
 
```
 Les paramètres de la requête sont :
 
| Le nom du paramètre| Taper| Chemin/chaîne de requête/HTTPBody|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin|Le nom du classeur.|
| NomFeuille| chaîne| chemin| Le nom de la feuille de calcul.|
| dossier| chaîne| mettre en doute| Le dossier workdook.|
| nom_stockage| chaîne| mettre en doute| nom de stockage.|
 
 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetRows) définit une interface de programmation accessible au public et permet d'effectuer des interactions REST directement depuis un navigateur Web.
 
Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers le Cloud API avec cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{

  "Rows": {

    "MaxRow": 20,

    "RowsCount": 17,

    "RowsList": [

      {

        "link": {

          "Href": "/0",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/1",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/2",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/3",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/4",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/5",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/6",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/7",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/8",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/9",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/10",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/11",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/12",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/13",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/14",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/15",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/16",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/17",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/18",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/19",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/20",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/21",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/22",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/23",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/24",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      }

    ],

    "link": {

      "Href": "/test.xlsx/worksheets/Sheet1/cells/rows",

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
 
## Famille SDK Cloud
 
 L'utilisation d'un SDK est le meilleur moyen d'accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le[Référentiel GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Cloud Aspose.Cells.
 
Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows" -H "accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Rows": {

    "MaxRow": 20,

    "RowsCount": 17,

    "RowsList": [

      {

        "link": {

          "Href": "/0",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/1",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/2",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/3",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/4",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/5",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/6",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/7",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/8",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/9",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/10",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/11",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/12",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/13",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/14",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/15",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/16",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/17",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/18",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/19",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/20",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/21",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/22",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/23",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      {

        "link": {

          "Href": "/24",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      }

    ],

    "link": {

      "Href": "/test.xlsx/worksheets/Sheet1/cells/rows",

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
## **Source du SDK**
Les SDK Cloud Aspose.Cells peuvent être téléchargés à partir de la page suivante :[SDK disponibles](/cells/fr/available-sdks/)
### **Exemples de SDK**
{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Rows-GetRowFromWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-rows-GetRowFromWorksheet-get-row-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Rows-GetWorksheetRow-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Rows-read_worksheet_row_data-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetRowFromWorkSheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Rows-GetRowFromWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-rows-GetRowFromWorksheet-get-row-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Rows-GetRowFromWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "6043e554797cdcc62fb1cc2f3babfc3f" >}}

{{< /tab >}}

{{< /tabs >}}
