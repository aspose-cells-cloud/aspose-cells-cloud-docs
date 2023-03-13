---
title: Support-Request-Datei in Aufgabe AP
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/tasks/support-request-file/
aliases: [/support-request-file-in-task-api/]
keywords: REST API, task, request, spreadsheets, exce
description: "Cells.Cloud API für Excel betreiben: Aufgaben-Support-Anfragedatei"
weight: 10
---
## REST API

|**API**|**Typ**|**Beschreibung**|**Ressourcen-Link**|
|:- |:- |:- |:- |
|/cells/task/runtask|POST|Aufgabe ausführen|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) definiert eine öffentlich zugängliche Programmierschnittstelle und lässt Sie REST-Interaktionen direkt von einem Webbrowser ausführen.

 Sie können verwenden**cURL** Befehlszeilentool für den einfachen Zugriff auf Aspose.Cells-Webdienste. Das folgende Beispiel zeigt, wie Sie Cloud API mit cURL anrufen.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" -H "accept: application/json" -H "Content-Type: application/json" -H "x-aspose-client: Containerize.Swagger" -d "{ <Tasks>\t<TaskDescription>\t <TaskType>ImportData</TaskType>\t <ImportDataTaskParameter>\t\t<Workbook>\t\t <FileSourceType>CloudFileSystem</FileSourceType>\t\t <FilePath>TaskBook.xlsx</FilePath>\t\t</Workbook>\t\t<ImportBatchDataOption>\t\t <DestinationWorksheet>Sheet1</DestinationWorksheet>\t\t <IsInsert>true</IsInsert>\t\t <Source>\t\t\t<FileSourceType>RequestFiles</FileSourceType>\t\t\t<FilePath>Batch_data_xml.txt</FilePath>\t\t </Source>\t\t</ImportBatchDataOption>\t </ImportDataTaskParameter>\t</TaskDescription>\t<TaskDescription>\t <TaskType>ImportData</TaskType>\t <ImportDataTaskParameter>\t\t<Workbook>\t\t <FileSourceType>InMemoryFiles</FileSourceType>\t\t <FilePath>TaskBook.xlsx</FilePath>\t\t</Workbook>\t\t<ImportBatchDataOption>\t\t <DestinationWorksheet>Sheet2</DestinationWorksheet>\t\t <IsInsert>true</IsInsert>\t\t <Source>\t\t\t<FileSourceType>RequestFiles</FileSourceType>\t\t\t<FilePath>Batch_data_xml_2.txt</FilePath>\t\t </Source>\t\t</ImportBatchDataOption>\t </ImportDataTaskParameter>\t</TaskDescription>\t<TaskDescription>\t <TaskType>SaveResult</TaskType>\t <SaveResultTaskParameter>\t\t<ResultSource>InMemoryFiles</ResultSource>\t\t<ResultDestination>\t\t <DestinationType>CloudFileSystem</DestinationType>\t\t <InputFile>TaskBook.xlsx</InputFile>\t\t <OutputFile>ImpDataBook.xlsx</OutputFile>\t\t</ResultDestination>\t </SaveResultTaskParameter>\t</TaskDescription> </Tasks></TaskData>}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

HttpResponseMessage with the operation result.

```

{{< /tab >}}

{{< /tabs >}}


## Cloud SDK-Familie

 Die Verwendung eines SDK ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und lässt Sie sich auf Ihre Projektaufgaben konzentrieren. Bitte überprüfen Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="1" tabID="4" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostTaskDataMultipart-.php" >}}

{{< /tab >}}

{{< /tabs >}}
