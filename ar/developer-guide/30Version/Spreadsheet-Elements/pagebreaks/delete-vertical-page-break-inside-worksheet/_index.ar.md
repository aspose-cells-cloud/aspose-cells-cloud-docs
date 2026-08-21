---
title: حذف فاصل الصف العمودي – واجهة Aspose.Cells Cloud REST API
description: إزالة فاصل صفحات عمودي من ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API (الإصدار v3.0). يشمل بناء الطلب، المعاملات، الأمثلة، رموز الاستجابة، وأجزاء كود SDK.
keywords: حذف فاصل الصف العمودي، Aspose.Cells Cloud، REST API
slug: delete-vertical-page-break
api_version: v3.0
---

# حذف فاصل الصف العمودي

حذف فاصل صفحات عمودي من ورقة عمل في ملف Excel باستخدام واجهة Aspose.Cells Cloud REST API.

---

## المتطلبات المسبقة

* يجب تزويد رمز **JWT للتوثيق** في الرأس `Authorization`.  
* يجب أن يكون ملف المصنف (`{name}`) مخزنًا في **المجلد** أو **التخزين** المحدَّد، وأن يكون متاحًا لعميل الواجهة البرمجية.

---

## طلب HTTP

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks/{index}
```

| المعامل | النوع | الموقع | الإلزام | الوصف |
|---------|-------|--------|--------|--------|
| **name**      | نص (string) | مسار (path) | نعم | اسم ملف Excel. |
| **sheetName** | نص (string) | مسار (path) | نعم | اسم ورقة العمل التي تحتوي على فاصل الصف. |
| **index**     | عدد صحيح (integer) | مسار (path) | نعم | الفهرس بصفر كقيمة أولية لفاصل الصف العمودي المراد حذفه. |
| **folder**    | نص (string) | استعلام (query) | لا | مسار المجلد الذي يُخزَّن فيه الملف. |
| **storageName**| نص (string) | استعلام (query) | لا | اسم خدمة التخزين. |

---

## مثال على الطلب

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/verticalpagebreaks/0?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

---

## استجابة ناجحة

| الرمز | الوصف |
|-------|--------|
| **200** | تم حذف فاصل الصف العمودي بنجاح. |

**مثال على حمولة البيانات (payload)**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

## استجابات الأخطاء

| رمز HTTP | الوصف |
|----------|--------|
| **401** | غير مُAUTHENTICATED – رمز مفقود أو غير صالح. |
| **404** | غير موجود – الملف أو ورقة العمل أو فهرس فاصل الصف المحدَّد غير موجود. |
| **400** | طلب غير صالح – بناء جملة الطلب أو المعاملات غير صحيحة. |
| **500** | خطأ داخلي في الخادم – تمت مواجهة حالة غير متوقعة. |

** أمثلة على حمولات البيانات للخطأ**

*401 – غير مُAUTHENTICATED*

```json
{
  "Code": 401,
  "Message": "رمز المصادقة غير صالح."
}
```

*404 – غير موجود*

```json
{
  "Code": 404,
  "Message": "لم يتم العثور على الملف أو ورقة العمل أو فهرس فاصل الصف المحدَّد."
}
```

*400 – طلب غير صالح*

```json
{
  "Code": 400,
  "Message": "معاملات الطلب غير صالحة أو بناؤها غير سليم."
}
```

*500 – خطأ داخلي في الخادم*

```json
{
  "Code": 500,
  "Message": "حدث خطأ غير متوقع في الخادم."
}
```

---

## أكواد أمثلة لـ SDK

تُظهر الأمثلة التالية كيفية استدعاء عملية **DeleteVerticalPageBreak** باستخدام مكتبات Aspose.Cells Cloud SDK المختلفة.

<details><summary>**C#**</summary>

```csharp
// Install-Package Aspose.Cells-Cloud
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("client_id", "client_secret");
string name = "Book1.xlsx";
string sheetName = "Sheet1";
int index = 0;
string folder = "Docs";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName);
    Console.WriteLine($"Status: {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.DeleteVerticalPageBreak: " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class DeleteVerticalPageBreak {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String folder = "Docs";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse resp = api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName);
            System.out.println("Status: " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"
api_client = ApiClient(configuration=config)
api = CellsApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
index = 0
folder = "Docs"
storage_name = "MyStorage"

try:
    response = api.delete_vertical_page_break(name, sheet_name, index, folder, storage_name)
    print("Status:", response.status)
except Exception as e:
    print("Error:", e)
```

</details>

<details><summary>**Node.js**</summary>

```javascript
const { CellsApi, ApiClient, Configuration } = require('asposecellscloud');

const config = new Configuration();
config.clientId = "client_id";
config.clientSecret = "client_secret";

const api = new CellsApi(new ApiClient(config));

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const folder = "Docs";
const storageName = "MyStorage";

api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName)
  .then(response => console.log('Status:', response.status))
  .catch(error => console.error('Error:', error));
```

</details>

<details><summary>**Go**</summary>

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration()
    config.ClientId = "client_id"
    config.ClientSecret = "client_secret"

    api := asposecellscloud.NewAPIClient(config).CellsApi
    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    folder := "Docs"
    storageName := "MyStorage"

    resp, _, err := api.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println("Status:", resp.Status)
}
```

</details>

*(تتبع أكواد SDK لـ PHP وRuby وPerl ولغات أخرى نفس النمط ومتاحة في مستودع GitHub الرسمي.)*

---

## موارد ذات صلة

* **مواصفات OpenAPI** – [DeleteVerticalPageBreak](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteVerticalPageBreak)  
* **مكتبات Aspose.Cells Cloud SDK** – <https://github.com/aspose-cells-cloud>  
* **دليل المصادقة** – <https://docs.aspose.cloud/cells/authentication/>  

--- 

*آخر تحديث للوثيقة: 2026‑07‑30*