---
title: 使用 ImportData 任务
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/tasks/importdata/
aliases: [/working-with-importdata-task/]
keywords: REST API, task, convert, spreadsheets, exce
description: Cells.Cloud API for Excel操作：任务支持导入数据到excel文件
weight: 40
---
## 休息 API

|**API**|**类型**|**描述**|**资源链接**|
|:- |:- |:- |:- |
|/细胞/任务/运行任务|邮政|运行任务|[运行后任务](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|


这[开放API规范](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)定义了一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

您可以使用**cURL**命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示如何使用 cURL 呼叫云端 API。

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

使用 SDK 是加快开发速度的最佳方式。 SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)有关 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

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

