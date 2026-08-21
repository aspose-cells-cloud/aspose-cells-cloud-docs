---
title: "รับแกนหมวดหมู่ที่สองของแผนภูมิ"
type: docs
url: /charts/second-category-axis/get/
weight: 60
keywords: "รับแกนหมวดหมู่ที่สองของแผนภูมิ, Aspose.Cells Cloud API, แกนแผนภูมิ Excel, REST API, แกนหมวดหมู่ที่สอง, Aspose.Cells"
description: "ดึงข้อมูลแกนหมวดหมู่ที่สองของแผนภูมิในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API ประกอบด้วยรูปแบบคำขอ พารามิเตอร์ ตัวอย่าง cURL โครงสร้างการตอบกลับ โค้ดสถานะ HTTP และหมายเหตุการใช้งาน"
ArticleTitle: "รับแกนหมวดหมู่ที่สองของแผนภูมิ – Aspose.Cells Cloud API"
---

REST API นี้ใช้ในการดึงข้อมูล **แกนหมวดหมู่ที่สอง** ของแผนภูมิ

## API GetChartSecondCategoryAxis

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่งพารามิเตอร์ (path/query) | คำอธิบาย                                      |
| ---------------- | ---------- | ------------------------------- | --------------------------------------------- |
| name             | string     | path                            | ชื่อไฟล์ Excel ที่จัดเก็บไว้ในคลาวด์         |
| sheetName        | string     | path                            | ชื่อแผ่นงานที่มีแผนภูมิอยู่                 |
| chartIndex       | integer    | path                            | ดัชนีแบบเริ่มต้นที่ 0 ของแผนภูมิที่ต้องการรับข้อมูลแกน |
| folder           | string     | query                           | เส้นทางโฟลเดอร์ในพื้นที่เก็บข้อมูลที่ไฟล์ตั้งอยู่ |
| storageName      | string     | query                           | ชื่อพื้นที่เก็บข้อมูลของ Aspose Cloud ที่จะใช้ (ไม่บังคับ) |

### **การตอบกลับ**

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

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                   | คำอธิบาย                                               |
|------|----------------------------|--------------------------------------------------------|
| 200  | OK                         | ใช้งานตัวกรองเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดการดำเนินการ |
| 400  | Bad Request                | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | Unauthorized               | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                         |
| 413  | Payload Too Large          | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                      |
| 500  | Internal Server Error      | เกิดข้อผิดพลาดภายในเซิร์ฟเวอร์โดยไม่คาดคิด            |

## วิธีใช้ API GetChartSecondCategoryAxis ร่วมกับ SDK

### ข้อกำหนดของ API GetChartSecondCategoryAxis

การดำเนินการ **Get-Chart-Second-Category-Axis** ถูกกำหนดไว้ใน [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/GetChartSecondCategoryAxis) ซึ่งช่วยให้สามารถโต้ตอบกับ REST API โดยตรงจากเบราว์เซอร์เว็บหรือไคลเอนต์ HTTP ใดๆ

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง `cURL` เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API ด้วย `cURL`

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

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

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการผสานรวม API นี้เข้ากับโปรเจกต์ของคุณ SDK จะจัดการรายละเอียดระดับต่ำ เช่น การยืนยันตัวตน การสร้างคำขอ และการแปลงคำตอบ ซึ่งทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจได้ รายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud อยู่ที่ [GitHub repository](https://github.com/aspose-cells-cloud)

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกการดำเนินการ **Get Chart Second Category Axis** โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// ตั้งค่าไคลเอนต์ API
var config = new Configuration
{
    ClientId = "<your-client-id>",
    ClientSecret = "<your-client-secret>"
};
var apiInstance = new ChartsApi(config);

// สร้างคำขอ
var request = new GetChartSecondCategoryAxisRequest(
    name: "Sample.xlsx",
    sheetName: "Sheet1",
    chartIndex: 0,
    folder: "Documents",
    storageName: null
);

// ดำเนินการ
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
        // ตั้งค่าไคลเอนต์ API
        Configuration config = new Configuration();
        config.setClientId("<your-client-id>");
        config.setClientSecret("<your-client-secret>");

        ChartsApi api = new ChartsApi(config);

        // สร้างคำขอ
        GetChartSecondCategoryAxisRequest request = new GetChartSecondCategoryAxisRequest(
                "Sample.xlsx", "Sheet1", 0, "Documents", null);

        // ดำเนินการ
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

// ตั้งค่า
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

# ตั้งค่า SDK
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

# ตั้งค่าไคลเอนต์ API
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
// ตัวอย่าง Node.js โดยใช้ Aspose.Cells Cloud SDK
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
// ตัวอย่าง Android (Java) โดยใช้ Aspose.Cells Cloud SDK สำหรับ Android
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