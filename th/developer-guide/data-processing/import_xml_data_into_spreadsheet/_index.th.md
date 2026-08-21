---
---
title: "นำเข้าข้อมูล XML ลงในสเปรดชีต"
ArticleTitle: "นำเข้าข้อมูล XML ลงในสเปรดชีต – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktype: "นำเข้าข้อมูล XML ลงในสเปรดชีต"
type: docs
url: /cells/import/data/xml
aliases: []
keywords: "นำเข้า XML, Aspose.Cells, API"
description: "นำเข้าไฟล์ข้อมูล XML ลงในสเปรดชีตในเครื่องโดยใช้ Aspose.Cells Cloud"
weight: 1000
---

## การนำเข้าข้อมูล XML ลงในสเปรดชีตของเว็บเซอร์วิส Aspose.Cells Cloud

นำเข้าไฟล์ข้อมูล XML ลงในสเปรดชีตในเครื่อง วิธีนี้จะแยกวิเคราะห์ XML แล้วแมปข้อมูลไปยังโครงสร้างเซลล์ของสเปรดชีต และบันทึกไฟล์ลงในเครื่อง รูปแบบสเปรดชีตที่รองรับ ได้แก่ .xlsx และ .ods

### จุดสิ้นสุดของเว็บ API

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/xml
```

### **ความปลอดภัยและการรับรองความถูกต้อง**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การรับรองความถูกต้องด้วยโทเค็น JWT</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | Path/Query String/HTTP Body | คำอธิบาย |
|------------------|---------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| datafile         | ไฟล์    | FormData                    | อัปโหลดไฟล์ข้อมูล |
| Spreadsheet      | ไฟล์    | FormData                    | อัปโหลดไฟล์สเปรดชีต |
| worksheet        | สตริง  | Query                       | ชีตที่ต้องการนำข้อมูล XML เข้าไป |
| startcell        | สตริง  | Query                       | ตำแหน่งเริ่มต้นสำหรับการนำเข้าข้อมูล |
| insert           | ค่าบูลีน | Query                       | ควบคุมพฤติกรรมการแทรกข้อมูล: true = แทรกข้อมูล; false = แทนที่ข้อมูลที่มีอยู่ ค่าเริ่มต้น: **true** |
| outPath          | สตริง  | Query                       | (ไม่บังคับ) เส้นทางโฟลเดอร์ที่เก็บสมุดงาน ค่าเริ่มต้นคือ null |
| outStorageName   | สตริง  | Query                       | ชื่อที่จัดเก็บไฟล์ผลลัพธ์ |
| fontsLocation    | สตริง  | Query                       | ใช้ฟอนต์แบบกำหนดเอง |
| region           | สตริง  | Query                       | การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) มีผลต่อการจัดรูปแบบตัวเลข การแยกวิเคราะห์วันที่ และพฤติกรรมเฉพาะพื้นที่ |
| password         | สตริง  | Query                       | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต |

### พารามิเตอร์ของเนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย |
|----------------|------|-------------|
| *ไม่มี*         | -    | -           |

### **การตอบกลับ**

```json
{
  "file": "<สตรีมไบนารีของสเปรดชีตที่อัปเดตแล้ว>"
}
```

**โค้ดสถานะการตอบกลับ**

| โค้ด | ความหมาย                 | คำอธิบาย |
|------|-------------------------|-------------------------------------------------------------------------------------------------------|
| 200  | สำเร็จ (OK)                      | นำเข้าข้อมูล XML สำเร็จ และส่งคืนไฟล์สเปรดชีตที่อัปเดตแล้ว |
| 400  | คำขอไม่ถูกต้อง (Bad Request)             | URL ของคำขอไม่ถูกต้องหรือไม่มีพารามิเตอร์ที่จำเป็น |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)            | การรับรองความถูกต้องล้มเหลวหรือไม่มีการส่งข้อมูลยืนยันตัวตนมา |
| 404  | ไม่พบ (Not Found)               | ไม่สามารถเข้าถึงไฟล์ต้นทางได้ |
| 413  | ข้อมูลในคำขอมีขนาดใหญ่เกินไป (Payload Too Large)       | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error)   | เกิดข้อผิดพลาดขณะสมุดงานดึงข้อมูล |

## วิธีใช้การนำเข้าข้อมูล XML ลงในสเปรดชีตพร้อม SDK

### ข้อกำหนดการนำเข้าข้อมูล XML ลงในสเปรดชีต

[ข้อกำหนด API สำหรับการนำเข้าข้อมูล XML ลงในสเปรดชีต](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{DataProcessingController}/ImportXMLDataIntoSpreadsheet) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells Cloud ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}

{< tab tabNum="1" >}

```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/xml?worksheet={worksheet}&startcell={startcell}&insert={insert}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@{DataFileName}" \
  -F "Spreadsheet=@{SpreadsheetFileName}"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<สตรีมไบนารีของสเปรดชีตที่อัปเดตแล้ว>"
}
```

{< /tab >}

{< /tabs >}

### ใช้ SDK ของ Aspose Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK จะซ่อนรายละเอียดระดับต่ำไว้ ให้คุณสามารถมุ่งเน้นไปที่งานโครงการของคุณได้ โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer"> kho่วเก็บ GitHub</a> เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ที่สมบูรณ์

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้เว็บเซอร์วิสของ Aspose Cells Cloud ด้วย SDK ต่างๆ:
`[TBD]`
---