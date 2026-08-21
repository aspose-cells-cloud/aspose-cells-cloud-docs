---
title: "كيفية تحويل تنسيقات ملفات جداول البيانات باستخدام Aspose.Cells Cloud"
linktitle: "كيفية تحويل تنسيقات ملفات جداول البيانات"
type: docs
url: /ar/how-to-convert-file-formats
description: "كيفية تحويل تنسيقات الملفات باستخدام Aspose.Cells Cloud."
weight: 10
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, كيفية تحويل تنسيقات الملفات عبر Aspose.Cells Cloud
---

## المقدمة

تقدم واجهة برمجة تطبيقات جداول بيانات Aspose.Cells Cloud مجموعة من الواجهات ذات القناتَين للتحويل، سواء كانت ملفات جداول البيانات محلية أو موجودة في السحابة. وتدعم التنسيقات مثل Excel (XLS و XLSX) وCSV وHTML وPDF، مما يسهّل عملية التحويل لتلبية مختلف الاحتياجات.

### ثلاثة أوضاع للتحويل · نموذج كائن موحّد · تغطية كاملة للتنسيقات

![أوضاع التحويل](image.png)

## **مصفوفة التحويل الأساسية**

| نوع التحويل            | مستوى الكائن        | واجهة برمجة التطبيق النموذجية   | تنسيقات الإخراج               |
|------------------------|--------------------|----------------------------------|-------------------------------|
| **التحويل المحلي**     | Workbook (كتاب عمل) | `ConvertSpreadsheet`             | PDF/XLSX/JSON/.... +30 تنسيق |
|                        | Worksheet (ورقة عمل) | `ConvertWorksheetToImage`       | PNG/JPEG/SVG                  |
|                        |                    | `ConvertWorksheetToPdf`         | PDF                           |
|                        | Table (جدول)       | `ConvertTableToImage`           | PNG/JPEG/SVG/....             |
|                        |                    | `ConvertTableToPdf`             | PDF                           |
|                        |                    | `ConvertTableToCsv`             | CSV                           |
|                        |                    | `ConvertTableToHtml`            | HTML                          |
|                        |                    | `ConvertTableToJson`            | JSON                          |
|                        | Range (نطاق)       | `ConvertRangeToImage`           | PNG/JPEG/SVG/....             |
|                        |                    | `ConvertRangeToPdf`             | PDF                           |
|                        |                    | `ConvertRangeToCsv`             | CSV                           |
|                        |                    | `ConvertRangeToHtml`            | HTML                          |
|                        |                    | `ConvertRangeToJson`            | JSON                          |
|                        | Chart (رسم بياني)  | `ConvertChartToImage`           | PNG/JPEG/SVG/....             |
|                        |                    | `ConvertChartToPdf`             | PDF                           |
| **التحويل السحابي**    | Workbook (كتاب عمل) | `ExportSpreadsheetAsFormat`     | PDF/XLSX/JSON/.... +30 تنسيق |
|                        | Worksheet (ورقة عمل) | `ExportWorksheetAsFormat`       | PDF/XLSX/JSON/.... +30 تنسيق |
|                        | Table (جدول)       | `ExportTableAsFormat`           | PDF/XLSX/JSON/.... +30 تنسيق |
|                        | Range (نطاق)       | `ExportRangeAsFormat`           | PDF/XLSX/JSON/.... +30 تنسيق |
|                        | Chart (رسم بياني)  | `ExportChartAsFormat`           | PDF/XLSX/JSON/.... +30 تنسيق |
| **الحفظ في السحابة**   | Workbook (كتاب عمل) | `SaveSpreadsheetAs`             | PDF/XLSX/JSON/.... +30 تنسيق |

### **التحويل المحلي للملفات**

```csharp
// الحصول على عميل واجهة برمجة تطبيقات Aspose.Cells Cloud
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **تحويل ملف Excel**

```c#
// تحويل ملف Excel المحلي إلى PDF
cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

- **تحويل رسم بياني في Excel إلى ملف SVG**

```c#
// تحويل الرسم البياني في Excel المحلي إلى تنسيق SVG
cellsApi.ConvertChartToImage(new SDK.Request.ConvertChartToImageRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    chartIndex = 0,
    format = "svg"
}, "EmployeeSalesSummary.svg");

```

- **تحويل جدول إلى ملف CSV**

```C#
# تحويل جدول سجلات المبيعات في ورقة العمل "Sales" إلى تنسيق CSV
result = api.ConvertTableToCsv( new SDK.Request.ConvertTableToCsvRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    tableName = "SaleLogs",
    format = "csv"
}, "EmployeeSalesLog.csv");

```

### **التحويل السحابي للملفات**

يجب أيضًا الحصول على عميل واجهة برمجة تطبيقات Aspose.Cells Cloud.

```csharp
// الحصول على عميل واجهة برمجة تطبيقات Aspose.Cells Cloud
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **تحويل Excel إلى PDF**

```csharp
// تحويل ملف Excel الموجود في السحابة إلى PDF وحفظه محليًا
cellsApi.ExportSpreadsheetAsFormat( new SDK.Request.ExportSpreadsheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx" ,
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary.pdf");   
```

- **تحويل ورقة عمل في Excel إلى PDF**

```csharp
// تحويل ورقة عمل في Excel الموجودة في السحابة إلى PDF وحفظها محليًا
cellsApi.ExportWorksheetAsFormat (new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary_Sales.pdf");   
```

```csharp
// تحويل ورقة عمل في Excel الموجودة في السحابة إلى PDF وحفظها محليًا
cellsApi.ExportWorksheetAsFormat (new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary_Sales.pdf");   
```

## تثبيت وتهيئة SDK لـ Aspose.Cells Cloud

قم بتثبيت حزمة Aspose.Cells-Cloud NuGet في مشروع .NET الخاص بك، يمكنك استخدام وحدة تحكم مدير الحزم NuGet أو مدير حزم NuGet في Visual Studio.  
إليك كيفية تثبيت الحزمة باستخدام وحدة تحكم مدير الحزم:

```powershell

Install-Package Aspose.Cells-Cloud

```

قم بإنشاء مثيل جديد من فئة CellsApi، وقم بتهيئته باستخدام معرّف العميل وسر العميل. فيما يلي تفاصيل مقتطف الكود المذكور أعلاه:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

تأكد من استبدال YOUR_API_KEY وYOUR_APP_SID وYOUR_APP_KEY بمفتاح API الفعلي وSID للتطبيق ومفتاح التطبيق الفعليين.

## **حالات استخدام تحويل تنسيقات الملفات**  

تقدم واجهة برمجة تطبيقات Aspose.Cells Cloud قدرات **تحويل جداول البيانات** على مستوى المؤسسات لسيناريوهات الأعمال الحرجة:  

1. **Excel → PDF**  
   إنشاء تقارير جاهزة للطباعة مع الحفاظ على التنسيق  
2. **جداول البيانات → HTML**  
   تضمين جداول تفاعلية في تطبيقات الويب  
3. **CSV → Excel (XLSX)**  
   تحويل البيانات الخام إلى كتب عمل قابلة للتحليل  
4. **ترميز تنسيقات مخصصة**  
   التحويل بين أكثر من 20 تنسيق (XLS و XLSB و ODS و FODS و TSV)  
![التحويل من تنسيقات الإدخال إلى تنسيقات الإخراج](image-1.png)

## **الخاتمة: تبسيط عمليات التحويل باستخدام استدعاء واحد لواجهة برمجة التطبيق**  

---