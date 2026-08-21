---
title: "API حذف تعليق ورقة العمل – Aspose.Cells Cloud"
description: "احذف تعليق خلية محددة في ورقة عمل Excel باستخدام REST API الخاص بـ Aspose.Cells Cloud (الإصدار 3.0). يتضمن الرابط المُوجّه، المَعَالِم، أمثلة للطلبات والاستجابات، مقاطع كود SDK، ومعالجة الأخطاء."
keywords: "Aspose.Cells, حذف تعليق, API Excel, REST, تعليق ورقة عمل"
date: "2026-07-30"
lastModified: "2026-07-30"
---

# API حذف تعليق ورقة العمل – Aspose.Cells Cloud

> **آخر تحديث للصفحة:** 30 يوليو، 2026  

## نظرة عامة
الـ **تعليق** هو ملاحظة نصية مُرفقة بخلية محددة في ورقة عمل Excel.  
يعمل عملية **حذف تعليق ورقة العمل** على إزالة التعليق من الخلية المحددة.

![Aspose.Cells Cloud – مخطط توضيحي لحذف تعليق ورقة العمل](/cells/images/Aspose-image-for-open-graph.jpg "Aspose.Cells Cloud – API حذف تعليق ورقة العمل")

## المصادقة
تتطلب جميع نقاط نهاية Aspose.Cells Cloud **المصادقة باستخدام رمز JWT**.  
أدرج الرمز في رأس `Authorization`:

```
Authorization: Bearer <jwt token>
```

