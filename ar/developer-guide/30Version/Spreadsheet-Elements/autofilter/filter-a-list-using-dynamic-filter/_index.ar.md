---
---
title: إضافة عامل تصفية ديناميكي في ورقة عمل Excel باستخدام API Aspose.Cells Cloud
description: تعلّم كيفية تطبيق عامل تصفية ديناميكي (مثل BelowAverage، Tomorrow، LastMonth) في ورقة عمل Excel باستخدام واجهة REST API الخاصة بـ Aspose.Cells Cloud. يتضمن معلومات عن المصادقة، بنية الطلب، المَعلمات، معالجة الاستجابة، وأمثلة SDK بلغات برمجة متعددة.
keywords: Aspose.Cells، عامل التصفية الديناميكي، Excel API، REST، عامل التصفية التلقائي، SDK السحابية
slug: add-dynamic-filter
api_version: v3.0
---

## نظرة عامة

تُضيف العملية **PutWorksheetDynamicFilter** عامل تصفية ديناميكي إلى النطاق المُحدّد في ورقة عمل Excel.  
تقوم عوامل التصفية الديناميكية بتقييم القيم تلقائيًا مثل التواريخ أو المتوسطات أو الخلايا الفارغة، مما يسمح لك بإنشاء عروض "ذكية" دون الحاجة إلى كتابة صيغ مخصصة.

## المتطلبات الأساسية

| المتطلبات | التفاصيل |
|-----------|---------|
| **المصادقة** | رمز JWT صالح تم الحصول عليه من نقطة النهاية `/connect/token`. يُضاف إلى رأس الطلب `Authorization: Bearer <token>`. |
| **التخزين** | يجب أن يكون الملف المصنف موجودًا في موقع تخزين Aspose Cloud (الافتراضي أو موقع مخصص). |
| **تنسيقات الملفات المدعومة** | `.xlsx`, `.xls`, `.xlsm`, `.xlsb`, `.csv`، وما إلى ذلك. |
| **الصلاحيات** | صلاحية القراءة والكتابة على المجلد/الملف المستهدف. |

## طلب HTTP

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dynamicFilter
```

### مَعلمات المسار (Path Parameters)

| المعلمة | النوع | الإجباري | الوصف |
|---------|-------|----------|--------|
| `name` | نص (string) | ✅ | اسم ملف Excel المصنف (مثال: `Book1.xlsx`). |
| `sheetName` | نص (string) | ✅ | اسم ورقة العمل التي تحتوي على النطاق المراد تطبيق التصفية عليه. |

### مَعلمات الاستعلام (Query Parameters)

| المعلمة | النوع | الإجباري | الوصف |
|---------|-------|----------|--------|
| `range` | نص (string) | ✅ | النطاق الذي تُطبّق عليه التصفية (مثال: `A1:B1`). |
| `fieldIndex` | عدد صحيح (integer) | ✅ | المؤشر الصفري (zero-based) للعمود داخل النطاق الذي سيُطبّق عليه عامل التصفية الديناميكي. |
| `dynamicFilterType` | نص (string) | ✅ | نوع عامل التصفية الديناميكي المراد تطبيقه (انظر **أنواع عوامل التصفية الديناميكية المدعومة**). |
| `matchBlanks` | منطقي (boolean) | ❌ | إذا كانت القيمة `true`، فسيتم تضمين الخلايا الفارغة في نتائج التصفية. القيمة الافتراضية: `false`. |
| `refresh` | منطقي (boolean) | ❌ | إذا كانت القيمة `true`، فسيتم تحديث عامل التصفية التلقائي بعد تطبيق عامل التصفية. |
| `folder` | نص (string) | ❌ | المسار إلى المجلد في التخزين حيث يوجد الملف المصنف. |
| `storageName` | نص (string) | ❌ | اسم تخزين Aspose Cloud المراد استخدامه. |

### جسم الطلب

يحتوي جسم الطلب على كائن JSON فارغ:

```json
{}
```

## أنواع عوامل التصفية الديناميكية المدعومة

| القيمة | المعنى |
|--------|----------|
| `BelowAverage` | الصفوف التي تكون قيمتها أقل من متوسط العمود. |
| `AboveAverage` | الصفوف التي تكون قيمتها أعلى من متوسط العمود. |
| `Tomorrow` | الصفوف التي تحتوي على تواريخ تساوي تاريخ الغد. |
| `Yesterday` | الصفوف التي تحتوي على تواريخ تساوي تاريخ الأمس. |
| `NextWeek` | الصفوف التي تحتوي على تواريخ تقع في الأسبوع القادم. |
| `LastMonth` | الصفوف التي تحتوي على تواريخ من الشهر السابق. |
| `ThisYear` | الصفوف التي تحتوي على تواريخ من السنة الجارية. |

## مثال على الطلب (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dynamicFilter?range=A1:B1&fieldIndex=0&dynamicFilterType=BelowAverage&matchBlanks=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'   # جسم JSON فارغ في طلب PUT
```

## مثال على الاستجابة

```json
{
    "Code": 200,
    "Status": "OK",
    "Message": "تم تطبيق عامل التصفية الديناميكي بنجاح."
}
```

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|-------|---------|--------|
| 200 | ناجح (OK) | تم تطبيق عامل التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صحيح (Bad Request) | معلمات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مصادق عليه (Unauthorized) | رمز JWT غير صالح أو مفقود. |
| 413 | حجم البيانات كبير جدًا (Payload Too Large) | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500 | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم. |

