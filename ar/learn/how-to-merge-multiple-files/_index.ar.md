---
title: كيفية دمج ملفات جدول بيانات متعددة باستخدام Aspose.Cells Clou
linktitle: كيفية دمج ملفات جداول البيانات المتعددة
type: docs
url: /ar/how-to-merge-multiple-files
description: كيفية دمج ملفات جداول البيانات المتعددة مع Aspose.Cells Cloud
weight: 10
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، كيفية دمج ملفات متعددة من خلال Aspose.Cells السحابة
---
## مقدمة

يُعدّ Aspose.Cells Cloud API حلاً سحابيًا فعالاً، مُصمّمًا لإنشاء ملفات جداول البيانات وتحريرها وتحويلها. في هذه المقالة، سنشرح لك عملية استخدام Aspose.Cells Cloud API لدمج تنسيقات الملفات، بما في ذلك حالات الاستخدام النموذجية ومثال على الكود.

## ملخص

 يوفر الإصدار Aspose.Cells Cloud API واجهات برمجة تطبيقات قوية لدمج ملفات جداول بيانات متعددة في ملف واحد بمختلف التنسيقات. تشمل التنسيقات المدعومة:**Excel** (XLS، XLSX)،**ملف CSV**, **HTML**, **PDF**والمزيد. باستخدام Aspose.Cells Cloud API، يمكنك دمج ملفات جداول بيانات متعددة بسهولة في ملف واحد بتنسيقات شائعة الاستخدام، لتلبية مجموعة متنوعة من المتطلبات.

تتوفر العديد من واجهات برمجة التطبيقات (APIs) لدمج الملفات، وهي متوافقة عمومًا مع مختلف بيئات الإنترنت. فيما يلي وصف تفصيلي لهذه الواجهات:

