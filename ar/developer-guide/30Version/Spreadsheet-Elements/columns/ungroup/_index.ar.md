---
title: إلغاء تجميع الأعمدة في Excel – واجهة برمجة تطبيقات Aspose.Cells Cloud  
description: إزالة تجميع الأعمدة في ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API (الإصدار 3.0). تتضمن النقطة النهائية (endpoint)، والمُعاملات المطلوبة، وطريقة المصادقة، ومثال باستخدام cURL، وتنسيق الاستجابة، وأجزاء كود SDK.  
keywords: Aspose.Cells، إلغاء التجميع، أعمدة، Excel، API، REST، سحابة، SDK  
slug: columns/ungroup  
date: 2026-07-30  
---  

# إلغاء تجميع الأعمدة في Excel  

تقدم Aspose.Cells Cloud عملية **POST** تُزيل تجميع الأعمدة من ورقة عمل محددة. تفصّل هذه الصفحة تنسيق الطلب، والمعاملات المطلوبة، وطريقة المصادقة، والأمثلة على الاستدعاءات، واستخدام SDK.

---  

## المتطلبات المسبقة  

| المتطلب | السبب في الحاجة إليه |
|----------|---------------------|
| **حساب Aspose Cloud** | للوصول إلى خدمات Aspose.Cells Cloud. |
| **رمز وصول JWT** | يجب تفويض جميع مكالمات API باستخدام رمز bearer. راجع [دليل مصادقة JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **ملف المصنف مخزن في مستودع Aspose Cloud** | تعمل الواجهة على الملفات الموجودة في مستودع السحابة (أو المستودع الخارجي المتصل). |
| **اسم ورقة العمل** | يجب أن توجد ورقة العمل المستهدفة داخل المصنف. |

---  

## المصادقة  

تتطلب جميع الطلبات رأس **Authorization** يحتوي على رمز JWT صالح:

```http
Authorization: Bearer <access_token>
```

يتم الحصول على الرمز عبر تدفق OAuth الخاص بـ Aspose Cloud. تكون الرموز صالحة لفترة محدودة؛ قم بتحديثها حسب الحاجة.

---  

## النقطة النهائية (Endpoint)  

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/ungroup
```

* `{name}` – **Path** – اسم ملف المصنف (مثل `test.xlsx`).  
* `{sheetName}` – **Path** – اسم ورقة العمل (مثل `Sheet1`).  

---  

## المُعاملات  

### مُعاملات المسار (Path Parameters)  

| الاسم | النوع | مطلوب | الوصف |
|------|------|-------|--------|
| `name` | string | نعم | اسم ملف المصنف. |
| `sheetName` | string | نعم | اسم ورقة العمل. |

### مُعاملات الاستعلام (Query Parameters)  

| الاسم | النوع | مطلوب | الوصف |
|------|------|-------|--------|
| `firstIndex` | integer | نعم | الفهرس بصفر كأساس لأول عمود سيتم إلغاء تجميعه. |
| `lastIndex` | integer | نعم | الفهرس بصفر كأساس لأخر عمود سيتم إلغاء تجميعه. |
| `folder` | string | لا | مسار المجلد الذي يحتوي على المصنف. |
| `storageName` | string | لا | اسم خدمة التخزين حيث يوجد الملف. |

---  

## مثال على الطلب (cURL)  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/ungroup?firstIndex=1&lastIndex=5" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

*استبدل `<access_token>` برمز JWT صالح.*

---  

## الاستجابة الناجحة  

```json
{
  "Code": 200,
  "Status": "OK",
  "Columns": {
    "FirstIndex": 1,
    "LastIndex": 5
  }
}
```

يحتوي كائن الاستجابة (`CellsCloudResponse`) على نطاق الأعمدة التي تم إلغاء تجميعها بنجاح.

### استجابة الخطأ  

عند فشل الطلب، تُرجع الخدمة حمولة JSON تحتوي على الحقول التالية:

| الحقل | المعنى |
|------|--------|
| `Code` | رمز خطأ على نمط HTTP (مثل 400، 401). |
| `Status` | وصف مختصر للخطأ. |
| `ErrorMessage` | وصف مفصّل للخطأ. |

---  

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|------|--------|-------|
| 200 | OK | تم تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | Bad Request | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | Unauthorized | رمز JWT غير صالح أو مفقود. |
| 413 | Payload Too Large | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500 | Internal Server Error | خطأ غير متوقع في الخادم. |
---  

## أجزاء كود SDK  

فيما يلي مقاطع جاهزة للتشغيل لأشهر SDKs. استبدل القيم المُوضعية (`<YourAccessToken>`، `<YourFileName>`، إلخ) ببياناتك الخاصة.

<details><summary>**C# (.NET)**</summary>  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "<YourAccessToken>",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        var response = cellsApi.PostUngroupWorksheetColumns(
            name: "test.xlsx",
            sheetName: "Sheet1",
            firstIndex: 1,
            lastIndex: 5,
            folder: null,
            storageName: null);

        Console.WriteLine($"Ungrouped columns: {response.Columns.FirstIndex} – {response.Columns.LastIndex}");
    }
}
```
</details>

<details><summary>**Java**</summary>  

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.CellsCloudResponse;
import com.aspose.cells.cloud.Configuration;

public class UngroupColumns {
    public static void main(String[] args) throws Exception {
        Configuration config = new Configuration();
        config.setAccessToken("<YourAccessToken>");
        config.setBaseUrl("https://api.aspose.cloud");
        CellsApi api = new CellsApi(config);

        CellsCloudResponse resp = api.postUngroupWorksheetColumns(
            "test.xlsx",
            "Sheet1",
            1,
            5,
            null,
            null);

        System.out.println("Ungrouped columns: " + resp.getColumns().getFirstIndex()
                           + " – " + resp.getColumns().getLastIndex());
    }
}
```
</details>

<details><summary>**Python**</summary>  

```python
from asposecellscloud import CellsApi, Configuration

config = Configuration()
config.access_token = "<YourAccessToken>"
config.base_url = "https://api.aspose.cloud"

api = CellsApi(config)

response = api.post_ungroup_worksheet_columns(
    name="test.xlsx",
    sheet_name="Sheet1",
    first_index=1,
    last_index=5,
    folder=None,
    storage_name=None)

print(f"Ungrouped columns: {response.columns.first_index} – {response.columns.last_index}")
```
</details>

<details><summary>**Node.js**</summary>  

```javascript
const { CellsApi, Configuration } = require('asposecellscloud');

const config = new Configuration({
    accessToken: "<YourAccessToken>",
    baseUrl: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postUngroupWorksheetColumns("test.xlsx", "Sheet1", 1, 5, null, null)
   .then(resp => {
       console.log(`Ungrouped columns: ${resp.columns.firstIndex} – ${resp.columns.lastIndex}`);
   })
   .catch(err => console.error(err));
```
</details>

<details><summary>**Go**</summary>  

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AccessToken = "<YourAccessToken>"
    config.BasePath = "https://api.aspose.cloud"

    api := sdk.NewCellsApi(config)

    resp, _, err := api.PostUngroupWorksheetColumns(
        "test.xlsx",
        "Sheet1",
        1,
        5,
        nil,
        nil,
    )
    if err != nil {
        panic(err)
    }
    fmt.Printf("Ungrouped columns: %d – %d\n", resp.Columns.FirstIndex, resp.Columns.LastIndex)
}
```
</details>

> **ملاحظة:** SDKs لـ PHP، Ruby، Perl، ولغات أخرى تتبع نفس ترتيب المُعاملات. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للأمثلة الكاملة.

---  

## المراجع  

* **مواصفات OpenAPI:** <https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetColumns>  
* **دليل المصادقة:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
* **مستودع SDK:** <https://github.com/aspose-cells-cloud>

---  

## تاريخ المراجعة  

| التاريخ | الكاتب | التغيير |
|---------|--------|---------|
| 2026‑07‑30 | AI Optimizer | إصلاح ترميز UTF‑8، إضافة المتطلبات المسبقة، تنظيف كلمات المفتاحية، تحسين تسلسل العناوين، وإدراج أجزاء كود SDK. |
| 2026‑07‑29 | الأصلي | المسودة الأولية للتوثيق. |

---