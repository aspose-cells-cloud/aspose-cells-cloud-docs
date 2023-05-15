---
title: Excel foglio di lavoro rinomina
second_title: Aspose.Cells Cloud Documen
linktitle: Renam
type: docs
url: /it/worksheets/rename/
aliases: [/rename-excel-worksheet/]
keywords: Rename an Excel worksheet name to new name on an Excel workbook
description: Aspose.Cells Cloud REST API supporta la ridenominazione del nome di un foglio di lavoro Excel in un nuovo nome in una cartella di lavoro Excel. L'SDK supporta i tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 20
---
Questo REST API indica `worksheet rename`
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/rename
 
```
 I parametri della richiesta sono:
 
| Nome parametro| Tipo| Percorso/Stringa di query/HTTPBody|Descrizione|
|:- |:- |:- |:- |
| nome| corda| sentiero||
| foglioNome| corda| sentiero||
| nuovo nome| corda| domanda||
| cartella| corda| domanda||
| storageName| corda| domanda| nome di archiviazione.|
 
 IL[Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostRenameWorksheet) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.
 
È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi Web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate a Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/rename?newname=newSheet" \
-X POST \
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
 
## Famiglia di SDK cloud
 
 L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Deposito GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.
 
I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:
 
{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostRenameWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-RenameWorksheet-rename-excel-worksheeet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostRenameWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-rename_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "RenameExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-RenameWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-RenameWorksheet-rename-excel-worksheeet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-RenameWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "accf2723cfaa2a328d3dea355156e4d9" >}}

{{< /tab >}}

{{< /tabs >}}