| وظيفة| وصف| API مرجع|
|:------------------------- |:------------------------- |:------------------------- |
|**[دمج جداول البيانات](https://docs.aspose.cloud/cells/merge-spreadsheets/)** |دمج ملفات جدول البيانات المحلية في ملف بتنسيق محدد.|[دمج جداول البيانات](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheets) |
|**[دمج جدول البيانات عن بُعد](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)** | دمج ملفات جدول البيانات الموجودة في مجلد التخزين السحابي في ملف بتنسيق محدد.|[دمج جدول البيانات عن بعد](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeRemoteSpreadsheet) |
|**[دمج جداول البيانات في مجلد بعيد](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)** | دمج ملفات جدول البيانات الموجودة في مجلد التخزين السحابي في ملف بتنسيق محدد.|[دمج جداول البيانات في المجلد البعيد](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheetsInRemoteFolder) |

# كيفية دمج ملفات متعددة في ملف واحد من خلال Aspose.Cells Cloud

 توفر السحابة Aspose.Cells API[مجموعات تطوير البرامج المتعددة](https://github.com/aspose-cells-cloud) للغات البرمجة المختلفة. اختر حزمة تطوير البرامج (SDK) التي تتوافق مع لغة البرمجة المفضلة لديك، واتبع الوثائق المرفقة للتثبيت والتهيئة. أو يمكنك تصميم حزمة تطوير البرامج (SDK) الخاصة بك وفقًا لـ[API مرجع](https://reference.aspose.cloud/cells/)في هذا القسم، سنستخدم C# كمثال لتفصيل عملية دمج الملفات.

## التسجيل والحصول على مفتاح API

قبل البدء، عليك أن:[تسجيل حساب سحابي Aspose](https://id.containerize.com/signup) و[احصل على مفتاح API للمصادقة](https://dashboard.aspose.cloud/applications)من خلال تسجيل الدخول إلى موقع Aspose Cloud الرسمي، يمكنك إنشاء حساب مجاني والحصول على مفتاح API لأغراض المصادقة.

 لمزيد من التفاصيل حول العمليات، يرجى الرجوع إلى المستندات التالية:[البدء السريع مع Cells Cloud](https://docs.aspose.cloud/cells/quickstart/)

## تثبيت وتكوين SDK السحابي Aspose.Cells

قم بتثبيت الحزمة Aspose.Cells-Cloud NuGet في مشروعك .NET، ويمكنك استخدام وحدة التحكم Package Manager NuGet أو Package Manager NuGet في Visual Studio.
إليك كيفية تثبيت الحزمة باستخدام وحدة التحكم في إدارة الحزم:

```Powershell

Install-Package Aspose.Cells-Cloud

```

يُنشئ مثيلًا جديدًا لفئة CellsApi، مع تهيئة مُعرّف العميل وسرّه. فيما يلي تفاصيل مقتطف الكود المذكور أعلاه:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

تأكد من استبدال الخاص بك_API_مفتاحك_برنامج_SID ومعرفك_برنامج_المفتاح مع المفتاح الفعلي API ومعرف تطبيق SID ومفتاح التطبيق.

## إنشاء الطلب API والاتصال بالرقم API

### استفد من خدمات السحابة لدمج جداول البيانات المحلية وتسليم الملفات الموحدة - إما كمخرجات محلية أو تدفقات في الذاكرة - بأي تنسيق مطلوب

```CSharp

using System.Collections.Generic;

var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));

// Suild merged spreadsheet request
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsRequest();
// Set need merged files.
IDictionary<string, System.IO.Stream> mapFiles = new Dictionary<string, System.IO.Stream>();
mapFiles.Add("Book1.xlsx", File.OpenRead("Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead("Book2.xlsx"));
request.Spreadsheet = mapFiles;
// Set output format
request.outFormat = "pdf";

cellsApi.MergeSpreadsheets(request, "MergedResultFile.pdf");

```

### دمج جداول البيانات المخزنة في السحابة وتسليم الملف الموحد - محليًا أو مرة أخرى إلى تخزين السحابة - بأي تنسيق مطلوب

```C#
// Get your Client ID and Client Secret from https://dashboard.aspose.cloud (free registration is required).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// Build merge request parameters 
var request = new Aspose.Cells.Cloud.SDK.Request.MergeRemoteSpreadsheetRequest();
// Set cloud main file
request.name = "Book1.xlsx";
request.folder = "RemoteFolder1";
// Set cloud merged file
request.mergedSpreadsheet = "RemoteFolder2/Book2.xlsx";
request.outFormat = "pdf";
cellsApi.MergeRemoteSpreadsheet(request, "MergedResultOutPutToLocalFile.pdf");
```

### دمج الملفات المتطابقة تلقائيًا في دليل سحابي، وتصدير النتيجة الموحدة بالتنسيق المحدد، وتسليمها محليًا أو مرة أخرى إلى التخزين السحابي

```csharp
// Get your Client ID and Client Secret from https://dashboard.aspose.cloud (free registration is required).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// Build merge request parameters 
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsInRemoteFolderRequest();
// Storage directory that needs to merge files
request.folder = "RemoteFolder";
request.fileMatchExpression = "*xlsx$";
request.outFormat = "pdf";
cellsApi.MergeSpreadsheetsInRemoteFolder(request, "MergedResultOutPutToLocalFile.pdf");
```

## حالات الاستخدام

 الملفات المتعددة**تم دمجها**ميزة Aspose.Cells Cloud API مفيدة في العديد من حالات الاستخدام العملي. إليك بعض السيناريوهات الشائعة:

- **دمج ملفات Excel متعددة في ملف Excel** لتحليل البيانات وتخزينها.
- **دمج ملفات البيانات في ملف Excel** لتحليل البيانات.
- **دمج ملفات صور متعددة في ملف PDF** للمشاركة بسهولة.
- **دمج ملفات متعددة في ملف HTML** للعرض والتضمين في صفحات الويب.

## خاتمة

مع Aspose.Cells Cloud API، يمكنك بسهولة دمج ملفات جداول بيانات متعددة في ملف واحد. من خلال إجراء مكالمات بسيطة API وضبط خيارات الدمج المناسبة، يمكنك تلبية متطلبات دمج الملفات المختلفة بكفاءة. ادمج Aspose.Cells Cloud API في تطبيقاتك لتحسين الإنتاجية وتوفير وقت التطوير.

يرجى ملاحظة أن الكود المثال أعلاه هو لأغراض العرض التوضيحي فقط، وسيلزم استبداله ببيانات اعتماد مصادقة ومسارات ملفات صالحة عند استخدامه عمليًا. بالإضافة إلى ذلك، يوفر Aspose.Cells Cloud API العديد من الميزات الأخرى، مثل إنشاء جداول البيانات وتحريرها ومعالجتها ومعالجة البيانات. يمكنك الاطلاع على وثائق API التفصيلية والكود المثال على[دليل المطور للموقع الرسمي Aspose](/developer-guide/).

نأمل أن تساعدك هذه المقالة على فهم كيفية استخدام Aspose.Cells Cloud API لدمج الملفات. نتمنى لك التوفيق في التنفيذ!
