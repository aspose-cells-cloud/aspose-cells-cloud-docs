---
title: "นำเข้าข้อมูล CSV ลงในสเปรดชีต"
ArticleTitle: "นำเข้าข้อมูล CSV ลงในสเปรดชีต – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktype: "docs"
url: /cells/import/data/csv
aliases: []
keywords: "Aspose.Cells, นำเข้า CSV, สเปรดชีต, API"
description: "นำเข้าไฟล์ข้อมูล CSV ลงในสเปรดชีตในเครื่องโดยใช้ Aspose.Cells Cloud API"
weight: 100
---

## การนำเข้าข้อมูล CSV ลงในสเปรดชีตของ Aspose.Cells Cloud Web Services

นำเข้าไฟล์ข้อมูล CSV ลงในสเปรดชีตในเครื่อง วิธีนี้จะวิเคราะห์ไฟล์ CSV แล้วแมปข้อมูลเข้ากับโครงสร้างเซลล์ของสเปรดชีต และบันทึกไฟล์ไว้ในเครื่อง รูปแบบสเปรดชีตที่รองรับ ได้แก่ .xlsx และ .ods

### จุดปลายทางของ Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/csv
```

### **ความปลอดภัยและการพิสูจน์ตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การพิสูจน์ตัวตนด้วย JWT token</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์       | ประเภท | Path/Query String/HTTP Body | คำอธิบาย                                                                                                                          |
|-----------------------|--------|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| datafile              | ไฟล์   | FormData                    | อัปโหลดไฟล์ข้อมูล                                                                                                                    |
| Spreadsheet           | ไฟล์   | FormData                    | อัปโหลดไฟล์สเปรดชีต                                                                                                                 |
| worksheet             | สตริง  | Query                       | ชีตที่ต้องการนำเข้าข้อมูล CSV (จำเป็น)                                                                              |
| startcell             | สตริง  | Query                       | ตำแหน่งเริ่มต้นสำหรับการนำเข้าข้อมูล (จำเป็น)                                                                                       |
| insert                | บูลีน | Query                       | ควบคุมพฤติกรรมการแทรกข้อมูล: true = แทรกข้อมูล; false = แทนที่ข้อมูลที่มีอยู่ ค่าเริ่มต้น: true (ไม่บังคับ)                     |
| convertNumericData    | บูลีน | Query                       | กำหนดว่าสตริงในไฟล์ข้อความจะถูกแปลงเป็นข้อมูลตัวเลขหรือไม่ ค่าเริ่มต้น: true (ไม่บังคับ)                                            |
| splitter              | สตริง  | Query                       | ตัวคั่นที่ใช้แยกฟิลด์ CSV ค่าเริ่มต้น: "," (ไม่บังคับ)                                                                         |
| outPath               | สตริง  | Query                       | (ไม่บังคับ) เส้นทางโฟลเดอร์ที่เก็บสมุดงาน ค่าเริ่มต้น: null (ไม่บังคับ)                                            |
| outStorageName        | สตริง  | Query                       | ชื่อพื้นที่จัดเก็บสำหรับไฟล์ผลลัพธ์ (ไม่บังคับ)                                                                                                |
| fontsLocation         | สตริง  | Query                       | ใช้ฟอนต์ที่กำหนดเอง (ไม่บังคับ)                                                                                                         |
| region                | สตริง  | Query                       | การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) ส่งผลต่อรูปแบบตัวเลข การแยกวิเคราะห์วันที่ และพฤติกรรมที่ขึ้นกับภาษาท้องถิ่น (ไม่บังคับ) |
| password              | สตริง  | Query                       | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต (ไม่บังคับ)                                                                              |

### พารามิเตอร์เนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **การตอบกลับ**

```json
{
  "file": "<สตรีมไบนารีของสเปรดชีตที่ได้>"
}
```

**รหัสสถานะของการตอบกลับ**

| รหัส | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | สำเร็จ | นำเข้าข้อมูล CSV สำเร็จ และส่งคืนไฟล์สเปรดชีตที่ได้ |
| 400 | คำขอไม่ถูกต้อง | พารามิเตอร์คำขอไม่ถูกต้องหรือ URL ผิดรูปแบบ |
| 401 | ไม่ได้รับอนุญาต | การพิสูจน์ตัวตนล้มเหลวหรือไม่ได้ให้ข้อมูลประจำตัว |
| 404 | ไม่พบ | ไม่สามารถเข้าถึงไฟล์ต้นฉบับได้ |
| 413 | ข้อมูลในคำขอมีขนาดใหญ่เกินไป | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่อนุญาต |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ | สเปรดชีตเกิดข้อผิดพลาดในการดึงข้อมูล |

## วิธีใช้การนำเข้าข้อมูล CSV ลงในสเปรดชีตพร้อม SDK

### ข้อมูลจำเพาะของการนำเข้าข้อมูล CSV ลงในสเปรดชีต

[ข้อมูลจำเพาะของ API การนำเข้าข้อมูล CSV ลงในสเปรดชีต](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/ImportCSVDataIntoSpreadsheet) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถโต้ตอบกับ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึง Aspose.Cells web services ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}

{< tab tabNum="1" >}

```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/csv?worksheet=Sheet1&startcell=A1&insert=true&convertNumericData=true&splitter=,&outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/custom/fonts&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@sample.csv" \
  -F "Spreadsheet=@workbook.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<สตรีมไบนารีของสเปรดชีตที่ได้>"
}
```

{< /tab >}

{< /tabs >}

### ใช้ Aspose Cells Cloud SDK

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK จะซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโปรเจกต์ของคุณ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer"> khoเก็บ GitHub</a> เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้ Aspose Cells Cloud web services โดยใช้ SDK ต่างๆ:
 `[TBD]`
---