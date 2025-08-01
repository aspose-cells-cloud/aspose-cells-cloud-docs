﻿---
title: Ottieni un oggetto elenco in un foglio di lavoro Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Ge
type: docs
url: /it/list-objects/get/
aliases: [/get-a-list-object-or-table-inside-the-worksheet/,/tables/get/]
keywords: Get a list object(table) into an Excel worksheet
description: Aspose.Cells Cloud REST API supporta l'inserimento di un oggetto elenco (tabella) in un foglio di lavoro Excel. L'SDK supporta diversi linguaggi di sviluppo, tra cui Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e Swift.
weight: 9
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Ottieni un oggetto elenco in un foglio di lavoro Excel
---
Questo REST API indica a `get` un elenco di informazioni sull'oggetto in base all'indice o converte un `list object` in un file di formato diverso in un foglio di lavoro Excel.

## RSET API

```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}
 
```

I parametri della richiesta sono:

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| nome| corda| sentiero| Nome del documento.|
| Nome del foglio| corda| sentiero| Nome del foglio di lavoro.|
| indiceoggettoelenco| intero| sentiero| elenca l'indice degli oggetti.|
| formato| corda| domanda| formato di esportazione.|
| cartella| corda| domanda| Cartella del documento.|
| Nome di archiviazione| corda| domanda| nome di archiviazione.|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/GetWorksheetListObject) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

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

## Famiglia Cloud SDK

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del progetto. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

Questo REST API ottiene un oggetto Excel `listobject` in un file di formato diverso.

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
