---
title: احصل على تفاصيل العمود – مرجع واجهة برمجة تطبيقات Aspose.Cells Cloud (الإصدار 4.0)
description: استرجاع معلومات مفصّلة حول عمود ورقة عمل (الفهرس، العرض، النمط، الحالة المخفية) باستخدام واجهة Aspose.Cells Cloud REST API.
keywords: Aspose.Cells، واجهة برمجة تطبيقات السحابة، عمود إكسل، احصل على عمود، واجهة REST API، JWT، ورقة عمل
date: 2026-07-30
---

# احصل على تفاصيل العمود  

استرجاع معلومات مفصّلة حول عمود ورقة عمل معيّن (الفهرس، العرض، النمط، الحالة المخفية) من ملف جدول عمل مخزّن في خدمة Aspose Cloud.

## جدول المحتويات
1. [المتطلبات المسبقة](#prerequisites)  
2. [المصادقة](#authentication)  
3. [النهاية (Endpoint)](#endpoint)  
4. [مُعاملات الطلب](#request-parameters)  
5. [مثال باستخدام cURL](#curl-example)  
6. [مثال على الاستجابة](#response-example)  
7. [مخطط الاستجابة](#response-schema)  
8. [الأخطاء المحتملة](#possible-errors)  
9. [أمثلة SDK](#sdk-examples)  
10. [موارد إضافية](#additional-resources)  

---

## المتطلبات المسبقة
- **رمز وصول JWT** صالح تم الحصول عليه عبر مصادقة Aspose Cloud.  
- يجب أن يكون ملف جدول العمل مخزّنًا في تخزين Aspose Cloud (أو في تخزين آخر مدعوم)، ويجب معرفة مسار المجلد (إن وُجد).  

---

## المصادقة
تستخدم جميع واجهات برمجة تطبيقات Aspose.Cells Cloud **المصادقة القائمة على رمز JWT**. أضف الرمز في رأس `Authorization` كالتالي:

```http
Authorization: Bearer <access_token>
```

للحصول على تفاصيل حول كيفية الحصول على رمز وصول، راجع [دليل المصادقة](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## النهاية (Endpoint)
```
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **{name}** – اسم ملف جدول العمل (مثال: `test.xlsx`).  
- **{sheetName}** – اسم ورقة العمل (مثال: `Sheet1`).  
- **{columnIndex}** – فهرس العمود المراد استرجاعه (يبدأ من الصفر).  

---

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتشترط <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">المصادقة القائمة على رمز JWT</a>.

## مُعاملات الطلب

| الاسم           | الموقع | النوع    | الإلزام | الوصف |
|----------------|--------|----------|---------|--------|
| **name**       | المسار | نص (string) | نعم     | اسم ملف جدول العمل. |
| **sheetName**  | المسار | نص (string) | نعم     | ورقة العمل التي يحتوي العمود عليها. |
| **columnIndex** | المسار | عدد صحيح (integer) | نعم | فهرس العمود المراد استرجاعه (يبدأ من الصفر). |
| **folder**     | الاستعلام | نص (string) | لا       | مجلد التخزين الذي يوجد فيه جدول العمل. |
| **storageName** | الاستعلام | نص (string) | لا       | اسم خدمة التخزين (مثال: تخزين Aspose Cloud). |

---

## مثال باستخدام cURL
```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0?folder=MyFolder&storageName=MyStorage" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

---

## مثال على الاستجابة
```json
{
  "Column": {
    "GroupLevel": 0,
    "Index": 0,
    "IsHidden": false,
    "Width": 8.5,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

---

## مخطط الاستجابة
| الحقل               | النوع    | الوصف |
|---------------------|----------|--------|
| `Column.GroupLevel` | عدد صحيح | المستوى التفصيلي (outline) للعمود (يُستخدم للتجميع). |
| `Column.Index`      | عدد صحيح | الفهرس المُعدّ من الصفر للعمود. |
| `Column.IsHidden`   | منطقي (boolean) | `true` إن كان العمود مخفيًا؛ خلاف ذلك `false`. |
| `Column.Width`      | رقم     | عرض العمود معبرًا عنه بالأحرف. |
| `Column.Style`      | كائن    | يحتوي على رابط (`link`) إلى مورد نمط العمود. |
| `Column.link`       | كائن    | رابط ذاتي إلى مورد العمود. |
| `Code`              | عدد صحيح | رمز حالة HTTP للرد. |
| `Status`            | نص (string) | وصف نصي للحالة (مثال: **OK**). |

---

## الأخطاء المحتملة
| حالة HTTP | الرمز | الرسالة                | متى يحدث الخطأ |
|-----------|--------|------------------------|----------------|
| 400       | 400    | Bad Request            | مُعاملات مطلوبة مفقودة أو مُعطّلة. |
| 401       | 401    | Unauthorized           | رأس `Authorization` مفقود أو غير صالح. |
| 404       | 404    | Not Found              | ملف جدول العمل أو ورقة العمل أو العمود غير موجود. |
| 500       | 500    | Internal Server Error  | مشكلة غير متوقعة في الخادم. |

### مثال – 404 Not Found
```json
{
  "Code": 404,
  "Message": "Column index out of range."
}
```

### مثال – 401 Unauthorized
```json
{
  "Code": 401,
  "Message": "Invalid or missing authentication token."
}
```

---

## أمثلة SDK
تُظهر مقاطع الكود التالية كيفية استدعاء عملية **Get Worksheet Columns** باستخدام SDKs الرسمية لـ Aspose.Cells Cloud. في حال عدم توفر أي Gist، يُقدَّم رمز المثال مباشرةً أدناه.

<details><summary>**C#**</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

// تهيئة عميل الواجهة
var apiInstance = new CellsApi("client_id", "client_secret");

// تحديد المُعاملات المطلوبة
string name = "test.xlsx";
string sheetName = "Sheet1";
int columnIndex = 0;
string folder = "MyFolder";          // اختياري
string storageName = "MyStorage";    // اختياري

try
{
    var response = apiInstance.GetWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
    Console.WriteLine("Column Index: " + response.Column.Index);
    Console.WriteLine("Width: " + response.Column.Width);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.GetWorksheetColumns: " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.ColumnsResponse;

public class GetWorksheetColumnsExample {
    public static void main(String[] args) {
        CellsApi apiInstance = new CellsApi("client_id", "client_secret");

        String name = "test.xlsx";
        String sheetName = "Sheet1";
        Integer columnIndex = 0;
        String folder = "MyFolder";          // اختياري
        String storageName = "MyStorage";    // اختياري

        try {
            ColumnsResponse result = apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
            System.out.println("Column index: " + result.getColumn().getIndex());
            System.out.println("Width: " + result.getColumn().getWidth());
        } catch (Exception e) {
            System.err.println("Exception while calling CellsApi#getWorksheetColumns");
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"

api_instance = CellsApi(ApiClient(config))

name = "test.xlsx"
sheet_name = "Sheet1"
column_index = 0
folder = "MyFolder"       # اختياري
storage_name = "MyStorage"  # اختياري

try:
    response = api_instance.get_worksheet_columns(name, sheet_name, column_index, folder, storage_name)
    print("Column index:", response.column.index)
    print("Width:", response.column.width)
except Exception as e:
    print("Exception when calling CellsApi->get_worksheet_columns:", e)
```

</details>

<details><summary>**Node.js (TypeScript)**</summary>

```typescript
import { CellsApi, Configuration } from "@asposecloud/cells-sdk";

const config = new Configuration({
    clientId: "client_id",
    clientSecret: "client_secret"
});
const apiInstance = new CellsApi(config);

const name = "test.xlsx";
const sheetName = "Sheet1";
const columnIndex = 0;
const folder = "MyFolder";       // اختياري
const storageName = "MyStorage"; // اختياري

apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName)
    .then((result) => {
        console.log("Column index:", result.column?.index);
        console.log("Width:", result.column?.width);
    })
    .catch((error) => {
        console.error("Error calling getWorksheetColumns:", error);
    });
```

</details>

> **ملاحظة:** تُعالِج جميع واجهات SDK تلقائيًا رأس `Authorization` بعد تزويد `client_id` و `client_secret`.

---

## موارد إضافية
- **مواصفات OpenAPI:** <https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetColumns>  
- **دليل المصادقة:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **مستودع GitHub (SDKs وأمثلة):** <https://github.com/aspose-cells-cloud>  

--- 

*تم تحديث الوثيقة_last_updated_ في 2026-07-30.*  
---