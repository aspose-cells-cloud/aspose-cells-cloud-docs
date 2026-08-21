---
title: "วิธีการจัดการการมองเห็นในแผ่นงาน Excel"
second_title: "เอกสาร"
linktype: "การมองเห็น"
type: docs
url: /worksheets/panes/
keywords: "Aspose.Cells Cloud, API ซ่อนแผ่นงาน, API ยกเลิกการซ่อนแผ่นงาน, การมองเห็นแผ่นงาน Excel, REST API สำหรับ Excel, Aspose.Cells v3.0"
description: "เรียนรู้วิธีซ่อนหรือยกเลิกการซ่อนแผ่นงาน Excel โดยใช้ REST API ของ Aspose.Cells Cloud อย่างเป็นโปรแกรม รวมตัวอย่าง URL คำขอ, cURL และ .NET SDK การจัดการข้อผิดพลาด และหมายเหตุเฉพาะรุ่น"
weight: 20
---

## การจัดการการมองเห็นในแผ่นงาน Excel

*การมองเห็นของแผ่นงาน* กำหนดว่าแผ่นงานจะแสดงให้ผู้ใช้ปลายทางเห็นหรือไม่ ด้วย Aspose.Cells Cloud คุณสามารถซ่อนหรือยกเลิกการซ่อนแผ่นงานได้ผ่านคำขอ REST ที่ง่ายดาย โดยจุดปลายทางของ API ที่ใช้คือ:

* **ซ่อนแผ่นงาน** – `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`  
* **ยกเลิกการซ่อนแผ่นงาน** – `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`

> **รุ่น API ที่รองรับ:** **v3.0** (ณ เดือนมีนาคม 2569)

### ข้อกำหนดเบื้องต้น
1. บัญชี **Aspose.Cells Cloud** ที่ยังมีผลใช้งาน  
2. **Client ID** และ **Client Secret** ที่ถูกต้อง (หรือโทเค็นการเข้าถึง OAuth 2.0)  
3. สมุดงาน (`{fileName}`) จะต้องถูกอัปโหลดไว้ในพื้นที่จัดเก็บบนคลาวด์ของ Aspose ก่อนแล้ว  

---

## การซ่อนแผ่นงาน

### คำขอ
```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": false
}
```

### การตอบกลับ
```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": false
  }
}
```

### ตัวอย่าง cURL
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": false }'
```

### ตัวอย่าง .NET SDK
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = false };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"ซ่อนแผ่นงานแล้ว: {response.Worksheet.Visible}");
```

### ข้อผิดพลาดที่พบบ่อย
| โค้ด HTTP | คำอธิบาย                                      | วิธีแก้ไข                                                |
|-----------|-----------------------------------------------|----------------------------------------------------------|
| 400       | เนื้อหา JSON ไม่ถูกต้องหรือขาดคีย์ `Visible` | ตรวจสอบให้แน่ใจว่าเนื้อหาคำขอเป็น JSON ที่ถูกต้องและมีคีย์นี้ |
| 401       | ไม่ได้รับอนุญาต – โทเค็นหายหรือหมดอายุ      | รีเฟรชโทเค็น OAuth และใส่ลงในส่วนหัวคำขอ               |
| 404       | ไม่พบแผ่นงานหรือไฟล์                         | ตรวจสอบว่า `{fileName}` และ `{sheetName}` ถูกต้อง        |
| 409       | แผ่นงานถูกซ่อนอยู่แล้ว                        | ตรวจสอบสถานะการมองเห็นปัจจุบันก่อนส่งคำขอ              |

---

## การยกเลิกการซ่อนแผ่นงาน

### คำขอ
```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": true
}
```

### การตอบกลับ
```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": true
  }
}
```

### ตัวอย่าง cURL
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": true }'
```

### ตัวอย่าง .NET SDK
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = true };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"แสดงแผ่นงานแล้ว: {response.Worksheet.Visible}");
```

### ข้อผิดพลาดที่พบบ่อย
| โค้ด HTTP | คำอธิบาย                                      | วิธีแก้ไข                                                |
|-----------|-----------------------------------------------|----------------------------------------------------------|
| 400       | เนื้อหา JSON ไม่ถูกต้องหรือขาดคีย์ `Visible` | ระบุ payload JSON ที่ถูกต้องพร้อม `"Visible": true`     |
| 401       | ไม่ได้รับอนุญาต – โทเค็นหายหรือหมดอายุ      | สร้างโทเค็นการเข้าถึงใหม่และลองอีกครั้ง                 |
| 404       | ไม่พบแผ่นงานหรือไฟล์                         | ยืนยันว่าชื่อไฟล์และแผ่นงานมีอยู่ในพื้นที่จัดเก็บ       |
| 409       | แผ่นงานถูกแสดงอยู่แล้ว                        | ไม่จำเป็นต้องดำเนินการใดๆ เพราะแผ่นงานถูกแสดงอยู่แล้ว |

---

## การดำเนินการที่เกี่ยวข้อง
> *冻结 Pane* | *Split Panes* | *Zoom* – ดูหน้าที่เกี่ยวข้องสำหรับการควบคุมการจัดวางแผ่นงานเพิ่มเติม

---

## คำถามที่พบบ่อย

<dl>
  <dt>ฉันจะซ่อนแผ่นงานโดยใช้ Aspose.Cells Cloud API ได้อย่างไร?</dt>
  <dd>ส่งคำขอ `PUT` ไปยัง `/cells/{fileName}/worksheets/{sheetName}/visibility` โดยมี JSON body เป็น `{ "Visible": false }` และแนบโทเค็น bearer OAuth 2.0 ที่ถูกต้อง ระบบจะตอบกลับด้วยโค้ด `200 OK` และส่งคืนวัตถุแผ่นงานที่อัปเดตแล้ว</dd>

  <dt>หลังจากยกเลิกการซ่อนแผ่นงาน ฉันจะได้รับการตอบกลับแบบใด?</dt>
  <dd>API จะตอบกลับด้วย `200 OK` พร้อม payload ที่มีวัตถุแผ่นงานซึ่ง `"Visible": true` โดยการตอบกลับจะระบุคุณสมบัติ `Name`, `Index` และ `Visible` ของแผ่นงานด้วย</dd>

  <dt>ฉันสามารถซ่อนหลายแผ่นงานในคำขอเดียวได้หรือไม่?</dt>
  <dd>ไม่สามารถทำได้ เพราะจุดปลายทางของการมองเห็นทำงานกับแผ่นงานเดียวที่ระบุโดย `{sheetName}` เท่านั้น หากต้องการซ่อนหลายแผ่นงาน ให้วนลูปผ่านแต่ละชื่อในโค้ดไคลเอ็นต์ของคุณ</dd>
</dl>

---

*เขียนโดยทีมงาน Aspose Docs – มีประสบการณ์มากกว่า 15 ปีในการอัตโนมัติเวิร์กโฟลว์ Excel*