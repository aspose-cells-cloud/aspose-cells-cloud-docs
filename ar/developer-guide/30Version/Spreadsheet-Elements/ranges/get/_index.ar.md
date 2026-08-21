---
title: "كيفية استرجاع محتوى نطاق من ورقة عمل إكسل"
second_title: "Document"
linktitle: "Get"
type: docs
url: /ar/ranges/get/
keywords: "Aspose.Cells, Excel, API, get, range, spreadsheet, REST"
description: "تعلم كيفية استرجاع محتوى نطاق من ورقة عمل إكسل باستخدام واجهة Aspose.Cells Cloud REST API. يتضمن بناء الجملة المطلوبة وأكواداً توضيحية."
weight: 20
ArticleTitle: "كيفية استرجاع محتوى نطاق من ورقة عمل إكسل – Aspose.Cells Cloud API"
---

## العمل مع استرجاع محتوى النطاق في ورقة عمل إكسل

- [كيفية استرجاع بيانات الخلية بناءً على اسم نطاق](/cells/ranges/get/values/)
- [كيفية استرجاع اسم نطاق من ملف إكسل](/cells/ranges/get/name/)

**المتطلبات المسبقة**

- رمز وصول صالح لـ Aspose Cloud (أو `client_id`/`client_secret` لاستخدام OAuth).
- يجب رفع ملف الإكسل إلى مجلد التخزين الهدف.
- إصدار SDK لـ Aspose.Cells Cloud الإصدار 3.0 أو أحدث.

تشغيلة **Get Range** تُعيد محتوى النطاق المحدّد في ورقة العمل.  
إنها طلب بسيط من نوع `GET` يُعيد بيانات النطاق بصيغة JSON (أو صيغ أخرى عند الطلب).

**نظرة عامة على الطلب**

| العنصر | القيمة |
|--------|--------|
| **طريقة HTTP** | `GET` |
| **النقطة النهائية (Endpoint)** | `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}` |
| **مُعاملات المسار (Path Parameters)** | `fileName` – اسم ملف الإكسل (مع امتداده) <br> `sheetName` – اسم ورقة العمل <br> `rangeName` – اسم النطاق (مثل `A1:B10`) |
| **المُعاملات الاستعلامية (Query Parameters)** (اختيارية) | `folder` – مجلد التخزين <br> `storage` – اسم التخزين <br> `outFormat` – تنسيق الاستجابة (مثل `json`, `xml`) |
| **الرؤوس (Headers)** | `Authorization: Bearer <access_token>` <br> `Accept: application/json` |

**مثال باستخدام cURL**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges/A1:B10?folder=Samples&storage=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/json"
```

**مثال بلغة C\#**

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

var apiInstance = new CellsApi("client_id", "client_secret");
var request = new GetRangeRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    rangeName: "A1:B10",
    folder: "Samples",
    storage: "MyStorage"
);
var response = apiInstance.GetRange(request);
Console.WriteLine(response);
```

**مثال بلغة Java**

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.requests.GetRangeRequest;

CellsApi api = new CellsApi("client_id", "client_secret");
GetRangeRequest request = new GetRangeRequest(
        "Book1.xlsx",
        "Sheet1",
        "A1:B10",
        "Samples",
        "MyStorage",
        null,
        null);
var response = api.getRange(request);
System.out.println(response);
```

**مثال بلغة Python**

```python
from asposecellscloud import CellsApi, GetRangeRequest

api = CellsApi(client_id="client_id", client_secret="client_secret")
request = GetRangeRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    range_name="A1:B10",
    folder="Samples",
    storage="MyStorage"
)
response = api.get_range(request)
print(response)
```

**مخطط الاستجابة (JSON)**

```json
{
  "Code": 200,
  "Status": "OK",
  "Range": {
    "ColumnCount": 2,
    "RowCount": 1,
    "FirstRow": 0,
    "FirstColumn": 0,
    "Values": [
      ["Value1", "Value2"]
    ]
  }
}
```

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|-------|---------|--------|
| 200 | OK | تم تطبيق العامل بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | Bad Request | مُعاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | Unauthorized | رمز JWT غير صالح أو مفقود. |
| 413 | Payload Too Large | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500 | Internal Server Error | خطأ غير متوقع في الخادم. |

- `200 OK` – تم استرجاع النطاق بنجاح.  
- `400 Bad Request` – مُعاملات مفقودة أو غير صالحة.  
- `401 Unauthorized` – رمز وصول غير صالح أو مفقود.  
- `404 Not Found` – الملف أو ورقة العمل أو النطاق المحدّد غير موجود.  
- `500 Internal Server Error` – خطأ غير متوقع في الخادم.

**أمثلة على استجابة الأخطاء**

```json
// 400 Bad Request
{
  "Code": 400,
  "Message": "المُعاملات في الطلب غير صالحة أو مفقودة."
}
```

```json
// 401 Unauthorized
{
  "Code": 401,
  "Message": "رمز الوصول غير صالح أو مفقود."
}
```

```json
// 404 Not Found
{
  "Code": 404,
  "Message": "لم يتم العثور على الملف أو ورقة العمل أو النطاق المحدّد."
}
```

**انظر أيضاً**

- [كيفية استرجاع بيانات الخلية بناءً على اسم نطاق](/cells/ranges/get/values/)  
- [كيفية استرجاع اسم نطاق من ملف إكسل](/cells/ranges/get/name/)  
- [تحديث محتوى النطاق](/cells/ranges/update/)  
- [حذف نطاق](/cells/ranges/delete/)  
---