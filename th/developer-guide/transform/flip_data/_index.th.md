---
title: "FlipData"
ArticleTitle: "FlipData – Aspose.Cells Cloud"
second_title: "เอกสาร"
linktype: "FlipData"
type: docs
url: /cells/flip
aliases: []
keywords: "FlipData, การเปลี่ยนรูปแบบข้อมูล, Aspose.Cells"
description: "หมุนหรือพลิกทิศทางช่วงข้อมูลที่ระบุในไฟล์สมุดงาน"
weight: 100
---

## FlipData ของ Aspose.Cells Cloud Web Services

API นี้จะพลิกทิศทางของเมทริกซ์ข้อมูลที่ระบุ ตัวอย่างเช่น ช่วงข้อมูลขนาด 3x2 (3 แถว 2 คอลัมน์) จะกลายเป็นช่วงขนาด 2x3 (2 แถว 3 คอลัมน์) ในผลลัพธ์ที่ได้ ฟังก์ชันนี้มักใช้เพื่อจัดโครงสร้างข้อมูลใหม่ให้สอดคล้องกับข้อกำหนดในการป้อนข้อมูลของแผนภูมิ รายงาน หรือโมเดลข้อมูลต่างๆ

### จุดสิ้นสุดของ Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/flip
```

### **ความปลอดภัยและการพิสูจน์ตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การพิสูจน์ตัวตนด้วย JWT token</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ประเภท | Path/Query String/HTTP Body | คำอธิบาย |
|----------------|---------|-----------------------------|-------------|
| Spreadsheet    | ไฟล์    | FormData                    | อัปโหลดไฟล์สมุดงาน |
| worksheet      | สตริง  | Query                       | ชื่อworksheet |
| cellArea       | สตริง  | Query                       | ช่วงข้อมูลที่ระบุ |
| Horizontal     | ค่าบูลีน | Query                       | การพลิกแนวนอน/แนวตั้ง | ค่าเริ่มต้น: true |
| outPath        | สตริง  | Query                       | (ไม่บังคับ) ที่อยู่โฟลเดอร์ที่เก็บสมุดงาน ค่าเริ่มต้นคือ null |
| outStorageName | สตริง  | Query                       | ชื่อ Storage สำหรับผลลัพธ์ |
| region         | สตริง  | Query                       | การตั้งค่าภูมิภาค/ภาษาของสมุดงาน (เช่น `en-US`, `fr-FR`) | ส่งผลต่อรูปแบบตัวเลข การแยกวิเคราะห์วันที่ และพฤติกรรมเฉพาะของภูมิภาค |
| password       | สตริง  | Query                       | รหัสผ่านสำหรับเปิดไฟล์สมุดงาน |

### พารามิเตอร์ของเนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย |
| -------------- | ---- | ----------- |
| *ไม่มี* | *N/A* | *ไม่จำเป็นต้องส่ง JSON body เพิ่มเติม; ไฟล์จะถูกส่งในรูปแบบ multipart/form-data* |

### **ผลลัพธ์ที่ได้**

```json
{
  "File": "<สตรีมไบนารีของสมุดงานที่ผ่านการแปลงรูปแล้ว>"
}
```

**รหัสสถานะของผลลัพธ์**

| รหัส | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | สำเร็จ | การดำเนินการเสร็จสมบูรณ์ และส่งกลับไฟล์สมุดงานที่ผ่านการแปลงรูปแล้ว |
| 400 | คำขอร้องผิดรูปแบบ | พารามิเตอร์ที่จำเป็นหนึ่งหรือหลายตัวหายไปหรือไม่ถูกต้อง |
| 401 | ไม่ได้รับอนุญาต | การพิสูจน์ตัวตนล้มเหลว – ไม่มีหรือ JWT token ไม่ถูกต้อง |
| 413 | ขนาดข้อมูลในคำขอมีขนาดใหญ่เกินไป | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

## วิธีใช้ FlipData ด้วย SDKs

### ข้อมูลเฉพาะของ FlipData

[ข้อมูลเฉพาะของ FlipData API](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TransformController/FlipData) นิยามอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่าน command-line เพื่อเข้าถึง Aspose.Cells Cloud web services ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="ผลลัพธ์" >}}

{{< tab tabNum="1" >}}

```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/flip?worksheet=Sheet1&cellArea=A1:B3&Horizontal=true&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "<สตรีมไบนารีของสมุดงานที่ผ่านการแปลงรูปแล้ว>"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ Aspose Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK ช่วยซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่ภารกิจของโครงการได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ที่สมบูรณ์

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้ Aspose Cells Cloud web services โดยใช้ SDK ต่างๆ:
 `[TBD]`
---