---
---
title: เพิ่มเงื่อนไขให้กับการจัดรูปแบบตามเงื่อนไข
description: เรียนรู้วิธีเพิ่มเงื่อนไขให้กับการจัดรูปแบบตามเงื่อนไขในเวิร์กชีตโดยใช้ Aspose.Cells Cloud REST API (v3.0) รวมถึง endpoint, พารามิเตอร์, การยืนยันตัวตน, ตัวอย่าง cURL, ตัวอย่างโค้ด SDK และการจัดการข้อผิดพลาด
keywords: "Aspose.Cells Cloud, การจัดรูปแบบตามเงื่อนไข, เพิ่มเงื่อนไข, REST API, Excel, เวิร์กชีต"
type: docs
url: /conditional-formattings/add-a-condition/
aliases:
  - /add-a-condition-for-format-condition/
weight: 40
---

# เพิ่มเงื่อนไขให้กับการจัดรูปแบบตามเงื่อนไข

เพิ่มเงื่อนไขให้กับกฎการจัดรูปแบบตามเงื่อนไขที่มีอยู่ในเวิร์กชีตโดยใช้ Aspose.Cells Cloud REST API (v3.0)

---

## ข้อกำหนดเบื้องต้น

| ข้อกำหนด | รายละเอียด |
|-------------|---------|
| **การยืนยันตัวตน** | โทเคน JWT ที่ถูกต้อง (Bearer) ที่ได้มาผ่านฟลows OAuth 2.0 |
| **เวอร์ชัน API** | v3.0 – URL endpoint จะมี `/v3.0/` |
| **ที่จัดเก็บข้อมูล (Storage)** | เวิร์กบุ๊กต้องอยู่ในตำแหน่งที่จัดเก็บที่ Aspose.Cells Cloud สามารถเข้าถึงได้ (ค่าเริ่มต้นคือ `Default`) |
| **สิทธิ์การใช้งาน** | มีสิทธิ์อ่าน/เขียนบนเวิร์กบุ๊กเป้าหมาย |
| **รูปแบบที่รองรับ** | รูปแบบเวิร์กบุ๊กใดก็ตามที่ Aspose.Cells รองรับ (เช่น `.xlsx`, `.xls`, `.xlsm`) |

---

## Endpoint

**วิธี HTTP:** `PUT`  
**URL:**  

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition
```

| พารามิเตอร์ | ตำแหน่ง | ชนิดข้อมูล | จำเป็น | คำอธิบาย |
|-----------|----------|------|----------|-------------|
| `name` | Path | string | **ใช่** | ชื่อไฟล์เวิร์กบุ๊ก (รวมนามสกุลด้วย) |
| `sheetName` | Path | string | **ใช่** | ชื่อเวิร์กชีตที่มีการจัดรูปแบบตามเงื่อนไข |
| `index` | Path | integer | **ใช่** | ดัชนีแบบเริ่มต้นที่ 0 ของคอลเลกชันการจัดรูปแบบตามเงื่อนไขที่ต้องการแก้ไข |
| `type` | Query | string | **ใช่** | ประเภทของเงื่อนไข ค่าที่อนุญาต: `CellValue`, `Expression`, `ColorScale`, `DataBar`, `IconSet`, `Top10`, `UniqueValues`, `DuplicateValues`, `ContainsText`, `NotContainsText`, `BeginsWith`, `EndsWith`, `ContainsBlanks`, `NotContainsBlanks`, `ContainsErrors`, `NotContainsErrors`, `TimePeriod`, `AboveAverage` |
| `operatorType` | Query | string | **ใช่** | ตัวดำเนินการสำหรับเงื่อนไข ค่าที่อนุญาต: `Between`, `Equal`, `GreaterThan`, `GreaterOrEqual`, `LessThan`, `None`, `NotBetween`, `NotEqual` |
| `formula1` | Query | string | **ใช่** | สูตร/ค่าแรกที่เกี่ยวข้องกับเงื่อนไข |
| `formula2` | Query | string | ไม่จำเป็น | สูตร/ค่าที่สอง (จำเป็นเฉพาะเมื่อใช้ตัวดำเนินการที่ต้องการค่าสองค่า เช่น `Between`) |
| `folder` | Query | string | ไม่จำเป็น | โฟลเดอร์ในที่จัดเก็บข้อมูลที่เวิร์กบุ๊กอยู่ |
| `storageName` | Query | string | ไม่จำเป็น | ชื่อของบริการที่จัดเก็บข้อมูล |

> **หมายเหตุ:** พารามิเตอร์ path ทั้งหมด (`name`, `sheetName`, `index`) และพารามิเตอร์ query `type`, `operatorType`, `formula1` นั้นจำเป็นต้องระบุ ส่วน `formula2`, `folder` และ `storageName` เป็นพารามิเตอร์ที่ไม่จำเป็น

---

## ตัวอย่างคำขอ (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition?type=CellValue&operatorType=Equal&formula1=v1&formula2=v2" \
 -X PUT \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt_token>"
```

