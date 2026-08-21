---
title: "GetMergedCellsInWorksheet"
ArticleTitle: "การรับเซลล์ที่ถูกผสานในชีตงาน – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktype: "GetMergedCellsInWorksheet"
type: docs
url: /th/cells/spreadsheet/mergedcells
aliases: []
keywords: "Aspose Cells, เซลล์ที่ถูกผสาน, ชีตงาน, API"
description: "รับพื้นที่เซลล์ที่ถูกผสานทั้งหมดจากชีตงานของไฟล์สเปรดชีตในเครื่อง"
weight: 1000
---

## การรับเซลล์ที่ถูกผสานในชีตงานของ Aspose.Cells Cloud Web Services

รับพื้นที่เซลล์ที่ถูกผสานทั้งหมดจากชีตงานของไฟล์สเปรดชีตในเครื่อง

### ปลายทาง API สำหรับเว็บ

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท | Path/Query String/HTTP Body | คำอธิบาย |
|----------------|------|-----------------------------|-------------|
| Spreadsheet | ไฟล์ | FormData | อัปโหลดไฟล์สเปรดชีต |
| worksheet | สตริง | Query | ชื่อชีตงาน |
| region | สตริง | Query | การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) ซึ่งส่งผลต่อการจัดรูปแบบตัวเลข การแปลงวันที่ และพฤติกรรมที่ขึ้นกับภาษาท้องถิ่น |
| password | สตริง | Query | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต |

### พารามิเตอร์เนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย |
| -------------- | ---- | ----------- |
| N/A | N/A | การดำเนินการนี้ไม่รับ JSON body; ไฟล์สเปรดชีตจะถูกส่งผ่าน `multipart/form-data` |

### **การตอบกลับ**

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

**รหัสสถานะการตอบกลับ**

| รหัส | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | สำเร็จ (OK) | รับพื้นที่เซลล์ที่ถูกผสานเรียบร้อยแล้ว |
| 400 | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์คำขอมีค่าไม่ถูกต้องหรือขาดหายไป |
| 401 | ไม่ได้รับอนุญาต (Unauthorized) | การยืนยันตัวตนล้มเหลว — โทเคน JWT ไม่ถูกต้องหรือขาดหายไป |
| 413 | ข้อมูลส่งมอบมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์สเปรดชีตที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

## วิธีใช้งานการรับเซลล์ที่ถูกผสานในชีตงานด้วย SDK

### ข้อกำหนดการรับเซลล์ที่ถูกผสานในชีตงาน

[ข้อกำหนด API การรับเซลล์ที่ถูกผสานในชีตงาน](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInWorksheet) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการโต้ตอบ REST ผ่านเว็บเบราว์เซอร์ได้โดยตรง

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ผ่าน cURL

{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}

{< tab tabNum="1" >}

```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells?worksheet=Sheet1&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

{< /tab >}

{< /tabs >}

### ใช้งาน Aspose Cells Cloud SDKs

การใช้งาน SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK ทำหน้าที่ซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บ GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose Cells Cloud ผ่าน SDK ต่างๆ:
 `[TBD]`
---