---
title: "ضبط صيغة الخلية في أوراق عمل Excel"
type: docs
url: /ar/set-formula-for-a-cell-in-excel-worksheets/
weight: 80
keywords: "Excel, Aspose.Cells, REST API, ضبط صيغة, ورقة عمل, خلية, Cloud SDK, cURL"
description: "تعلم كيفية ضبط صيغة لخلية محددة في ورقة عمل Excel باستخدام Aspose.Cells Cloud REST API. يتضمن مثال cURL، وقائمة كاملة بالمعلمات، وتعامل الأخطاء، وأمثلة لكود SDK."
---

تقوم هذه الواجهة البرمجية (REST API) بضبط **صيغة الخلية** في ملف Excel.

## الواجهة البرمجية REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```

## الأمان والمصادقة

تتطلب واجهات Aspose.Cells Cloud APIs مصادقة تعتمد على [رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) وهي آمنة.

## **معلمات الطلب**

| اسم المعلمة | النوع | الموقع | الإلزام | الوصف |
|------------|-------|--------|---------|--------|
| name | string | path | نعم | اسم ملف Excel. |
| sheetName | string | path | نعم | اسم ورقة العمل. |
| cellName | string | path | نعم | عنوان الخلية المستهدفة (مثل **A1**). |
| value | string | query | لا | القيمة المراد تعيينها للخلية. |
| type | string | query | لا | نوع البيانات للقيمة (مثل **string**). |
| formula | string | query | لا | الصيغة المراد تطبيقها على الخلية (مثل **sum(A1,A2)**). |
| folder | string | query | لا | المجلد الذي يحتوي على المستند. |
| storageName | string | query | لا | اسم خدمة التخزين. |

## **الاستجابة**

ترجع استجابة من نوع CellResponse.

- **نظرة عامة على حقول الاستجابة**

| الحقل | النوع | الوصف |
|-------|-------|--------|
| `Name` | string | عنوان الخلية (مثل `F341`). |
| `Row` | integer | فهرس الصف (مبني على الصفر). |
| `Column` | integer | فهرس العمود (مبني على الصفر). |
| `Value` | string | القيمة المعروضة في الخلية. |
| `Type` | string | نوع بيانات الخلية (مثل `IsString`). |
| `Formula` | string | نص الصيغة إذا كانت الخلية تحتوي على صيغة. |
| `IsFormula` | bool | يشير إلى ما إذا كانت الخلية تحتوي على صيغة. |
| `IsMerged` | bool | يشير إلى ما إذا كانت الخلية جزءًا من نطاق مدمج. |
| `IsArrayHeader` | bool | يشير إلى ما إذا كانت الخلية رأس مصفوفة. |
| `IsInArray` | bool | يشير إلى ما إذا كانت الخلية تنتمي إلى مصفوفة. |
| `IsErrorValue` | bool | يشير إلى ما إذا كانت الخلية تحتوي على قيمة خطأ. |
| `IsInTable` | bool | يشير إلى ما إذا كانت الخلية داخل جدول. |
| `IsStyleSet` | bool | يشير إلى ما إذا تم تطبيق نمط على الخلية. |
| `HtmlString` | string | التمثيل المشفر بـ HTML لقيمة الخلية. |
| `Style/link` | object | رابط تشعبي لمورد النمط. |

