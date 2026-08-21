---
title: "استرجاع صف واحد من ورقة عمل Excel باستخدام API Aspose.Cells Cloud"
description: "تعلم كيفية استرجاع صف محدد من ورقة عمل Excel المخزنة في تخزين Aspose Cloud باستخدام API REST لـ Aspose.Cells Cloud. يشمل بناء الجملة المطلوبة، المعلمات، مخطط الاستجابة، مثال cURL، ورموز SDK (C#، Java، Python)."
keywords: "Aspose.Cells Cloud، استرجاع الصف، API Excel، REST للجداول الحسابية، SDK C#، SDK Java، SDK Python"
date: 2026-07-30
api_version: "v3.0"
---

# استرجاع صف واحد من ورقة عمل Excel

**النقطة النهائية (Endpoint)**: `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/rows/{rowIndex}`  

استرجاع صف من ورقة عمل مخزنة في تخزين Aspose Cloud. تتطلب هذه العملية رمز وصول OAuth 2.0 صالحًا مع نطاق **قراءة (Read)**.

---

## جدول المحتويات
1. [المتطلبات المسبقة](#prerequisites)  
2. [طلب HTTP](#http-request)  
3. [المعلمات](#parameters)  
   - [المعلمات المسار (Path parameters)](#path-parameters)  
   - [المعلمات الاستعلام (Query parameters)](#query-parameters)  
4. [مثال باستخدام cURL](#curl-example)  
5. [الاستجابة](#response)  
   - [مخطط النجاح](#success-schema)  
   - [رموز الحالة (Status codes)](#status-codes)  
6. [أمثلة لرموز SDK](#sdk-code-samples)  
   - [C#](#c)  
   - [Java](#java)  
   - [Python](#python)  
7. [العمليات ذات الصلة](#related-operations)  
8. [ملاحظات وقيود](#notes--limits)  

---

## المتطلبات المسبقة
- **حساب Aspose Cloud** مع اشتراك نشط.  
- **رمز وصول OAuth 2.0** يحتوي على نطاق **قراءة (Read)**.  
- يجب أن يكون المصنف المستهدف موجودًا مسبقًا في تخزين Aspose Cloud.  

---

## طلب HTTP
```http
GET /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}?folder={folder}&storageName={storageName} HTTP/1.1
Host: api.aspose.cloud
Authorization: Bearer {access_token}
Accept: application/json
```

*عنوان URL الأساسي*: `https://api.aspose.cloud/v3.0`

---

## المعلمات

### المعلمات المسار (Path parameters)
| الاسم      | النوع   | مطلوب | الوصف                         |
|-----------|--------|----------|-------------------------------------|
| `name`    | سلسلة نصية (string) | ✅       | اسم ملف المصنف (مثل `MyWorkbook.xlsx`). |
| `sheetName`| سلسلة نصية (string) | ✅     | اسم ورقة العمل (مثل `Sheet1`). |
| `rowIndex`| عدد صحيح (integer)| ✅       | الفهرس المبدأ من الصفر (zero-based) للصف المراد استرجاعه. |

### معلمات الاستعلام (Query parameters) *(اختيارية)*
| الاسم        | النوع   | مطلوب | الوصف |
|-------------|--------|----------|-------------|
| `folder`    | سلسلة نصية (string) | ❌       | مسار المجلد في التخزين السحابي حيث يوجد المصنف. |
| `storageName`| سلسلة نصية (string)| ❌       | اسم خدمة التخزين (في حال استخدام تخزين مخصص). |

---

## مثال باستخدام cURL
```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/rows/5?folder=Docs&storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## الاستجابة

### مخطط النجاح (`200 OK`)
```json
{
  "Code": 200,
  "Status": "OK",
  "Row": {
    "Index": 5,
    "Height": 15.0,
    "Style": { /* كائن النمط (style object) */ },
    "Cells": [
      { "ColumnIndex": 0, "Value": "A6", "DataType": "String" },
      { "ColumnIndex": 1, "Value": 123, "DataType": "Number" }
      /* ...خلايا إضافية... */
    ]
  }
}
```

### رموز الحالة (Status codes)
| الرمز | المعنى |
|------|---------|
| **200** | تم استرجاع الصف بنجاح. |
| **401** | غير مُخوّل (Unauthorized) – رمز الوصول مفقود أو غير صالح. |
| **404** | المصنف أو ورقة العمل أو الصف غير موجود. |
| **500** | خطأ داخلي في الخادم. |

### مثال على خطأ (`401 Unauthorized`)
```json
{
  "Code": 401,
  "Message": "رمز الوصول مفقود أو غير صالح."
}
```

---

## أمثلة لرموز SDK

### C#  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var clientId = "YOUR_CLIENT_ID";
var clientSecret = "YOUR_CLIENT_SECRET";

var api = new CellsApi(clientId, clientSecret);
var response = api.CellsRows_GetWorksheetRow(
    name: "MyWorkbook.xlsx",
    sheetName: "Sheet1",
    rowIndex: 5,
    folder: "Docs",
    storageName: null   // اختياري
);

Console.WriteLine($"تم استرجاع الصف {response.Row.Index} مع {response.Row.Cells.Count} خلية.");
```

### Java  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.RowResponse;

CellsApi api = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");
RowResponse response = api.cellsRowsGetWorksheetRow(
    "MyWorkbook.xlsx",
    "Sheet1",
    5,
    "Docs",
    null   // storageName – اختياري
);

System.out.println("فهرس الصف: " + response.getRow().getIndex());
System.out.println("عدد الخلايا: " + response.getRow().getCells().size());
```

### Python  
```python
from asposecellscloud import CellsApi, ApiException
from asposecellscloud.models import RowResponse

client_id = "YOUR_CLIENT_ID"
client_secret = "YOUR_CLIENT_SECRET"

api = CellsApi(client_id, client_secret)

try:
    response = api.cells_rows_get_worksheet_row(
        name="MyWorkbook.xlsx",
        sheet_name="Sheet1",
        row_index=5,
        folder="Docs",
        storage_name=None
    )
    print(f"تم استرجاع الصف {response.row.index} مع {len(response.row.cells)} خلية.")
except ApiException as e:
    print("حدث استثناء عند استدعاء CellsApi->cells_rows_get_worksheet_row:", e)
```

---

## العمليات ذات الصلة
| العملية | الوصف |
|-----------|-------------|
| **إضافة صف (Add Row)** | `POST /cells/{name}/worksheets/{sheetName}/rows` – إدراج صف جديد في ورقة العمل. |
| **حذف صف (Delete Row)** | `DELETE /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}` – إزالة صف موجود. |
| **استرجاع صفوف متعددة (Get Multiple Rows)** | `GET /cells/{name}/worksheets/{sheetName}/rows` – استرجاع مجموعة من الصفوف. |
| **نظرة عامة على الصفوف (Rows Overview)** | `/cells/rows/` – توثيق عام لنقاط النهاية المتعلقة بالصفوف. |

---

## ملاحظات وقيود
- **حد معدل الطلبات**: 100 طلب في الدقيقة لكل حساب.  
- **التنسيقات المدعومة**: XLS، XLSX، CSV، ODS.  
- الفهرس الخاص بالصف يبدأ من الصفر (zero-based)، لذا الصف الأول هو `0`.  
- تأكد من تحميل المصنف في المجلد المحدد في `folder` قبل استدعاء هذه النقطة النهائية.  

---