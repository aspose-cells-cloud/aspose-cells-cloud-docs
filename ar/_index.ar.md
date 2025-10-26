---
title: "Aspose.Cells Cloud Web: التخزين السحابي، وتحويل جداول البيانات، والدمج، والتقسيم، والحماية، ومعالجة البيانات، والمزيد"
second_title: Documen
ArticleTitle: "Aspose.Cells Cloud Web: Cloud storage, Spreadsheet conversion, merged, splitting, protecting, data processing, and mor"
linktitle: مركز المطورين
type: docs
url: /ar/
description: تدعم واجهات برمجة تطبيقات الويب السحابية Aspose.Cells Spreadsheet/Excel لإنشاء وتحويل ودمج وتقسيم وحماية وتنفيذ عمليات الكائنات الداخلية، من بين وظائف أخرى. توفر Aspose.Cells Cloud مستندًا كاملاً، وتدعم واجهات RESTful، وأمثلة التعليمات البرمجية لمساعدة المطورين على التكامل بسرعة
weight: 10
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، Aspose.Cells مستند السحابة
---
## ما هي واجهات برمجة التطبيقات السحابية Aspose.Cells؟

Aspose.Cells Cloud APIs عبارة عن مجموعة من خدمات Spreadsheet/Excel السحابية - لا حاجة لتثبيت Office، ولا حاجة لتكوين الخوادم، فقط أرسل طلب HTTP، ويمكنك إجراء جميع العمليات الشائعة مثل الإنشاء والتحرير وتحويل التنسيق وتنظيف البيانات والرسوم البيانية وجداول البيانات المحورية والتشفير والتقسيم والدمج والعلامات المائية والتوقيعات الرقمية وما إلى ذلك، في أي مكان وبأي لغة.

## لماذا تستخدم واجهات برمجة التطبيقات السحابية Aspose.Cells؟

- إنشاء جداول البيانات وتحريرها وتحويلها وتحليلها في التخزين السحابي استنادًا إلى خدمات Aspose.Cells Cloud Web API.
- إنشاء ملفات جداول البيانات المحلية وتحريرها وتحويلها وتحليلها استنادًا إلى خدمات Aspose.Cells Cloud Web API.
- تنسيقات الملفات المدعومة هي 30، مثل xlsx، csv، ods، xlsb، وما إلى ذلك.
- قم بتشغيل جداول البيانات مباشرةً من خلال Aspose.Cells Cloud Web API دون الحاجة إلى التبعيات Microsoft Excel.
- 150 مكالمة مجانية API شهريًا.
- الشحن على مراحل، كم يستخدم المستخدمون، وكم يتقاضون، وكلما زاد استخدامهم، زادت الخصومات التي يقدمونها.
- **الرمز المختصر**:الأشياء التي يمكن القيام بها في جملة واحدة.
  - **تحويل XLSX إلى PDF** → تحويل جدول البيانات إلى PDF
  - **حذف المسافات الزائدة في الملف بأكمله** → تقليم محتوى جدول البيانات
  - **دمج أكثر من 10 ملفات في تقرير واحد** → دمج جداول البيانات

## **كيفية استخدام واجهات برمجة التطبيقات السحابية Aspose.Cells؟**

###  الخطوة 1:**احصل على بيانات اعتماد API**

