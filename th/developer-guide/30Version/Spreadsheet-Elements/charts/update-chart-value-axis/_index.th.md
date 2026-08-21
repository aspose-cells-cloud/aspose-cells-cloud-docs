---
title: "Aspose.Cells Cloud API – อัปเดตแกนค่าของแผนภูมิ (POST /valueaxis)"
description: "อัปเดตแกนค่าของแผนภูมิในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API ครอบคลุม endpoint, พารามิเตอร์, โครงสร้าง request body, ตัวอย่าง (cURL และ SDK), การตอบกลับ และการจัดการข้อผิดพลาด"
keywords:
  - Aspose.Cells Cloud
  - อัปเดตแกนค่าของแผนภูมิ
  - REST API
  - แกนแผนภูมิใน Excel
  - POST valueaxis
  - ตัวอย่าง cURL
  - SDK
  - JSON payload
  - การตั้งค่าแกนแผนภูมิ
last_updated: 2026-07-30
---

# อัปเดตแกนค่าของแผนภูมิ (POST /valueaxis)

**สรุป:**  
ปรับแก้แกนค่าของแผนภูมิที่ระบุในสมุดงาน Excel ที่จัดเก็บไว้ใน Aspose Cloud คุณสามารถตั้งค่าขอบเขต หน่วยแท็ก แบบจำลองเชิงล็อกาลิทึม และคุณสมบัติอื่นๆ ของแกนได้ในคำขอเดียว

---

## เงื่อนไขเบื้องต้น

1. **โทเคน JWT** – รับโทเคนตามที่อธิบายไว้ใน[คู่มือการตรวจสอบสิทธิ์](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
2. **สมุดงานเป้าหมาย** ต้องอัปโหลดไว้ในพื้นที่จัดเก็บของ Aspose Cloud แล้ว (หรือใช้พื้นที่จัดเก็บเริ่มต้น)  
3. ทราบ **ชื่อชีต** และ **ดัชนีแผนภูมิแบบเริ่มต้นที่ 0** ที่ต้องการแก้ไข

---

## Endpoint

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

*แทนค่าตัวแปรด้วยข้อมูลจริงของคุณ*

| ตัวแปรแทน | คำอธิบาย |
|-----------|----------|
| `{name}` | ชื่อไฟล์ Excel (เช่น `Book1.xlsx`) |
| `{sheetName}` | ชีตที่มีแผนภูมิ (เช่น `Sheet1`) |
| `{chartIndex}` | ดัชนีแผนภูมิแบบเริ่มต้นที่ 0 (เช่น `0`) |

---

## การตรวจสอบสิทธิ์

API ใช้การตรวจสอบสิทธิ์แบบโทเคน JWT ใส่โทเคนใน header `Authorization`:

```
Authorization: Bearer <jwt token>
```

---

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้การตรวจสอบสิทธิ์แบบโทเคน JWT [ดูรายละเอียดเพิ่มเติม](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## พารามิเตอร์คำขอ

| ชื่อ          | ตำแหน่ง | ประเภท | จำเป็น | คำอธิบาย |
|---------------|----------|--------|--------|----------|
| **name**      | Path     | string | ใช่    | ชื่อไฟล์ Excel ที่จัดเก็บไว้บนคลาวด์ |
| **sheetName** | Path     | string | ใช่    | ชีตที่มีแผนภูมิ |
| **chartIndex**| Path     | int    | ใช่    | ดัชนีแผนภูมิแบบเริ่มต้นที่ 0 ที่ต้องการอัปเดต |
| **axis**      | Body     | object | ใช่    | การตั้งค่าแกน (ดู *โครงสร้าง request body*) |
| **folder**    | Query    | string | ไม่จำเป็น | เส้นทางโฟลเดอร์บนคลาวด์ที่ไฟล์อยู่ |
| **storageName**| Query   | string | ไม่จำเป็น | ชื่อของบริการจัดเก็บที่ต้องการใช้ |

---

## โครงสร้าง Request Body (ออบเจกต์ `axis`)

คุณต้องระบุเฉพาะคุณสมบัติที่ต้องการเปลี่ยนแปลงเท่านั้น

| คุณสมบัติ       | ประเภท    | จำเป็น | คำอธิบาย |
|----------------|----------|--------|----------|
| `minimum`      | number   | ไม่จำเป็น | ขอบเขตล่างของแกน |
| `maximum`      | number   | ไม่จำเป็น | ขอบเขตบนของแกน |
| `majorUnit`    | number   | ไม่จำเป็น | ช่วงห่างระหว่างแท็กหลัก |
| `minorUnit`    | number   | ไม่จำเป็น | ช่วงห่างระหว่างแท็กย่อย |
| `logBase`      | number   | ไม่จำเป็น | ฐานของล็อกาลิทึมเมื่อ `isLogarithmic` เป็น `true` |
| `isLogarithmic`| boolean  | ไม่จำเป็น | ระบุว่าแกนใช้แบบจำลองเชิงล็อกาลิทึมหรือไม่ |
| `displayUnit`  | string   | ไม่จำเป็น | ป้ายชื่อหน่วยที่แสดงบนแกน (เช่น `"Thousands"`) |
| `tickMark`     | string   | ไม่จำเป็น | สไตล์ของแท็ก (`"inside"`, `"outside"` เป็นต้น) |
| `crossAt`      | number   | ไม่จำเป็น | ตำแหน่งที่แกนตัดแกนตั้งฉาก |

### ตัวอย่าง Request Body

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

## ตัวอย่างคำขอ

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

### ตัวอย่าง SDK  

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
// ตัวอย่าง Node.js
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
// ตัวอย่าง Android (Java)
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

## การตอบกลับ

### สำเร็จ (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

ประเภทการตอบกลับคือ `CellsCloudResponse`

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | คำอธิบาย                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                 | ใช้ตัวกรองเรียบร้อย; การตอบกลับมีรายละเอียดการดำเนินการ |
| 400  | คำขอผิดรูปแบบ (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือไม่มี |
| 413  | Payload ใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดในเซิร์ฟเวอร์ |
---

## ทรัพยากรเพิ่มเติม

- **สเปค OpenAPI** – [ดู / ดาวน์โหลด JSON-YAML](https://apireference.aspose.cloud/cells/#/Charts/PostChartValueAxis)  
- **Repository SDK** – <https://github.com/aspose-cells-cloud>  
- **คู่มือการตรวจสอบสิทธิ์** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>

---

*หากมีคำถามหรือข้อเสนอแนะใดๆ กรุณาติดต่อทีมสนับสนุนของ Aspose.Cells Cloud*