```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|------|--------|-------|
| 200 | OK | تمت تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | Bad Request | معلمات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | Unauthorized | رمز JWT غير صالح أو مفقود. |
| 413 | Payload Too Large | حجم الملف المرفوع يتجاوز الحد المسموح به. |
| 500 | Internal Server Error | خطأ غير متوقع في الخادم. |

## كيفية استخدام واجزة PostWorksheetCellSetValue API باستخدام SDKs

### مواصفات PostWorksheetCellSetValue API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue) واجهة برمجة تطبيقات قابلة للوصول العام، وتمكّنك من إجراء تفاعلات REST مباشرة من متصفح الويب.

استخدم أداة سطر الأوامر cURL لاستدعاء خدمات Aspose.Cells عبر الويب.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A1?value=1234&type=string&formula=sum(A2:A15)" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access‑token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فتتولى SDK التعامل مع التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات لخدمات الويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// مثال بلغة C# – ضبط صيغة خلية
// استبدل <access-token> و <file-name> وما إلى ذلك بقيمك الخاصة.
var api = new CellsApi("<client-id>", "<client-secret>", "https://api.aspose.cloud");
var response = api.PostWorksheetCellSetValue(
    name: "myWorkbook.xlsx",
    sheetName: "Sheet1",
    cellName: "A3",
    value: "1234",
    type: "string",
    formula: "SUM(A1,A2)",
    folder: null,
    storageName: null);
Console.WriteLine(response.Status);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// مثال بلغة Java – ضبط صيغة خلية
CellsApi api = new CellsApi("<client-id>", "<client-secret>", "https://api.aspose.cloud");
PostWorksheetCellSetValueRequest request = new PostWorksheetCellSetValueRequest()
        .name("myWorkbook.xlsx")
        .sheetName("Sheet1")
        .cellName("A3")
        .value("1234")
        .type("string")
        .formula("SUM(A1,A2)");
CellsResponse response = api.postWorksheetCellSetValue(request);
System.out.println(response.getStatus());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
// مثال بلغة PHP – ضبط صيغة خلية
require_once('vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppKey('<client-id>');
$config->setAppSid('<client-secret>');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new Aspose\Cells\Api\CellsApi($config);
$result = $apiInstance->postWorksheetCellSetValue(
    "myWorkbook.xlsx",
    "Sheet1",
    "A3",
    "1234",
    "string",
    "SUM(A1,A2)"
);
echo $result->getStatus();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# مثال بلغة Ruby – ضبط صيغة خلية
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.api_key['client_id'] = '<client-id>'
config.api_key['client_secret'] = '<client-secret>'
config.host = 'https://api.aspose.cloud'

api = AsposeCellsCloud::CellsApi.new
result = api.post_worksheet_cell_set_value(
  name: 'myWorkbook.xlsx',
  sheet_name: 'Sheet1',
  cell_name: 'A3',
  value: '1234',
  type: 'string',
  formula: 'SUM(A1,A2)'
)
puts result.status
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# مثال بلغة Python – ضبط صيغة خلية
import asposecellscloud

client = asposecellscloud.CellsApiClient(
    client_id='<client-id>',
    client_secret='<client-secret>',
    base_url='https://api.aspose.cloud'
)

api = asposecellscloud.CellsApi(client)
response = api.post_worksheet_cell_set_value(
    name='myWorkbook.xlsx',
    sheet_name='Sheet1',
    cell_name='A3',
    value='1234',
    type='string',
    formula='SUM(A1,A2)'
)
print(response.status)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// مثال بلغة Node.js – ضبط صيغة خلية
const { CellsApi, ApiClient } = require('asposecellscloud');
const client = new ApiClient();
client.config = {
    clientId: '<client-id>',
    clientSecret: '<client-secret>',
    baseUrl: 'https://api.aspose.cloud'
};

const cellsApi = new CellsApi(client);
cellsApi.postWorksheetCellSetValue({
    name: 'myWorkbook.xlsx',
    sheetName: 'Sheet1',
    cellName: 'A3',
    value: '1234',
    type: 'string',
    formula: 'SUM(A1,A2)'
}).then(res => console.log(res.status));
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// مثال لأندرويد (Java) – ضبط صيغة خلية
// مشابه للمثال القياسي بلغة Java؛ تأكد من استخدام SDK المتوافق مع منصة Android.
```

{{< /tab >}}

{{< tab tabNum="8" >}}

**مثال بلغة Swift غير متوفر حالياً**. جاري تطوير SDK الخاص بلغة Swift.

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# مثال بلغة Perl – ضبط صيغة خلية
use AsposeCellsCloud::CellsApi;
my $api_instance = AsposeCellsCloud::CellsApi->new(
    client_id => '<client-id>',
    client_secret => '<client-secret>',
    base_url => 'https://api.aspose.cloud'
);
my $result = $api_instance->post_worksheet_cell_set_value(
    name => 'myWorkbook.xlsx',
    sheet_name => 'Sheet1',
    cell_name => 'A3',
    value => '1234',
    type => 'string',
    formula => 'SUM(A1,A2)'
);
print $result->{Status};
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
// مثال بلغة Go – ضبط صيغة خلية
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration()
    config.ClientId = "<client-id>"
    config.ClientSecret = "<client-secret>"
    config.BasePath = "https://api.aspose.cloud"

    api := asposecellscloud.NewAPIClient(config).CellsApi
    resp, _, err := api.PostWorksheetCellSetValue(
        "myWorkbook.xlsx",
        "Sheet1",
        "A3",
        map[string]string{
            "value":   "1234",
            "type":    "string",
            "formula": "SUM(A1,A2)",
        },
        nil,
        nil,
    )
    if err != nil {
        fmt.Println(err)
        return
    }
    fmt.Println(resp.Status)
}
```

{{< /tab >}}

{{< /tabs >}}