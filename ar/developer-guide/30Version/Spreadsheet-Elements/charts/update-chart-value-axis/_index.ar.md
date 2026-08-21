---
title: "واجهة برمجة تطبيقات Aspose.Cells Cloud – تحديث محور القيم في المخطط (POST /valueaxis)"
description: "قم بتحديث محور القيم في مخطط موجود في ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API. يتضمن عنوان النهاية، المعلمات، مخطط جسم الطلب، أمثلة (cURL ووحدات SDK)، الاستجابات، ومعالجة الأخطاء."
keywords:
  - Aspose.Cells Cloud
  - Update Chart Value Axis
  - REST API
  - محور مخطط Excel
  - POST valueaxis
  - مثال cURL
  - SDK
  - JSON payload
  - إعدادات محور المخطط
last_updated: 2026-07-30
---

# تحديث محور القيم في المخطط (POST /valueaxis)

**الملخص:**  
قم بتعديل محور القيم في مخطط محدد داخل ملف Excel مخزّن في خدمة Aspose Cloud. يمكنك ضبط الحدود، وحدات العلامات، ونطاق المقياس اللوغاريثمي، وغيرها من خصائص المحور في طلب واحد.

---

## المتطلبات المسبقة

1. **رمز وصول JWT** – احصل على رمز كما هو موضح في [دليل المصادقة](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).  
2. يجب أن يكون **ملف العمل** (workbook) الذي تستهدفه قد تم رفعه مسبقًا إلى مساحة التخزين في Aspose Cloud (أو التخزين الافتراضي).  
3. تأكد من معرفة **اسم ورقة العمل** و**فهرس المخطط (الذي يبدأ من الصفر)** التي ترغب في تعديلها.

---

## عنوان النهاية

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

*استبدل الأسماء الرمزية بقيمك الفعلية.*

| الاسم الرمزي | الوصف |
|-------------|-------------|
| `{name}` | اسم ملف Excel (مثال: `Book1.xlsx`). |
| `{sheetName}` | ورقة العمل التي يحتوي على المخطط (مثال: `Sheet1`). |
| `{chartIndex}` | الفهرس الذي يبدأ من الصفر للمخطط (مثال: `0`). |

---

## المصادقة

تستخدم الواجهة برمجية تطبيقات **المصادقة القائمة على رمز JWT**. شمل الرمز في الرأس `Authorization` كالتالي:

```
Authorization: Bearer <jwt token>
```

---

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة قائمة على رمز JWT</a>.

## معلمات الطلب

| الاسم | الموقع | النوع | الإلزامية | الوصف |
|-------|--------|--------|-----------|--------|
| **name** | المسار (Path) | نص (string) | نعم | اسم ملف Excel المخزّن في السحابة. |
| **sheetName** | المسار (Path) | نص (string) | نعم | ورقة العمل التي تحتوي على المخطط. |
| **chartIndex** | المسار (Path) | عدد صحيح (int) | نعم | الفهرس الذي يبدأ من الصفر للمخطط المراد تحديثه. |
| **axis** | جسم الطلب (Body) | كائن (object) | نعم | إعدادات المحور (انظر *مخطط جسم الطلب*). |
| **folder** | الاستعلام (Query) | نص (string) | لا | مسار المجلد في السحابة حيث يقع الملف. |
| **storageName** | الاستعلام (Query) | نص (string) | لا | اسم خدمة التخزين المراد استخدامها. |

---

## مخطط جسم الطلب (كائن `axis`)

ينبغي أن تتضمّن فقط الخصائص التي ترغب في تغييرها.

| الخاصية | النوع | الإلزامية | الوصف |
|---------|--------|----------|--------|
| `minimum` | رقم | لا | الحد الأدنى للمحور. |
| `maximum` | رقم | لا | الحد الأقصى للمحور. |
| `majorUnit` | رقم | لا | الفاصل بين علامات التقييم الرئيسية. |
| `minorUnit` | رقم | لا | الفاصل بين علامات التقييم الثانوية. |
| `logBase` | رقم | لا | القاعدة للأس اللوغاريثمي عند `isLogarithmic` = `true`. |
| `isLogarithmic` | منطقي (boolean) | لا | ما إذا كان المحور يستخدم مقياسًا لوغاريتميًا. |
| `displayUnit` | نص (string) | لا | تسمية الوحدة المعروضة على المحور (مثال: `"Thousands"`). |
| `tickMark` | نص (string) | لا | نمط علامات التقييم (`"inside"`, `"outside"`، إلخ). |
| `crossAt` | رقم | لا | الموقع الذي يقطع فيه المحور المحور العمودي عليه. |