للحصول على تفاصيل حول كيفية الحصول على رمز JWT، راجع [دليل المصادقة](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## المتطلبات المسبقة
- رمز وصول JWT سارٍ.  
- يجب أن يكون ملف المصنف المستهدف (`{name}`) موجودًا في موقع التخزين المُحدد.  
- اختياري: أحد SDKs الخاصة بـ Aspose.Cells Cloud المُثبَّتة للغة البرمجة التي تفضّلها.

## طلب HTTP

### نقطة النهاية
```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### مَعَالِم المسار
| المعامل | النوع | مطلوب | الوصف |
|---------|-------|-------|--------|
| `name`      | نص | ✅ | اسم ملف Excel (مثل `test.xlsx`). |
| `sheetName` | نص | ✅ | اسم ورقة العمل التي تحتوي على التعليق. |
| `cellName`  | نص | ✅ | عنوان الخلية التي سيتم حذف تعليقها (مثل `A1`). |

### مَعَالِم الاستعلام
| المعامل     | النوع | مطلوب | الوصف |
|-------------|-------|-------|--------|
| `folder`      | نص | ❌ | مسار المجلد حيث يُخزَّن المصنف. إذا تُرك فارغًا، يُستخدم المجلد الجذر. |
| `storageName` | نص | ❌ | اسم خدمة التخزين (مثل `MyCloud`). إذا تُرك فارغًا، تُستخدم خدمة التخزين الافتراضية. |

## مثال على الطلب

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

## الاستجابة

### نجاح (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                      |
|-------|----------------------------|---------------------------------------------|
| 200   | OK (نجاح)                 | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | Bad Request (طلب غير صالح) | معالِمات ناقصة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401   | Unauthorized (غير مصرّح)   | رمز JWT غير صالح أو مفقود. |
| 413   | Payload Too Large (حمولة كبيرة جدًا) | تجاوز حجم الملف المرفوع الحد المسموح. |
| 500   | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم. |
### استجابات الأخطاء

| رمز HTTP | الوصف | مثال |
|----------|-------|------|
| 400 | طلب غير صالح – معالِمات ناقصة أو معطوبة. | `{ "Code": 400, "Message": "Invalid parameters." }` |
| 401 | غير مصرّح – رمز غير صالح أو مفقود. | `{ "Code": 401, "Message": "Authentication required." }` |
| 404 | غير موجود – الملف أو ورقة العمل أو التعليق غير موجود. | `{ "Code": 404, "Message": "Resource not found." }` |
| 500 | خطأ داخلي في الخادم – حالة غير متوقعة على الخادم. | `{ "Code": 500, "Message": "Server error." }` |

## أمثلة باستخدام SDKs
فيما يلي مقاطع جاهزة للتشغيل باللغات الأكثر شيوعًا. استبدل `<jwt token>` و`test.xlsx` و`Sheet1` و`A1` بقيمك الخاصة.

### C#
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using Aspose.Cells.Cloud.SDK.Client;

// Configure the API client
var config = new Configuration
{
    AccessToken = "<jwt token>",
    BasePath = "https://api.aspose.cloud"
};

var apiInstance = new WorksheetsApi(config);
try
{
    var result = apiInstance.DeleteWorksheetComment(
        name: "test.xlsx",
        sheetName: "Sheet1",
        cellName: "A1",
        folder: "Docs",
        storageName: "MyStorage"
    );
    Console.WriteLine("Comment deleted. Status: " + result.Status);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling WorksheetsApi.DeleteWorksheetComment: " + e.Message);
}
```

### Java
```java
import com.aspose.cloud.cells.api.WorksheetsApi;
import com.aspose.cloud.cells.client.ApiException;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class DeleteWorksheetCommentExample {
    public static void main(String[] args) {
        WorksheetsApi api = new WorksheetsApi();
        api.getApiClient().setAccessToken("<jwt token>");
        try {
            CellsCloudResponse response = api.deleteWorksheetComment(
                "test.xlsx",
                "Sheet1",
                "A1",
                "Docs",
                "MyStorage"
            );
            System.out.println("Deleted comment, status: " + response.getStatus());
        } catch (ApiException e) {
            System.err.println("Exception when calling WorksheetsApi#deleteWorksheetComment");
            e.printStackTrace();
        }
    }
}
```

### PHP
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAccessToken('<jwt token>');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new Aspose\Cells\Api\WorksheetsApi(
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->deleteWorksheetComment(
        'test.xlsx',
        'Sheet1',
        'A1',
        'Docs',
        'MyStorage'
    );
    echo "Comment deleted. Status: " . $result->getStatus();
} catch (Exception $e) {
    echo 'Exception when calling WorksheetsApi->deleteWorksheetComment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Ruby
```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '<jwt token>'
config.host = 'https://api.aspose.cloud'

api_instance = AsposeCellsCloud::WorksheetsApi.new
begin
  result = api_instance.delete_worksheet_comment('test.xlsx', 'Sheet1', 'A1', 'Docs', 'MyStorage')
  puts "Comment deleted – status: #{result.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling WorksheetsApi->delete_worksheet_comment: #{e}"
end
```

### Node.js (TypeScript)
```typescript
import { WorksheetsApi, Configuration } from "@asposecloud/cells-cloud";

const config = new Configuration({
    accessToken: "<jwt token>",
    basePath: "https://api.aspose.cloud"
});

const api = new WorksheetsApi(config);

api.deleteWorksheetComment("test.xlsx", "Sheet1", "A1", "Docs", "MyStorage")
    .then((response) => {
        console.log("Comment deleted. Status:", response.status);
    })
    .catch((error) => {
        console.error("Error deleting comment:", error);
    });
```

### Python
```python
from asposecellscloud.apis import WorksheetsApi
from asposecellscloud import Configuration, ApiClient

config = Configuration()
config.access_token = "<jwt token>"
config.host = "https://api.aspose.cloud"

api_client = ApiClient(configuration=config)
api = WorksheetsApi(api_client)

try:
    response = api.delete_worksheet_comment(
        name="test.xlsx",
        sheet_name="Sheet1",
        cell_name="A1",
        folder="Docs",
        storage_name="MyStorage"
    )
    print("Comment deleted. Status:", response.status)
except Exception as e:
    print("Exception when calling WorksheetsApi->delete_worksheet_comment:", e)
```

### Perl
```perl
use AsposeCellsCloud::Api::WorksheetsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    access_token => '<jwt token>',
    host => 'https://api.aspose.cloud'
);
my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new($config);

eval {
    my $result = $api_instance->delete_worksheet_comment(
        name        => 'test.xlsx',
        sheet_name  => 'Sheet1',
        cell_name   => 'A1',
        folder      => 'Docs',
        storage_name=> 'MyStorage'
    );
    print "Comment deleted. Status: " . $result->{status} . "\n";
};
if ($@) {
    warn "Exception when calling WorksheetsApi->delete_worksheet_comment: $@\n";
}
```

### Go
```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/api"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/config"
)

func main() {
    cfg := config.NewConfiguration()
    cfg.AccessToken = "<jwt token>"
    cfg.Host = "https://api.aspose.cloud"

    apiInstance := api.NewWorksheetsApi(cfg)

    result, _, err := apiInstance.DeleteWorksheetComment(
        "test.xlsx",   // name
        "Sheet1",      // sheetName
        "A1",          // cellName
        "Docs",        // folder (optional)
        "MyStorage",   // storageName (optional)
    )
    if err != nil {
        fmt.Printf("Error when calling DeleteWorksheetComment: %v\n", err)
        return
    }
    fmt.Printf("Comment deleted. Status: %s\n", result.Status)
}
```

## العمليات ذات الصلة
- [إضافة تعليق لورقة عمل](/comments/add/)  
- [تحديث تعليق ورقة عمل](/comments/update/)  

## تحديد معدل الطلبات
تفرض Aspose.Cells Cloud **حدًا أقصى قدره 100 طلب في الدقيقة لكل حساب** افتراضيًا. يؤدي تجاوز هذا الحد إلى استجابة HTTP 429 (Too Many Requests). نفّذ خوارزمية التأخير الأسي (exponential back-off) أو التزم برأس `Retry-After` لتفادي التقييد.

## انظر أيضًا
- **مواصفات OpenAPI:** <https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComment>  
- **دليل المصادقة:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **مستودع SDKs:** <https://github.com/aspose-cells-cloud>  

---