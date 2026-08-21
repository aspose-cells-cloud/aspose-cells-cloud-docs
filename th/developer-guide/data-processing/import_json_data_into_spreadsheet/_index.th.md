---
title: "นำเข้าข้อมูล JSON ลงในสเปรดชีต"
ArticleTitle: "นำเข้าข้อมูล JSON ลงในสเปรดชีต – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktype: "นำเข้าข้อมูล JSON ลงในสเปรดชีต"
type: docs
url: /cells/import/data/json
aliases: []
keywords: "นำเข้า JSON, Aspose.Cells, สเปรดชีต, API"
description: "นำเข้าไฟล์ข้อมูล JSON ลงในสเปรดชีตในเครื่อง"
weight: 1
---

## การนำเข้าข้อมูล JSON ลงในสเปรดชีตของ Aspose.Cells Cloud Web Services

นำเข้าไฟล์ข้อมูล JSON ลงในสเปรดชีตในเครื่อง วิธีการนี้จะแยกวิเคราะห์ JSON แล้วแมปข้อมูลเข้ากับโครงสร้างเซลล์ของสเปรดชีต และบันทึกไฟล์ลงในเครื่อง รูปแบบสเปรดชีตที่รองรับได้แก่ .xlsx และ .ods

### จุดสิ้นสุดของเว็บ API

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/json
```

### **ความปลอดภัยและการรับรองความถูกต้อง**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การรับรองความถูกต้องด้วย JWT token</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | เส้นทาง/สตริงของ Query/เนื้อหา HTTP | คำอธิบาย |
|----------------|--------|-----------------------------|-------------|
| datafile       | ไฟล์   | FormData                    | อัปโหลดไฟล์ข้อมูล |
| Spreadsheet    | ไฟล์   | FormData                    | อัปโหลดไฟล์สเปรดชีต |
| worksheet      | สตริง | Query                       | ต้องการนำเข้าข้อมูล JSON ลงในชีตงาน |
| startcell      | สตริง | Query                       | ตำแหน่งเริ่มต้นสำหรับการนำเข้าข้อมูล |
| insert         | บูลีน| Query                       | ควบคุมพฤติกรรมการแทรกข้อมูล: true = แทรกข้อมูล; false = เขียนทับข้อมูลที่มีอยู่ (ค่าเริ่มต้น: true) |
| outPath        | สตริง | Query                       | (ทางเลือก) เส้นทางโฟลเดอร์ที่จัดเก็บสมุดงาน ค่าเริ่มต้นคือ null |
| outStorageName | สตริง | Query                       | ชื่อพื้นที่จัดเก็บสำหรับไฟล์ผลลัพธ์ |
| fontsLocation  | สตริง | Query                       | ใช้ฟอนต์ที่กำหนดเอง |
| region         | สตริง | Query                       | การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) มีผลต่อการจัดรูปแบบตัวเลข การแยกวิเคราะห์วันที่ และพฤติกรรมเฉพาะตามภูมิภาค |
| password       | สตริง | Query                       | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต |

### พารามิเตอร์ของเนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **การตอบกลับ**

```json
{
  "file": "สตรีมไบนารี"
}
```

**รหัสสถานะการตอบกลับ**

| รหัส | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | สำเร็จ (OK) | ไฟล์ถูกสร้างและส่งกลับสำเร็จ |
| 400 | คำขอไม่ถูกต้อง (Bad Request) | URL ไม่ถูกต้อง |
| 401 | ไม่ได้รับอนุญาต (Unauthorized) | การรับรองความถูกต้องล้มเหลว หรือไม่ได้ระบุข้อมูลการรับรอง |
| 404 | ไม่พบ (Not Found) | ไม่สามารถเข้าถึงไฟล์ต้นทางได้ |
| 413 | ข้อมูลส่งไปขนาดใหญ่เกินไป (Payload Too Large) | [TBD] |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | สเปรดชีตพบข้อผิดพลาดระหว่างการดึงข้อมูล |

## วิธีใช้การนำเข้าข้อมูล JSON ลงในสเปรดชีตด้วย SDK

### ข้อกำหนดของการนำเข้าข้อมูล JSON ลงในสเปรดชีต

[ข้อกำหนด API การนำเข้าข้อมูล JSON ลงในสเปรดชีต](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/ImportJSONDataIntoSpreadsheet) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้จากภายนอก และช่วยให้คุณดำเนินการปฏิสัมพันธ์แบบ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ที่ใช้ในคำสั่งระบบที่ใช้ในบรรทัดคำสั่งเพื่อเข้าถึง Aspose Cells Cloud web services ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}
{< tab tabNum="1" >}
```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/json?worksheet=Sheet1&startcell=A1&insert=true&outPath=output%2F&outStorageName=MyStorage&fontsLocation=%2Ffonts&region=en-US&password=Secret" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@data.json" \
  -F "Spreadsheet=@workbook.xlsx"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "file": "สตรีมไบนารี"
}
```
{< /tab >}
{< /tabs >}

### ใช้ Aspose Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK จะซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บบน GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้ Aspose Cells Cloud web services ด้วย SDK ต่างๆ:
 `[TBD]`
---