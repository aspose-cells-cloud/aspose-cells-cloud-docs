---
title: "รับแผ่นงานจากไฟล์สเปรดชีตในเครื่อง"
ArticleTitle: "รับแผ่นงานจากไฟล์สเปรดชีตในเครื่อง – Aspose.Cells Cloud"
second_title: "เอกสาร"
linktitle: "รับแผ่นงานจากไฟล์สเปรดชีตในเครื่อง"
type: docs
url: /th/cells/spreadsheet/worksheets
aliases: []
keywords: "Aspose.Cells, Worksheets, Local Spreadsheet, API"
description: "ดึงรายการแผ่นงานทั้งหมดจากไฟล์สเปรดชีตในเครื่องที่กำลังใช้งานอยู่"
weight: 1000
---

## การรับแผ่นงานจากไฟล์สเปรดชีตในเครื่องของเว็บเซอร์วิส Aspose.Cells Cloud

ปลายทาง (endpoint) นี้เชื่อมต่อกับแอปพลิเคชันสเปรดชีตในเครื่อง (เช่น Excel) ผ่าน interop หรือ API ภายในเครื่อง แล้วรวบรวมชื่อและประเภท (เช่น แบบมาตรฐาน, แผนภูมิ, แมโคร) ของแผ่นงานทุกแผ่น และส่งกลับในรูปแบบอาร์เรย์ JSON ที่มีโครงสร้าง ซึ่งมักใช้เพื่อเติมข้อมูลในส่วนเลือกแผ่นงานของ UI หรือเพื่อตรวจสอบเนื้อหาของสเปรดชีต

### ปลายทางเว็บ API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheets
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ประเภท | Path/Query String/HTTP Body | คำอธิบาย |
|----------------|--------|-----------------------------|-------------|
| Spreadsheet    | ไฟล์   | FormData (HTTP Body)        | อัปโหลดไฟล์สเปรดชีต |
| region         | สตริง | Query                       | การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) ซึ่งมีผลต่อการจัดรูปแบบตัวเลข การแยกวิเคราะห์วันที่ และพฤติกรรมเฉพาะของท้องถิ่น *(ไม่บังคับ)* |
| password       | สตริง | Query                       | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต *(ไม่บังคับ)* |

### พารามิเตอร์ของเนื้อหาคำขอ (Request Body)

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย |
|----------------|------|-------------|
| Spreadsheet    | ไฟล์ | อัปโหลดไฟล์สเปรดชีต |

### **การตอบกลับ (Response)**

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Id": 0,
      "Type": "Standard"
    },
    {
      "Name": "Chart1",
      "Id": 1,
      "Type": "Chart"
    }
    // ... แผ่นงานเพิ่มเติม
  ]
}
```

**โค้ดสถานะของการตอบกลับ**

| โค้ด | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | สำเร็จ (OK) | ดึงรายการแผ่นงานเรียบร้อยแล้ว |
| 400 | คำขอไม่ถูกต้อง (Bad Request) | คำขอไม่ถูกต้อง (เช่น URL ผิดรูปแบบ หรือขาดข้อมูลที่จำเป็น) |
| 401 | ไม่ได้รับอนุญาต (Unauthorized) | การยืนยันตัวตนล้มเหลว หรือไม่ได้ระบุข้อมูลประจำตัว |
| 404 | ไม่พบ (Not Found) | ไม่สามารถเข้าถึงไฟล์ต้นทางได้ |
| 413 | ข้อมูลในคำขอใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่อนุญาต |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | สเปรดชีตมีข้อผิดพลาดในการดึงข้อมูล |

## วิธีใช้การรับแผ่นงานจากไฟล์สเปรดชีตในเครื่องด้วย SDK

### ข้อมูลจำเพาะของการรับแผ่นงานจากไฟล์สเปรดชีตในเครื่อง

[ข้อมูลจำเพาะ API การรับแผ่นงานจากไฟล์สเปรดชีตในเครื่อง](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetWorksheetsWithLocalSpreadsheet) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้จากภายนอก และช่วยให้คุณสามารถโต้ตอบกับ REST API ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells Cloud ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheets?region=en-US&password=yourPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
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
      "Id": 0,
      "Type": "Standard"
    },
    {
      "Name": "Chart1",
      "Id": 1,
      "Type": "Chart"
    }
    // ... แผ่นงานเพิ่มเติม
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK ทำหน้าที่ซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานของโครงการได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้เว็บเซอร์วิสของ Aspose.Cells Cloud โดยใช้ SDK ต่างๆ:
`[TBD]`
---