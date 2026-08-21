---
title: "كيفية دمج ملفات جداول البيانات المتعددة باستخدام Aspose.Cells Cloud"
linktitle: "كيفية دمج ملفات جداول البيانات المتعددة"
type: docs
url: /how-to-merge-multiple-files
description: "كيفية دمج ملفات جداول البيانات المتعددة باستخدام Aspose.Cells Cloud."
weight: 10
kwords: Excel، Office Cloud، REST API، جدول بيانات، PDF، CSV، JSON، Markdown، كيفية دمج ملفات متعددة باستخدام Aspose.Cells Cloud
---

## المقدمة

تُعد واجهة برمجة تطبيقات Aspose.Cells Cloud حلاً قويًا قائمًا على الحوسبة السحابية مُصممٍ لإنشاء جداول البيانات وتعديلها وتحويلها. في هذه المقالة، سنوضح لك بالتفصيل كيفية استخدام واجهة برمجة تطبيقات Aspose.Cells Cloud لدمج ملفات بتنسيقات مختلفة، بما في ذلك الحالات الشائعة للاستخدام وأمثلة الكود.

## نظرة عامة

تقدم واجهة برمجة تطبيقات Aspose.Cells Cloud واجهات برمجة قوية لدمج ملفات جداول البيانات المتعددة في ملف واحد بتنسيق مُحدّد. وتدعم هذه الواجهة العديد من التنسيقات، ومن أبرزها: **Excel** (XLS، XLSX)، و**CSV**، و**HTML**، و**PDF**، وغيرها. وباستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud، يمكنك بسهولة دمج ملفات جداول البيانات المتعددة في ملف واحد بتنسيق شائع، لتلبية مجموعة متنوعة من المتطلبات.

توجد العديد من الواجهات البرمجية المتاحة لدمج الملفات، وهي عادة ما تكون متوافقة مع مختلف البيئات عبر الإنترنت. وفيما يلي وصف تفصيلي لهذه الواجهات:

| الوظيفة | الوصف | مرجع الواجهة البرمجية |
| :------------------------- | :------------------------- | :------------------------- |
| **[MergeSpreadsheets](https://docs.aspose.cloud/cells/merge-spreadsheets/)** | دمج ملفات جداول البيانات المحلية في ملف بتنسيق محدّد. | [MergeSpreadsheets](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheets) |
| **[MergeRemoteSpreadsheet](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)** | دمج ملفات جداول البيانات الموجودة في مجلد مخزن سحابي في ملف بتنسيق محدّد. | [Merge Remote Spreadsheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeRemoteSpreadsheet) |
| **[Merge Spreadsheets In Remote Folder](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)** | دمج ملفات جداول البيانات الموجودة في مجلد مخزن سحابي في ملف بتنسيق محدّد. | [Merge Spreadsheets In Remote Folder](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheetsInRemoteFolder) |

# كيفية دمج ملفات متعددة في ملف واحد باستخدام Aspose.Cells Cloud

توفر واجهة برمجة تطبيقات Aspose.Cells Cloud [عدة SDKs](https://github.com/aspose-cells-cloud) تدعم لغات برمجة مختلفة. اختر الـ SDK المناسب للغة البرمجة التي تفضّلها، واتّبع الوثائق المرافقة لتثبيته وتهيئته. يمكنك أيضًا إنشاء SDK مخصّص وفقًا لمرجع [واجهة برمجة التطبيقات](https://reference.aspose.cloud/cells/). وفي هذا القسم، سنستخدم لغة C# كمثال لشرح تفصيلي لعملية دمج الملفات.

## التسجيل والحصول على مفتاح API

قبل البدء، يجب عليك [تسجيل حساب في Aspose Cloud](https://id.containerize.com/signup)، والحصول على [مفتاح API للتوثيق](https://dashboard.aspose.cloud/applications). وبتسجيل الدخول إلى الموقع الرسمي لـ Aspose Cloud، يمكنك إنشاء حساب مجاني والحصول على مفتاح API لأغراض المصادقة.

للمزيد من العمليات المتقدمة، يُرجى الرجوع إلى الوثائق التالية: [البدء السريع مع Cells Cloud](https://docs.aspose.cloud/cells/quickstart/)

## تثبيت وتهيئة SDK لـ Aspose.Cells Cloud

قم بتثبيت حزمة Aspose.Cells-Cloud NuGet ضمن مشروع .NET الخاص بك، ويمكنك استخدام Package Manager Console أو Package Manager في Visual Studio.  
إليك كيفية تثبيت الحزمة باستخدام Package Manager Console:

```Powershell

Install-Package Aspose.Cells-Cloud

```

قم بإنشاء مثيل جديد من فئة CellsApi، مع تهيئة المثيل باستخدام مُعرّف العميل (Client ID) ومُعرّف السر (Client Secret). وفيما يلي تفاصيل مقتطف الكود المذكور أعلاه:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

تأكد من استبدال YOUR_API_KEY وYOUR_APP_SID وYOUR_APP_KEY بمفتاح API الفعلي واسم التطبيق (Application SID) ومفتاح التطبيق (Application Key).

## بناء طلب الواجهة البرمجية واستدعائها

### استخدام الخدمات السحابية لدمج جداول البيانات المحلية وإنتاج الملفات المُدمجة إما كملفات محلية أو كتيّارات في الذاكرة (in-memory streams) بأي تنسيق مطلوب

```CSharp

using System.Collections.Generic;

var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));

// إنشاء طلب دمج جداول البيانات
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsRequest();
// تحديد الملفات المراد دمجها
IDictionary<string, System.IO.Stream> mapFiles = new Dictionary<string, System.IO.Stream>();
mapFiles.Add("Book1.xlsx", File.OpenRead("Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead("Book2.xlsx"));
request.Spreadsheet = mapFiles;
// تحديد تنسيق الإخراج
request.outFormat = "pdf";

cellsApi.MergeSpreadsheets(request, "MergedResultFile.pdf");

```

### دمج جداول البيانات المخزّنة في السحابة إلكترونيًا وإنتاج الملف المُدمج محليًا أو إعادة تخزينه في المخزن السحابي بأي تنسيق مطلوب

```C#
// احصل على مُعرّف العميل (Client ID) ومُعرّف السر (Client Secret) من https://dashboard.aspose.cloud (التسجيل مجاني).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// إعداد متغيّرات طلب الدمج
var request = new Aspose.Cells.Cloud.SDK.Request.MergeRemoteSpreadsheetRequest();
// تحديد الملف الرئيسي في السحابة
request.name = "Book1.xlsx";
request.folder = "RemoteFolder1";
// تحديد ملف الجدول المراد دمجه
request.mergedSpreadsheet = "RemoteFolder2/Book2.xlsx";
request.outFormat = "pdf";
cellsApi.MergeRemoteSpreadsheet(request, "MergedResultOutPutToLocalFile.pdf");
```

### دمج الملفات المتطابقة تلقائيًا من دليل في السحابة، وتصدير النتيجة المُدمجة بالتنسيق المحدّد، وإنتاجها محليًا أو إعادة تخزينها في السحابة

```csharp
// احصل على مُعرّف العميل (Client ID) ومُعرّف السر (Client Secret) من https://dashboard.aspose.cloud (التسجيل مجاني).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// إعداد متغيّرات طلب الدمج
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsInRemoteFolderRequest();
// تحديد الدليل المخزّن في السحابة الذي يحتوي على الملفات المراد دمجها
request.folder = "RemoteFolder";
request.fileMatchExpression = "*xlsx$";
request.outFormat = "pdf";
cellsApi.MergeSpreadsheetsInRemoteFolder(request, "MergedResultOutPutToLocalFile.pdf");
```

## حالات الاستخدام

ميزة دمج الملفات المتعددة في واجهة برمجة تطبيقات Aspose.Cells Cloud مفيدة في عدّة سيناريوهات عملية. ومن أبرز هذه الاستخدامات:

- **دمج ملفات Excel متعددة في ملف Excel واحد** لغرض تحليل البيانات وتخزينها.
- **دمج ملفات البيانات في ملف Excel واحد** لأغراض تحليل البيانات.
- **دمج ملفات الصور المتعددة في ملف PDF واحد** لسهولة المشاركة.
- **دمج ملفات متعددة في ملف HTML واحد** لعرضها أو تضمينها في صفحات الويب.

## الخلاصة

باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud، يمكنك بسهولة دمج ملفات جداول البيانات المتعددة في ملف واحد. ومن خلال إجراء مكالمات بسيطة لواجهة برمجة التطبيقات وتحديد خيارات دمج مناسبة، يمكنك تنفيذ متطلبات دمج الملفات بكفاءة عالية. ويمكنك دمج واجهة برمجة تطبيقات Aspose.Cells Cloud في تطبيقاتك لتعزيز الإنتاجية وتوفير وقت التطوير.

يرجى ملاحظة أن كود المثال أعلاه يُستخدم لأغراض توضيحية فقط، وسيتوجب عليك استبداله ببيانات اعتماد مصادقة صحيحة ومسارات ملفات فعّالة عند الاستخدام الفعلي. بالإضافة إلى ذلك، توفر واجهة برمجة تطبيقات Aspose.Cells Cloud العديد من الميزات الأخرى مثل إنشاء جداول البيانات وتعديلها ومعالجتها وتحليل البيانات. ويمكنك الاطّلاع على وثائق الواجهة البرمجية التفصيلية وأمثلة الكود في [دليل المطوّر على الموقع الرسمي لـ Aspose](/developer-guide/).

نتمنى أن تساعدك هذه المقالة على فهم كيفية استخدام واجهة برمجة تطبيقات Aspose.Cells Cloud لدمج الملفات. نتمنى لك التوفيق في تنفيذك!