*แทน `<jwt_token>` ด้วยโทเคนเข้าถึงที่ถูกต้อง และปรับค่า `name`, `sheetName`, `index` และค่า query ตามความจำเป็น*

---

## การตอบกลับที่ประสบความสำเร็จ

```json
{
  "Code": "200",
  "Status": "OK"
}
```

การตอบกลับนี้บ่งชี้ว่าเพิ่มเงื่อนไขสำเร็จแล้ว การดำเนินการจะคืนค่าออบเจกต์ `CellsCloudResponse` ทั่วไปซึ่งประกอบด้วยรหัสสถานะ HTTP และข้อความสถานะสั้นๆ

---

## การตอบกลับข้อผิดพลาด

| รหัส HTTP | เหตุผล | ตัวอย่างเนื้อหา |
|-----------|--------|--------------|
| **400** | คำขอไม่ถูกต้อง – พารามิเตอร์หายไปหรือไม่ถูกต้อง | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | ไม่ได้รับอนุญาต – โทเคน JWT หายไปหรือไม่ถูกต้อง | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | ไม่พบ – เวิร์กบุ๊ก เวิร์กชีต หรือดัชนีการจัดรูปแบบตามเงื่อนไขไม่มีอยู่ | `{ "Code":"404", "Message":"File not found." }` |
| **500** | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เซิร์ฟเวอร์ล้มเหลวอย่างไม่คาดคิด | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

---

## หมายเหตุและข้อควรระวังทั่วไป

* **การเข้ารหัสพารามิเตอร์** – ต้องเข้ารหัสอักขระพิเศษใน `formula1`/`formula2` (เช่น ช่องว่าง → `%20`)  
* **ความเข้ากันได้ของตัวดำเนินการ** – ตัวดำเนินการบางชนิด (เช่น `Between`) ต้องการทั้ง `formula1` และ `formula2` ใช้เพียง `formula1` สำหรับตัวดำเนินการที่ต้องการค่าเดียวเท่านั้น  
* **ดัชนีการจัดรูปแบบตามเงื่อนไข** – ดัชนีเริ่มต้นที่ 0 ใช้ endpoint **Get Conditional Formattings** เพื่อดึงดัชนีที่ถูกต้องหากคุณไม่แน่ใจ  
* **โฟลเดอร์ที่จัดเก็บข้อมูล** – หากเวิร์กบุ๊กอยู่ในโฟลเดอร์ที่ไม่ใช่ค่าเริ่มต้น ให้ระบุพารามิเตอร์ query `folder` มิฉะนั้น API จะถือว่าอยู่ในโฟลเดอร์ราก  
* **การจำกัดอัตรา** – Aspose.Cells Cloud บังคับใช้ข้อจำกัดจำนวนคำขอต่อบัญชี หากได้รับการตอบกลับ 429 ให้รอสักครู่แล้วลองใหม่  

---

## ตัวอย่าง SDK