## أمثلة لواجهات برمجة التطبيقات (SDK)

فيما يلي مقاطع جاهزة للتشغيل لأكثر واجهات SDK شعبية. استبدل `YOUR_JWT_TOKEN` و`YOUR_FILE_NAME` وباقي العناصر القابلة للاستبدال بقيمك الفعلية.

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

var apiInstance = new AutoFilterApi();
var name = "Book1.xlsx"; // string | اسم الملف المصنف.
var sheetName = "Sheet1"; // string | اسم ورقة العمل.
var range = "A1:B1"; // string | النطاق المراد تطبيق التصفية عليه.
var fieldIndex = 0; // int? | المؤشر الصفري للعمود.
var dynamicFilterType = "BelowAverage"; // string | نوع عامل التصفية الديناميكي.
var matchBlanks = true; // bool? | تضمين الخلايا الفارغة.
var refresh = true; // bool? | التحديث بعد التصفية.
var folder = "myFolder"; // string (اختياري)
var storageName = null; // string (اختياري)

try
{
    var response = apiInstance.PutWorksheetDynamicFilter(name, sheetName, range, fieldIndex, dynamicFilterType, matchBlanks, refresh, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("حدث استثناء عند استدعاء AutoFilterApi.PutWorksheetDynamicFilter: " + e.Message );
}
```

### Java  

```java
import com.aspose.cloud.cells.api.AutoFilterApi;
import com.aspose.cloud.cells.model.*;

public class PutWorksheetDynamicFilterExample {
    public static void main(String[] args) {
        AutoFilterApi api = new AutoFilterApi();
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        String range = "A1:B1";
        Integer fieldIndex = 0;
        String dynamicFilterType = "BelowAverage";
        Boolean matchBlanks = true;
        Boolean refresh = true;
        String folder = "myFolder";
        String storageName = null;

        try {
            CellsCloudResponse resp = api.putWorksheetDynamicFilter(name, sheetName, range, fieldIndex,
                    dynamicFilterType, matchBlanks, refresh, folder, storageName);
            System.out.println(resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python  

```python
from asposecellscloud import AutoFilterApi, ApiClient, Configuration

config = Configuration()
config.access_token = "<jwt token>"
api_client = ApiClient(configuration=config)
api = AutoFilterApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
range_ = "A1:B1"
field_index = 0
dynamic_filter_type = "BelowAverage"
match_blanks = True
refresh = True
folder = "myFolder"
storage_name = None

response = api.put_worksheet_dynamic_filter(
    name=name,
    sheet_name=sheet_name,
    range=range_,
    field_index=field_index,
    dynamic_filter_type=dynamic_filter_type,
    match_blanks=match_blanks,
    refresh=refresh,
    folder=folder,
    storage_name=storage_name
)

print(response.status)
```

### Node.js (TypeScript)  

```typescript
import { AutoFilterApi, Configuration, CellsCloudResponse } from "@asposecloud/cells-sdk";

const config = new Configuration({
    accessToken: "<jwt token>"
});
const api = new AutoFilterApi(config);

(async () => {
    try {
        const resp: CellsCloudResponse = await api.putWorksheetDynamicFilter(
            "Book1.xlsx",          // name
            "Sheet1",              // sheetName
            "A1:B1",               // range
            0,                     // fieldIndex
            "BelowAverage",        // dynamicFilterType
            true,                  // matchBlanks
            true,                  // refresh
            "myFolder",            // folder (اختياري)
            undefined              // storageName (اختياري)
        );
        console.log(resp.status);
    } catch (error) {
        console.error(error);
    }
})();
```

*(تتوفر مقاطع مماثلة بلغات Ruby و PHP و Go و Perl في مستودع SDK الرسمي.)*

## مواضيع ذات صلة

- **إضافة عامل تصفية تلقائي قياسي** – [إضافة عامل تصفية قياسي](/autofilter/add-filter)  
- **إضافة عامل تصفية حسب التاريخ** – [إضافة عامل تصفية حسب التاريخ](/autofilter/add-date-filter)  
- **حذف عامل التصفية التلقائي** – [حذف عامل التصفية التلقائي](/autofilter/delete-filter)  
- **العمل مع أوراق العمل** – [نظرة عامة على واجهة برمجة تطبيقات أوراق العمل](/worksheets/)

## ملاحظات

* تم مراجعة جميع الصور المستخدمة في الوثائق الأصلية لضمان إمكانية الوصول. تُعلَّم الرموز التعبيرية الزخرفية بـ `alt=""` و `role="presentation"`؛ بينما تحتفظ الرموز الوظيفية بنصوص `alt` وصفية.  
* تم تنظيف كلمات التصنيف التعريفية (Meta Keywords) لإزالة المدخلات الفارغة والتكرارات.  
* تُطبّق هذه الصفحة الآن هيكلًا واضحًا للعناوين (عنوان H1 واحد في front matter، و H2 للأقسام الرئيسية، و H3/H4 للمقاطع الفرعية) لتحسين تحسين محركات البحث (SEO) وسهولة التنقل مع قارئات الشاشة.  

---  
---