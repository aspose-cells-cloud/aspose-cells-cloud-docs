---
---
title: "GetSpreadsheetStructure"
ArticleTitle: "GetSpreadsheetStructure – Aspose.Cells Cloud"
second_title: "เอกสาร"
linktype: "docs"
url: /cells/spreadsheet/structure
aliases: []
keywords: "Aspose.Cells, โครงสร้างสเปรดชีต, API"
description: "แปลงโครงสร้างข้อมูลหลักของสมุดงาน Excel ได้แก่ เมตาดาต้า แผ่นงาน ตาราง ตารางพิวอัต พิวพิวแท็บล์ แผนภูมิ รูปร่าง และข้อมูลอื่นๆ ให้อยู่ในรูปแบบ JSON แบบ JObject"
weight: 1000
---

## GetSpreadsheetStructure ของเว็บเซอร์วิส Aspose.Cells Cloud

แปลงโครงสร้างข้อมูลหลักของสมุดงาน Excel ได้แก่ เมตาดาต้า แผ่นงาน ตาราง ตารางพิวอัต พิวพิวแท็บล์ แผนภูมิ รูปร่าง และข้อมูลอื่นๆ ให้อยู่ในรูปแบบ JSON แบบ JObject สำหรับกรณีการใช้งานต่างๆ เช่น การส่งออกข้อมูล การตอบกลับจาก API และการบันทึกบันทึกย่อ

### ปลายทาง API สำหรับเว็บ

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/structure
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท | Path/Query String/HTTP Body | คำอธิบาย |
|----------------|--------|-----------------------------|-------------|
| Spreadsheet    | ไฟล์   | FormData (body)             | อัปโหลดไฟล์สเปรดชีต |
| region         | ข้อความ | Query                       | ตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) มีผลต่อการจัดรูปแบบตัวเลข การแปลงวันที่ และพฤติกรรมเฉพาะของโลคอล |
| password       | ข้อความ | Query                       | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต |

### พารามิเตอร์เนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย |
| -------------- | ---- | ----------- |
| Spreadsheet    | ไฟล์ | อัปโหลดไฟล์สเปรดชีต |

### **การตอบกลับ**

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "DocumentProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z"
  }
}
```

**รหัสสถานะของการตอบกลับ**

| รหัส | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | สำเร็จ | ดึงโครงสร้างสเปรดชีตเรียบร้อยแล้ว |
| 400 | คำขอไม่ถูกต้อง | พารามิเตอร์คำขอหรือรูปแบบไฟล์ไม่ถูกต้อง |
| 401 | ไม่ได้รับอนุญาต | การยืนยันตัวตนล้มเหลวหรือไม่มี JWT token |
| 413 | เนื้อหาส่งไปขนาดใหญ่เกินไป | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด |
| 500 | เกิดข้อผิดพลาดภายในเซิร์ฟเวอร์ | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

## วิธีใช้ GetSpreadsheetStructure ด้วย SDK

### ข้อมูลกำกับ GetSpreadsheetStructure

[ข้อมูลกำกับ API GetSpreadsheetStructure](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetSpreadsheetStructure) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้公开 และช่วยให้คุณสามารถดำเนินการ REST interaction ผ่านเว็บเบราว์เซอร์ได้โดยตรง

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงเว็บเซอร์วิส Aspose Cells Cloud ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API ผ่าน cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/structure?region=en-US&password=yourPassword" \
  -X PUT \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "DocumentProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK ช่วยซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่งานโครงการของคุณได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บบน GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกเว็บเซอร์วิส Aspose Cells Cloud ผ่าน SDK ต่างๆ:
`[TBD]`
---