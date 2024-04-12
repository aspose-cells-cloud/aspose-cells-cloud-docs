---
title: ImportData Tas ile Çalışma
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/tasks/importdata/
aliases: [/working-with-importdata-task/]
keywords: REST API, task, convert, spreadsheets, exce
description: "Cells.Cloud API, Excel için çalışır: görevler, verileri excel dosyasına aktarmayı destekler"
weight: 40
---
## DİNLENME API

|**API**|**Tip**|**Tanım**|**Kaynak Bağlantısı**|
|:- |:- |:- |:- |
|/hücreler/görev/çalıştırma görevi|POSTALAMAK|Görevi Çalıştır|[Çalıştırma SonrasıGörev](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|


[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

 Kullanabilirsiniz**cURL** Aspose.Cells web hizmetlerine kolayca erişmek için komut satırı aracı. Aşağıdaki örnekte, cURL ile Cloud API'e nasıl çağrı yapılacağı gösterilmektedir.

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

 SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük düzeyli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanıza olanak tanır. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:

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