### مثال على جسم الطلب

```json
{
  "minimum": 0,
  "maximum": 200,
  "majorUnit": 20,
  "minorUnit": 5,
  "logBase": 10,
  "isLogarithmic": false,
  "displayUnit": "Units",
  "tickMark": "inside",
  "crossAt": 0
}
```

---

## أمثلة على الطلبات

### cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/<code class=\"placeholder\">{name}</code>/worksheets/<code class=\"placeholder\">{sheetName}</code>/charts/<code class=\"placeholder\">{chartIndex}</code>/valueaxis?folder=<code class=\"placeholder\">{folder}</code>&storageName=<code class=\"placeholder\">{storageName}</code>" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "minimum": 0,
        "maximum": 200,
        "majorUnit": 20,
        "minorUnit": 5,
        "logBase": 10,
        "isLogarithmic": false,
        "displayUnit": "Units",
        "tickMark": "inside",
        "crossAt": 0
      }'
```

### عينات SDK  

{{< tabs tabTotal="10" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var api = new ChartsApi("client_id", "client_secret");
var axis = new Axis()
{
    Minimum = 0,
    Maximum = 200,
    MajorUnit = 20,
    MinorUnit = 5,
    LogBase = 10,
    IsLogarithmic = false,
    DisplayUnit = "Units",
    TickMark = "inside",
    CrossAt = 0
};

var response = api.PostChartValueAxis("Book1.xlsx", "Sheet1", 0, axis);
Console.WriteLine($"Status: {response.Status}");
```
{{< /tab >}}

{{< tab tabNum="2" >}}
```java
import com.aspose.cells.cloud.api.ChartsApi;
import com.aspose.cells.cloud.model.Axis;

ChartsApi api = new ChartsApi("client_id", "client_secret");
Axis axis = new Axis()
        .minimum(0.0)
        .maximum(200.0)
        .majorUnit(20.0)
        .minorUnit(5.0)
        .logBase(10.0)
        .isLogarithmic(false)
        .displayUnit("Units")
        .tickMark("inside")
        .crossAt(0.0);

api.postChartValueAxis("Book1.xlsx", "Sheet1", 0, axis);
System.out.println("Value axis updated.");
```
{{< /tab >}}

{{< tab tabNum="3" >}}
```php
<?php
require 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\ChartsApi;
use Aspose\Cells\Cloud\Model\Axis;

$api = new ChartsApi('client_id', 'client_secret');
$axis = new Axis([
    'minimum' => 0,
    'maximum' => 200,
    'majorUnit' => 20,
    'minorUnit' => 5,
    'logBase' => 10,
    'isLogarithmic' => false,
    'displayUnit' => 'Units',
    'tickMark' => 'inside',
    'crossAt' => 0
]);

$api->postChartValueAxis('Book1.xlsx', 'Sheet1', 0, $axis);
echo "Value axis updated.\n";
?>
```
{{< /tab >}}

{{< tab tabNum="4" >}}
```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::ChartsApi.new('client_id', 'client_secret')
axis = AsposeCellsCloud::Axis.new(
  minimum: 0,
  maximum: 200,
  majorUnit: 20,
  minorUnit: 5,
  logBase: 10,
  isLogarithmic: false,
  displayUnit: 'Units',
  tickMark: 'inside',
  crossAt: 0
)

api.post_chart_value_axis('Book1.xlsx', 'Sheet1', 0, axis)
puts 'Value axis updated.'
```
{{< /tab >}}

{{< tab tabNum="5" >}}
```python
from asposecellscloud import ChartsApi, Axis

api = ChartsApi('client_id', 'client_secret')
axis = Axis(
    minimum=0,
    maximum=200,
    majorUnit=20,
    minorUnit=5,
    logBase=10,
    isLogarithmic=False,
    displayUnit='Units',
    tickMark='inside',
    crossAt=0
)

api.post_chart_value_axis('Book1.xlsx', 'Sheet1', 0, axis)
print('Value axis updated.')
```
{{< /tab >}}

