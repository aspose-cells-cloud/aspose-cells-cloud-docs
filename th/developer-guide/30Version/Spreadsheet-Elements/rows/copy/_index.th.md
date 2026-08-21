---
---
title: "คัดลอกแถวในเวิร์กชีต Excel"
description: "คัดลอกข้อมูลและรูปแบบจากแถวทั้งแถวที่ระบุในเวิร์กชีต Excel โดยใช้ Aspose.Cells Cloud REST API (v3.0) ประกอบด้วยข้อมูลการตรวจสอบสิทธิ์ รายละเอียดคำขอ/การตอบกลับ การจัดการข้อผิดพลาด และตัวอย่าง SDK"
api_version: "v3.0"
endpoint: "/cells/{name}/worksheets/{sheetName}/cells/rows/copy"
method: "POST"
weight: 30
---

# คัดลอกแถวในเวิร์กชีต Excel <span style="float:right;">v3.0</span>

คัดลอกข้อมูลและรูปแบบจากแถวทั้งแถวที่ระบุในเวิร์กชีต

---

## ข้อกำหนดเบื้องต้น

| ลำดับ | ข้อกำหนด |
|---|-------------|
| 1 | โทเค็น **JWT** ที่ถูกต้อง ดูคำแนะนำการตรวจสอบสิทธิ์ได้ที่ [คู่มือการตรวจสอบสิทธิ์](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) |
| 2 | สมุดงาน (`{name}`) ต้องมีอยู่แล้วใน **โฟลเดอร์** / **พื้นที่จัดเก็บ** ที่เลือกไว้ |
| 3 | เวิร์กชีตเป้าหมาย (`{sheetName}`) ต้องมีอยู่ในสมุดงาน |
| 4 | (ไม่บังคับ) ระบุ **โฟลเดอร์** และ **storageName** หากไฟล์ไม่อยู่ในตำแหน่งเริ่มต้น |

---

