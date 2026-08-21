---
---
title: "Aspose.Cells Cloud API – รับรายการวัตถุ (ตาราง) จากแผ่นงาน"
description: "ดึง ListObject (ตาราง) จากแผ่นงานในสมุด Excel โดยใช้ Aspose.Cells Cloud REST API รองรับการส่งออกเป็นรูปแบบต่างๆ (PDF, CSV, JSON, …)"
keywords:
  - Aspose.Cells
  - Cloud API
  - Excel
  - ListObject
  - ตาราง
  - REST
  - SDK
type: docs
slug: /list-objects/get/
weight: 9
---

# Aspose.Cells Cloud API – รับรายการวัตถุ (ตาราง) จากแผ่นงาน

ดึง **รายการวัตถุ** (หรือที่เรียกว่า *ตาราง*) จากแผ่นงานเฉพาะในสมุด Excel จุดสิ้นสุดนี้ยังสามารถส่งออกตารางไปยังรูปแบบที่เลือกโดยใช้พารามิเตอร์การคิวรี `format` แบบเสริมได้ด้วย

---

## ข้อกำหนดเบื้องต้น

| ข้อกำหนด | รายละเอียด |
|----------|-----------|
| **การยืนยันตัวตน** | ต้องมีโทเค็น **JWT** (Bearer) ที่ถูกต้อง รับโทเค็นผ่านขั้นตอนการยืนยันตัวตนแบบ **OAuth2** ตามที่อธิบายไว้ใน[คู่มือการยืนยันตัวตน](/authentication/) |
| **พื้นที่จัดเก็บ** | สมุดงานต้องถูกจัดเก็บไว้ในตำแหน่งพื้นที่จัดเก็บของ Aspose Cloud หากไฟล์อยู่ในพื้นที่จัดเก็บที่ไม่ใช่ค่าเริ่มต้น ให้ระบุพารามิเตอร์การคิวรี `storageName` |
| **ขีดจำกัดอัตราการใช้งาน** | API นี้ปฏิบัติตามนโยบายขีดจำกัดอัตราการใช้งานแบบมาตรฐานของ Aspose Cloud (ค่าเริ่มต้น = 100 คำขอ/นาทีต่อบัญชี) |
| **SDK (ทางเลือก)** | การใช้หนึ่งใน SDK อย่างเป็นทางการ (C#, Java, Python, …) จะช่วยให้การสร้างคำขอและการจัดการการตอบกลับทำได้ง่ายขึ้น ดูหัวข้อ **ตัวอย่าง SDK** ด้านล่าง |

---

## คำขอ

### HTTP GET

```
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}
```

| พารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | จำเป็น | คำอธิบาย |
|-------------|----------|---------|--------|-----------|
| **name** | `string` | Path | ✔️ | ชื่อไฟล์ Excel (รวมส่วนขยาย) |
| **sheetName** | `string` | Path | ✔️ | แผ่นงานที่มีรายการวัตถุ |
| **listobjectindex** | `integer` | Path | ✔️ | ดัชนีแบบเริ่มต้นที่ 0 ของรายการวัตถุที่ต้องการดึง |
| **format** | `string` | Query | ❌ | รูปแบบการส่งออกที่ต้องการ (เช่น `pdf`, `csv`, `json`) |
| **folder** | `string` | Query | ❌ | ที่อยู่โฟลเดอร์ที่เก็บสมุดงานไว้ |
| **storageName** | `string` | Query | ❌ | ชื่อพื้นที่จัดเก็บของ Aspose Cloud ที่ต้องการใช้งาน |

#### หมายเหตุ

* ทุกคำขอ **ต้อง** ส่งผ่าน HTTPS เท่านั้น  
* เมื่อมีการระบุพารามิเตอร์ `format` ส่วนเนื้อหาการตอบกลับจะเป็นสตรีมไฟล์ที่ส่งออกแล้ว (เช่น `application/pdf`)  
* หากไม่มี `format` API จะคืนค่าคำอธิบาย JSON ของ ListObject กลับมา

---

## ตัวอย่าง cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/1?format=csv" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

*แทนที่ `<your_jwt_token>` ด้วย JWT ที่ถูกต้องที่ได้มาจากรหัสจุดสิ้นสุดการยืนยันตัวตน*

---

## การตอบกลับที่สำเร็จ (JSON)

เมื่อ **ไม่ได้ระบุ `format`** API จะส่งค่า JSON ที่อธิบายรายละเอียด ListObject กลับมา

```json
{
  "ListObject": {
    "AutoFilter": {
      "FilterColumns": [],
      "Range": "B2:F11",
      "Sorter": {
        "CaseSensitive": false,
        "HasHeaders": false,
        "KeyList": [],
        "SortLeftToRight": false
      }
    },
    "DisplayName": "Table3",
    "StartColumn": 1,
    "StartRow": 1,
    "EndColumn": 5,
    "EndRow": 10,
    "ListColumns": [
      {
        "Name": "Column1",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 1,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$B$2:$B$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column2",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 2,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$C$2:$C$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column3",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 3,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$D$2:$D$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column4",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 4,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$E$2:$E$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column5",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 5,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$F$2:$F$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      }
    ],
    "ShowHeaderRow": true,
    "ShowTableStyleColumnStripes": false,
    "ShowTableStyleFirstColumn": false,
    "ShowTableStyleLastColumn": false,
    "ShowTableStyleRowStripes": true,
    "ShowTotals": false,
    "TableStyleName": "None",
    "TableStyleType": "None",
    "link": {
      "Href": "api-qa.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

เมื่อ **มีการระบุ `format`** ส่วนเนื้อหาการตอบกลับจะเป็นสตรีมไบนารีของไฟล์ตามรูปแบบที่ร้องขอ (เช่น `Content-Type: text/csv`)

---

## การจัดการข้อผิดพลาด

| HTTP Code | ความหมาย | ตัวอย่าง JSON |
|-----------|----------|---------------|
| **400** | คำขอไม่ถูกต้อง – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง | `{"Code":400,"Message":"Invalid format parameter."}` |
| **401** | ไม่ได้รับอนุญาต – โทเค็น JWT ขาดหายหรือไม่ถูกต้อง | `{"Code":401,"Message":"Authentication failed."}` |
| **404** | ไม่พบ – สมุดงาน แผ่นงาน หรือรายการวัตถุไม่มีอยู่จริง | `{"Code":404,"Message":"ListObject not found."}` |
| **500** | ข้อผิดพลาดภายในเซิร์ฟเวอร์ | `{"Code":500,"Message":"Unexpected server error."}` |

### ข้อผิดพลาดที่พบบ่อย (หมายเหตุ)

* **ดัชนีแบบเริ่มต้นที่ 0** – `listobjectindex` เริ่มต้นที่ **0** การร้องขอดัชนี `1` จะส่งคืนตารางตารางที่สองในแผ่นงาน  
* **โฟลเดอร์และพื้นที่จัดเก็บ** – หากสมุดงานถูกจัดเก็บไว้ในโฟลเดอร์ย่อย ให้ระบุพารามิเตอร์การคิวรี `folder` (เช่น `?folder=Reports/2024`)  
* **รูปแบบการส่งออก** – อนุญาตเฉพาะรูปแบบที่ได้รับการสนับสนุนโดยเครื่องมือแปลงของ Aspose.Cells (`pdf`, `xlsx`, `csv`, `json`, …) การระบุค่าที่ไม่รองรับจะทำให้เกิดข้อผิดพลาด **400**

---

## ตัวอย่าง SDK

โค้ดตัวอย่างต่อไปนี้แสดงวิธีการเรียกจุดสิ้นสุดโดยใช้ SDK อย่างเป็นทางการของ Aspose.Cells Cloud แทนที่ค่าตัวแปร (`<YOUR_CLIENT>`, `<YOUR_JWT>` เป็นต้น) ด้วยการตั้งค่าจริงของคุณ

<details>
<summary>💻 C#</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// เริ่มต้น API client
var apiInstance = new ListObjectsApi();

// สร้างคำขอ
var request = new GetWorksheetListObjectRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: null,               // เช่น "csv" เพื่อส่งออก
    folder: null,
    storageName: null
);

// ดำเนินการ
var response = apiInstance.GetWorksheetListObject(request);
Console.WriteLine(response);
```
</details>

<details>
<summary>☕ Java</summary>

```java
import com.aspose.cells.cloud.api.ListObjectsApi;
import com.aspose.cells.cloud.model.*;
import com.aspose.cells.cloud.model.requests.*;

public class GetWorksheetListObjectExample {
    public static void main(String[] args) throws ApiException {
        ListObjectsApi apiInstance = new ListObjectsApi();

        GetWorksheetListObjectRequest request = new GetWorksheetListObjectRequest(
                "Book1.xlsx",   // name
                "Sheet1",       // sheetName
                1,              // listobjectindex
                null,           // format
                null,           // folder
                null            // storageName
        );

        ListObjectResponse result = apiInstance.getWorksheetListObject(request);
        System.out.println(result);
    }
}
```
</details>

<details>
<summary>🐍 Python</summary>

```python
from asposecellscloud.apis.list_objects_api import ListObjectsApi
from asposecellscloud.models import GetWorksheetListObjectRequest

api = ListObjectsApi()

request = GetWorksheetListObjectRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    listobjectindex=1,
    format=None,
    folder=None,
    storage_name=None
)

response = api.get_worksheet_list_object(request)
print(response)
```
</details>

<details>
<summary>🟢 Node.js (TypeScript)</summary>

```typescript
import { ListObjectsApi, GetWorksheetListObjectRequest } from "@asposecellscloud/asposecellscloud";

const api = new ListObjectsApi();

const request = new GetWorksheetListObjectRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: undefined,
    folder: undefined,
    storageName: undefined
});

api.getWorksheetListObject(request)
   .then(response => console.log(response))
   .catch(err => console.error(err));
```
</details>

<details>
<summary>🐘 PHP</summary>

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

use Aspose\Cells\Cloud\Api\ListObjectsApi;
use Aspose\Cells\Cloud\Model\Requests\GetWorksheetListObjectRequest;

$listObjectsApi = new ListObjectsApi();

$request = new GetWorksheetListObjectRequest(
    "Book1.xlsx",   // name
    "Sheet1",       // sheetName
    1,              // listobjectindex
    null,           // format
    null,           // folder
    null            // storageName
);

$response = $listObjectsApi->getWorksheetListObject($request);
print_r($response);
?>
```
</details>

<details>
<summary>💎 Ruby</summary>

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::ListObjectsApi.new

request = AsposeCellsCloud::GetWorksheetListObjectRequest.new(
  name: 'Book1.xlsx',
  sheet_name: 'Sheet1',
  listobjectindex: 1,
  format: nil,
  folder: nil,
  storage_name: nil
)

result = api_instance.get_worksheet_list_object(request)
puts result
```
</details>

<details>
<summary>🦪 Go</summary>

```go
package main

import (
    "fmt"
    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
)

func main() {
    cfg := cells.NewConfiguration()
    cfg.AddDefaultHeader("Authorization", "Bearer <your_jwt>")
    client := api.NewAPIClient(cfg)

    request := api.GetWorksheetListObjectRequest{
        Name:            "Book1.xlsx",
        SheetName:       "Sheet1",
        Listobjectindex: 1,
        Format:          nil,
        Folder:          nil,
        StorageName:     nil,
    }

    result, _, err := client.ListObjectsApi.GetWorksheetListObject(request)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Printf("%+v\n", result)
}
```
</details>

---

## ดูเพิ่มเติม

| จุดสิ้นสุดที่เกี่ยวข้อง | คำอธิบาย |
|------------------------|-----------|
| **เพิ่ม ListObject** | `POST /cells/{name}/worksheets/{sheetName}/listobjects` – สร้างตารางใหม่ |
| **อัปเดต ListObject** | `PUT /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` – แก้ไขคุณสมบัติของตาราง |
| **ลบ ListObject** | `DELETE /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` – ลบตารางออก |
| **แสดงรายการ ListObjects ทั้งหมด** | `GET /cells/{name}/worksheets/{sheetName}/listobjects` – แสดงรายการตารางทั้งหมดในแผ่นงาน |

---

## อ้างอิง

* **สเปค OpenAPI** – <https://apireference.aspose.cloud/cells/#/ListObjects/GetWorksheetListObject>  
* **คู่มือการยืนยันตัวตน** – <https://docs.aspose.cloud/cells/authentication/>  
* **ที่เก็บ GitHub (SDKs)** – <https://github.com/aspose-cells-cloud>  

---
---