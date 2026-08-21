---
title: إضافة CellArea إلى التنسيق الشرطي
description: إضافة منطقة خلايا إلى قاعدة تنسيق شرطي في ورقة عمل Excel باستخدام REST API الخاص بـ Aspose.Cells Cloud (الإصدار 3.0). يشمل ذلك عنوان_endpoint_، المعلمات، أمثلة باستخدام cURL وSDK، مخطط الاستجابة، ومعالجة الأخطاء.
keywords: Aspose.Cells، التنسيق الشرطي، CellArea، REST API، Excel، Cloud SDK
weight: 30
aliases:
  - /add-a-cell-area-for-format-condition/
---

# إضافة CellArea إلى التنسيق الشرطي

**الملخص** – يُضيف منطقة خلايا إلى قاعدة تنسيق شرطي موجودة بالفعل في ورقة عمل.

---

## المتطلبات المسبقة

1. **حساب Aspose.Cells Cloud** – احصل على **App SID** و**App Key**.  
2. **رمز JWT** –ولّد رمز JWT باستخدام App SID/Key (انظر [دليل المصادقة](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)).  
3. يجب أن تكون ملف Excel المستهدف موجودًا مسبقًا في المخزن/المجلد المحدد.

---

## المصادقة

تتطلب جميع الاستدعاءات **مصادقة مبنية على رمز JWT**. قم بتمرير الرمز في رأس `Authorization`:

```http
Authorization: Bearer <jwt token>
```

---

## طلب HTTP

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area
```

### معلمات المسار

| الاسم        | النوع   | الوصف                                     |
|-------------|---------|-------------------------------------------|
| `name`      | نص (string) | اسم ملف Excel (مثل `Book1.xlsx`).         |
| `sheetName` | نص (string) | اسم ورقة العمل التي تحتوي على القاعدة (مثل `Sheet1`). |
| `index`     | عدد صحيح (integer) | المؤشر المبدئي (صفر-الأساس) لقاعدة التنسيق الشرطي. |

### معلمات الاستعلام

| الاسم           | النوع   | مطلوب | الوصف                                   |
|----------------|---------|--------|------------------------------------------|
| `cellArea`     | نص (string) | **نعم** | نطاق الخلايا المراد إضافته، بصيغة A1 (مثل `A1:C3`). |
| `folder`       | نص (string) | لا     | مسار المجلد الذي يحتوي على الملف.        |
| `storageName`  | نص (string) | لا     | اسم خدمة التخزين.                        |

---

## مثال على الطلب (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/area?cellArea=A1:C3" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### الاستجابة المتوقعة عند النجاح

```json
{
  "Code": "200",
  "Status": "OK",
  "CellArea": {
    "StartRow": 0,
    "StartColumn": 0,
    "EndRow": 2,
    "EndColumn": 2
  }
}
```

**مخطط الاستجابة – `CellArea`**

| الخصائص         | النوع | الوصف                                      |
|------------------|-------|---------------------------------------------|
| `StartRow`       | عدد صحيح | المؤشر المبدئي (صفر-الأساس) للصف الأول.    |
| `StartColumn`    | عدد صحيح | المؤشر المبدئي (صفر-الأساس) للعمود الأول.  |
| `EndRow`         | عدد صحيح | المؤشر المبدئي (صفر-الأساس) للصف الأخير.   |
| `EndColumn`      | عدد صحيح | المؤشر المبدئي (صفر-الأساس) للعمود الأخير. |

---

**رموز حالة HTTP**

| الرمز | المعنى                   | الوصف                                      |
|-------|---------------------------|---------------------------------------------|
| 200   | OK (نجاح)                | تم تطبيق العامل بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | Bad Request (طلب خاطئ)   | معلمات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401   | Unauthorized (غير مفوض)   | رمز JWT غير صالح أو مفقود.                |
| 413   | Payload Too Large (حمولة كبيرة جدًا) | تجاوز حجم الملف المرفوع الحد المسموح. |
| 500   | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم. |

---

## أمثلة باستخدام SDK

فيما يلي مقاطع قصيرة لأشهر SDKs. استبدل `YOUR_APP_SID` و`YOUR_APP_KEY` ببيانات الاعتماد الخاصة بك، وعيّن رمز JWT الذي تم توليده عند الحاجة.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.Sdk;
using Aspose.Cells.Cloud.Sdk.Model;

var config = new Configuration
{
    AppSid = "YOUR_APP_SID",
    AppKey = "YOUR_APP_KEY"
};

var api = new ConditionalFormattingsApi(config);
var result = api.PutWorksheetFormatConditionArea(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    cellArea: "A1:C3",
    folder: null,
    storageName: null);

Console.WriteLine(result);
```

### Java

```java
import com.aspose.cells.cloud.ApiClient;
import com.aspose.cells.cloud.Configuration;
import com.aspose.cells.cloud.api.ConditionalFormattingsApi;

Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(new ApiClient(config));

try {
    com.aspose.cells.cloud.model.ResponseMessage resp = api.putWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", null, null);
    System.out.println(resp);
} catch (Exception e) {
    e.printStackTrace();
}
```

### PHP

