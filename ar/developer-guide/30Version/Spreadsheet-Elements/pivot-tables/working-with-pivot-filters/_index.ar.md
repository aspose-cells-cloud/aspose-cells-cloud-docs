---
title: "العمل مع مرشحات الجداول المحورية"
second_title: "المستند"
linktitle: المرشحات
type: docs
url: /pivot-tables/add-filters/
aliases: [/working-with-pivot-filters/]
keywords: "Aspose.Cells، الجدول المحوري، المرشح، واجهة برمجة التطبيقات REST، السحابة"
description: "تعرّف على كيفية إضافة وجلب وحذف مرشحات الجداول المحورية باستخدام واجهة برمجة التطبيقات REST لـ Aspose.Cells Cloud. يتضمن بنية الطلب، المعلمات المطلوبة، مثال على cURL، ومقتطفات كود للغتي C# وGo."
weight: 50
ArticleTitle: "العمل مع مرشحات الجداول المحورية – وثائق Aspose.Cells Cloud"
---

تُضيف هذه الواجهة البرمجية REST **مرشحًا جذريًا** (Pivot Filter) إلى الجدول المحوري الموجود عند الفهرس المحدد.

**المتطلبات المسبقة**  
قبل استدعاء هذه النقطة النهائية (endpoint)، يجب أن:

- تولّد رمز وصول OAuth/JWT صالحًا وتضمينه في رأس `Authorization`.  
- تتأكد من أن ملف المصنف المستهدف محفوظ في مجلد سحابي يمكنك الوصول إليه (حدد `folder` واختياريًا `storageName`).  
- تستخدم إصدار 3.0 أو أحدث من واجهة برمجة تطبيقات Aspose.Cells Cloud.

