---
title: "GetStructureInRemoteSpreadsheet"
ArticleTitle: "Get Structure In Remote Spreadsheet – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktitle: "GetStructureInRemoteSpreadsheet"
type: docs
url: /cells/{name}/structure
aliases: []
keywords: "Aspose.Cells, GetStructure, สเปรดชีต, โครงสร้าง"
description: "ดึงข้อมูลเมตาของสมุดงาน Excel ระยะไกล ซึ่งรวมถึงเวิร์กชีต ตาราง ตารางพิวอัต พิวอัตชีต แผนภูมิ รูปร่าง และข้อมูลหลักอื่นๆ"
weight: 100
---

## การดึงโครงสร้างในสเปรดชีตระยะไกลของ Aspose.Cells Cloud Web Services

แปลงโครงสร้างข้อมูลเมตา ซึ่งประกอบด้วยเวิร์กชีต ตาราง ตารางพิวอัต พิวอัตชีต แผนภูมิ รูปร่าง และข้อมูลอื่นๆ ของสมุดงาน Excel ให้อยู่ในรูปแบบ JSON ที่เป็น JObject สำหรับสถานการณ์ต่างๆ เช่น การส่งออกข้อมูล การตอบกลับจาก API และการบันทึกข้อมูลในบันทึกระบบ

### จุดสิ้นสุดของเว็บ API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/structure
```

### **ความปลอดภัยและการรับรองความถูกต้อง**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การรับรองความถูกต้องด้วยโทเคน JWT</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ประเภท | เส้นทาง/สตริงคิวรี/เนื้อหา HTTP Body | คำอธิบาย |
|----------------|------|-----------------------------|-------------|
| name | string | Path | ชื่อไฟล์สเปรดชีต |
| folder | string | Query | โฟลเดอร์ที่ไฟล์ตั้งอยู่ (ไม่บังคับ) |
| storageName | string | Query | (ไม่บังคับ) ชื่อของพื้นที่จัดเก็บข้อมูลหากใช้พื้นที่จัดเก็บข้อมูลบนคลาวด์แบบกำหนดเอง หากไม่ระบุ จะใช้พื้นที่จัดเก็บข้อมูลเริ่มต้น |
| region | string | Query | การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) ส่งผลต่อการจัดรูปแบบตัวเลข การแปลงวันที่ และพฤติกรรมเฉพาะของภูมิภาค |
| password | string | Query | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต |

### พารามิเตอร์ของเนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

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
  "WorkbookProperties": {
    "Author": "string",
    "Created": "string",
    "Version": "string"
  },
  "DocumentProperties": {
    "Title": "string",
    "Subject": "string",
    "Keywords": "string"
  }
}
```

**โค้ดสถานะการตอบกลับ**

| โค้ด | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | สำเร็จ (OK) | ดึงโครงสร้างสมุดงานสำเร็จ |
| 400 | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์คำขอไม่ถูกต้อง |
| 401 | ไม่ได้รับอนุญาต (Unauthorized) | การรับรองความถูกต้องล้มเหลวหรือไม่มีโทเคน |
| 413 | เนื้อหาคำขอมีขนาดใหญ่เกินไป (Payload Too Large) | ขนาดเนื้อหาคำขอเกินขีดจำกัดที่อนุญาต |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดภายในเซิร์ฟเวอร์ |

## วิธีใช้การดึงโครงสร้างในสเปรดชีตระยะไกลพร้อม SDK

### ข้อกำหนดการดึงโครงสร้างในสเปรดชีตระยะไกล

[ข้อกำหนด API การดึงโครงสร้างในสเปรดชีตระยะไกล](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetStructureInRemoteSpreadsheet) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้จากภายนอก และช่วยให้คุณดำเนินการโต้ตอบแบบ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ที่อยู่ในบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ผ่าน cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/structure?folder=myFolder&storageName=MyStorage&region=en-US&password=SecretPwd" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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
  "WorkbookProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z",
    "Version": "16.0"
  },
  "DocumentProperties": {
    "Title": "SalesReport",
    "Subject": "Quarterly Sales",
    "Keywords": "sales,report,2023"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK จะซ่อนรายละเอียดระดับต่ำไว้ ช่วยให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose Cells Cloud ด้วย SDK ต่างๆ:
`[TBD]`
---