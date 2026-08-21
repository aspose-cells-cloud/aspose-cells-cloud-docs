---
---
title: "คำนวณสูตรทั้งหมดในสมุดงาน Excel"
second_title: "เอกสาร"
linktitle: "คำนวณ"
type: docs
url: /calculate-all-formulas-on-an-excel-file/
aliases:
  [/calculate-all-formulas-in-a-workbook/, /workbook/calculate-all-formulas/]
keywords: "Aspose.Cells, คำนวณสูตร, Excel API, SDK บนคลาวด์"
description: "คำนวณสูตรทุกสูตรในสมุดงาน Excel ผ่าน REST API ของ Aspose.Cells Cloud พร้อมตัวอย่าง cURL พารามิเตอร์คำขอ โครงสร้างการตอบกลับ ข้อกำหนดเบื้องต้น และตัวอย่างโค้ด SDK สำหรับภาษาต่างๆ"
weight: 140
ArticleTitle: "คำนวณสูตรทั้งหมดในสมุดงาน Excel"
---

REST API นี้ใช้คำนวณ **สูตรทั้งหมด** ในสมุดงาน Excel

**ข้อกำหนดเบื้องต้น:** ก่อนเรียกใช้เอนด์พอยต์นี้ ให้แน่ใจว่าคุณมี:
- โทเค็นยืนยันตัวตน JWT ที่ถูกต้อง (ดู[คู่มือการยืนยันตัวตน](/authentication/))  
- ไคลเอนต์ไอดีและคีย์ลับของ Aspose.Cells Cloud  
- สมุดงานเป้าหมายอัปโหลดไว้ในตำแหน่งจัดเก็บที่กำหนดแล้ว (ดู[การตั้งค่าพื้นที่จัดเก็บ](/storage/))

## API PostWorkbookCalculateFormula

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/calculateformula
```

พารามิเตอร์คำขอมีดังนี้:

| ชื่อพารามิเตอร์ | ชนิดข้อมูล        | ตำแหน่ง | คำอธิบาย                                                                 |
| ---------------- | ----------------- | -------- | ------------------------------------------------------------------------ |
| **name**         | string            | path     | ชื่อไฟล์สมุดงาน                                                         |
| **options**      | CalculationOptions | body     | ออบเจกต์ JSON ที่ระบุการตั้งค่าการคำนวณ (เช่น `CalcStackSize`, `IgnoreError`) |
| **ignoreError**  | boolean           | query    | เมื่อตั้งค่าเป็น `true` จะละเว้นข้อผิดพลาดที่เกิดขึ้นระหว่างการคำนวณ     |
| **folder**       | string            | query    | ตำแหน่งโฟลเดอร์ที่เก็บสมุดงาน                                          |
| **storageName**  | string            | query    | ชื่อของบริการจัดเก็บข้อมูลที่เก็บสมุดงานไว้                            |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookCalculateFormula) นิยามอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถใช้ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

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

#### รายละเอียดการตอบกลับ

| ฟิลด์           | ชนิดข้อมูล | คำอธิบาย                                                        |
| --------------- | ---------- | --------------------------------------------------------------- |
| **Code**        | int        | รหัสสถานะแบบ HTTP (200 หมายถึงความสำเร็จ)                      |
| **Status**      | string     | คำอธิบายสั้นๆ ของผลลัพธ์ (เช่น `OK`)                            |
| **WorkbookUrl** | string     | URL โดยตรงสำหรับดาวน์โหลดสมุดงานที่อัปเดตแล้ว                  |
| **ErrorMessage**| string     | ข้อมูลข้อผิดพลาดโดยละเอียดเมื่อคำขอล้มเหลว; เป็น `null` เมื่อสำเร็จ |

#### ขั้นตอนถัดไป / ข้อผิดพลาดที่พบบ่อย

- **จัดการข้อผิดพลาดจากการคำนวณ** – ตั้งค่า `ignoreError=false` เพื่อรับการตอบกลับข้อผิดพลาดเมื่อสูตรไม่สามารถประเมินผลได้
- **รับรู้ข้อจำกัดอัตรา (Rate-limit)** – ตรวจสอบหัวข้อ `X-RateLimit-Remaining`; หากค่าเป็น `0` ให้รอแล้วลองใหม่
- **คำแนะนำเกี่ยวกับรหัสสถานะ HTTP**:
  - `400` – พารามิเตอร์คำขอไม่ถูกต้อง
  - `401` – การยืนยันตัวตนล้มเหลว (โทเค็น JWT ไม่ถูกต้องหรือหมดอายุ)
  - `404` – ไม่พบสมุดงาน
  - `500` – ข้อผิดพลาดฝั่งเซิร์ฟเวอร์; ติดต่อทีมสนับสนุนของ Aspose หากยังคงเกิดข้อผิดพลาดนี้

| รหัส | ความหมาย               | เกิดขึ้นเมื่อ                                             |
|-----|-------------------------|----------------------------------------------------------|
| 400 | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์คำขอไม่ถูกต้องหรือ JSON มีรูปแบบไม่ถูกต้อง |
| 401 | ไม่ได้รับอนุญาต (Unauthorized) | ไม่มี หรือโทเค็น JWT ไม่ถูกต้องหรือหมดอายุ              |
| 404 | ไม่พบ (Not Found)        | สมุดงานที่ระบุไม่มีอยู่ในพื้นที่จัดเก็บ                  |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดฝั่งเซิร์ฟเวอร์; ติดต่อทีมสนับสนุนของ Aspose |

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณได้ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ[ที่เก็บบน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

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