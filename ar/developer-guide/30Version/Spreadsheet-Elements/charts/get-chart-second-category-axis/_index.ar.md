---
title: "الحصول على محور الفئة الثانية في المخطط"
type: docs
url: /charts/second-category-axis/get/
weight: 60
keywords: "الحصول على محور الفئة الثانية في المخطط، واجهة Aspose.Cells Cloud API، محور مخطط Excel، واجهة REST API، محور الفئة الثانية، Aspose.Cells"
description: "استرجاع محور الفئة الثانية في مخطط موجود في ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API. يتضمن تنسيق الطلب، المعلمات، مثال باستخدام cURL، مخطط الاستجابة، رموز الحالة، وملاحظات الاستخدام."
ArticleTitle: "الحصول على محور الفئة الثانية في المخطط – Aspose.Cells Cloud API"
---

تقوم هذه الواجهة REST باسترجاع **محور الفئة الثانية** في مخطط.

## واجهة GetChartSecondCategoryAxis

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### **الأمان والمصادقة**

تُعد واجهات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معلمات الطلب

| اسم المعلمة | النوع | موقع المعلمة (path/query) | الوصف |
| ------------ | ------- | ------------------------------- | ------------------------------------------------------ |
| name | string | path | اسم ملف Excel المخزن في السحابة. |
| sheetName | string | path | اسم ورقة العمل التي يحتوي المخطط عليها. |
| chartIndex | integer | path | المؤشر الصفري للفهرس للمخطط الذي يُطلب محوره. |
| folder | string | query | مسار المجلد في التخزين حيث يوجد الملف. |
| storageName | string | query | اسم تخزين Aspose Cloud المراد استخدامه (اختياري). |

### **الاستجابة**

```json
{
  "Code": 200,
  "Status": "OK",
  "Axis": {
    "Name": "Second Category Axis",
    "IsVisible": true,
    "AxisLine": { "Style": "Solid", "Weight": 1 },
    "TickMarks": "Inside",
    "Label": {
      "Font": { "Size": 10, "Color": "#000000" },
      "Format": "General"
    }
  }
}
```

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|------|-----------------------------|--------------------------------------------------|
| 200 | OK | تمت تطبيق المرشح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | Bad Request | معلمات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | Unauthorized | رمز JWT غير صالح أو مفقود. |
| 413 | Payload Too Large | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500 | Internal Server Error | خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة GetChartSecondCategoryAxis مع وحدات التطوير (SDKs)

### مواصفات واجهة GetChartSecondCategoryAxis

يتم تعريف العملية **Get-Chart-Second-Category-Axis** في [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetChartSecondCategoryAxis)، وتتيح التفاعل المباشر عبر REST من متصفح الويب أو أي عميل HTTP.

