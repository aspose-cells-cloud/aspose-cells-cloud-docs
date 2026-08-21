---
---
title: "ConvertWorksheetToPdf"
ArticleTitle: "การแปลงแผ่นงานเป็น PDF – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktype: "ConvertWorksheetToPdf"
type: docs
url: /cells/convert/worksheet/pdf
aliases: []
keywords: "Aspose.Cells, แปลงแผ่นงานเป็น PDF, API"
description: "แปลงแผ่นงานของไฟล์สเปรดชีตเป็น PDF โดยใช้ Aspose.Cells Cloud"
weight: 10
---

## ConvertWorksheetToPdf ของเว็บเซอร์วิส Aspose.Cells Cloud

เมธอดนี้อ่านไฟล์สเปรดชีตจากระบบไฟล์ท้องถิ่น แปลงแผ่นงานของไฟล์ดังกล่าวเป็นไฟล์ PDF และส่งคืนผลลัพธ์ที่แปลงแล้ว คุณต้องระบุพาธของไฟล์ต้นทางและรูปแบบเป้าหมายอย่างถูกต้อง ตรวจสอบให้แน่ใจว่ามีสิทธิ์ที่จำเป็นในการอ่านไฟล์ต้นทางและเขียนไฟล์ที่แปลงแล้ว (หากมี) กระบวนการแปลงจะเกิดขึ้นทั้งหมดบนเซิร์ฟเวอร์คลาวด์ จึงไม่จำเป็นต้องใช้พื้นที่จัดเก็บข้อมูลในคลาวด์หรือดาวน์โหลดจากภายนอก

คุณสมบัติหลัก ได้แก่ การแปลงแบบเนื้อแท้คลาวด์ การลดภาระทรัพยากรคลาวด์ และกระบวนการการทำงานที่เรียบง่าย

### จุดสิ้นสุดของเว็บ API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **ความปลอดภัยและการพิสูจน์ตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้การพิสูจน์ตัวตนแบบ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ประเภท | Path/Query String/HTTP Body | คำอธิบาย |
|------------------|---------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | ไฟล์    | FormData                    | อัปโหลดไฟล์สเปรดชีต |
| worksheet        | สตริง   | Query                       | ชื่อแผ่นงานของสเปรดชีต |
| outPath          | สตริง   | Query                       | (ไม่บังคับ) พาธของโฟลเดอร์ที่เก็บสมุดงาน ค่าเริ่มต้นคือ null |
| outStorageName   | สตริง   | Query                       | ชื่อพื้นที่จัดเก็บสำหรับไฟล์ผลลัพธ์ |
| fontsLocation    | สตริง   | Query                       | ใช้ฟอนต์ที่กำหนดเอง |
| AutoRowsFit      | บูลีน  | Query                       | (ไม่บังคับ) ปรับความสูงของแถวทั้งหมดในแผ่นงานอัตโนมัติ |
| AutoColumnsFit   | บูลีน  | Query                       | (ไม่บังคับ) ปรับความกว้างของคอลัมน์ทั้งหมดในแผ่นงานอัตโนมัติ |
| region           | สตริง   | Query                       | การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) มีผลต่อการจัดรูปแบบตัวเลข การแยกวิเคราะห์วันที่ และพฤติกรรมเฉพาะของแต่ละภูมิภาค |
| password         | สตริง   | Query                       | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต |

### พารามิเตอร์ของเนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย |
| -------------- | ---- | ----------- |
| [TBD]          |      |             |

### **การตอบกลับ**

```json
{
  "file": "<สตรีมไบนารีของไฟล์ PDF ที่สร้างขึ้น>"
}
```

**โค้ดสถานะของการตอบกลับ**

| โค้ด | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | สำเร็จ | แผ่นงานได้รับการแปลงเป็น PDF สำเร็จและส่งคืนเป็นสตรีมไฟล์ |
| 400 | คำขอไม่ถูกต้อง | พารามิเตอร์ของคำขอไม่ถูกต้องหรือ URL ผิดรูปแบบ |
| 401 | ไม่ได้รับอนุญาต | การพิสูจน์ตัวตนล้มเหลว หรือไม่มีการให้ข้อมูลรับรอง |
| 404 | ไม่พบ | ไฟล์ต้นทางไม่สามารถเข้าถึงได้ |
| 413 | ข้อมูลในคำขอขนาดใหญ่เกินไป | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่อนุญาต |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ | สเปรดชีตมีข้อผิดพลาดระหว่างกระบวนการแปลง |

## วิธีใช้ ConvertWorksheetToPdf ร่วมกับ SDK

### ข้อมูลเฉพาะของ ConvertWorksheetToPdf

[ConvertWorksheetToPdf API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#Conversion/ConvertWorksheetToPdf) กำหนดอินเทอร์เฟซการโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}

{< tab tabNum="1" >}

```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf?worksheet=Sheet1&outPath=output%2Ffolder&outStorageName=MyStorage&fontsLocation=%2Fcustom%2Ffonts&AutoRowsFit=true&AutoColumnsFit=true&region=en-US&password=SecretPwd" \
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
  "file": "<สตรีมไบนารีของไฟล์ PDF ที่สร้างขึ้น>"
}
```

{< /tab >}

{< /tabs >}

### ใช้ Aspose Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK ซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่งานโครงการของคุณได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้เว็บเซอร์วิสของ Aspose Cells Cloud ด้วย SDK ต่างๆ:
`[TBD]`
---