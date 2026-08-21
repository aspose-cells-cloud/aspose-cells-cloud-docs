---
title: "حساب جميع الصيغ في ملف Excel"
second_title: "مستند"
linktitle: "حساب"
type: docs
url: /ar/calculate-all-formulas-on-an-excel-file/
aliases:
  [/calculate-all-formulas-in-a-workbook/, /workbook/calculate-all-formulas/]
keywords: "Aspose.Cells, حساب الصيغ, واجهة برمجة تطبيقات Excel, SDK للحاسوب السحابي"
description: "احسب كل صيغة في ملف Excel باستخدام واجهة Aspose.Cells Cloud REST API. يتضمن مثالًا لـ cURL، ومُعلَمات الطلب، ومخطط الاستجابة، والمتطلبات الأساسية، ومقاطع كود SDK بعدة لغات."
weight: 140
ArticleTitle: "حساب جميع الصيغ في ملف Excel"
---

تقوم هذه الواجهة البرمجية لـ REST بحساب **جميع الصيغ** في ملف Excel.

**المتطلبات المسبقة:** قبل استدعاء هذه النقطة النهائية، تأكد من وجود:
- رمز مصادقة JWT صالح. (انظر [دليل المصادقة](/authentication/).)
- مُعرِّف العميل وسرّ خدمة Aspose.Cells Cloud.
- ملف Excel المستهدف المرفوع إلى موقع التخزين المُخصَّص. (انظر [إعداد التخزين](/storage/).)

## واجهة PostWorkbookCalculateFormula API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/calculateformula
```

تُسرد مُعلَمات الطلب أدناه:

| اسم المُعلَمة    | النوع               | الموقع | الوصف                                                                                     |
| ----------------- | ------------------ | ------ | ----------------------------------------------------------------------------------------- |
| **name**          | string             | path   | اسم ملف المصنف.                                                                          |
| **options**       | CalculationOptions | body   | كائن JSON يحدّد إعدادات الحساب (مثل `CalcStackSize`، `IgnoreError`).                    |
| **ignoreError**   | boolean            | query  | إذا كانت القيمة `true`، يتم تجاهل الأخطاء التي تظهر أثناء الحساب.                        |
| **folder**        | string             | query  | مسار المجلد الذي يحتوي على المصنف.                                                      |
| **storageName**   | string             | query  | اسم خدمة التخزين التي يُخزَّن فيها المصنف.                                               |

تُعرِّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookCalculateFormula) واجهة برمجة تطبيقات متاحة عمومًا وتتيح إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إرسال طلب إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/calculateformula?ignoreError=true" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CalcStackSize": 1,
        "IgnoreError": true,
        "PrecisionStrategy": "string",
        "Recursive": true
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "WorkbookUrl": "https://api.aspose.cloud/v3.0/storage/file/Book1.xlsx",
  "ErrorMessage": null
}
```

{{< /tab >}}

{{< /tabs >}}

#### تفاصيل الاستجابة

| الحقل             | النوع   | الوصف                                                                 |
| ----------------- | ------- | --------------------------------------------------------------------- |
| **Code**          | int     | رمز حالة مشابه لـ HTTP (200 يشير إلى النجاح).                        |
| **Status**        | string  | وصف نصّي موجّه للنتيجة (مثل `OK`).                                   |
| **WorkbookUrl**   | string  | الرابط المباشر لتنزيل المصنف المُحدَّث.                               |
| **ErrorMessage**  | string  | معلومات مفصّلة عن الخطأ عند فشل الطلب؛ تكون `null` عند النجاح.      |

#### الخطوات التالية / الأخطاء الشائعة

- **معالجة أخطاء الحساب** – اضبط `ignoreError=false` لتلقي استجابة خطأ عند تعذّر تقييم صيغة.
- **الانتباه إلى حدّ معدل الطلبات** – راجع رأس `X-RateLimit-Remaining`؛ إذا وصلت قيمته إلى `0`، توقّف مؤقتًا قبل إعادة المحاولة.
- **إرشادات رموز الحالة HTTP**:
  - `400` – مُعلَمات طلب غير صالحة.
  - `401` – فشلت المصادقة (رمز JWT غير صالح أو منتهٍ).
  - `404` – لم يتم العثور على المصنف.
  - `500` – خطأ من جانب الخادم؛ اتصل بدعم Aspose إذا استمرّ الخطأ.

| الرمز | المعنى                | وقت الإرجاع                                               |
| ------ | --------------------- | ---------------------------------------------------------- |
| 400    | طلب غير صالح          | مُعلَمات طلب غير صالحة أو JSON غير منسّق.                |
| 401    | غير مصرّح به          | رمز JWT مفقود أو غير صالح أو منتهٍ.                       |
| 404    | غير موجود             | المصنف المحدّد غير موجود في التخزين.                      |
| 500    | خطأ داخلي في الخادم   | فشل غير متوقّع من جانب الخادم؛ اتصل بدعم Aspose.         |

