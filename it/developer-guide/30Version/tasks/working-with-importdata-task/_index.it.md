---
title: Lavorare con ImportData Tas
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/tasks/importdata/
aliases: [/working-with-importdata-task/]
keywords: REST API, task, convert, spreadsheets, exce
description: "Cells.Cloud API per Excel opera: le attività supportano l'importazione di dati in file Excel"
weight: 40
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Utilizzo dell'attività ImportData
---
## RIPOSO API

|**API**|**Tipo**|**Descrizione**|**Link alla risorsa**|
|:- |:- |:- |:- |
|/cells/task/runtask|INVIARE|Esegui attività|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|


 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

 Puoi usare**cURL** Strumento da riga di comando per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" -H "accept: application/json" -H "Content-Type: application/json" -H "x-aspose-client: Containerize.Swagger" -d "{<Tasks> <TaskDescription> <TaskType>ImportData</TaskType> <ImportDataTaskParameter> <Workbook> <FileSourceType>CloudFileSystem</FileSourceType> <FilePath>TaskBook.xlsx</FilePath> </Workbook> <ImportBatchDataOption> <DestinationWorksheet>Sheet1</DestinationWorksheet> <IsInsert>true</IsInsert> <Source> <FileSourceType>RequestFiles</FileSourceType> <FilePath>Batch_data_xml.txt</FilePath> </Source> </ImportBatchDataOption> </ImportDataTaskParameter> </TaskDescription> <TaskDescription> <TaskType>ImportData</TaskType> <ImportDataTaskParameter> <Workbook> <FileSourceType>InMemoryFiles</FileSourceType> <FilePath>TaskBook.xlsx</FilePath> </Workbook> <ImportBatchDataOption> <DestinationWorksheet>Sheet2</DestinationWorksheet> <IsInsert>true</IsInsert> <Source> <FileSourceType>RequestFiles</FileSourceType> <FilePath>Batch_data_xml_2.txt</FilePath> </Source> </ImportBatchDataOption> </ImportDataTaskParameter> </TaskDescription> <TaskDescription> <TaskType>SaveResult</TaskType> <SaveResultTaskParameter> <ResultSource>InMemoryFiles</ResultSource> <ResultDestination> <DestinationType>CloudFileSystem</DestinationType> <InputFile>TaskBook.xlsx</InputFile> <OutputFile>ImpDataBook.xlsx</OutputFile> </ResultDestination> </SaveResultTaskParameter> </TaskDescription> </Tasks></TaskData>}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

HttpResponseMessage with the operation result.

```

{{< /tab >}}

{{< /tabs >}}

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del progetto. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="5" tabID="8" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Tasks-ImportTaskData-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostTaskDataMultipart-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_run_task-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Tasks-ImportTaskData-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ImportData-postImportDataMultipartContent-1.pl" >}}

{{< /tab >}}

{{< /tabs >}}

