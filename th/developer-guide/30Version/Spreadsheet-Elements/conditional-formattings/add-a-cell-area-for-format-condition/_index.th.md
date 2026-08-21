---
---
title: เพิ่ม CellArea ให้กับการจัดรูปแบบแบบมีเงื่อนไข
description: เพิ่มพื้นที่เซลล์ให้กับกฎการจัดรูปแบบแบบมีเงื่อนไขในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API (v3.0) ประกอบด้วย endpoint, พารามิเตอร์, ตัวอย่าง cURL และ SDK ต่างๆ โครงสร้างการตอบกลับ และการจัดการข้อผิดพลาด
keywords: Aspose.Cells, การจัดรูปแบบแบบมีเงื่อนไข, CellArea, REST API, Excel, Cloud SDK
weight: 30
aliases:
  - /add-a-cell-area-for-format-condition/
---

# เพิ่ม CellArea ให้กับการจัดรูปแบบแบบมีเงื่อนไข

**สรุป** – เพิ่มพื้นที่เซลล์ให้กับกฎการจัดรูปแบบแบบมีเงื่อนไขที่มีอยู่ในแผ่นงาน

---

## สิ่งที่ต้องมีก่อน

1. **บัญชี Aspose.Cells Cloud** – รับ **App SID** และ **App Key** ของคุณ  
2. **โทเค็น JWT** – สร้างโทเค็น JWT โดยใช้ App SID/Key (ดูคู่มือการ [ตรวจสอบสิทธิ์](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/))  
3. ไฟล์ Excel ที่ต้องการใช้งานต้องมีอยู่แล้วในพื้นที่จัดเก็บ/โฟลเดอร์ที่ระบุ

---

## การตรวจสอบสิทธิ์

การเรียกใช้งานทั้งหมดต้องใช้การตรวจสอบสิทธิ์แบบใช้โทเค็น JWT โดยส่งโทเค็นในส่วนหัว `Authorization`:

```http
Authorization: Bearer <jwt token>
```

---

## คำขอ HTTP

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area
```

### พารามิเตอร์ในเส้นทาง (Path Parameters)

| ชื่อ         | ชนิดข้อมูล | คำอธิบาย                              |
|--------------|------------|---------------------------------------|
| `name`       | string     | ชื่อไฟล์ Excel (เช่น `Book1.xlsx`)     |
| `sheetName`  | string     | ชื่อแผ่นงานที่มีกฎนี้ (เช่น `Sheet1`) |
| `index`      | integer    | ดัชนีแบบเริ่มต้นที่ 0 ของกฎการจัดรูปแบบแบบมีเงื่อนไข |

### พารามิเตอร์ในส่วนคิวรี (Query Parameters)

| ชื่อ          | ชนิดข้อมูล | จำเป็น | คำอธิบาย                                      |
|---------------|------------|--------|-----------------------------------------------|
| `cellArea`    | string     | **ใช่**| ช่วงเซลล์ที่จะเพิ่ม โดยใช้รูปแบบ A1 (เช่น `A1:C3`) |
| `folder`      | string     | ไม่จำเป็น | เส้นทางโฟลเดอร์ที่เก็บไฟล์ไว้                |
| `storageName` | string     | ไม่จำเป็น | ชื่อของบริการพื้นที่จัดเก็บ                  |

---

## ตัวอย่างคำขอ (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/area?cellArea=A1:C3" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### การตอบกลับที่คาดว่าจะได้รับเมื่อสำเร็จ

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

**โครงสร้างการตอบกลับ – `CellArea`**

| คุณสมบัติ        | ชนิดข้อมูล | คำอธิบาย                                      |
|------------------|------------|-----------------------------------------------|
| `StartRow`       | int        | ดัชนีของแถวแรก (เริ่มต้นที่ 0)                |
| `StartColumn`    | int        | ดัชนีของคอลัมน์แรก (เริ่มต้นที่ 0)           |
| `EndRow`         | int        | ดัชนีของแถวสุดท้าย (เริ่มต้นที่ 0)           |
| `EndColumn`      | int        | ดัชนีของคอลัมน์สุดท้าย (เริ่มต้นที่ 0)       |

---

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                 | คำอธิบาย                                            |
|------|---------------------------|-----------------------------------------------------|
| 200  | OK                        | ใช้งานตัวกรองสำเร็จ; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400  | Bad Request               | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401  | Unauthorized              | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                    |
| 413  | Payload Too Large         | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                  |
| 500  | Internal Server Error     | เกิดข้อผิดพลาดภายในเซิร์ฟเวอร์โดยไม่คาดคิด         |

---

## ตัวอย่าง SDK

ด้านล่างนี้คือโค้ดตัวอย่างสั้นๆ สำหรับ SDK ที่นิยมใช้กันมากที่สุด แทนที่ `YOUR_APP_SID` และ `YOUR_APP_KEY` ด้วยข้อมูลประจำตัวของคุณ และตั้งค่าโทเค็น JWT ที่สร้างขึ้นแล้วตามที่จำเป็น

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

## หมายเหตุและเคล็ดลับ

- **รูปแบบ CellArea** – ต้องเป็นช่วง A1 ที่ถูกต้อง (เช่น `A1`, `A1:C3`, `Sheet2!B2:D5`) รูปแบบที่ไม่ถูกต้องจะส่งคืน **400 Bad Request**
- **พื้นที่ซ้อนทับกัน** – การเพิ่มช่วงที่ซ้อนทับกับพื้นที่ที่มีอยู่แล้วของกฎเดียวกันจะส่งคืน **409 Conflict**
- **การนับดัชนีแบบเริ่มต้นที่ 0** – ดัชนีของแถวและคอลัมน์ในการตอบกลับจะเริ่มที่ `0` แปลงเป็นรูปแบบ 1-แบบที่ Excel ใช้หากจำเป็น
- **พื้นที่จัดเก็บ** – หากไม่ระบุ `folder` และ `storageName` API จะใช้พื้นที่จัดเก็บเริ่มต้น/โฟลเดอร์รูท

---

## การดำเนินการที่เกี่ยวข้อง

- **ลบ CellArea** – `DELETE /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area`
- **เพิ่มเงื่อนไขให้กับการจัดรูปแบบแบบมีเงื่อนไข** – `POST /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`
- **รับข้อมูลการจัดรูปแบบแบบมีเงื่อนไข** – `GET /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}`

การดำเนินการเหล่านี้สามารถรวมกันเพื่อสร้างเวิร์กโฟลว์การจัดรูปแบบแบบมีเงื่อนไขแบบเต็มรูปแบบ

---
---