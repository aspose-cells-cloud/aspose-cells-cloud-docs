---
title: "تعيين قيمة الخلية – مرجع واجهة برمجة تطبيقات Aspose.Cells Cloud (الإصدار 3.0)"  
type: docs  
url: /ar/set-value-of-a-cell-in-a-worksheet/
weight: 70  
keywords: "واجهة برمجة تطبيقات Aspose Cells تعيين قيمة الخلية، تحديث خلية إكسل عبر REST، مثال cURL لـ Aspose.Cells Cloud"  
description: "تعرّف على كيفية تعيين قيمة خلية معيّنة في ورقة عمل إكسل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. يتضمن بنية الطلب، المعاملات، مثال cURL عبر HTTPS، وأمثلة لرموز SDK."  
---  

تقوم هذه الواجهة البرمجية لواجهة برمجة التطبيقات (REST API) بتعيين **قيمة الخلية** في ملف إكسل.

## واجهة برمجة التطبيقات (REST API)  

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```  

## الأمان والمصادقة

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب [مصادقة تعتمد على رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

**معاملات الطلب**

| الاسم           | النوع   | الموقع | الوصف                                              |
|----------------|---------|--------|----------------------------------------------------|
| name           | نص (string) | مسار (path) | اسم مستند إكسل (مع امتداد الملف).                 |
| sheetName      | نص (string) | مسار (path) | اسم ورقة العمل (مع مراعاة حالة الأحرف).           |
| cellName       | نص (string) | مسار (path) | عنوان الخلية المستهدفة بنظام A1 (مثل `A1`).      |
| value          | نص (string) | استعلام (query) | القيمة المراد تعيينها في الخلية.                   |
| type           | نص (string) | استعلام (query) | نوع البيانات للقيمة (`int`، `string`، `float`، إلخ). |
| formula        | نص (string) | استعلام (query) | الصيغة المراد تطبيقها على الخلية (اختيارية).       |
| folder         | نص (string) | استعلام (query) | المجلد الذي يحتوي على المستند (اختياري).          |
| storageName    | نص (string) | استعلام (query) | اسم وحدة التخزين التي يوجد فيها الملف (اختياري).   |

## **الاستجابة**

ترجع كائن `CellResponse`.

- **نظرة عامة على حقول الاستجابة**

| الحقل             | النوع    | الوصف                                                 |
| ------------------ | -------- | ------------------------------------------------------ |
| `Name`            | نص (string) | عنوان الخلية (مثل `F341`).                             |
| `Row`             | عدد صحيح (integer) | فهرس الصف (بدءًا من الصفر).                             |
| `Column`          | عدد صحيح (integer) | فهرس العمود (بدءًا من الصفر).                           |
| `Value`           | نص (string) | القيمة المعروضة في الخلية.                             |
| `Type`            | نص (string) | نوع بيانات الخلية (مثل `IsString`).                   |
| `Formula`         | نص (string) | نص الصيغة إذا كانت الخلية تحتوي على صيغة.              |
| `IsFormula`       | منطقي (bool) | يشير إلى ما إذا كانت الخلية تحتوي على صيغة.            |
| `IsMerged`        | منطقي (bool) | يشير إلى ما إذا كانت الخلية جزءًا من نطاق مدمج.        |
| `IsArrayHeader`   | منطقي (bool) | يشير إلى ما إذا كانت الخلية رأس مصفوفة.               |
| `IsInArray`       | منطقي (bool) | يشير إلى ما إذا كانت الخلية تابعة لمصفوفة.            |
| `IsErrorValue`    | منطقي (bool) | يشير إلى ما إذا كانت الخلية تحتوي على قيمة خطأ.        |
| `IsInTable`       | منطقي (bool) | يشير إلى ما إذا كانت الخلية داخل جدول.                |
| `IsStyleSet`      | منطقي (bool) | يشير إلى ما إذا تم تطبيق نمط على الخلية.              |
| `HtmlString`      | نص (string) | تمثيل القيمة بالخلية بصيغة مشفرة بـ HTML.             |
| `Style/link`      | كائن (object) | رابط تشعبي لموارد النمط.                              |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

**رموز حالة HTTP**

| الرمز | المعنى                      | الوصف                                               |
|------|----------------------------|-----------------------------------------------------|
| 200  | ناجح (OK)                  | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح (Bad Request) | معاملات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401  | غير مُصادَق (Unauthorized)  | رمز JWT غير صالح أو مفقود.                         |
| 413  | حجم البيانات كبير جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح به.           |
| 500  | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                           |

## كيفية استخدام واجهة PostWorksheetCellSetValue API مع مكتبات SDK

### مواصفات واجهة PostWorksheetCellSetValue API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue) واجهة برمجة تطبيقات قابلة للوصول العام، ما يمكّن المطورين من استدعاء نقاط نهاية REST مباشرةً من المتصفح أو أي عميل HTTP.

يمكنك استخدام أداة **cURL** سطر الأوامر لاستدعاء خدمات Aspose.Cells. يوضح المثال التالي كيفية تعيين قيمة خلية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?value=1234&type=int" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Cell":{
    "Name":"A3",
    "Row": 2,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام مكتبة SDK يُسرّع عملية التطوير من خلال التعامل مع التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مشروعك. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الرموز التالية كيفية استدعاء خدمات Aspose.Cells باستخدام مكتبات SDK المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellSetValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellSetValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellSetValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellSetValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellSetValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellSetValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellSetValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellSetValue.go" >}}

{{< /tab >}}

{{< /tabs >}}