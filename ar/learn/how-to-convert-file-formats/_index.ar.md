---
title: كيفية تحويل تنسيقات ملفات جداول البيانات باستخدام Aspose.Cells Clou
linktitle: كيفية تحويل تنسيق ملف جدول البيانات
type: docs
url: /ar/how-to-convert-file-formats
description: كيفية تحويل تنسيقات الملفات باستخدام Aspose.Cells Cloud
weight: 10
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، كيفية تحويل تنسيقات الملفات من خلال Aspose.Cells السحابة
---
## مقدمة

يوفر جدول بيانات السحابة Aspose.Cells مجموعة من الواجهات ثنائية القناة لتحويل ملفات جداول البيانات المحلية والسحابية. يدعم تنسيقات مثل Excel (XLS، XLSX)، وCSV، وHTML، وPDF، مما يجعل التحويل سهلاً لتلبية مختلف الاحتياجات.

### ثلاثة أوضاع تحويل · نموذج كائن موحد · تغطية تنسيق كاملة

![أوضاع التحويل](image.png)

## **مصفوفة التحويل الأساسية**

| نوع التحويل| مستوى الكائن| نموذجي API| تنسيقات الإخراج|
|-----------------|-------------|---------------------------|--------------------------|
|**التحويل المحلي**  | كتاب العمل|`ConvertSpreadsheet`            | PDF/XLSX/JSON/.... أكثر من 30 تنسيقًا|
|| ورقة عمل|`ConvertWorksheetToImage`       |PNG/JPEG/SVG                   |
|||`ConvertWorksheetToPdf`         | ملف بي دي إف|
|| طاولة|`ConvertTableToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertTableToPdf`             | ملف بي دي إف|
|||`ConvertTableToCsv`             | ملف CSV|
|||`ConvertTableToHtml`            | HTML|
|||`ConvertTableToJson`            | HTML|
|| يتراوح|`ConvertRangeToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertRangeToPdf`             | ملف بي دي إف|
|||`ConvertRangeToCsv`             | ملف CSV|
|||`ConvertRangeToHtml`            | HTML|
|||`ConvertRangeToJson`            | JSON|
|| جدول|`ConvertChartToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertChartToPdf`             |PDF                            |
|**تحويل السحابة**  | كتاب العمل|`ExportSpreadsheetAsFormat`     | PDF/XLSX/JSON/.... أكثر من 30 تنسيقًا|
|| ورقة عمل|`ExportWorksheetAsFormat`       | PDF/XLSX/JSON/.... أكثر من 30 تنسيقًا|
|| طاولة|`ExportTableAsFormat`           | PDF/XLSX/JSON/.... أكثر من 30 تنسيقًا|
|| يتراوح|`ExportRangeAsFormat`           | PDF/XLSX/JSON/.... أكثر من 30 تنسيقًا|
|| جدول|`ExportChartAsFormat`           | PDF/XLSX/JSON/.... أكثر من 30 تنسيقًا|
|**حفظ باسم السحابة**     | كتاب العمل|`SaveSpreadsheetAs`             | PDF/XLSX/JSON/.... أكثر من 30 تنسيقًا|

### **تحويل الملفات المحلية**

```csharp
// Get Cells Cloud API client
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Excel تحويل الملفات**

```c#
// Convert local Excel to PDF
cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

- **تحويل مخطط Excel إلى ملف SVG**

```c#
// Convert local Excel Chart to Svg
cellsApi.ConvertChartToImage(new SDK.Request.ConvertChartToImageRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    chartIndex = 0,
    format = "svg"
}, "EmployeeSalesSummary.svg");

```

- **تحويل الجدول إلى ملف CSV**

```C#
# Convert the sale logs table of the Sales worksheet to csv
result = api.ConvertTableToCsv( new SDK.Request.ConvertTableToCsvRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    tableName = "SaleLogs",
    format = "csv"
}, "EmployeeSalesLog.csv");

```

### **تحويل الملفات السحابية**

يجب أيضًا الحصول على العميل Aspose Cells Cloud API.

```csharp
// Get Cells Cloud API client
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **تحويل Excel إلى PDF**

```csharp
// Convert cloud Excel to PDF, Save to local file
cellsApi.ExportSpreadsheetAsFormat( new SDK.Request.ExportSpreadsheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx" ,
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary.pdf");   
```

- **تحويل ورقة العمل Excel إلى pdf**

```csharp
// Convert cloud Excel worksheet to PDF, Save to local file
cellsApi.ExportWorksheetAsFormat (new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary_Sales.pdf");   
```

```csharp
// Convert cloud Excel worksheet to PDF, Save to local file
cellsApi.ExportWorksheetAsFormat (new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary_Sales.pdf");   
```

## تثبيت وتكوين SDK السحابي Aspose.Cells

قم بتثبيت الحزمة Aspose.Cells-Cloud NuGet في مشروعك .NET، ويمكنك استخدام وحدة التحكم Package Manager NuGet أو Package Manager NuGet في Visual Studio.
إليك كيفية تثبيت الحزمة باستخدام وحدة التحكم في إدارة الحزم:

```powershell

Install-Package Aspose.Cells-Cloud

```

يُنشئ مثيلًا جديدًا لفئة CellsApi، مع تهيئة مُعرّف العميل وسرّه. فيما يلي تفاصيل مقتطف الكود المذكور أعلاه:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

تأكد من استبدال الخاص بك_API_مفتاحك_برنامج_SID ومعرفك_برنامج_المفتاح مع المفتاح الفعلي API ومعرف تطبيق SID ومفتاح التطبيق.

## **حالات استخدام تحويل تنسيق الملف**

 Aspose Cells Cloud API توفر خدمات على مستوى المؤسسة**تحويل جدول البيانات** القدرات اللازمة لسيناريوهات الأعمال الحرجة:

1. **Excel → PDF**  
 إنشاء تقارير جاهزة للطباعة مع التنسيق المحفوظ
2. **جداول البيانات → HTML**  
 تضمين الجداول التفاعلية في تطبيقات الويب
3. **CSV → Excel (XLSX)**  
 تحويل البيانات الخام إلى مصنفات قابلة للتحليل
4. **تحويل التنسيق المخصص**  
 التحويل بين أكثر من 20 تنسيقًا (XLS، XLSB، ODS، FODS، TSV)
![التحويل من تنسيقات الإدخال إلى تنسيقات الإخراج](image-1.png)

## **الاستنتاج: تبسيط التحويلات بمكالمة واحدة على الرقم API**