ด้านล่างนี้คือตัวอย่างโค้ดที่พร้อมรันสำหรับ SDK ที่นิยมมากที่สุด แทนที่ค่าตัวแปรจำเพาะ (`YOUR_FILE`, `YOUR_SHEET` เป็นต้น) ด้วยข้อมูลของคุณเอง

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var apiInstance = new ConditionalFormattingsApi();
        string name = "Book1.xlsx";
        string sheetName = "Sheet1";
        int index = 0;
        string type = "CellValue";
        string operatorType = "Equal";
        string formula1 = "v1";
        string formula2 = "v2";
        string folder = null;          // optional
        string storageName = null;     // optional

        try
        {
            var response = apiInstance.PutWorksheetFormatConditionCondition(
                name, sheetName, index, type, operatorType, formula1, formula2, folder, storageName);
            Console.WriteLine($"Status: {response.Status}");
        }
        catch (Exception e)
        {
            Console.WriteLine("Exception when calling ConditionalFormattingsApi.PutWorksheetFormatConditionCondition: " + e.Message);
        }
    }
}
```

### Java

```java
import com.aspose.cloud.cells.api.ConditionalFormattingsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class AddConditionExample {
    public static void main(String[] args) {
        ConditionalFormattingsApi api = new ConditionalFormattingsApi();

        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String type = "CellValue";
        String operatorType = "Equal";
        String formula1 = "v1";
        String formula2 = "v2";

        try {
            CellsCloudResponse resp = api.putWorksheetFormatConditionCondition(
                    name, sheetName, index, type, operatorType, formula1, formula2, null, null);
            System.out.println("Response: " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Node.js

```javascript
const { ConditionalFormattingsApi, ApiClient } = require('asposecellscloud');
const api = new ConditionalFormattingsApi();

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const type = "CellValue";
const operatorType = "Equal";
const formula1 = "v1";
const formula2 = "v2";

api.putWorksheetFormatConditionCondition(
    name,
    sheetName,
    index,
    type,
    operatorType,
    formula1,
    formula2,
    null,
    null
).then((response) => {
    console.log('Status:', response.body.Status);
}).catch((err) => {
    console.error(err);
});
```

### Ruby

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::ConditionalFormattingsApi.new
name = 'Book1.xlsx'
sheet_name = 'Sheet1'
index = 0
type = 'CellValue'
operator_type = 'Equal'
formula1 = 'v1'
formula2 = 'v2'

begin
  result = api_instance.put_worksheet_format_condition_condition(
    name, sheet_name, index, type, operator_type, formula1, formula2, nil, nil
  )
  puts "Status: #{result.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling ConditionalFormattingsApi->put_worksheet_format_condition_condition: #{e}"
end
```

### Perl

```perl
use AsposeCellsCloud::ConditionalFormattingsApi;

my $api_instance = AsposeCellsCloud::ConditionalFormattingsApi->new();

my $name         = 'Book1.xlsx';
my $sheet_name   = 'Sheet1';
my $index        = 0;
my $type         = 'CellValue';
my $operatorType = 'Equal';
my $formula1     = 'v1';
my $formula2     = 'v2';

eval {
    my $result = $api_instance->put_worksheet_format_condition_condition(
        name => $name,
        sheet_name => $sheet_name,
        index => $index,
        type => $type,
        operator_type => $operatorType,
        formula1 => $formula1,
        formula2 => $formula2,
        folder => undef,
        storage_name => undef
    );
    print "Status: " . $result->{status} . "\n";
};
if ($@) {
    warn "Exception when calling ConditionalFormattingsApi->put_worksheet_format_condition_condition: $@\n";
}
```

### Go

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    cfg := sdk.NewConfiguration()
    cfg.AccessToken = "YOUR_JWT_TOKEN"
    api := sdk.NewConditionalFormattingsApi(cfg)

    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    condType := "CellValue"
    operatorType := "Equal"
    formula1 := "v1"
    formula2 := "v2"

    resp, _, err := api.PutWorksheetFormatConditionCondition(
        name, sheetName, index, condType, operatorType, formula1, formula2, nil, nil,
    )
    if err != nil {
        fmt.Printf("Error: %v\n", err)
        return
    }
    fmt.Printf("Status: %s\n", resp.Status)
}
```

> **SDK ที่ขาดหายไป** – หากภาษาที่คุณต้องการใช้ไม่อยู่ในรายการ ให้อ้างอิงจาก **API Reference** แบบทั่วไป และสร้างคำขอ HTTP ด้วยตนเอง

---

## ดูเพิ่มเติม

- **[รับรายการการจัดรูปแบบตามเงื่อนไข](https://docs.aspose.cloud/cells/conditional-formattings/get-conditional-formattings/)** – ดึงรายการกฎการจัดรูปแบบตามเงื่อนไขของเวิร์กชีต  
- **[ลบการจัดรูปแบบตามเงื่อนไข](https://docs.aspose.cloud/cells/conditional-formattings/delete-a-conditional-formatting/)** – ลบกฎการจัดรูปแบบตามเงื่อนไขที่มีอยู่  
- **[สเปค OpenAPI](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatConditionCondition)** – คำนิยามแบบอ่านได้โดยเครื่องจักรทั้งหมดของการดำเนินการนี้  

---  
---