يمكنك استخدام أداة سطر الأوامر `cURL` للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية استدعاء الواجهة باستخدام `cURL`.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis?folder={folder}&storageName={storageName}" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Axis": {
    "Name": "Second Category Axis",
    "IsVisible": true,
    "AxisLine": { "Style": "Solid", "Weight": 1 },
    "TickMarks": "Inside",
    "Label": {
      "Font": { "Size": 10, "Color": "#000000" },
      "Format": "General"
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام وحدات تطوير Aspose.Cells Cloud (SDKs)

استخدام وحدات التطوير (SDKs) هو أسرع طريقة لدمج هذه الواجهة في مشروعك. فوحدات التطوير تتعامل مع التفاصيل منخفضة المستوى مثل المصادقة، وبناء الطلب، وتحليل الاستجابة، مما يسمح لك بالتركيز على المنطق التجاري. يمكنك الاطلاع على القائمة الكاملة لوحدات تطوير Aspose.Cells Cloud في [مستودع GitHub](https://github.com/aspose-cells-cloud).

توضح أمثلة الكود التالية كيفية استدعاء العملية **Get Chart Second Category Axis** باستخدام وحدات تطوير مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// تكوين عميل الواجهة
var config = new Configuration
{
    ClientId = "<your-client-id>",
    ClientSecret = "<your-client-secret>"
};
var apiInstance = new ChartsApi(config);

// بناء الطلب
var request = new GetChartSecondCategoryAxisRequest(
    name: "Sample.xlsx",
    sheetName: "Sheet1",
    chartIndex: 0,
    folder: "Documents",
    storageName: null
);

// التنفيذ
var response = apiInstance.GetChartSecondCategoryAxis(request);
Console.WriteLine($"Axis Name: {response.Axis.Name}");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.ChartsApi;
import com.aspose.cells.cloud.model.*;
import com.aspose.cells.cloud.model.requests.*;

public class GetSecondCategoryAxis {
    public static void main(String[] args) {
        // تكوين عميل الواجهة
        Configuration config = new Configuration();
        config.setClientId("<your-client-id>");
        config.setClientSecret("<your-client-secret>");

        ChartsApi api = new ChartsApi(config);

        // بناء الطلب
        GetChartSecondCategoryAxisRequest request = new GetChartSecondCategoryAxisRequest(
                "Sample.xlsx", "Sheet1", 0, "Documents", null);

        // التنفيذ
        AxisResponse response = api.getChartSecondCategoryAxis(request);
        System.out.println("Axis Name: " + response.getAxis().getName());
    }
}
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
use Aspose\Cells\Cloud\Sdk\Api\ChartsApi;
use Aspose\Cells\Cloud\Sdk\Configuration;
use Aspose\Cells\Cloud\Sdk\Model\Requests\GetChartSecondCategoryAxisRequest;

// التكوين
$config = new Configuration();
$config->setClientId('<your-client-id>');
$config->setClientSecret('<your-client-secret>');

$apiInstance = new ChartsApi($config);

$request = new GetChartSecondCategoryAxisRequest(
    'Sample.xlsx',       // name
    'Sheet1',            // sheetName
    0,                   // chartIndex
    'Documents',         // folder
    null                 // storageName
);

try {
    $result = $apiInstance->getChartSecondCategoryAxis($request);
    echo "Axis Name: " . $result->getAxis()->getName();
} catch (Exception $e) {
    echo 'Exception when calling ChartsApi->getChartSecondCategoryAxis: ', $e->getMessage(), PHP_EOL;
}
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

# تكوين وحدة التطوير
config = AsposeCellsCloud::Configuration.new
config.client_id = '<your-client-id>'
config.client_secret = '<your-client-secret>'

api_instance = AsposeCellsCloud::ChartsApi.new

begin
  result = api_instance.get_chart_second_category_axis(
    name: 'Sample.xlsx',
    sheet_name: 'Sheet1',
    chart_index: 0,
    folder: 'Documents'
  )
  puts "Axis Name: #{result.axis.name}"
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling ChartsApi->get_chart_second_category_axis: #{e}"
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
import asposecellscloud
from asposecellscloud.rest import ApiException
from asposecellscloud.apis.charts_api import ChartsApi
from asposecellscloud.models import GetChartSecondCategoryAxisRequest

# تكوين عميل الواجهة
config = asposecellscloud.Configuration()
config.client_id = '<your-client-id>'
config.client_secret = '<your-client-secret>'

api_instance = ChartsApi(asposecellscloud.ApiClient(config))

request = GetChartSecondCategoryAxisRequest(
    name='Sample.xlsx',
    sheet_name='Sheet1',
    chart_index=0,
    folder='Documents'
)

try:
    response = api_instance.get_chart_second_category_axis(request)
    print('Axis Name:', response.axis.name)
except ApiException as e:
    print('Exception when calling ChartsApi->get_chart_second_category_axis:', e)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// مثال Node.js باستخدام وحدة Aspose.Cells Cloud SDK
const { ChartsApi, Configuration } = require('asposecellscloud');

const config = new Configuration({
    clientId: '<your-client-id>',
    clientSecret: '<your-client-secret>'
});
const api = new ChartsApi(config);

(async () => {
    try {
        const response = await api.getChartSecondCategoryAxis({
            name: 'Sample.xlsx',
            sheetName: 'Sheet1',
            chartIndex: 0,
            folder: 'Documents'
        });
        console.log('Axis Name:', response.axis.name);
    } catch (error) {
        console.error('Error:', error);
    }
})();
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// مثال Android (Java) باستخدام وحدة Aspose.Cells Cloud SDK لمنصة Android
import com.aspose.cells.cloud.sdk.api.ChartsApi;
import com.aspose.cells.cloud.sdk.model.*;
import com.aspose.cells.cloud.sdk.model.requests.*;

public class GetSecondCategoryAxisAndroid {
    public void execute() {
        Configuration config = new Configuration();
        config.setClientId("<your-client-id>");
        config.setClientSecret("<your-client-secret>");

        ChartsApi api = new ChartsApi(config);
        GetChartSecondCategoryAxisRequest request = new GetChartSecondCategoryAxisRequest(
                "Sample.xlsx", "Sheet1", 0, "Documents", null);

        try {
            AxisResponse response = api.getChartSecondCategoryAxis(request);
            System.out.println("Axis Name: " + response.getAxis().getName());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
import AsposeCellsCloud

let config = Configuration(clientId: "<your-client-id>", clientSecret: "<your-client-secret>")
let api = ChartsApi(configuration: config)

let request = GetChartSecondCategoryAxisRequest(
    name: "Sample.xlsx",
    sheetName: "Sheet1",
    chartIndex: 0,
    folder: "Documents",
    storageName: nil
)

api.getChartSecondCategoryAxis(request: request) { result, error in
    if let axis = result?.axis {
        print("Axis Name: \(axis.name ?? "")")
    } else if let err = error {
        print("Error: \(err)")
    }
}
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
use Aspose::Cells::Cloud::Sdk::Api::ChartsApi;
use Aspose::Cells::Cloud::Sdk::Configuration;

my $config = Aspose::Cells::Cloud::Sdk::Configuration->new(
    client_id     => '<your-client-id>',
    client_secret => '<your-client-secret>'
);
my $api = Aspose::Cells::Cloud::Sdk::Api::ChartsApi->new($config);

my $response = $api->get_chart_second_category_axis(
    name        => 'Sample.xlsx',
    sheet_name  => 'Sheet1',
    chart_index => 0,
    folder      => 'Documents'
);
print "Axis Name: " . $response->axis->name . "\n";
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
)

func main() {
    cfg := asposecellscloud.NewConfiguration()
    cfg.ClientId = "<your-client-id>"
    cfg.ClientSecret = "<your-client-secret>"

    apiInstance := api.NewChartsApi(cfg)

    request := asposecellscloud.GetChartSecondCategoryAxisRequest{
        Name:      "Sample.xlsx",
        SheetName: "Sheet1",
        ChartIndex: 0,
        Folder:    "Documents",
        StorageName: nil,
    }

    result, _, err := apiInstance.GetChartSecondCategoryAxis(request)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println("Axis Name:", result.Axis.Name)
}
```

{{< /tab >}}

{{< /tabs >}}