## จุดปลายทาง (Endpoint)

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/copy
```

*พารามิเตอร์ในเส้นทางทั้งหมดมีการแยกแยะตัวพิมพ์เล็ก-ใหญ่*

### พารามิเตอร์ในเส้นทาง

| พารามิเตอร์ | ประเภท | จำเป็น | คำอธิบาย |
|-----------|--------|----------|-------------|
| `name`    | สตริง | ✅ | ชื่อไฟล์สมุดงาน (เช่น `test.xlsx`) |
| `sheetName` | สตริง | ✅ | ชื่อเวิร์กชีต (เช่น `Sheet1`) |

### พารามิเตอร์คิวรี

| พารามิเตอร์            | ประเภท | จำเป็น | คำอธิบาย |
|----------------------|---------|----------|-------------|
| `sourceRowIndex`     | จำนวนเต็ม | ✅ | ดัชนีของแถวต้นทาง (เริ่มจาก 0) |
| `destinationRowIndex`| จำนวนเต็ม | ✅ | ดัชนีของแถวที่จะวาง (เริ่มจาก 0) |
| `rowNumber`          | จำนวนเต็ม | ✅ | จำนวนแถวที่จะคัดลอก |
| `worksheet`          | สตริง  | ❌ | ตัวระบุเวิร์กชีต โดยทั่วไปจะเหมือนกับ **sheetName** |
| `folder`             | สตริง  | ❌ | เส้นทางไปยังโฟลเดอร์ที่เก็บสมุดงาน |
| `storageName`        | สตริง  | ❌ | ชื่อของบริการพื้นที่จัดเก็บ |

---

## ตัวอย่างคำขอ (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/copy?sourceRowIndex=1&destinationRowIndex=12&rowNumber=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **หมายเหตุ**  
> แทนที่ `<jwt token>` ด้วยโทเค็น JWT ที่ถูกต้องที่ได้รับจากบริการตรวจสอบสิทธิ์

---

## การตอบกลับเมื่อสำเร็จ

| โค้ด | คำอธิบาย |
|------|-------------|
| **200** | คัดลอกแถวเรียบร้อยแล้ว |

```json
{
  "Code": 200,
  "Status": "OK"
}
```

เนื้อหาการตอบกลับเป็นอินสแตนซ์ของ `CellsCloudResponse`

---

## การจัดการข้อผิดพลาด

| โค้ด HTTP | ความหมาย                              | ตัวอย่างเนื้อหา |
|-----------|--------------------------------------|--------------|
| **400**   | คำขอไม่ถูกต้อง – ขาดหรือพารามิเตอร์ไม่ถูกต้อง | `{ "Code": 400, "Message": "Invalid sourceRowIndex." }` |
| **401**   | ไม่มีสิทธิ์ – โทเค็น JWT ไม่ถูกต้องหรือขาดหาย | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**   | ไม่พบ – สมุดงานหรือเวิร์กชีตไม่มีอยู่ | `{ "Code": 404, "Message": "File not found." }` |
| **500**   | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เงื่อนไขที่ไม่คาดคิดของเซิร์ฟเวอร์ | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

**แนวทางการจัดการ**

* **400** – ตรวจสอบให้แน่ใจว่าพารามิเตอร์คิวรีที่จำเป็นทั้งหมดมีอยู่และอยู่ในรูปแบบที่ถูกต้อง  
* **401** – สร้างใหม่หรือรีเฟรชโทเค็น JWT  
* **404** – ยืนยันชื่อสมุดงานและเวิร์กชีต และตรวจสอบให้แน่ใจว่าไฟล์มีอยู่ในโฟลเดอร์/พื้นที่จัดเก็บที่ระบุ  
* **500** – ลองใหม่อีกครั้งหลังจากหน่วงเวลาสั้นๆ หากปัญหายังคงอยู่ โปรดติดต่อทีมสนับสนุนของ Aspose  

---

## ตัวอย่าง SDK

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้การดำเนินการ **คัดลอกแถว** โดยใช้ SDK ทางการของ Aspose.Cells Cloud

| ภาษา | ตัวอย่าง |
|----------|---------|
| **C#**   | <details><summary>แสดงโค้ด</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new CellsApi("clientId", "clientSecret");\nawait api.PostCopyWorksheetRowsAsync(name: "test.xlsx", sheetName: "Sheet1", sourceRowIndex: 1, destinationRowIndex: 12, rowNumber: 10);\n```</details> |
| **Java** | <details><summary>แสดงโค้ด</summary>```java\nCellsApi api = new CellsApi("clientId", "clientSecret");\napi.postCopyWorksheetRows("test.xlsx", "Sheet1", 1, 12, 10, null, null, null);\n```</details> |
| **Python** | <details><summary>แสดงโค้ด</summary>```python\nfrom asposecellscloud import CellsApi\napi = CellsApi(client_id='clientId', client_secret='clientSecret')\napi.post_copy_worksheet_rows(name='test.xlsx', sheet_name='Sheet1', source_row_index=1, destination_row_index=12, row_number=10)\n```</details> |
| **Node.js** | <details><summary>แสดงโค้ด</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi('clientId', 'clientSecret');\nawait api.postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Go** | <details><summary>แสดงโค้ด</summary>```go\nimport \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\napi := cells.NewCellsApiClient(\"clientId\", \"clientSecret\")\n_, err := api.PostCopyWorksheetRows(context.Background(), \"test.xlsx\", \"Sheet1\", 1, 12, 10, nil, nil, nil)\n```</details> |
| **PHP** | <details><summary>แสดงโค้ด</summary>```php\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi('clientId', 'clientSecret');\n$api->postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Ruby** | <details><summary>แสดงโค้ด</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new('clientId', 'clientSecret')\napi.post_copy_worksheet_rows('test.xlsx', 'Sheet1', 1, 12, 10)\n```</details> |
| **Perl** | <details><summary>แสดงโค้ด</summary>```perl\nuse Aspose::Cells::CellsApi;\nmy $api = Aspose::Cells::CellsApi->new('clientId', 'clientSecret');\n$api->postCopyWorksheetRows(name => 'test.xlsx', sheetName => 'Sheet1', sourceRowIndex => 1, destinationRowIndex => 12, rowNumber => 10);\n```</details> |

*ไฟล์ต้นฉบับแบบเต็มมีให้ดาวน์โหลดใน [GitHub repository ของ Aspose‑Cells‑Cloud](https://github.com/aspose-cells-cloud)*

---

## ดูเพิ่มเติม

- [เพิ่มแถวในเวิร์กชีต Excel](/rows/add/)  
- [ลบแถวในเวิร์กชีต Excel](/rows/delete/)  
- [อัปเดตแถวในเวิร์กชีต Excel](/rows/update/)  

---

*หน้านี้สร้างเมื่อ **{{DATE}}** สำหรับเวอร์ชันล่าสุดของ API นี้ โปรดดูที่ [สเปค OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetRows)*