---
---
title: "واجهة برمجة تطبيقات Aspose.Cells Cloud – استرجاع كائن القائمة (الجدول) من ورقة العمل"
description: "استرجاع كائن القائمة (الجدول) من ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API. يدعم التصدير إلى صيغ متعددة (PDF وCSV وJSON، ...)."
keywords:
  - Aspose.Cells
  - واجهة برمجة تطبيقات سحابية
  - Excel
  - ListObject
  - جدول
  - REST
  - SDK
type: docs
slug: /list-objects/get/
weight: 9
---

# واجهة برمجة تطبيقات Aspose.Cells Cloud – استرجاع كائن القائمة (الجدول) من ورقة العمل

استرجاع **كائن القائمة** (ويُعرف أيضًا باسم *الجدول*) من ورقة عمل معيّنة في ملف Excel. يمكن لهذه النقطة النهائية أيضًا تصدير الجدول مباشرةً إلى صيغة محددة باستخدام معامل الاستعلام الاختياري `format`.

---

## المتطلبات الأساسية

| المتطلب | التفاصيل |
|---------|---------|
| **المصادقة** | مطلوب رمز **JWT** (Bearer) صالح. احصل على الرمز عبر تدفق مصادقة **OAuth2** الموصوف في [دليل المصادقة](/authentication/). |
| **التخزين** | يجب أن يكون ملف جدول البيانات مخزنًا في موقع تخزين Aspose Cloud. إذا كان الملف موجودًا في مخزن غير افتراضي، فحدّد معامل الاستعلام `storageName`. |
| **حدود معدل الطلبات** | تتبع واجهة البرمجة سياسة معدل الطلب القياسية في Aspose Cloud (الافتراضي = 100 طلب/دقيقة لكل حساب). |
| **مكتبات SDK (اختيارية)** | استخدام إحدى مكتبات SDK الرسمية (C# أو Java أو Python، ...) يبسّط بناء الطلبات ومعالجة الاستجابات. راجع قسم **أمثلة SDK** أدناه. |

---

## الطلب

### HTTP GET

```
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}
```

| المعامل | النوع | الموقع | الإلزام | الوصف |
|---------|-------|--------|---------|--------|
| **name** | `string` | المسار | ✔️ | اسم ملف Excel (مع الامتداد). |
| **sheetName** | `string` | المسار | ✔️ | ورقة العمل التي تحتوي على كائن القائمة. |
| **listobjectindex** | `integer` | المسار | ✔️ | المؤشر المُعدّ من الصفر لكائن القائمة المراد استرجاعه. |
| **format** | `string` | استعلام | ❌ | صيغة التصدير المطلوبة (مثل `pdf` أو `csv` أو `json`). |
| **folder** | `string` | استعلام | ❌ | مسار المجلد الذي يخزن فيه ملف جدول البيانات. |
| **storageName** | `string` | استعلام | ❌ | اسم مخزن Aspose Cloud المراد استخدامه. |

#### ملاحظات

* يجب إجراء جميع الاستدعاءات عبر **HTTPS**.  
* عند تزويده، يكون محتوى جسم الاستجابة لمعامل `format` تدفق الملف المُصدَّر (مثل `application/pdf`).  
* بدون `format`، تُعيد واجهة البرمجة وصفًا بالصيغة JSON لكائن القائمة.

---

## مثال باستخدام cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/1?format=csv" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

*استبدل `<your_jwt_token>` برمز JWT صالح تم الحصول عليه من نقطة نهاية المصادقة.*

---

## الاستجابة الناجحة (JSON)

عند **إهمال** معامل `format`، تُعيد واجهة البرمجة حمولة JSON تصف كائن القائمة.

```json
{
  "ListObject": {
    "AutoFilter": {
      "FilterColumns": [],
      "Range": "B2:F11",
      "Sorter": {
        "CaseSensitive": false,
        "HasHeaders": false,
        "KeyList": [],
        "SortLeftToRight": false
      }
    },
    "DisplayName": "Table3",
    "StartColumn": 1,
    "StartRow": 1,
    "EndColumn": 5,
    "EndRow": 10,
    "ListColumns": [
      {
        "Name": "Column1",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 1,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$B$2:$B$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column2",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 2,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$C$2:$C$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column3",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 3,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$D$2:$D$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column4",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 4,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$E$2:$E$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column5",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 5,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$F$2:$F$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      }
    ],
    "ShowHeaderRow": true,
    "ShowTableStyleColumnStripes": false,
    "ShowTableStyleFirstColumn": false,
    "ShowTableStyleLastColumn": false,
    "ShowTableStyleRowStripes": true,
    "ShowTotals": false,
    "TableStyleName": "None",
    "TableStyleType": "None",
    "link": {
      "Href": "api-qa.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

عند **توفير** معامل `format`، يكون محتوى جسم الاستجابة تدفقًا ثنائيًا من نوع الملف المطلوب (مثل `Content-Type: text/csv`).

---

## معالجة الأخطاء

| رمز HTTP | المعنى | مثال JSON |
|----------|---------|------------|
| **400** | طلب غير صالح – معاملات مفقودة أو غير صالحة. | `{"Code":400,"Message":"Invalid format parameter."}` |
| **401** | غير مُصرّح – رمز JWT مفقود أو غير صالح. | `{"Code":401,"Message":"Authentication failed."}` |
| **404** | غير موجود – ملف جدول البيانات أو ورقة العمل أو كائن القائمة غير موجود. | `{"Code":404,"Message":"ListObject not found."}` |
| **500** | خطأ داخلي في الخادم. | `{"Code":500,"Message":"Unexpected server error."}` |

### أخطاء شائعة (ملاحظات)

* **المؤشر المعدّ من الصفر** – يبدأ `listobjectindex` من **0**. ولطلب المؤشر `1` سيُعاد الجدول الثاني في الورقة.  
* **المجلد والتخزين** – إذا كان ملف جدول البيانات مخزنًا في مجلد فرعي، فضُمّن معامل الاستعلام `folder` (مثل `?folder=Reports/2024`).  
* **صيغة التصدير** – لا يُسمح إلا بالصيغ المدعومة من محرك تحويل Aspose.Cells (`pdf` أو `xlsx` أو `csv` أو `json`، ...). يؤدي تزويده بقيمة غير مدعومة إلى حدوث خطأ **400**.

---

## أمثلة لـ SDKs

تُظهر المقتطفات التالية كيفية استدعاء نقطة النهاية باستخدام مكتبات SDK الرسمية لـ Aspose.Cells Cloud. استبدل القيم الوهمية (`<YOUR_CLIENT>` و `<YOUR_JWT>`، إلخ) بإعداداتك الفعلية.

<details>
<summary>💻 C#</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// تهيئة عميل واجهة البرمجة
var apiInstance = new ListObjectsApi();

// بناء الطلب
var request = new GetWorksheetListObjectRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: null,               // مثلًا "csv" للتصدير
    folder: null,
    storageName: null
);

// تنفيذ الطلب
var response = apiInstance.GetWorksheetListObject(request);
Console.WriteLine(response);
```
</details>

<details>
<summary>☕ Java</summary>

```java
import com.aspose.cells.cloud.api.ListObjectsApi;
import com.aspose.cells.cloud.model.*;
import com.aspose.cells.cloud.model.requests.*;

public class GetWorksheetListObjectExample {
    public static void main(String[] args) throws ApiException {
        ListObjectsApi apiInstance = new ListObjectsApi();

        GetWorksheetListObjectRequest request = new GetWorksheetListObjectRequest(
                "Book1.xlsx",   // name
                "Sheet1",       // sheetName
                1,              // listobjectindex
                null,           // format
                null,           // folder
                null            // storageName
        );

        ListObjectResponse result = apiInstance.getWorksheetListObject(request);
        System.out.println(result);
    }
}
```
</details>

<details>
<summary>🐍 Python</summary>

```python
from asposecellscloud.apis.list_objects_api import ListObjectsApi
from asposecellscloud.models import GetWorksheetListObjectRequest

api = ListObjectsApi()

request = GetWorksheetListObjectRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    listobjectindex=1,
    format=None,
    folder=None,
    storage_name=None
)

response = api.get_worksheet_list_object(request)
print(response)
```
</details>

<details>
<summary>🟢 Node.js (TypeScript)</summary>

```typescript
import { ListObjectsApi, GetWorksheetListObjectRequest } from "@asposecellscloud/asposecellscloud";

const api = new ListObjectsApi();

const request = new GetWorksheetListObjectRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: undefined,
    folder: undefined,
    storageName: undefined
});

api.getWorksheetListObject(request)
   .then(response => console.log(response))
   .catch(err => console.error(err));
```
</details>

<details>
<summary>🐘 PHP</summary>

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

use Aspose\Cells\Cloud\Api\ListObjectsApi;
use Aspose\Cells\Cloud\Model\Requests\GetWorksheetListObjectRequest;

$listObjectsApi = new ListObjectsApi();

$request = new GetWorksheetListObjectRequest(
    "Book1.xlsx",   // name
    "Sheet1",       // sheetName
    1,              // listobjectindex
    null,           // format
    null,           // folder
    null            // storageName
);

$response = $listObjectsApi->getWorksheetListObject($request);
print_r($response);
?>
```
</details>

<details>
<summary>💎 Ruby</summary>

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::ListObjectsApi.new

request = AsposeCellsCloud::GetWorksheetListObjectRequest.new(
  name: 'Book1.xlsx',
  sheet_name: 'Sheet1',
  listobjectindex: 1,
  format: nil,
  folder: nil,
  storage_name: nil
)

result = api_instance.get_worksheet_list_object(request)
puts result
```
</details>

<details>
<summary>🦪 Go</summary>

```go
package main

import (
    "fmt"
    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
)

func main() {
    cfg := cells.NewConfiguration()
    cfg.AddDefaultHeader("Authorization", "Bearer <your_jwt>")
    client := api.NewAPIClient(cfg)

    request := api.GetWorksheetListObjectRequest{
        Name:            "Book1.xlsx",
        SheetName:       "Sheet1",
        Listobjectindex: 1,
        Format:          nil,
        Folder:          nil,
        StorageName:     nil,
    }

    result, _, err := client.ListObjectsApi.GetWorksheetListObject(request)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Printf("%+v\n", result)
}
```
</details>

---

## انظر أيضًا

| نقطة نهاية ذات صلة | الوصف |
|--------------------|--------|
| **إضافة كائن قائمة** | `POST /cells/{name}/worksheets/{sheetName}/listobjects` – إنشاء جدول جديد. |
| **تحديث كائن القائمة** | `PUT /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` – تعديل خصائص الجدول. |
| **حذف كائن القائمة** | `DELETE /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` – إزالة جدول. |
| **سرد جميع كائنات القوائم** | `GET /cells/{name}/worksheets/{sheetName}/listobjects` – سرد الجداول في ورقة عمل. |

---

## المراجع

* **مواصفات OpenAPI** – <https://apireference.aspose.cloud/cells/#/ListObjects/GetWorksheetListObject>  
* **دليل المصادقة** – <https://docs.aspose.cloud/cells/authentication/>  
* **مستودع GitHub (SDKs)** – <https://github.com/aspose-cells-cloud>  

---
---