```php
<?php
require 'vendor/autoload.php';

use Aspose\Cells\Cloud\Sdk\Api\ConditionalFormattingsApi;
use Aspose\Cells\Cloud\Sdk\Configuration;

$config = new Configuration();
$config->setAppSid('YOUR_APP_SID');
$config->setAppKey('YOUR_APP_KEY');

$api = new ConditionalFormattingsApi($config);

try {
    $result = $api->putWorksheetFormatConditionArea(
        'Book1.xlsx',
        'Sheet1',
        0,
        'A1:C3',
        null,
        null
    );
    print_r($result);
} catch (Exception $e) {
    echo 'Error: ', $e->getMessage();
}
?>
```

### Ruby

```ruby
require 'aspose_cells_cloud_sdk'

config = AsposeCellsCloud::Configuration.new
config.app_sid = 'YOUR_APP_SID'
config.app_key = 'YOUR_APP_KEY'

api_instance = AsposeCellsCloud::ConditionalFormattingsApi.new
begin
  result = api_instance.put_worksheet_format_condition_area(
    'Book1.xlsx', 'Sheet1', 0, 'A1:C3')
  puts result
rescue StandardError => e
  puts "Error: #{e}"
end
```

### Node.js

```javascript
const { Configuration, ConditionalFormattingsApi } = require('asposecellscloudsdk');

const config = new Configuration();
config.appSid = 'YOUR_APP_SID';
config.appKey = 'YOUR_APP_KEY';

const api = new ConditionalFormattingsApi(config);

api.putWorksheetFormatConditionArea('Book1.xlsx', 'Sheet1', 0, 'A1:C3')
   .then(res => console.log(res))
   .catch(err => console.error('Error:', err));
```

### Python

```python
import asposecellscloudsdk
from asposecellscloudsdk.rest import ApiException
from asposecellscloudsdk import Configuration, ApiClient
from asposecellscloudsdk.api import conditional_formattings_api

config = Configuration()
config.app_sid = 'YOUR_APP_SID'
config.app_key = 'YOUR_APP_KEY'

api_instance = conditional_formattings_api.ConditionalFormattingsApi(ApiClient(config))

try:
    result = api_instance.put_worksheet_format_condition_area(
        name='Book1.xlsx',
        sheet_name='Sheet1',
        index=0,
        cell_area='A1:C3')
    print(result)
except ApiException as e:
    print("Exception:", e)
```

### Android (Java)

```java
import com.aspose.cloud.cells.api.ConditionalFormattingsApi;
import com.aspose.cloud.cells.client.ApiClient;
import com.aspose.cloud.cells.client.Configuration;

Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(new ApiClient(config));

try {
    com.aspose.cloud.cells.model.ResponseMessage resp = api.putWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", null, null);
    System.out.println(resp);
} catch (Exception e) {
    e.printStackTrace();
}
```

### Swift

```swift
import AsposeCellsCloud

let config = Configuration(appSid: "YOUR_APP_SID", appKey: "YOUR_APP_KEY")
let api = ConditionalFormattingsApi(configuration: config)

api.putWorksheetFormatConditionArea(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    cellArea: "A1:C3",
    folder: nil,
    storageName: nil) { result, error in
        if let err = error {
            print("Error:", err)
        } else if let res = result {
            print(res)
        }
}
```

### Perl

```perl
use AsposeCellsCloud::Api::ConditionalFormattingsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    app_sid  => 'YOUR_APP_SID',
    app_key  => 'YOUR_APP_KEY'
);
my $api = AsposeCellsCloud::Api::ConditionalFormattingsApi->new($config);

my $result = $api->putWorksheetFormatConditionArea(
    name      => 'Book1.xlsx',
    sheetName => 'Sheet1',
    index     => 0,
    cellArea  => 'A1:C3'
);
print $result;
```

### Go

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AppSid = "YOUR_APP_SID"
    config.AppKey = "YOUR_APP_KEY"

    api := sdk.NewConditionalFormattingsApi(config)

    resp, _, err := api.PutWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", nil, nil)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println(resp)
}
```

---

## ملاحظات ونصائح

- **صيغة CellArea** – يجب أن يكون نطاق A1 صحيحًا (`A1`، `A1:C3`، `Sheet2!B2:D5`). الصيغ غير الصالحة تُعيد **400 Bad Request**.
- **المناطق المتداخلة** – إضافة نطاق يتقاطع مع منطقة موجودة مسبقًا في نفس القاعدة يُسبب **409 Conflict**.
- **الترقيم بصفر-الأساس** – مؤشرات الصفوف والأعمدة في الاستجابة تبدأ من `0`. قم بالتحويل إلى التدوين 1-الأساس في Excel إذا لزم الأمر.
- **التخزين** – إذا حذفت `folder` و`storageName`، فسيستخدم API التخزين الافتراضي/المجلد الجذري.

---

## العمليات ذات الصلة

- **حذف منطقة الخلايا** – `DELETE /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area`
- **إضافة شرط إلى التنسيق الشرطي** – `POST /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`
- **الحصول على التنسيق الشرطي** – `GET /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}`

يمكن دمج هذه العمليات لبناء سير عمل كامل للتنسيق الشرطي.

---