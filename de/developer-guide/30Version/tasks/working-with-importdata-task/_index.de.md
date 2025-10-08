---
title: Arbeiten mit ImportData Tas
second_title: Documen
type: docs
url: /de/tasks/importdata/
aliases: [/working-with-importdata-task/]
keywords: REST API, task, convert, spreadsheets, exce
description: "Cells.Cloud API für Excel betreiben: Aufgaben unterstützen den Import von Daten in Excel-Datei"
weight: 40
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, Arbeiten mit ImportData-Aufgabe
---
## REST API

|**API**|**Typ**|**Beschreibung**|**Ressourcenlink**|
|:- |:- |:- |:- |
|/Zellen/Aufgabe/Ausführen der Aufgabe|POST|Task ausführen|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|


 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

 Sie können**cURL** Befehlszeilentool für den einfachen Zugriff auf Aspose.Cells-Webdienste. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an Cloud API tätigen.

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

 Die Verwendung eines SDKs beschleunigt die Entwicklung am besten. Ein SDK kümmert sich um die Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte beachten Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

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

