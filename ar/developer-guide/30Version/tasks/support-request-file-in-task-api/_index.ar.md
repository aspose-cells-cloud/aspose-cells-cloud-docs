---
title: ملف طلب الدعم في مهمة AP
second_title: Documen
type: docs
url: /ar/tasks/support-request-file/
aliases: [/support-request-file-in-task-api/]
keywords: REST API, task, request, spreadsheets, exce
description: "Cells.Cloud API لتشغيل Excel: ملف طلب دعم المهام"
weight: 10
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، ملف طلب الدعم في المهمة API
---
## الباقي API

|**API**|**يكتب**|**وصف**|**رابط المورد**|
|:- |:- |:- |:- |
|/الخلايا/المهمة/تشغيل المهمة|بريد|تشغيل المهمة|[مهمة ما بعد التشغيل](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

 يمكنك استخدام**cURL** أداة سطر أوامر للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API باستخدام cURL.

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


## عائلة SDK السحابية

 يُعد استخدام حزمة تطوير برمجيات (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل البسيطة وتُتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="1" tabID="4" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostTaskDataMultipart-.php" >}}

{{< /tab >}}

{{< /tabs >}}
