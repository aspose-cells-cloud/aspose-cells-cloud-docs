---
title: Obtenir un objet de liste dans une feuille de calcul Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Gé
type: docs
url: /fr/list-objects/get/
aliases: [/get-a-list-object-or-table-inside-the-worksheet/,/tables/get/]
keywords: Get a list object(table) into an Excel worksheet
description: Aspose.Cells Cloud REST API prend en charge l'insertion d'un objet liste (table) dans une feuille de calcul Excel. Le SDK prend en charge différents langages de développement, notamment Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 9
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Obtenir un objet de liste dans une feuille de calcul Excel
---
Ce REST API indique à `get` une liste d'informations d'objet par index ou convertit un `list object` en un fichier de format différent dans une feuille de calcul Excel.

## RSET API

```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}
 
```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin| Nom du document.|
| nom de la feuille| chaîne| chemin| Le nom de la feuille de calcul.|
| index d'objets de liste| entier| chemin| index d'objet de liste.|
| format| chaîne| requête| format d'exportation.|
| dossier| chaîne| requête| Dossier du document.|
| nom de stockage| chaîne| requête| nom de stockage.|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/GetWorksheetListObject) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```bash
{
 "ListObject": {
  "AutoFilter": {
   "FilterColumns": [],
   "Range": "B2:F11",
   "Sorter": {
    "CaseSensitive": false,
    "HasHeaders": false,
    "KeyList": [],
    "SortLeftToRight": false
   }
  },
  "DisplayName": "Table3",
  "StartColumn": 1,
  "StartRow": 1,
  "EndColumn": 5,
  "EndRow": 10,
  "ListColumns": [{
   "Name": "Column1",
   "Range": {
    "ColumnCount": 1,
    "ColumnWidth": 8.5,
    "FirstColumn": 1,
    "FirstRow": 1,
    "RefersTo": "=Sheet1!$B$2:$B$11",
    "RowCount": 10,
    "RowHeight": 13.5,
    "Worksheet": "Sheet1"
   },
   "TotalsCalculation": "None"
  }, {
   "Name": "Column2",
   "Range": {
    "ColumnCount": 1,
    "ColumnWidth": 8.5,
    "FirstColumn": 2,
    "FirstRow": 1,
    "RefersTo": "=Sheet1!$C$2:$C$11",
    "RowCount": 10,
    "RowHeight": 13.5,
    "Worksheet": "Sheet1"
   },
   "TotalsCalculation": "None"
  }, {
   "Name": "Column3",
   "Range": {
    "ColumnCount": 1,
    "ColumnWidth": 8.5,
    "FirstColumn": 3,
    "FirstRow": 1,
    "RefersTo": "=Sheet1!$D$2:$D$11",
    "RowCount": 10,
    "RowHeight": 13.5,
    "Worksheet": "Sheet1"
   },
   "TotalsCalculation": "None"
  }, {
   "Name": "Column4",
   "Range": {
    "ColumnCount": 1,
    "ColumnWidth": 8.5,
    "FirstColumn": 4,
    "FirstRow": 1,
    "RefersTo": "=Sheet1!$E$2:$E$11",
    "RowCount": 10,
    "RowHeight": 13.5,
    "Worksheet": "Sheet1"
   },
   "TotalsCalculation": "None"
  }, {
   "Name": "Column5",
   "Range": {
    "ColumnCount": 1,
    "ColumnWidth": 8.5,
    "FirstColumn": 5,
    "FirstRow": 1,
    "RefersTo": "=Sheet1!$F$2:$F$11",
    "RowCount": 10,
    "RowHeight": 13.5,
    "Worksheet": "Sheet1"
   },
   "TotalsCalculation": "None"
  }],
  "ShowHeaderRow": true,
  "ShowTableStyleColumnStripes": false,
  "ShowTableStyleFirstColumn": false,
  "ShowTableStyleLastColumn": false,
  "ShowTableStyleRowStripes": true,
  "ShowTotals": false,
  "TableStyleName": "None",
  "TableStyleType": "None",
  "link": {
   "Href": "api-qa.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0",
   "Rel": "self"
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

Ce REST API obtient un objet Excel `listobject` dans un fichier de format différent.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
