---
---
title: "อัปเดตไฮเปอร์ลิงก์ในสมุดงาน Excel – คู่มือ API ของ Aspose.Cells Cloud"
description: "เรียนรู้วิธีการอัปเดตไฮเปอร์ลิงก์ในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API (เวอร์ชัน 3.0) ซึ่งรวมถึงอีนพอยต์ พารามิเตอร์ โครงสร้างของเนื้อหาคำขอ ตัวอย่าง cURL ตัวอย่างโค้ด SDK การจัดการข้อผิดพลาด การจำกัดอัตรา และข้อกำหนดเบื้องต้น"
keywords:
  - "Aspose.Cells"
  - "การอัปเดตไฮเปอร์ลิงก์"
  - "Excel API"
  - "REST API"
  - "สเปรดชีตบนคลาวด์"
  - "v3.0"
weight: 30
aliases:
  - /hyperlinks/update/
  - /update-hyperlinks-in-excel-worksheet/
---

# อัปเดตไฮเปอร์ลิงก์ในสมุดงาน Excel  

**เวอร์ชัน API:** v3.0  

การดำเนินการ **PostWorksheetHyperlink** ใช้อัปเดตไฮเปอร์ลิงก์ที่มีอยู่ในเวิร์กชีตที่ระบุด้วยดัชนีแบบเริ่มต้นที่ 0

---

