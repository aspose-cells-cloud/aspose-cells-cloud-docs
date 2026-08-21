---
title: "การแปลงแผ่นงานเป็นตาราง HTML"
ArticleTitle: "การแปลงแผ่นงานเป็นตาราง HTML – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktype: "ConvertWorksheetToHtmlTable"
type: docs
url: /th/cells/convert/worksheet/html-table
aliases: []
keywords: "Aspose.Cells, ConvertWorksheetToHtmlTable, ตาราง HTML, API"
description: "แปลงแผ่นงานของไฟล์สเปรดชีตในไดรฟ์ภายในเครื่องเป็นไฟล์ตาราง HTML โดยใช้ Aspose.Cells Cloud"
weight: 100
---

## การแปลงแผ่นงานเป็นตาราง HTML ของบริการเว็บ Aspose.Cells Cloud

การดำเนินการนี้อ่านไฟล์สเปรดชีตจากระบบไฟล์ในเครื่อง แปลงแผ่นงานที่ระบุเป็นตาราง HTML และส่งคืนผลลัพธ์ที่แปลงแล้วเป็นสตรีมไบนารี การแปลงดำเนินการทั้งหมดบนเซิร์ฟเวอร์คลาวด์ ดังนั้นจึงไม่จำเป็นต้องอัปโหลดไฟล์ไปยังพื้นที่จัดเก็บข้อมูลบนคลาวด์ล่วงหน้า รองรับการตั้งค่าLocale (การตั้งค่าภูมิภาค/ภาษา) และสมุดงานที่มีรหัสผ่าน

### ปลายทาง API ของเว็บ

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์แบบใช้โทเคน JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | Path/Query String/HTTP Body | คำอธิบาย |
|----------------|--------|-----------------------------|-------------|
| Spreadsheet    | ไฟล์   | FormData                    | อัปโหลดไฟล์สเปรดชีต |
| worksheet      | สตริง | Query                       | ชื่อแผ่นงานของสเปรดชีต (จำเป็นต้องระบุ) |
| region         | สตริง | Query                       | การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) ส่งผลต่อการจัดรูปแบบตัวเลข การแยกวิเคราะห์วันที่ และพฤติกรรมที่เกี่ยวข้องกับLocale |
| password       | สตริง | Query                       | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต |

### พารามิเตอร์เนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย |
| -------------- | ---- | ----------- |
| *ไม่มี* | *ไม่มี* | *ไม่จำเป็นต้องส่ง JSON body; ไฟล์จะถูกส่งผ่าน multipart/form-data* |

### **การตอบกลับ**

```json
{
  "File": "สตรีมไบนารีของตาราง HTML ที่สร้างขึ้น"
}
```

**โค้ดสถานะการตอบกลับ**

| โค้ด | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | สำเร็จ | แผ่นงานถูกแปลงเป็นตาราง HTML แล้วและส่งคืนเป็นสตรีมไฟล์ |
| 400 | คำขอไม่ถูกต้อง | URL คำขอไม่ถูกต้องหรือพารามิเตอร์ที่จำเป็นขาดหายไป |
| 401 | ไม่ได้รับอนุญาต | การตรวจสอบสิทธิ์ล้มเหลวหรือไม่ได้ระบุข้อมูลยืนยันตัวตน |
| 404 | ไม่พบ | ไม่สามารถเข้าถึงไฟล์ต้นทางได้ |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ | ไฟล์สเปรดชีตเกิดข้อผิดพลาดขณะดึงข้อมูลสำหรับการแปลง |
| 413 | ข้อมูลส่งไปมีขนาดใหญ่เกินไป | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่อนุญาต |

## วิธีใช้การแปลงแผ่นงานเป็นตาราง HTML ด้วย SDK

### ข้อกำหนดการแปลงแผ่นงานเป็นตาราง HTML

[ข้อกำหนด API การแปลงแผ่นงานเป็นตาราง HTML](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToHtmlTable) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}

{< tab tabNum="1" >}

```bash
# ใช้ HTTPS เพื่อเชื่อมต่อแบบปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table?worksheet={worksheet}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "สตรีมไบนารีของตาราง HTML ที่สร้างขึ้น"
}
```

{< /tab >}

{< /tabs >}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK ช่วยซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บ GitHub</a> เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud อย่างครบถ้วน

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells Cloud ด้วย SDK ต่างๆ:
`[TBD]`
---