---
title: Работа с ImportData Tas
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/tasks/importdata/
aliases: [/working-with-importdata-task/]
keywords: REST API, task, convert, spreadsheets, exce
description: "Cells.Облако API для Excel работает: задачи поддерживают импорт данных в файл Excel."
weight: 40
---
## ОТДЫХ API

|**API**|**Тип**|**Описание**|**Ссылка на ресурс**|
|:- |:- |:- |:- |
|/cells/task/runtask|ПОЧТА|Запустить задачу|[Пострантаск](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|


[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) определяет общедоступный интерфейс программирования и позволяет выполнять взаимодействие с REST непосредственно из веб-браузера.

 Вы можете использовать**cURL** инструмент командной строки для легкого доступа к веб-службам Aspose.Cells. В следующем примере показано, как позвонить на Cloud API с помощью cURL.

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

 Использование SDK — лучший способ ускорить разработку. SDK заботится о деталях низкого уровня и позволяет вам сосредоточиться на задачах проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для получения полного списка Aspose.Cells Cloud SDK.

Следующие примеры кода демонстрируют, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:

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

