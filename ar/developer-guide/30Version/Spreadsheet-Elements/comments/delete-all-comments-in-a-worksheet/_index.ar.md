---
title: "حذف جميع تعليقات ورقة العمل"
description: "احذف جميع التعليقات من ورقة عمل في ملف Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud. تعلّم عن نقطة النهاية DELETE، والمعطيات المطلوبة، والمصادقة، وطلب cURL النموذجي، وصيغة الاستجابة، وأكواد الأخطاء، وأمثلة SDK."
keywords: "Aspose, Cells, حذف التعليقات, ورقة العمل, API, REST, Excel, cloud"
url: /comments/clear/
aliases:
  - /delete-all-comments-in-a-worksheet/
weight: 50
---

# حذف جميع تعليقات ورقة العمل

**إصدار الواجهة:** `v3.0`  
**المورد:** `Worksheets` → `DeleteWorksheetComments`  

تقدم Aspose.Cells Cloud نقطة نهاية REST قوية تُزيل **جميع** التعليقات من ورقة عمل مُحددة. هذه العملية غير قابلة للعكس؛ وبمجرد تنفيذها، لا يمكن استعادة التعليقات.

---

## المتطلبات المسبقة

| المتطلب | التفاصيل |
|----------|----------|
| **المصادقة** | مطلوب رمز وصول JWT صالح في رأس `Authorization` (`Bearer <jwt token>`). احصل على الرمز عبر [عملية مصادقة OAuth2](https://docs.aspose.cloud/cells/authentication/). |
| **المخزن** | يجب أن يكون الملف موجودًا في مخزن يمكن الوصول إليه من قِبل Aspose.Cells Cloud (يُستخدم المخزن الافتراضي إذا تم حذف `storageName`). |
| **الأذونات** | يجب أن يمتلك الرمز إذن قراءة وكتابة الملف المستهدف. |
| **حزم SDK (اختياري)** | تتوفر حزم SDK لـ .NET وJava وPHP وRuby وNode.js وPython وPerl وGo (انظر قسم **أمثلة SDK**). |

---

## طلب HTTP

### نقطة النهاية

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments
```

### معطيات المسار

| الاسم        | النوع   | الوصف |
|-------------|---------|--------|
| `name`      | نص (string) | اسم ملف Excel (مثل `test.xlsx`). |
| `sheetName` | نص (string) | اسم ورقة العمل (مثل `Sheet1`). |

### معطيات الاستعلام

| الاسم          | النوع   | الإلزام | الوصف |
|----------------|---------|---------|--------|
| `folder`       | نص (string) | اختياري | مسار المجلد الذي يحتوي على الملف. |
| `storageName`  | نص (string) | اختياري | اسم المخزن الذي يوجد فيه الملف. |

### رؤوس الطلب

| الرأس                   | القيمة                              |
|--------------------------|-------------------------------------|
| `Authorization`          | `Bearer <jwt token>`                |
| `Accept`                 | `application/json`                  |
| `Content-Type`           | `application/json`                  |

---

## مثال على الطلب (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments?folder=Documents&storageName=MyStorage" \
  -X DELETE \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*استبدل `test.xlsx` و`Sheet1` و`Documents` و`MyStorage` و`<jwt token>` بقيمك الفعلية.*

---

## الاستجابة

### نجاح (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

يتوافق نص الاستجابة مع نموذج `CellsCloudResponse`.

### استجابات الأخطاء

| كود HTTP | المعنى                          | مثال على النص |
|----------|----------------------------------|----------------|
| **400**  | طلب خاطئ – معطيات غير صحيحة.   | `{ "Code": 400, "Message": "Invalid request." }` |
| **401**  | عدم مصادقة – رمز JWT مفقود أو غير صالح. | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**  | غير موجود – الملف أو ورقة العمل غير موجودة. | `{ "Code": 404, "Message": "Resource not found." }` |
| **500**  | خطأ داخلي في الخادم.             | `{ "Code": 500, "Message": "Server error." }` |

---

## أمثلة باستخدام حزم SDK

توضح المقاطع التالية كيفية استدعاء نقطة النهاية باستخدام حزم SDK الرسمية لـ Aspose.Cells Cloud (الإصدار 3.13.0). استبدل القيم الوهمية (`<fileName>` و`<sheet>` و`<jwt token>`، إلخ) ببياناتك الخاصة.

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new WorksheetsApi();
var name = "test.xlsx"; // string | اسم الملف.
var sheetName = "Sheet1"; // string | اسم ورقة العمل.
var folder = "Documents"; // string | مسار المجلد (اختياري)
var storageName = "MyStorage"; // string | اسم المخزن (اختياري)

try
{
    var response = apiInstance.DeleteWorksheetComments(name, sheetName, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling WorksheetsApi.DeleteWorksheetComments: " + e.Message );
}
```

### Java  

```java
import com.aspose.cells.cloud.sdk.api.WorksheetsApi;
import com.aspose.cells.cloud.sdk.model.*;

public class DeleteWorksheetComments {
    public static void main(String[] args) {
        WorksheetsApi api = new WorksheetsApi();
        String name = "test.xlsx";
        String sheetName = "Sheet1";
        String folder = "Documents";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse resp = api.deleteWorksheetComments(name, sheetName, folder, storageName);
            System.out.println(resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### PHP  

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

use Aspose\Cells\Cloud\Api\WorksheetsApi;

$apiInstance = new WorksheetsApi();
$name = "test.xlsx";
$sheetName = "Sheet1";
$folder = "Documents";
$storageName = "MyStorage";

try {
    $result = $apiInstance->deleteWorksheetComments($name, $sheetName, $folder, $storageName);
    echo $result->getStatus();
} catch (Exception $e) {
    echo 'Exception when calling WorksheetsApi->deleteWorksheetComments: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Ruby  

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::WorksheetsApi.new
name = 'test.xlsx'
sheet_name = 'Sheet1'
folder = 'Documents'          # اختياري
storage_name = 'MyStorage'    # اختياري

begin
  result = api_instance.delete_worksheet_comments(name, sheet_name, folder, storage_name)
  puts result.status
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling WorksheetsApi->delete_worksheet_comments: #{e}"
end
```

### Node.js (TypeScript)  

```typescript
import { WorksheetsApi } from "@asposecloud/cells-sdk";

const api = new WorksheetsApi();
const name = "test.xlsx";
const sheetName = "Sheet1";
const folder = "Documents";
const storageName = "MyStorage";

api.deleteWorksheetComments(name, sheetName, folder, storageName)
    .then((response) => console.log(response.status))
    .catch((error) => console.error("Error:", error));
```

### Python  

```python
from asposecellscloud import WorksheetsApi

api_instance = WorksheetsApi()
name = "test.xlsx"
sheet_name = "Sheet1"
folder = "Documents"          # اختياري
storage_name = "MyStorage"    # اختياري

try:
    response = api_instance.delete_worksheet_comments(name, sheet_name, folder, storage_name)
    print(response.status)
except Exception as e:
    print("Exception when calling WorksheetsApi->delete_worksheet_comments:", e)
```

### Perl  

```perl
use AsposeCellsCloud::Api::WorksheetsApi;

my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new();

my $name = 'test.xlsx';
my $sheet_name = 'Sheet1';
my $folder = 'Documents';
my $storage_name = 'MyStorage';

eval {
    my $result = $api_instance->delete_worksheet_comments(
        name => $name,
        sheet_name => $sheet_name,
        folder => $folder,
        storage_name => $storage_name
    );
    print $result->{status}, "\n";
};
if ($@) {
    print "Exception when calling WorksheetsApi->delete_worksheet_comments: $@\n";
}
```

### Go  

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    cfg := sdk.NewConfiguration()
    cfg.AddDefaultHeader("Authorization", "Bearer <jwt token>")
    api := sdk.NewWorksheetsApi(cfg)

    name := "test.xlsx"
    sheetName := "Sheet1"
    folder := "Documents"
    storageName := "MyStorage"

    resp, _, err := api.DeleteWorksheetComments(name, sheetName, folder, storageName)
    if err != nil {
        fmt.Printf("Error: %v\n", err)
        return
    }
    fmt.Println(resp.Status)
}
```

---

## ملاحظات وقيود

* تُحذف هذه العملية **جميع التعليقات** في ورقة العمل المحددة. استخدمها بحذر؛ لا توجد خاصية تراجع (Undo).
* لا يقبل الطلب **نصًا للطلب**؛ وتُعبَّر جميع المعلومات المطلوبة عبر عنوان URL والرؤوس.
* إذا كان الملف المستهدف **محميًا** أو كانت ورقة العمل **مقروءة فقط**، فستُعيد الواجهة خطأ `400` أو `401` حسب السبب الكامن وراء الخطأ.
* تعمل نقطة النهاية مع الملفات المخزنة في **Aspose Cloud Storage**، وكذلك مع **Amazon S3** أو **Azure Blob** أو **Google Cloud Storage** عند الإشارة إليها بشكل صحيح عبر `storageName`.

---

## موارد ذات صلة

* **مواصفات OpenAPI** – [DeleteWorksheetComments](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComments)
* **دليل المصادقة** – [OAuth2 لـ Aspose.Cells Cloud](https://docs.aspose.cloud/cells/authentication/)
* **مستودع SDK** – <https://github.com/aspose-cells-cloud>
* **واجهة برمجة تطبيقات ورقات العمل العامة** – <https://docs.aspose.cloud/cells/worksheets/>

---

*آخر تحديث: 2026‑07‑30*