- **[تسجيل حساب سحابي Aspose](https://dashboard.aspose.cloud/signup)**
- **[الحصول على بيانات اعتماد العميل](https://dashboard.aspose.cloud/#/applications)**

###  الخطوة 2:**استدعاء واجهات برمجة تطبيقات الويب الخاصة بجداول البيانات باستخدام مجموعة أدوات تطوير البرامج (موصى بها)**

من المستحسن استخدام SDK الرسمي لتبسيط عملية المصادقة والطلب.

#### **[تثبيت SDK (باستخدام .NET كمثال)](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab)**

```powershell

dotnet add package Aspose.Cells-Cloud --version 25.8.0

```

####  مثال:**تحويل Excel إلى PDF باستخدام SDK**

```C#
    CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
    cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

#### وصف

- **جدول بيانات**:اسم الملف Excel الذي يجب أن يكون في وحدة التخزين المحلية.
- **شكل**:تنسيق الهدف. على سبيل المثال pdf، png، csv، json، إلخ.
- **ملف الإخراج** سيتم حفظه في الموقع المحلي. "EmployeeSalesSummary.pdf" هو اسم ملف الإخراج.

## **الوظائف الأساسية**

توفر Aspose.Cells Cloud الميزات الرئيسية التالية لتلبية احتياجات أتمتة جداول البيانات على مستوى المؤسسة:

### **تحويل جدول البيانات**

- **[تحويل جدول بيانات إلى ملف PDF](https://docs.aspose.cloud/cells/convert-excel-file-to-pdf-file/)**
- **[تحويل مخطط جدول بيانات إلى صورة](https://docs.aspose.cloud/cells/convert-chart-to-image/)**
- **[حفظ جدول البيانات باسم](https://docs.aspose.cloud/cells/save-an-excel-file-as-other-formats-files/)**

### **معالجة البيانات**

- **[دمج جداول البيانات](https://docs.aspose.cloud/cells/merge-spreadsheets/)**
- **[تقسيم جداول البيانات](https://docs.aspose.cloud/cells/split-spreadsheet/)**
- **[حذف الصفوف الفارغة في جدول البيانات](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-rows/)**
- **[حذف الأعمدة الفارغة في جدول البيانات](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-columns/)**
- **[استبدال محتوى جدول البيانات](https://docs.aspose.cloud/cells/replace-spreadsheet-content/)**

## دعم SDKs(**مجموعات تطوير البرامج المتاحة**)

-  Aspose.Cells عروض السحابة[مجموعات تطوير البرامج (SDKs)](https://github.com/aspose-cells-cloud)**متوفر بعدة لغات وجاهز للاستخدام:

| لغة| طريقة التثبيت| مستودع GitHub|
||----|-------|
|[Java](https://www.oracle.com/java/) |[Maven](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Aspose.Cells.Cloud.pom.xml) |[Java SDK مستودع GitHub](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java) |
|[.NET](https://dotnet.microsoft.com/) |[NuGet](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab) |[.NET SDK مستودع GitHub](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet) |
|[Python](https://www.python.org/) |[نقطة](https://pypi.org/project/asposecellscloud/) |[Python SDK مستودع GitHub](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python) |
|[نود.جي اس](https://nodejs.org/en) |[npm](https://www.npmjs.com/package/asposecellscloud) |[مستودع GitHub لـ Node.js SDK](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node) |
|[PHP](https://www.php.net/) |[ملحن](https://packagist.org/packages/aspose/cells-sdk-php) |[PHP SDK مستودع GitHub](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php) |
|[جولانج](https://go.dev/) |[وحدات Go](https://pkg.go.dev/github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25) |[مستودع GoLang SDK على GitHub](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go) |
|[روبي](https://www.ruby-lang.org/) |[روبي جيمز](https://rubygems.org/gems/aspose_cells_cloud) |[مستودع Ruby SDK على GitHub](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby) |
|[Perl](https://www.perl.org/) |[شبكة سي بي ايه ان](https://metacpan.org/dist/AsposeCellsCloud-CellsApi) |[Perl SDK مستودع GitHub](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl) |

- **API نقطة النهاية**: [Aspose.Cells Cloud Spreadsheet Web API مرجع](https://reference.aspose.cloud/cells/)

## **أمثلة على التعليمات البرمجية والمشاريع مفتوحة المصدر**

جميع حزم SDK مفتوحة المصدر وتتضمن أمثلة غنية:

- [Java أمثلة SDK على Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/tree/master/Examples)
- [.NET أمثلة SDK على Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/tree/master/examples)
- [Python أمثلة SDK على Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/tree/master/examples)
- [أمثلة SDK لـ Node.js على Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/tree/master/Examples)
- [PHP أمثلة SDK على Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/tree/master/examples)
- [أمثلة Go SDK على Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/tree/master/examples)
- [أمثلة SDK Ruby على Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/tree/master/examples)
- [Perl أمثلة SDK على Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/tree/master/examples)
