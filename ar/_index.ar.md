---
title: "واجهة برمجة تطبيقات Aspose.Cells السحابية – تحويل ودمج وتقسيم وحماية ملفات Excel"
second_title: "وثيقة"
ArticleTitle: "واجهة برمجة تطبيقات Aspose.Cells السحابية – تحويل ودمج وتقسيم وحماية ملفات Excel"
linktitle: "مركز المطورين"
type: docs
url: /
description: "تفتح واجهة برمجة تطبيقات Aspose.Cells Cloud REST إمكانات تحويل ودمج وتقسيم وحماية ملفات جداول البيانات Excel ومعالجتها بشكل شامل. تشمل الخطة المجانية 150 استدعاءً شهريًا، مع توفر حزم SDK لـ 8 لغات برمجية."
weight: 10
keywords: "Aspose.Cells Cloud، Excel API، تحويل جدول البيانات، دمج ملفات Excel، تقسيم ملفات Excel، حماية ملفات Excel، حزمة SDK لجداول البيانات السحابية، واجهة REST API، معالجة Excel"
---

## ما هي واجهات برمجة تطبيقات Aspose.Cells Cloud؟

واجهة برمجة تطبيقات Aspose.Cells Cloud هي مجموعة من خدمات جداول البيانات/Excel القائمة على الحوسبة السحابية. لا يتطلب الأمر تثبيت Microsoft Office أو إعدادات خادم — ما عليك سوى إرسال طلب HTTP، وستتمكن من إنشاء وتعديل وتحويل جداول البيانات، وتنظيف البيانات، وإنشاء المخططات، وبناء الجداول المحورية، والتشفير، والتقسيم، والدمج، وإضافة العلامات المائية، وتطبيق التوقيعات الرقمية، وأكثر من ذلك، من أي لغة برمجة.

## لماذا استخدام واجهات برمجة تطبيقات Aspose.Cells Cloud؟

- إنشاء وتعديل وتحويل وتحليل جداول البيانات المخزنة في مساحة تخزين سحابية باستخدام خدمات واجهة ويب Aspose.Cells Cloud.  
- إنشاء وتعديل وتحويل وتحليل ملفات جداول البيانات المحلية باستخدام خدمات واجهة ويب Aspose.Cells Cloud.  
- تدعم واجهة برمجة التطبيقات 30 تنسيقًا للملفات، منها **xlsx** و **csv** و **ods** و **xlsb**، إلخ.  
- يمكنك التعامل مع جداول البيانات مباشرة عبر واجهة ويب Aspose.Cells Cloud دون الحاجة إلى تثبيت Microsoft Excel.  
- تشمل الخطة المجانية ما يصل إلى 150 استدعاءً لواجهة برمجة التطبيقات شهريًا.  
- تُطبّق نموذج الدفع حسب الاستخدام.  
- **الكود القصير**: عمليات يمكن تنفيذها في جملة واحدة.  
  - **تحويل XLSX إلى PDF** → ConvertSpreadsheetToPdf  
  - **حذف المسافات الزائدة في الملف بالكامل** → TrimSpreadsheetContent  
  - **دمج أكثر من 10 ملفات في تقرير واحد** → MergeSpreadsheets  

## **كيفية استخدام واجهات برمجة تطبيقات Aspose.Cells Cloud؟**

### الخطوة 1: **الحصول على بيانات اعتماد واجهة برمجة التطبيقات**  

