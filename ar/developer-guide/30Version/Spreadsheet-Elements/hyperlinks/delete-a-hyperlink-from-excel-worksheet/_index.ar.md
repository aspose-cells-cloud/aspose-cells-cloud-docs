---
title: "حذف رابط تشعبي في ورقة العمل"
type: docs
url: /ar/hyperlinks/delete/
description: "احذف رابطًا تشعبيًا في ورقة عمل حسب المؤشر باستخدام واجهة Aspose.Cells Cloud API. تعلّم المعلمات المطلوبة، وطريقة المصادقة، وشاهد أمثلة للكود بلغات C#، Java، Python، والمزيد."
keywords: "Aspose.Cells، Cloud، حذف رابط تشعبي، Excel API، REST، رابط تشعبي في ورقة العمل"
ArticleTitle: "حذف رابط تشعبي في ورقة العمل – وثائق Aspose.Cells Cloud API"
weight: 40
---

تقوم هذه الواجهة البرمجية REST بحذف رابط تشعبي في ورقة عمل Excel حسب مؤشره.

## الأمان والمصادقة
تتطلب واجهات Aspose.Cells Cloud API مصادقة مبنية على رمز [JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) لتكون آمنة.

### واجهة REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

### معلمات الطلب

| اسم المعلمة     | النوع    | الموقع | مطلوب | الوصف                                                    |
| ------------------ | ------- | -------- | -------- | -------------------------------------------------------------- |
| **name**           | نص    | المسار     | ✅       | اسم ملف Excel.                                    |
| **sheetName**      | نص  | المسار     | ✅       | اسم ورقة العمل.                                         |
| **hyperlinkIndex** | عدد صحيح | المسار     | ✅       | المؤشر البسيط (من الصفر) للرابط التشعبي المراد حذفه.                   |
| **folder**         | نص  | الاستعلام    | ❌       | المجلد الذي يحتوي على المستند (الافتراضي: الجذر).                |
| **storageName**    | نص  | الاستعلام    | ❌       | اسم خدمة التخزين (يُستخدم التخزين الافتراضي إذا تُركت فارغة). |

#### الاستجابات

| رمز الحالة                   | الوصف                                             | محتوى الاستجابة (مثال)                                       |
| ----------------------------- | ------------------------------------------------------- | -------------------------------------------------- |
| **200 OK**                    | تم حذف الرابط التشعبي بنجاح.                         | `{"Code":200,"Status":"OK"}`                       |
| **400 Bad Request**           | معلمات ناقصة أو غير صالحة.                          | `{"Code":400,"Message":"hyperlinkIndex غير صالح."}` |
| **401 Unauthorized**          | رمز المصادقة ناقص أو غير صالح.             | `{"Code":401,"Message":"رمز وصول غير صالح."}`   |
| **404 Not Found**             | الملف أو ورقة العمل أو مؤشر الرابط التشعبي غير موجود. | `{"Code":404,"Message":"المورد غير موجود."}`     |
| **500 Internal Server Error** | خطأ غير متوقع في الخادم.                                | `{"Code":500,"Message":"خطأ داخلي في الخادم."}`  |

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Hypelinks/DeleteWorksheetHyperlink) واجهة برمجة قابلة للوصول العام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر `cURL` للوصول إلى خدمات Aspose.Cells عبر الويب بسهولة. يوضح المثال التالي كيفية استدعاء الواجهة باستخدام `cURL`.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test1.xlsx/worksheets/Sheet1/hyperlinks/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK للسحابة

استخدام SDK هو أسرع طريقة للتطوير. فتتولى SDK إدارة التفاصيل من المستوى المنخفض، مما يتيح لك التركيز على مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تعرض أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر SDKs مختلفة. وُضعت اقتباسات مباشرة داخل الكود لضمان الموثوقية، مع الاحتفاظ برابط مباشر للنسخة الأصلية على Gist للرجوع إليها.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// ExampleDeleteWorksheetHyperlink.cs
// Source: https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("<client_id>", "<client_secret>");
var response = apiInstance.DeleteWorksheetHyperlink(
    name: "test1.xlsx",
    sheetName: "Sheet1",
    hyperlinkIndex: 0,
    folder: null,
    storageName: null);
Console.WriteLine(response.Status);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Example_DeleteWorksheetHyperlink.java
// Source: https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

CellsApi api = new CellsApi("<client_id>", "<client_secret>");
ApiResponse<Void> response = api.deleteWorksheetHyperlink(
    "test1.xlsx",
    "Sheet1",
    0,
    null,
    null);
System.out.println("Status: " + response.getStatusCode());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// Example_DeleteWorksheetHyperlink.php
// Source: https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152
require_once('vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppSid('<client_id>');
$config->setAppKey('<client_secret>');

$apiInstance = new Aspose\Cells\Api\CellsApi($config);
$response = $apiInstance->deleteWorksheetHyperlink(
    "test1.xlsx",
    "Sheet1",
    0,
    null,
    null);
echo $response->getStatusCode();
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Example_DeleteWorksheetHyperlink.rb
# Source: https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new('<client_id>', '<client_secret>')
result = api.delete_worksheet_hyperlink('test1.xlsx', 'Sheet1', 0)
puts result.status
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
// Example_DeleteWorksheetHyperlink.ts (Node.js)
// Source: https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0
const AsposeCellsCloud = require("asposecellscloud");
const api = new AsposeCellsCloud.CellsApi("<client_id>", "<client_secret>");

api
  .deleteWorksheetHyperlink("test1.xlsx", "Sheet1", 0, null, null)
  .then(() => console.log("Hyperlink deleted"))
  .catch((err) => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
# Example_DeleteWorksheetHyperlink.py
# Source: https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1
from asposecellscloud import CellsApi, Configuration

config = Configuration(app_sid='<client_id>', app_key='<client_secret>')
api = CellsApi(config)

api.delete_worksheet_hyperlink('test1.xlsx', 'Sheet1', 0)
print('Hyperlink deleted')
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
# Example_DeleteWorksheetHyperlink.pl
# Source: https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca
use AsposeCellsCloud::CellsApi;

my $api_instance = AsposeCellsCloud::CellsApi->new('<client_id>', '<client_secret>');
my $result = $api_instance->delete_worksheet_hyperlink(
    name => 'test1.xlsx',
    sheet_name => 'Sheet1',
    hyperlink_index => 0);
print "Status: $result->{status}\n";
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
// Example_DeleteWorksheetHyperlink.go
// Source: https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration("<client_id>", "<client_secret>")
    api := asposecellscloud.NewAPIClient(config).CellsApi
    _, err := api.DeleteWorksheetHyperlink("test1.xlsx", "Sheet1", 0, nil, nil)
    if err != nil {
        fmt.Println(err)
    } else {
        fmt.Println("Hyperlink deleted")
    }
}
```

{{< /tab >}}

{{< /tabs >}}