## عائلة SDK للحاسوب السحابي

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. يعتني SDK بالتفاصيل منخفضة المستوى، بحيث يمكنك التركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطّلاع على قائمة كاملة بـ SDKs لـ Aspose.Cells Cloud.

تُظهر مقاطع الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("<clientId>", "<clientSecret>");
var request = new PostWorkbookCalculateFormulaRequest(
    name: "Book1.xlsx",
    folder: "",
    storageName: "",
    ignoreError: true,
    options: new CalculationOptions { CalcStackSize = 1, IgnoreError = true });

var response = api.PostWorkbookCalculateFormula(request);
Console.WriteLine($"Status: {response.Status}");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

CellsApi api = new CellsApi("<clientId>", "<clientSecret>");
PostWorkbookCalculateFormulaRequest request = new PostWorkbookCalculateFormulaRequest()
        .name("Book1.xlsx")
        .ignoreError(true)
        .options(new CalculationOptions().calcStackSize(1).ignoreError(true));

WorkbookResponse result = api.postWorkbookCalculateFormula(request);
System.out.println("Status: " + result.getStatus());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\CellsApi;
use Aspose\Cells\Cloud\Model\CalculationOptions;
use Aspose\Cells\Cloud\Model\PostWorkbookCalculateFormulaRequest;

$api = new CellsApi("<clientId>", "<clientSecret>");
$options = new CalculationOptions([
    "CalcStackSize" => 1,
    "IgnoreError"   => true
]);

$request = new PostWorkbookCalculateFormulaRequest([
    "name"    => "Book1.xlsx",
    "ignoreError" => true,
    "options" => $options
]);

$response = $api->postWorkbookCalculateFormula($request);
echo "Status: " . $response->getStatus();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new("<clientId>", "<clientSecret>")
options = AsposeCellsCloud::CalculationOptions.new(
  calc_stack_size: 1,
  ignore_error: true
)

request = AsposeCellsCloud::PostWorkbookCalculateFormulaRequest.new(
  name: 'Book1.xlsx',
  ignore_error: true,
  options: options
)

response = api.post_workbook_calculate_formula(request)
puts "Status: #{response.status}"
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const {
  CellsApi,
  PostWorkbookCalculateFormulaRequest,
  CalculationOptions,
} = require("asposecellscloud");

const api = new CellsApi("<clientId>", "<clientSecret>");
const options = new CalculationOptions({ CalcStackSize: 1, IgnoreError: true });

const request = new PostWorkbookCalculateFormulaRequest({
  name: "Book1.xlsx",
  ignoreError: true,
  options: options,
});

api.postWorkbookCalculateFormula(request).then((response) => {
  console.log(`Status: ${response.status}`);
});
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
from asposecellscloud import CellsApi, PostWorkbookCalculateFormulaRequest, CalculationOptions

api = CellsApi("<clientId>", "<clientSecret>")
options = CalculationOptions(calc_stack_size=1, ignore_error=True)

request = PostWorkbookCalculateFormulaRequest(
    name="Book1.xlsx",
    ignore_error=True,
    options=options
)

response = api.post_workbook_calculate_formula(request)
print(f"Status: {response.status}")
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::CellsApi;
use AsposeCellsCloud::Object::PostWorkbookCalculateFormulaRequest;
use AsposeCellsCloud::Object::CalculationOptions;

my $api = AsposeCellsCloud::CellsApi->new(
    client_id     => '<clientId>',
    client_secret => '<clientSecret>'
);

my $options = AsposeCellsCloud::Object::CalculationOptions->new(
    CalcStackSize => 1,
    IgnoreError   => JSON::true
);

my $request = AsposeCellsCloud::Object::PostWorkbookCalculateFormulaRequest->new(
    name        => 'Book1.xlsx',
    ignoreError => JSON::true,
    options     => $options
);

my $response = $api->post_workbook_calculate_formula(request => $request);
print "Status: " . $response->{Status} . "\n";
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3/api"
    "github.com/asposecellscloud/asposecellscloud-go/v3/model"
)

func main() {
    cfg := api.NewConfiguration()
    cfg.AddDefaultHeader("client-id", "<clientId>")
    cfg.AddDefaultHeader("client-secret", "<clientSecret>")
    client := api.NewAPIClient(cfg)

    opts := model.CalculationOptions{
        CalcStackSize: 1,
        IgnoreError:   true,
    }

    req := model.PostWorkbookCalculateFormulaRequest{
        Name:        "Book1.xlsx",
        IgnoreError: true,
        Options:     &opts,
    }

    resp, _, err := client.CellsApi.PostWorkbookCalculateFormula(req)
    if err != nil {
        panic(err)
    }
    fmt.Printf("Status: %s\n", resp.Status)
}
```

{{< /tab >}}

{{< /tabs >}}