## สารบัญ
1. [ข้อกำหนดเบื้องต้น](#prerequisites)  
2. [การจำกัดอัตรา](#rate-limiting)  
3. [อีนพอยต์](#endpoint)  
4. [พารามิเตอร์](#parameters)  
   - [พารามิเตอร์เส้นทาง](#path-parameters)  
   - [พารามิเตอร์แบบคิวรี](#query-parameters)  
   - [โครงสร้างของเนื้อหาคำขอ](#request-body-schema)  
5. [การตอบกลับ](#responses)  
   - [การตอบกลับที่สำเร็จ](#success-response)  
   - [การตอบกลับข้อผิดพลาด](#error-responses)  
6. [ตัวอย่าง cURL](#curl-example)  
7. [ตัวอย่างโค้ด SDK](#sdk-code-samples)  
8. [ดูเพิ่มเติม](#see-also)  

---

## ข้อกำหนดเบื้องต้น <a name="prerequisites"></a>

| ข้อกำหนด | คำอธิบาย |
|----------|-----------|
| **การยืนยันตัวตน** | การยืนยันตัวตนแบบใช้โทเค็น JWT รับโทเค็นได้ตามคำแนะนำใน [คู่มือการยืนยันตัวตน](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) |
| **การจัดเก็บ** | สมุดงานต้องถูกจัดเก็บไว้ในพื้นที่เก็บข้อมูลที่รองรับของ Aspose Cloud (ค่าเริ่มต้นคือ **Default**) |
| **สิทธิ์** | โทเค็น JWT ต้องมีสิทธิ์ในการอ่านและเขียนสมุดงานเป้าหมาย |
| **เฮดเดอร์** | จำเป็นต้องใช้ `Content-Type: application/json` และ `Accept: application/json` สำหรับคำขอทั้งหมด |

---

## การจำกัดอัตรา <a name="rate-limiting"></a>

Aspose.Cells Cloud จำกัดการเรียก API **สูงสุด 60 คำขอต่อนาทีต่อโทเค็นการเข้าถึง** หากเกินขีดจำกัดนี้ จะได้รับ HTTP **429 Too Many Requests** ให้ใช้การหน่วงเวลารูปแบบ exponential back‑off หรือปฏิบัติตามเฮดเดอร์ `Retry-After` เมื่อเกิดการจำกัดอัตรา

---

## อีนพอยต์ <a name="endpoint"></a>

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

*อัปเดตไฮเปอร์ลิงก์ที่ระบุด้วย `hyperlinkIndex` ในเวิร์กชีต `sheetName` ของไฟล์ `name`*

---

## พารามิเตอร์ <a name="parameters"></a>

### พารามิเตอร์เส้นทาง <a name="path-parameters"></a>

| ชื่อพารามิเตอร์ | ประเภท | จำเป็น | คำอธิบาย |
|----------------|--------|--------|-----------|
| `name`         | string | ✅ | ชื่อไฟล์ Excel (รวมนามสกุลด้วย) |
| `sheetName`    | string | ✅ | ชื่อเวิร์กชีตที่มีไฮเปอร์ลิงก์ |
| `hyperlinkIndex`| integer| ✅ | ดัชนีแบบเริ่มต้นที่ 0 ของไฮเปอร์ลิงก์ที่ต้องการอัปเดต |

### พารามิเตอร์แบบคิวรี <a name="query-parameters"></a>

| ชื่อพารามิเตอร์ | ประเภท | จำเป็น | คำอธิบาย |
|----------------|--------|--------|-----------|
| `folder`       | string | ❌ | เส้นทางโฟลเดอร์ในพื้นที่เก็บข้อมูลที่สมุดงานตั้งอยู่ |
| `storageName`  | string | ❌ | ชื่อบริการพื้นที่เก็บข้อมูล (เช่น `Default`) |

### โครงสร้างของเนื้อหาคำขอ <a name="request-body-schema"></a>

เนื้อหาคำขอต้องมีออบเจกต์ **`hyperlink`** เฉพาะฟิลด์ที่ต้องการเปลี่ยนแปลงเท่านั้นที่ต้องระบุ ฟิลด์ทางเลือกที่ไม่ระบุจะคงค่าเดิมไว้

| ฟิลด์         | ประเภท | จำเป็น | คำอธิบาย |
|---------------|--------|--------|-----------|
| `Address`     | string | ✅ | URL เป้าหมายของไฮเปอร์ลิงก์ |
| `Area`        | object | ✅ | ช่วงเซลล์ที่วางไฮเปอร์ลิงก์ ต้องมี `StartRow`, `StartColumn`, `EndRow`, `EndColumn` (ล้วนเป็นจำนวนเต็มแบบเริ่มต้นที่ 0) |
| `ScreenTip`   | string | ❌ | ข้อความคำใบ้เมื่อเลื่อนเมาส์ผ่าน |
| `TextToDisplay`| string| ❌ | ข้อความที่แสดงภายในเซลล์ |
| `link`        | object| ❌ | ลิงก์ไฮเปอร์มีเดีย (`Href`, `Rel`, `Title`, `Type`) โดยทั่วไปไม่ต้องระบุในเนื้อหาคำขอ |

**นิยามออบเจกต์ `Area`**

| ฟิลด์ย่อย     | ประเภท | จำเป็น | คำอธิบาย |
|---------------|--------|--------|-----------|
| `StartRow`    | integer| ✅ | ดัชนีแถวเริ่มต้นแบบเริ่มต้นที่ 0 |
| `StartColumn` | integer| ✅ | ดัชนีคอลัมน์เริ่มต้นแบบเริ่มต้นที่ 0 |
| `EndRow`      | integer| ✅ | ดัชนีแถวสิ้นสุดแบบเริ่มต้นที่ 0 |
| `EndColumn`   | integer| ✅ | ดัชนีคอลัมน์สิ้นสุดแบบเริ่มต้นที่ 0 |

---

## การตอบกลับ <a name="responses"></a>

### การตอบกลับที่สำเร็จ <a name="success-response"></a>

| ฟิลด์ | ประเภท | คำอธิบาย |
|-------|--------|-----------|
| `Code`| integer| โค้ดสถานะ HTTP (200 สำหรับความสำเร็จ) |
| `Status`| string| สถานะแบบข้อความ (`OK`) |
| `Hyperlink`| object (ไม่บังคับ) | ออบเจกต์ไฮเปอร์ลิงก์ที่อัปเดตแล้ว ซึ่งจะส่งกลับเมื่อขอออบเจกต์ย่อย `link` |

**ตัวอย่าง JSON**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### การตอบกลับข้อผิดพลาด <a name="error-responses"></a>

| โค้ด HTTP | เหตุผล | ตัวอย่างเนื้อหา |
|-----------|--------|----------------|
| **400** | คำขอไม่ถูกต้อง – พารามิเตอร์ขาดหรือไม่ถูกต้อง | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | ไม่มีสิทธิ์ – โทเค็น JWT ขาดหรือไม่ถูกต้อง | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | ไม่พบ – สมุดงาน เวิร์กชีต หรือไฮเปอร์ลิงก์ไม่มีอยู่ | `{ "Code":"404", "Message":"File not found." }` |
| **429** | คำขอมากเกินไป – เกินขีดจำกัดอัตรา | `{ "Code":"429", "Message":"Request limit exceeded. Retry later." }` |
| **500** | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เซิร์ฟเวอร์ล้มเหลวอย่างไม่คาดคิด | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

---

## ตัวอย่าง cURL <a name="curl-example"></a>

```bash
curl -L -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/1" \
  -H "Authorization: Bearer <YOUR_JWT_TOKEN>" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -d '{
        "hyperlink": {
          "Address": "https://www.msnbc.com/",
          "Area": {
            "StartRow": 1,
            "StartColumn": 6,
            "EndRow": 1,
            "EndColumn": 6
          },
          "ScreenTip": "MSNBC homepage",
          "TextToDisplay": "MSNBC"
        },
        "folder": "samples",
        "storageName": "Default"
      }'
```

**การตอบกลับ**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*เคล็ดลับ:* บันทึกเนื้อหา JSON ลงในไฟล์ (เช่น `payload.json`) และอ้างอิงโดยใช้ `--data @payload.json` เพื่อคัดลอกและวางได้ง่ายขึ้น

---

## ตัวอย่างโค้ด SDK <a name="sdk-code-samples"></a>

ตัวอย่างต่อไปนี้แสดงวิธีการเรียก **PostWorksheetHyperlink** โดยใช้ SDK ทางการของ Aspose.Cells Cloud แทนค่าตัวแปร (`<YOUR_JWT_TOKEN>`, `<FILE_NAME>` เป็นต้น) ด้วยข้อมูลจริง

| ภาษา | ตัวอย่าง |
|------|---------|
| **C#** | ```csharp\nvar api = new CellsApi("<client_id>", "<client_secret>");\nvar hyperlink = new Hyperlink {\n    Address = \"https://www.msnbc.com/\",\n    Area = new LinkArea { StartRow = 1, StartColumn = 6, EndRow = 1, EndColumn = 6 },\n    ScreenTip = \"MSNBC homepage\",\n    TextToDisplay = \"MSNBC\"\n};\nvar response = api.PostWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, folder: \"samples\");\n``` |
| **Java** | ```java\nCellsApi api = new CellsApi(clientId, clientSecret);\nHyperlink hyperlink = new Hyperlink();\nhyperlink.setAddress(\"https://www.msnbc.com/\");\nLinkArea area = new LinkArea();\narea.setStartRow(1);\narea.setStartColumn(6);\narea.setEndRow(1);\narea.setEndColumn(6);\nhyperlink.setArea(area);\nhyperlink.setScreenTip(\"MSNBC homepage\");\nhyperlink.setTextToDisplay(\"MSNBC\");\nCellsCloudResponse resp = api.postWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, \"samples\", null);\n``` |
| **Python** | ```python\nimport asposecellscloud\nfrom asposecellscloud.apis.cells_api import CellsApi\napi = CellsApi(client_id, client_secret)\nhyperlink = asposecellscloud.models.Hyperlink(\n    address=\"https://www.msnbc.com/\",\n    area=asposecellscloud.models.LinkArea(start_row=1, start_column=6, end_row=1, end_column=6),\n    screen_tip=\"MSNBC homepage\",\n    text_to_display=\"MSNBC\"\n)\nresponse = api.post_worksheet_hyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, folder=\"samples\")\n``` |
| **Node.js** | ```javascript\nconst { CellsApi, Hyperlink, LinkArea } = require('asposecellscloud');\nconst api = new CellsApi(clientId, clientSecret);\nlet hyperlink = new Hyperlink({\n  address: 'https://www.msnbc.com/',\n  area: new LinkArea({ startRow: 1, startColumn: 6, endRow: 1, endColumn: 6 }),\n  screenTip: 'MSNBC homepage',\n  textToDisplay: 'MSNBC'\n});\napi.postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, hyperlink, { folder: 'samples' })\n  .then(resp => console.log(resp));\n``` |
| **Go** | ```go\nimport (\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3/api\"\n)\nclient := api.NewCellsApiClient(clientId, clientSecret)\narea := asposecellscloud.LinkArea{StartRow: 1, StartColumn: 6, EndRow: 1, EndColumn: 6}\nhyperlink := asposecellscloud.Hyperlink{Address: \"https://www.msnbc.com/\", Area: &area, ScreenTip: \"MSNBC homepage\", TextToDisplay: \"MSNBC\"}\nresp, _ := client.PostWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, \"samples\", \"\")\nfmt.Println(resp)\n``` |
| **PHP** | ```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi($clientId, $clientSecret);\n$hyperlink = new \\Aspose\\Cells\\Model\\Hyperlink();\n$hyperlink->setAddress('https://www.msnbc.com/');\n$area = new \\Aspose\\Cells\\Model\\LinkArea();\n$area->setStartRow(1);\n$area->setStartColumn(6);\n$area->setEndRow(1);\n$area->setEndColumn(6);\n$hyperlink->setArea($area);\n$hyperlink->setScreenTip('MSNBC homepage');\n$hyperlink->setTextToDisplay('MSNBC');\n$response = $api->postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, $hyperlink, 'samples');\nprint_r($response);\n?>\n``` |
| **Ruby** | ```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new(client_id: CLIENT_ID, client_secret: CLIENT_SECRET)\nhyperlink = AsposeCellsCloud::Hyperlink.new(\n  address: 'https://www.msnbc.com/',\n  area: AsposeCellsCloud::LinkArea.new(start_row: 1, start_column: 6, end_row: 1, end_column: 6),\n  screen_tip: 'MSNBC homepage',\n  text_to_display: 'MSNBC'\n)\nresult = api.post_worksheet_hyperlink('test.xlsx', 'Sheet1', 1, hyperlink, folder: 'samples')\nputs result\n``` |
| **Perl** | ```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new(client_id => $client_id, client_secret => $client_secret);\nmy $area = AsposeCellsCloud::LinkArea->new(startRow => 1, startColumn => 6, endRow => 1, endColumn => 6);\nmy $hyperlink = AsposeCellsCloud::Hyperlink->new(address => 'https://www.msnbc.com/', area => $area, screenTip => 'MSNBC homepage', textToDisplay => 'MSNBC');\nmy $resp = $api->post_worksheet_hyperlink(name=>'test.xlsx', sheetName=>'Sheet1', hyperlinkIndex=>1, hyperlink=>$hyperlink, folder=>'samples');\nprint $resp->{Code}, \" \", $resp->{Status}, \"\\n\";\n``` |

*SDK ทั้งหมดเป็นโอเพนซอร์ส และสามารถค้นหาได้ที่ [ที่เก็บ GitHub ของ Aspose.Cells Cloud](https://github.com/aspose-cells-cloud)*

---

## ดูเพิ่มเติม <a name="see-also"></a>

- **การยืนยันตัวตน** – [เริ่มต้นใช้งานกับโทเค็น JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **การดำเนินการกับพื้นที่เก็บข้อมูล** – [อัปโหลดไฟล์](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)  
- **การดำเนินการอื่นกับไฮเปอร์ลิงก์** – [เพิ่มไฮเปอร์ลิงก์](https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink) \| [ลบไฮเปอร์ลิงก์](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlink)  
- **ข้อมูลจำเพาะ OpenAPI** – นิยามแบบเต็มของอีนพอยต์: <https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink>  

--- 

*เอกสารปรับปรุงล่าสุดเมื่อ: 2026-07-30*