{{< tab tabNum="6" >}}
```javascript
// مثال Node.js
const { ChartsApi, Axis } = require('asposecellscloud');

const api = new ChartsApi('client_id', 'client_secret');
const axis = new Axis({
    minimum: 0,
    maximum: 200,
    majorUnit: 20,
    minorUnit: 5,
    logBase: 10,
    isLogarithmic: false,
    displayUnit: 'Units',
    tickMark: 'inside',
    crossAt: 0
});

api.postChartValueAxis('Book1.xlsx', 'Sheet1', 0, axis)
   .then(response => console.log('Value axis updated.'))
   .catch(err => console.error(err));
```
{{< /tab >}}

{{< tab tabNum="7" >}}
```java
// مثال Android (Java)
ChartsApi api = new ChartsApi("client_id", "client_secret");
Axis axis = new Axis()
        .minimum(0.0)
        .maximum(200.0)
        .majorUnit(20.0)
        .minorUnit(5.0)
        .logBase(10.0)
        .isLogarithmic(false)
        .displayUnit("Units")
        .tickMark("inside")
        .crossAt(0.0);

api.postChartValueAxis("Book1.xlsx", "Sheet1", 0, axis);
```
{{< /tab >}}

{{< tab tabNum="8" >}}
```swift
import AsposeCellsCloud

let api = ChartsApi(clientId: "client_id", clientSecret: "client_secret")
var axis = Axis()
axis.minimum = 0
axis.maximum = 200
axis.majorUnit = 20
axis.minorUnit = 5
axis.logBase = 10
axis.isLogarithmic = false
axis.displayUnit = "Units"
axis.tickMark = "inside"
axis.crossAt = 0

api.postChartValueAxis(name: "Book1.xlsx", sheetName: "Sheet1", chartIndex: 0, axis: axis) { result, error in
    if let error = error {
        print("Error: \\(error)")
    } else {
        print("Value axis updated.")
    }
}
```
{{< /tab >}}

{{< tab tabNum="9" >}}
```perl
use Aspose::Cells::Cloud::Api::ChartsApi;
use Aspose::Cells::Cloud::Model::Axis;

my $api  = ChartsApi->new('client_id', 'client_secret');
my $axis = Axis->new(
    minimum        => 0,
    maximum        => 200,
    majorUnit      => 20,
    minorUnit      => 5,
    logBase        => 10,
    isLogarithmic  => JSON::false,
    displayUnit    => 'Units',
    tickMark       => 'inside',
    crossAt        => 0
);

$api->postChartValueAxis('Book1.xlsx', 'Sheet1', 0, $axis);
print "Value axis updated.\n";
```
{{< /tab >}}

{{< tab tabNum="10" >}}
```go
package main

import (
    "context"
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v2/api"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v2/model"
)

func main() {
    cfg := api.NewConfiguration()
    cfg.AddDefaultHeader("client_id", "client_id")
    cfg.AddDefaultHeader("client_secret", "client_secret")
    client := api.NewAPIClient(cfg)

    axis := model.Axis{
        Minimum:       0,
        Maximum:       200,
        MajorUnit:     20,
        MinorUnit:     5,
        LogBase:       10,
        IsLogarithmic: false,
        DisplayUnit:   "Units",
        TickMark:      "inside",
        CrossAt:       0,
    }

    _, err := client.ChartsApi.PostChartValueAxis(context.Background(), "Book1.xlsx", "Sheet1", 0, axis)
    if err != nil {
        fmt.Println("Error:", err)
    } else {
        fmt.Println("Value axis updated.")
    }
}
```
{{< /tab >}}

{{< /tabs >}}

---

## الاستجابات

### نجاح (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

نوع الاستجابة هو `CellsCloudResponse`.

**رموز حالة HTTP**

| الكود | المعنى | الوصف |
|------|---------|--------|
| 200  | نجاح (OK) | تم تطبيق المرشّح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب خاطئ (Bad Request) | معلمات ناقصة أو غير صالحة (مثال: نوع ملف غير مدعوم). |
| 401  | غير مصرّح (Unauthorized) | رمز JWT غير صالح أو مفقود. |
| 413  | حجم حمل الطلب كبير جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح. |
| 500  | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم. |
---

## موارد إضافية

- **مواصفات OpenAPI** – [عرض / تنزيل بصيغة JSON-YAML](https://apireference.aspose.cloud/cells/#/Charts/PostChartValueAxis)  
- **مستودع SDK** – <https://github.com/aspose-cells-cloud>  
- **دليل المصادقة** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>

---

*لأي استفسارات أو ملاحظات، يُرجى التواصل مع فريق دعم Aspose.Cells Cloud.*