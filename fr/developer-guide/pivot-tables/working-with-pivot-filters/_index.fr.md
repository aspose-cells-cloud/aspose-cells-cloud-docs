﻿---
title: Travailler avec le filtre pivot
second_title: Aspose.Cells Cloud Documen
linktitle: Filtres
type: docs
url: /fr/pivot-tables/add-filters/
aliases: [/working-with-pivot-filters/]
keywords: Add filter for a pivot table
description: Aspose.Cells Cloud REST API prend en charge l'ajout d'un filtre pour un tableau croisé dynamique. SDK prend en charge les types de langages de développement. Ils incluent Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift
weight: 50
---
Ce REST API indique `add` pivot `filter` pour l'index de table piovt
 
## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotFilters
 
```
 Les paramètres de la requête sont :
 
| Le nom du paramètre| Taper| Chemin/chaîne de requête/HTTPBody|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin||
| NomFeuille| chaîne| chemin||
| indextablepivot| entier| chemin||
| filtre|| corps||
| besoin de recalculer| booléen| mettre en doute| FAUX|
| dossier| chaîne| mettre en doute||
| nom_stockage| chaîne| mettre en doute| nom de stockage.|
 
 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTableFilter) définit une interface de programmation accessible au public et permet d'effectuer des interactions REST directement depuis un navigateur Web.
 
Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers le Cloud API avec cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotFilters?needReCalculate=true" \
-X PUT \
-d "{ \"AutoFilter\": { \"link\": { \"Href\": \"string\", \"Rel\": \"string\", \"Title\": \"string\", \"Type\": \"string\" }, \"FilterColumns\": [ { \"FieldIndex\": 0, \"FilterType\": \"string\", \"MultipleFilters\": { \"MatchBlank\": true, \"MultipleFilterList\": [ {} ] }, \"ColorFilter\": { \"FilterByFillColor\": \"string\", \"Pattern\": \"string\", \"Color\": { \"Color\": { \"A\": 0, \"R\": 0, \"G\": 0, \"B\": 0 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"string\", \"Tint\": 0 }, \"Type\": \"string\" }, \"ForegroundColorColor\": { \"Color\": { \"A\": 0, \"R\": 0, \"G\": 0, \"B\": 0 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"string\", \"Tint\": 0 }, \"Type\": \"string\" }, \"BackgroundColor\": { \"Color\": { \"A\": 0, \"R\": 0, \"G\": 0, \"B\": 0 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"string\", \"Tint\": 0 }, \"Type\": \"string\" } }, \"CustomFilters\": [ { \"FilterOperatorType\": \"string\" } ], \"DynamicFilter\": { \"DynamicFilterType\": \"string\" }, \"IconFilter\": { \"IconId\": 0, \"IconSetType\": \"string\" }, \"Top10Filter\": { \"Criteria\": \"string\", \"IsPercent\": true, \"IsTop\": true, \"Items\": 0 }, \"Visibledropdown\": \"string\" } ], \"Range\": \"string\", \"Sorter\": { \"CaseSensitive\": true, \"HasHeaders\": true, \"KeyList\": [ { \"Key\": 0, \"SortOrder\": \"string\", \"CustomList\": \"string\" } ], \"SortLeftToRight\": true } }, \"EvaluationOrder\": 0, \"FieldIndex\": 0, \"FilterType\": \"string\", \"MeasureFldIndex\": 0, \"MemberPropertyFieldIndex\": 0, \"Name\": \"string\", \"Value1\": \"string\", \"Value2\": \"string\"}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
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
 
 
 

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp

public void Run_PivotTable_PivotFilter()

{

    url = @"http://api.aspose.com/v3.0/storage/file/Temp/V17.02.00_01.xlsx";

    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

    url = @"http://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx?folder=Temp";

    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

    url = @"http://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet?folder=Temp";

    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

    url = @"http://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/Sheet2?folder=Temp";

    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

    url = @"http://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/importdata?folder=Temp";

    data = "{ \"BatchData\":[{\"rowIndex\":0,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Sport\",\"style\":null},{\"rowIndex\":0,\"columnIndex\":1,\"type\":\"String\",\"value\":\"Year\",\"style\":null},{\"rowIndex\":0,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Quarter\",\"style\":null},{\"rowIndex\":0,\"columnIndex\":3,\"type\":\"String\",\"value\":\"Sales\",\"style\":null},{\"rowIndex\":0,\"columnIndex\":4,\"type\":\"String\",\"value\":\"YearSales\",\"style\":null},{\"rowIndex\":1,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Golf\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Golf\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Tennis\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Tennis\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Tennis\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Tennis\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Golf\",\"style\":null},{\"rowIndex\":1,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2014\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2014\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2014\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2013\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2013\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2013\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2013\",\"style\":null},{\"rowIndex\":1,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr4\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr4\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":3,\"type\":\"int\",\"value\":\"1500\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":3,\"type\":\"int\",\"value\":\"2000\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":3,\"type\":\"int\",\"value\":\"600\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":3,\"type\":\"int\",\"value\":\"1500\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":3,\"type\":\"int\",\"value\":\"4070\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":3,\"type\":\"int\",\"value\":\"5000\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":3,\"type\":\"int\",\"value\":\"6430\",\"style\":null},{\"rowIndex\":1,\"columnIndex\":4,\"type\":\"int\",\"value\":\"15000\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":4,\"type\":\"int\",\"value\":\"20000\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":4,\"type\":\"int\",\"value\":\"600\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":4,\"type\":\"int\",\"value\":\"1500\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":4,\"type\":\"int\",\"value\":\"4070\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":4,\"type\":\"int\",\"value\":\"5000\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":4,\"type\":\"int\",\"value\":\"6430\",\"style\":null}],\"DestinationWorksheet\":\"Sheet2\",\"IsInsert\":false}";

    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

    url = "http://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables?folder=Temp";

    data = "{\"Name\":\"TestPivot\",\"SourceData\":\"=Sheet2!A1:E8\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";

    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

    url = "http://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotFilters?folder=Temp";

    data = "{\"AutoFilter\":null,\"EvaluationOrder\":null,\"FieldIndex\":1,\"FilterType\":\"Count\",\"MeasureFldIndex\":null,\"MemberPropertyFieldIndex\":null,\"Name\":null,\"Value1\":null,\"Value2\":null}";

    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

    url = "http://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotFilters/0?folder=Temp";

    using (HttpWebResponse response = _helper.CallGet(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

    url = "http://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotFilters?folder=Temp";

    using (HttpWebResponse response = _helper.CallGet(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

    url = "http://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotFilters/0?folder=Temp";

    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

    url = "http://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotFilters?folder=Temp";

    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

}

```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "2a2aa16c2d9fd7e46b1b19f5fea5842b" >}}

{{< /tab >}}

{{< /tabs >}}