- **[تسجيل حساب Aspose Cloud](https://dashboard.aspose.cloud/signup)**  
- **[الحصول على بيانات اعتماد العميل](https://dashboard.aspose.cloud/#/applications)**  

### الخطوة 2: **استدعاء واجهات ويب جداول البيانات باستخدام حزمة SDK (موصى بها)**  

يوصى باستخدام حزمة SDK الرسمية لتبسيط عملية المصادقة وإدارة الطلبات. تُحصل حزمة SDK تلقائيًا على رموز الوصول وتُجَدِّدها عند الحاجة.

#### **[تثبيت حزمة SDK لـ .NET (NuGet)](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab)**

```powershell
dotnet add package Aspose.Cells-Cloud --version 26.6.0
```

#### مثال: **تحويل ملف Excel إلى PDF باستخدام حزمة SDK**

```csharp
CellsApi cellsApi = new CellsApi(
    Environment.GetEnvironmentVariable("ProductClientId"),
    Environment.GetEnvironmentVariable("ProductClientSecret"));
cellsApi.ConvertSpreadsheet(
    new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" },
    "EmployeeSalesSummary.pdf");
```

#### الشرح

- **Spreadsheet**: اسم ملف Excel الموجود في التخزين المحلي.  
- **Format**: التنسيق المستهدف (مثل: pdf أو png أو csv أو json).  
- **Output file**: سيتم حفظ الملف الناتج محليًا باسم محدد.  

## **الوظائف الأساسية**

تقدم Aspose.Cells Cloud الميزات الرئيسية التالية لتلبية احتياجات أتمتة جداول البيانات على مستوى المؤسسات:

### **تحويل جدول البيانات**

- **[تحويل جدول البيانات إلى ملف PDF](https://docs.aspose.cloud/cells/convert-excel-file-to-pdf-file/)**  
- **[تحويل مخطط جدول البيانات إلى صورة](https://docs.aspose.cloud/cells/convert-chart-to-image/)**  
- **[حفظ جدول البيانات بتنسيق آخر](https://docs.aspose.cloud/cells/save-an-excel-file-as-other-formats-files/)**  

### **معالجة البيانات**

- **[دمج جداول البيانات](https://docs.aspose.cloud/cells/merge-spreadsheets/)**  
- **[تقسيم جداول البيانات](https://docs.aspose.cloud/cells/split-spreadsheet/)**  
- **[حذف الصفوف الفارغة من جدول البيانات](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-rows/)**  
- **[حذف الأعمدة الفارغة من جدول البيانات](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-columns/)**  
- **[استبدال محتوى جدول البيانات](https://docs.aspose.cloud/cells/replace-spreadsheet-content/)**  

> **ملاحظة:** تتوافر مخططات الطلبات والاستجابات التفصيلية، وطرق HTTP، ومعلمات الاستعلام، واستجابات العينات لكل نقطة نهاية في **مرجع واجهة برمجة تطبيقات ويب جداول بيانات Aspose.Cells Cloud** المرتبطة أدناه.

**مرجع سريع لنقاط النهاية**

| العملية | طريقة HTTP | المسار | المعلمات المطلوبة | استجابة عينية |
|---------|-------------|--------|--------------------|----------------|
| تحويل جدول البيانات | POST | `/cells/convert` | `Spreadsheet` (ملف)، `format` (نص) | ملف ثنائي (مثل: PDF) |
| دمج جداول البيانات | POST | `/cells/worksheets/merge` | `files` (قائمة ملفات) | ملف عمل مدمج |
| تقسيم جدول البيانات | POST | `/cells/worksheets/split` | `Spreadsheet` (ملف)، `format` (نص) | أرشيف الملفات المُقسَّمة |
| حذف الصفوف الفارغة | POST | `/cells/worksheets/blankrows/delete` | `Spreadsheet` (ملف) | ملف عمل محدّث |
| استبدال المحتوى | POST | `/cells/replace` | `Spreadsheet` (ملف)، `oldValue`، `newValue` | ملف عمل محدّث |

## حزم SDK المدعومة (**الحزم المتاحة**)

- توفر Aspose.Cells Cloud [حزم SDK](https://github.com/aspose-cells-cloud) جاهزة فورًا لأي لغة برمجة رئيسية — اسحب الكود وطبّقه وأطلقه:

| اللغة | طريقة التثبيت | مستودع GitHub |
|------|----------|-------------|
| [Java](https://www.oracle.com/java/) | [Maven](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Aspose.Cells.Cloud.pom.xml) | [مستودع حزمة SDK لـ Java على GitHub](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java) |
| [.NET](https://dotnet.microsoft.com/) | [NuGet](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab) | [مستودع حزمة SDK لـ .NET على GitHub](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet) |
| [Python](https://www.python.org/) | [pip](https://pypi.org/project/asposecellscloud/) | [مستودع حزمة SDK لـ Python على GitHub](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python) |
| [Node.js](https://nodejs.org/en) | [npm](https://www.npmjs.com/package/asposecellscloud) | [مستودع حزمة SDK لـ Node.js على GitHub](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node) |
| [PHP](https://www.php.net/) | [Composer](https://packagist.org/packages/aspose/cells-sdk-php) | [مستودع حزمة SDK لـ PHP على GitHub](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php) |
| [GoLang](https://go.dev/) | [Go Modules](https://pkg.go.dev/github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25) | [مستودع حزمة SDK لـ GoLang على GitHub](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go) |
| [Ruby](https://www.ruby-lang.org/) | [RubyGems](https://rubygems.org/gems/aspose_cells_cloud) | [مستودع حزمة SDK لـ Ruby على GitHub](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby) |
| [Perl](https://www.perl.org/) | [CPAN](https://metacpan.org/dist/AsposeCellsCloud-CellsApi) | [مستودع حزمة SDK لـ Perl على GitHub](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl) |
| **نقطة نهاية API** | [مرجع واجهة برمجة تطبيقات ويب جداول بيانات Aspose.Cells Cloud](https://reference.aspose.cloud/cells/) |  |

## **أمثلة على الكود ومشاريع مفتوحة المصدر**

تتميز جميع حزم SDK بأنها مفتوحة المصدر وتضم أمثلة غنية:

- [أمثلة حزمة SDK لـ Java على GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/tree/master/Examples)  
- [أمثلة حزمة SDK لـ .NET على GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/tree/master/examples)  
- [أمثلة حزمة SDK لـ Python على GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/tree/master/examples)  
- [أمثلة حزمة SDK لـ Node.js على GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/tree/master/Examples)  
- [أمثلة حزمة SDK لـ PHP على GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/tree/master/examples)  
- [أمثلة حزمة SDK لـ Go على GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/tree/master/examples)  
- [أمثلة حزمة SDK لـ Ruby على GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/tree/master/examples)  
- [أمثلة حزمة SDK لـ Perl على GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/tree/master/examples)  
---