## واجهة PutWorksheetPivotTableFilter البرمجية

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotFilters
```

### **الأمان والمصادقة**

تُقدّم واجهات برمجة تطبيقات Aspose.Cells Cloud بشكل آمن وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة مبنية على رمز JWT</a>.

### معلمات الطلب

| اسم المعلمة         | النوع    | الموقع   | الوصف                                                                                       |
|---------------------|----------|-----------|----------------------------------------------------------------------------------------------|
| **name**            | نص (string) | المسار (path) | اسم ملف Excel.                                                                               |
| **sheetName**       | نص (string) | المسار (path) | الورقة التي تحتوي على الجدول المحوري.                                                         |
| **pivotTableIndex** | عدد صحيح (integer) | المسار (path) | فهرس الجدول المحوري (يبدأ من الصفر) الذي سيتم تطبيق المرشح عليه.                              |
| **filter**          | كائن (object) | الجسم (body) | كائن JSON يُعرّف إعدادات المرشح. انظر جدول **مخطط المرشح** أدناه.                               |
| **needReCalculate** | منطقي (boolean) | الاستعلام (query) | عند القيمة **true**، يُجبر المصنف على إعادة الحساب بعد إضافة المرشح. القيمة الافتراضية: **false**. |
| **folder**          | نص (string) | الاستعلام (query) | المجلد في التخزين السحابي حيث يوجد الملف.                                                    |
| **storageName**     | نص (string) | الاستعلام (query) | اسم خدمة التخزين السحابي.                                                                    |

**مخطط المرشح (filter schema)**

| الخاصية                      | النوع    | الوصف                                                                                      |
|-----------------------------|----------|---------------------------------------------------------------------------------------------|
| **AutoFilter**              | كائن (object) | إعدادات المرشح التلقائي (AutoFilter)؛ يمكن تجاهلها إن لم تُستخدم.                           |
| **EvaluationOrder**         | عدد صحيح (integer) | ترتيب تقييم المرشح.                                                                         |
| **FieldIndex**              | عدد صحيح (integer) | فهرس الحقل (يبدأ من الصفر) الذي يطبّق عليه المرشح.                                         |
| **FilterType**              | نص (string) | نوع المرشح (مثل: `Value`، `Count`، `Label`).                                                |
| **MeasureFldIndex**         | عدد صحيح (integer) | فهرس حقل القياس، إن وُجد.                                                                   |
| **MemberPropertyFieldIndex**| عدد صحيح (integer) | فهرس حقل خاصية العضو، إن وُجد.                                                              |
| **Name**                    | نص (string) | اسم اختياري للمرشح.                                                                         |
| **Value1**                  | نص (string) | القيمة الأولى المستخدمة في المرشح (مثل: الحد الأدنى للنطاق).                                 |
| **Value2**                  | نص (string) | القيمة الثانية المستخدمة في المرشح (مثل: الحد الأقصى للنطاق).                                |
| **CustomFilters**           | مصفوفة (array) | مجموعة كائنات المرشح المخصصة (كل منها يحتوي على `FilterOperatorType`، `Value1`، `Value2`). |
| **DynamicFilter**           | كائن (object) | إعدادات المرشح الديناميكي (مثل: Top10، Bottom10).                                           |
| **IconFilter**              | كائن (object) | إعدادات المرشح القائم على الأيقونات.                                                         |
| **Top10Filter**             | كائن (object) | إعدادات مرشح Top10/Bottom10.                                                                |
| **ColorFilter**             | كائن (object) | إعدادات المرشح القائم على اللون.                                                             |
| **Visibledropdown**         | منطقي (boolean) | يُشير إلى ظهور القائمة المنسدلة للمرشح.                                                    |

> **ملاحظة:** جميع المعلمات المذكورة أعلاه إجبارية ما لم يُشار صراحةً إلى كونها اختيارية في وثائق الواجهة البرمجية.

### أكواد الاستجابة

| الكود | المعنى                                         |
|-------|------------------------------------------------|
| 200   | تمت إضافة المرشح بنجاح.                       |
| 400   | طلب غير صالح – معلمات غير صحيحة.              |
| 401   | غير مصرّح – رمز مفقود أو غير صالح.            |
| 404   | غير موجود – المصنف أو الجدول المحوري مفقود.   |
| 500   | خطأ داخلي في الخادم.                          |

**أفضل الممارسات**  
- حافظ على صغر حجم كائنات المرشح قدر الإمكان؛ فالتعريفات الكبيرة للمرشحات قد تزيد من زمن الاستجابة.  
- تكون المكالمات مُتكررة (Idempotent) — إضافة نفس المرشح مرتين لن تُنتِج نسخًا مكررة.  
- التزم بحدّ معدل طلبات الواجهة البرمجية: 100 طلب في الدقيقة لكل حساب.  

*ملاحظات إضافية:*  
- الحد الأقصى لحجم تعريف المرشح هو 1 ميغابايت؛ سيتم رفض الحمولات الأكبر بخطأ 400.  
- عند استخدام `needReCalculate=true`، قد يؤدي إعادة الحساب إلى زيادة زمن الاستجابة، خاصةً مع المصنفات الكبيرة.  

يمكنك استكشاف تعريف OpenAPI الكامل هنا:  
[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTableFilter)

### مثال على طلب cURL

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotFilters?needReCalculate=true" \
  -X PUT \
  -d '{
        "AutoFilter": {
          "link": { "Href": "https://example.com", "Rel": "self", "Title": "AutoFilter Link", "Type": "application/json" },
          "FilterColumns": [
            {
              "FieldIndex": 0,
              "FilterType": "Value",
              "MultipleFilters": {
                "MatchBlank": true,
                "MultipleFilterList": [ { "Value": "example" } ]
              },
              "ColorFilter": {
                "FilterByFillColor": "FF0000",
                "Pattern": "Solid",
                "Color": {
                  "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                  "ColorIndex": 3,
                  "IsShapeColor": false,
                  "ThemeColor": { "ColorType": "Accent1", "Tint": 0 },
                  "Type": "Rgb"
                },
                "ForegroundColorColor": null,
                "BackgroundColor": null
              },
              "CustomFilters": [ { "FilterOperatorType": "Equals", "Value1": "Example" } ],
              "DynamicFilter": { "DynamicFilterType": "Top10" },
              "IconFilter": { "IconId": 1, "IconSetType": "3Arrows" },
              "Top10Filter": { "Criteria": "Top", "IsPercent": true, "IsTop": true, "Items": 10 },
              "Visibledropdown": "true"
            }
          ],
          "Range": "A1:D100",
          "Sorter": {
            "CaseSensitive": false,
            "HasHeaders": true,
            "KeyList": [ { "Key": 0, "SortOrder": "Ascending", "CustomList": null } ],
            "SortLeftToRight": false
          }
        },
        "EvaluationOrder": 0,
        "FieldIndex": 0,
        "FilterType": "Value",
        "MeasureFldIndex": 0,
        "MemberPropertyFieldIndex": 0,
        "Name": "MyFilter",
        "Value1": "10",
        "Value2": "20"
      }' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK السحابية

استخدام SDK هو أسرع طريقة لتطوير تطبيقاتك ضد Aspose.Cells Cloud. فالمكتبات البرمجية تتعامل مع التفاصيل منخفضة المستوى، مما يتيح لك التركيز على منطق تطبيقك. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح الأمثلة التالية كيفية إجراء مكالمات لخدمات الويب Aspose.Cells باستخدام مكتبات SDK مختلفة.

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using System;
using System.Threading.Tasks;
using Aspose.Cells.Cloud.Sdk.Api;
using Aspose.Cells.Cloud.Sdk.Model;

public class PivotFilterExample
{
    public static async Task AddPivotFilterAsync()
    {
        // تهيئة عميل الواجهة البرمجية (استبدل بالمُعطيات الخاصة بك)
        var config = new Configuration
        {
            ClientId = "YOUR_CLIENT_ID",
            ClientSecret = "YOUR_CLIENT_SECRET"
        };
        var apiInstance = new CellsApi(config);

        // بناء كائن المرشح
        var filter = new PivotFilter
        {
            AutoFilter = null,
            EvaluationOrder = 0,
            FieldIndex = 1,
            FilterType = "Count"
        };

        // إعداد الطلب
        var request = new PutWorksheetPivotTableFilterRequest(
            name: "Book1.xlsx",
            sheetName: "PivotSheet",
            pivotTableIndex: 0,
            filter: filter,
            needReCalculate: true,
            folder: "Temp",
            storageName: null);

        // تنفيذ الطلب
        var response = await apiInstance.PutWorksheetPivotTableFilterAsync(request);
        Console.WriteLine($"Status: {response.Status}");
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "2a2aa16c2d9fd7e46b1b19f5fea5842b" >}}

{{< /tab >}}

{{< /tabs >}}

للمزيد من العمليات المتعلقة بالجداول المحورية، راجع وثائق **الإضافة** و**الحذف** و**المسح** للمرشحات.
---