---
title: "ตั้งค่าสูตรในเซลล์ของสมุดงาน Excel"
type: docs
url: /set-formula-for-a-cell-in-excel-worksheets/
weight: 80
keywords: "Excel, Aspose.Cells, REST API, ตั้งค่าสูตร, worksheet, เซลล์, Cloud SDK, cURL"
description: "เรียนรู้วิธีการตั้งค่าสูตรให้กับเซลล์เฉพาะในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API พร้อมตัวอย่าง cURL รายการพารามิเตอร์แบบเต็ม การจัดการข้อผิดพลาด และตัวอย่างโค้ด SDK"
---

REST API นี้จะตั้งค่า **สูตรในเซลล์** ให้กับไฟล์ Excel

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```

## การรักษาความปลอดภัยและการพิสูจน์ตัวตน

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ [การพิสูจน์ตัวตนแบบใช้ JWT token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

**พารามิเตอร์ของคำขอ**

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | จำเป็น | คำอธิบาย                                        |
|------------------|--------|----------|--------|-------------------------------------------------|
| name             | string | path     | ใช่    | ชื่อของไฟล์ Excel                               |
| sheetName        | string | path     | ใช่    | ชื่อของ worksheet                              |
| cellName         | string | path     | ใช่    | ที่อยู่ของเซลล์เป้าหมาย (เช่น **A1**)          |
| value            | string | query    | ไม่จำเป็น | ค่าที่จะกำหนดให้กับเซลล์                       |
| type           | string | query    | ไม่จำเป็น | ประเภทข้อมูลของค่า (เช่น **string**)            |
| formula          | string | query    | ไม่จำเป็น | สูตรที่จะใช้กับเซลล์ (เช่น **sum(A1,A2)**)       |
| folder           | string | query    | ไม่จำเป็น | โฟลเดอร์ที่เก็บเอกสารไว้                        |
| storageName      | string | query    | ไม่จำเป็น | ชื่อของบริการจัดเก็บข้อมูล                      |

## **การตอบกลับ**

ส่งคืน CellResponse

- **ภาพรวมฟิลด์ของการตอบกลับ**

| ฟิลด์           | ประเภท  | คำอธิบาย                                               |
| --------------- | ------- | ------------------------------------------------------ |
| `Name`          | string  | ที่อยู่ของเซลล์ (เช่น `F341`)                          |
| `Row`           | integer | ดัชนีแถวแบบเริ่มต้นที่ 0                               |
| `Column`        | integer | ดัชนีคอลัมน์แบบเริ่มต้นที่ 0                           |
| `Value`         | string  | ค่าที่แสดงในเซลล์                                     |
| `Type`          | string  | ประเภทข้อมูลของเซลล์ (เช่น `IsString`)                |
| `Formula`       | string  | ข้อความสูตรหากเซลล์มีสูตร                              |
| `IsFormula`     | bool    | บ่งชี้ว่าเซลล์มีสูตรหรือไม่                            |
| `IsMerged`      | bool    | บ่งชี้ว่าเซลล์อยู่ในช่วงที่ถูกรวม (merged) หรือไม่    |
| `IsArrayHeader` | bool    | บ่งชี้ว่าเซลล์เป็นหัวตารางอาเรย์ (array header) หรือไม่ |
| `IsInArray`     | bool    | บ่งชี้ว่าเซลล์อยู่ในอาเรย์หรือไม่                      |
| `IsErrorValue`  | bool    | บ่งชี้ว่าเซลล์มีค่าผิดพลาดหรือไม่                     |
| `IsInTable`     | bool    | บ่งชี้ว่าเซลล์อยู่ในตารางหรือไม่                      |
| `IsStyleSet`    | bool    | บ่งชี้ว่ามีการใช้รูปแบบให้กับเซลล์หรือไม่             |
| `HtmlString`    | string  | การแสดงค่าของเซลล์ในรูปแบบ HTML-encode               |
| `Style/link`    | object  | ลิงก์ไปยังทรัพยากรรูปแบบ                             |

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

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | คำอธิบาย                                             |
|------|------------------------------|-------------------------------------------------------|
| 200  | OK                           | กรองสำเร็จ; การตอบกลับประกอบด้วยรายละเอียดการดำเนินการ |
| 400  | Bad Request                  | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | Unauthorized                 | JWT token ไม่ถูกต้องหรือขาดหาย                         |
| 413  | Payload Too Large            | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                      |
| 500  | Internal Server Error        | เกิดข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด               |

## วิธีใช้ PostWorksheetCellSetValue API ด้วย SDK

### ข้อกำหนด PostWorksheetCellSetValue API

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue) นิยาม API แบบ public ที่เข้าถึงได้ และช่วยให้คุณเรียกใช้งาน REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

ใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเรียกใช้บริการเว็บของ Aspose.Cells

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

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ โดยคุณสามารถมุ่งเน้นไปที่งานหลักของโปรเจกต์ได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ที่มีทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// ตัวอย่าง C# – ตั้งค่าสูตรให้กับเซลล์
// แทนที่ <access-token>, <file-name> ฯลฯ ด้วยค่าของคุณ
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
// ตัวอย่าง Java – ตั้งค่าสูตรให้กับเซลล์
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
// ตัวอย่าง PHP – ตั้งค่าสูตรให้กับเซลล์
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
# ตัวอย่าง Ruby – ตั้งค่าสูตรให้กับเซลล์
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
# ตัวอย่าง Python – ตั้งค่าสูตรให้กับเซลล์
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
// ตัวอย่าง Node.js – ตั้งค่าสูตรให้กับเซลล์
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
// ตัวอย่าง Android (Java) – ตั้งค่าสูตรให้กับเซลล์
// คล้ายกับตัวอย่าง Java ทั่วไป; ตรวจสอบให้แน่ใจว่าคุณใช้ SDK ที่รองรับ Android
```

{{< /tab >}}

{{< tab tabNum="8" >}}

**ไม่มีตัวอย่าง Swift** SDK สำหรับ Swift กำลังอยู่ในขั้นตอนการพัฒนา

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# ตัวอย่าง Perl – ตั้งค่าสูตรให้กับเซลล์
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
// ตัวอย่าง Go – ตั้งค่าสูตรให้กับเซลล์
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