---
title: Ottieni intervalli denominati su un workboo Excel
second_title: Aspose.Cells Cloud Documen
linktitle: nome
type: docs
url: /it/ranges/get/name/
aliases: [/get-named-ranges-inside-the-workbook/]
keywords: Get cells data based on named range on an Excel worksheet
description: Aspose.Cells Cloud REST API supporta l'acquisizione dei dati delle celle in base all'intervallo denominato su un foglio di lavoro Excel. L'SDK supporta tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 10
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdwon, Ottieni intervalli denominati su una cartella di lavoro Excel
---
Questo REST API indica le informazioni sugli intervalli di lettura dei fogli di lavoro.
 
## RSETAPI
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/ranges
 
```
 I parametri della richiesta sono:
 
| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| nome| corda| sentiero| Nome del documento.|
| cartella| corda| domanda| Cartella documenti.|
| storageName| corda| domanda| nome dell'archivio.|
 
 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetNamedRanges) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.
 
È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi Web Aspose.Cells. Nell'esempio seguente viene illustrato come effettuare chiamate al Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/ranges" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{

  "Ranges": {

    "RangeList": [

      {

        "ColumnCount": 7,

        "ColumnWidth": 8.428571428571429,

        "FirstColumn": 1,

        "FirstRow": 9,

        "Name": "data",

        "RefersTo": "=Sheet1!$B$10:$H$10",

        "RowCount": 1,

        "RowHeight": 15,

        "Worksheet": "Sheet1"

      }

    ]

  },

  "Code": 200,

  "Status": "OK"

}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Famiglia di SDK Cloud
 
 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si prende cura dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Repositorio GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK Cloud Aspose.Cells.
 
I seguenti esempi di codice dimostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:
 
 
{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="Ruby" tabName3="Go" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}



{{< /tab >}}

{{< tab tabNum="3" >}}



{{< gist "aspose-cells-cloud-gists" "c75da9aa06645e27e899a9fb6cdc134c" >}}

{{< /tab >}}

{{< /tabs >}}
