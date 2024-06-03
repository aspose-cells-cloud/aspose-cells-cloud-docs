---
title: Copia intervallo in un foglio di lavoro con l'opzione Incolla
second_title: Aspose.Cells Cloud Documen
linktitle: Poliziotto
type: docs
url: /it/ranges/copy/
aliases: [/copy-range-in-a-worksheet-with-paste-options/]
keywords: Copy a range in an Excel worksheet with paste options
description: Aspose.Cells Cloud REST API supporta la copia di un intervallo in un foglio di lavoro Excel con opzioni di incolla. L'SDK supporta tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 20
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdwon, Copia intervallo in un foglio di lavoro con opzioni Incolla
---
Questo REST API indica di copiare l'intervallo nel foglio di lavoro su un foglio di lavoro Excel.
 
## RSETAPI
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges
 
```
 I parametri della richiesta sono:
 
| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| nome| corda| sentiero| nome della cartella di lavoro|
| nomefoglio| corda| sentiero| nome del foglio di lavoro|
| rangeOperate|| corpo| copydata,copystyle,copyto,copyvalue|
| cartella| corda| domanda| Cartella della cartella di lavoro.|
| storageName| corda| domanda| nome dell'archivio.|
 
 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRanges) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.
 
È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi Web Aspose.Cells. Nell'esempio seguente viene illustrato come effettuare chiamate al Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-d "{ \"Operate\": \"string\", \"Source\": { \"ColumnCount\": 0, \"ColumnWidth\": 0, \"FirstColumn\": 0, \"FirstRow\": 0, \"Name\": \"string\", \"RefersTo\": \"string\", \"RowCount\": 0, \"RowHeight\": 0, \"Worksheet\": \"string\" }, \"Target\": { \"ColumnCount\": 0, \"ColumnWidth\": 0, \"FirstColumn\": 0, \"FirstRow\": 0, \"Name\": \"string\", \"RefersTo\": \"string\", \"RowCount\": 0, \"RowHeight\": 0, \"Worksheet\": \"string\" }, \"PasteOptions\": { \"OnlyVisibleCells\": true, \"PasteType\": \"string\", \"SkipBlanks\": true, \"Transpose\": true }}"

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
 
## Famiglia di SDK Cloud
 
 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si prende cura dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Repositorio GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK Cloud Aspose.Cells.
 
I seguenti esempi di codice dimostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:
 
 
 
{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp

string Client_Id = "Use your Client_Id";

string Client_Secret = "Use your Client_Secret";

//Copy Range in a Worksheet with Paste Options - URL

string url = "http://api.aspose.cloud/v3.0/cells/sampleRangeCopyTo.xlsx/worksheets/Sheet1/ranges";

//JSON - Part of Request Body

string strJson = "{ \"Operate\": \"copyto\", \"Source\": { \"ColumnCount\": 5, \"ColumnWidth\": 8.43, \"FirstColumn\": 1, \"FirstRow\": 0, \"RowCount\": 7, \"RowHeight\": 15, }, \"Target\": { \"ColumnCount\": 5, \"ColumnWidth\": 8.43, \"FirstColumn\": 10, \"FirstRow\": 20, \"RowCount\": 7, \"RowHeight\": 15, } , \"PasteOptions\": { \"OnlyVisibleCells\": true, \"PasteType\": \"All\", \"SkipBlanks\": true, \"Transpose\": false } }";

//Sign the URL

string surl = Sign(url, Client_Id, Client_Secret);

//Process Command - Post Signed URL with JSON body

using (Stream stream = ProcessCommand(surl, "Post", strJson, "json"))

{

	//Your code

}

```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "4b9529b9d4238c301f3ee4855843874b" >}}

{{< /tab >}}

{{< /tabs >}}




