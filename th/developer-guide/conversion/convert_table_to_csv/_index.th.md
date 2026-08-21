---
title: "แปลงตารางเป็น CSV"
ArticleTitle: "แปลงตารางเป็น CSV – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktype: "docs"
url: /th/cells/convert/table/csv
aliases: []
keywords: "แปลงตารางเป็น CSV, Aspose.Cells, Cloud API"
description: "แปลงตารางของสมุดงานในระบบไฟล์ท้องถิ่นเป็นไฟล์ CSV"
weight: 1
---

## การแปลงตารางเป็น CSV ด้วยเว็บเซอร์วิสของ Aspose.Cells Cloud

เมธอดนี้อ่านไฟล์สมุดงานจากระบบไฟล์ท้องถิ่น แปลงตารางที่ระบุเป็นไฟล์ CSV และส่งคืนผลลัพธ์ที่แปลงแล้ว กระบวนการนี้ดำเนินการทั้งหมดบนเซิร์ฟเวอร์คลาวด์ ดังนั้นจึงไม่จำเป็นต้องอัปโหลดไฟล์ไปยังที่เก็บข้อมูลบนคลาวด์ก่อนหน้า ต้องระบุเส้นทางไฟล์ต้นทางและรูปแบบปลายทางอย่างถูกต้อง รวมทั้งต้องมีสิทธิ์ที่เหมาะสมในการอ่านไฟล์ต้นทาง ข้อผิดพลาด เช่น ไฟล์หายไป เส้นทางไม่สามารถเข้าถึงได้ หรือการแปลงล้มเหลว จะส่งผลให้เกิดข้อยกเว้นที่เหมาะสม

### จุดสิ้นสุดของเว็บ API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์แบบ JWT token</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ประเภท | Path/Query String/HTTP Body | คำอธิบาย |
|------------------|--------|-----------------------------|-------------|
| Spreadsheet      | ไฟล์   | FormData                    | อัปโหลดไฟล์สมุดงาน |
| worksheet        | สตริง | Query                       | ชื่อเวิร์กชีตของสมุดงาน |
| tableName        | สตริง | Query                       | ชื่อตาราง |
| outPath          | สตริง | Query                       | (ไม่บังคับ) เส้นทางโฟลเดอร์ที่จัดเก็บสมุดงาน โดยค่าเริ่มต้นเป็นค่า null |
| outStorageName   | สตริง | Query                       | ชื่อที่เก็บข้อมูลสำหรับไฟล์ผลลัพธ์ |
| fontsLocation    | สตริง | Query                       | ใช้ฟอนต์ที่กำหนดเอง |
| AutoRowsFit      | ค่าบูลีน | Query                    | (ไม่บังคับ) ปรับขนาดความสูงของแถวทั้งหมดในเวิร์กชีตอัตโนมัติ |
| AutoColumnsFit   | ค่าบูลีน | Query                    | (ไม่บังคับ) ปรับขนาดความกว้างของคอลัมน์ทั้งหมดในเวิร์กชีตอัตโนมัติ |
| region           | สตริง | Query                       | การตั้งค่าภูมิภาค/ภาษาของสมุดงาน (เช่น `en-US`, `fr-FR`) มีผลต่อการจัดรูปแบบตัวเลข การแยกวิเคราะห์วันที่ และพฤติกรรมเฉพาะของโลคอล |
| password         | สตริง | Query                       | รหัสผ่านสำหรับเปิดไฟล์สมุดงาน |

### พารามิเตอร์ของเนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย |
| -------------- | ---- | ----------- |
| *ไม่มี* | *ไม่มี* | *ไม่จำเป็นต้องส่งเนื้อหาคำขอ; ไฟล์จะถูกส่งผ่าน multipart/form-data* |

### **การตอบกลับ**

```json
{
  "file": "สตรีมไบนารีของไฟล์ CSV ที่สร้างขึ้น"
}
```

**รหัสสถานะของการตอบกลับ**

| รหัส | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | สำเร็จ | แปลงตารางเรียบร้อยแล้ว และส่งคืนไฟล์ CSV |
| 400 | คำขอไม่ถูกต้อง | พารามิเตอร์คำขอไม่ถูกต้องหรือ URL ผิดรูปแบบ |
| 401 | ไม่ได้รับอนุญาต | การตรวจสอบสิทธิ์ล้มเหลวหรือไม่ได้ระบุข้อมูลประจำตัว |
| 404 | ไม่พบ | ไฟล์ต้นทางไม่สามารถเข้าถึงได้หรือไม่มีอยู่จริง |
| 413 | เนื้อหาที่ส่งมามีขนาดใหญ่เกินไป | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่อนุญาต |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ | สมุดงานเกิดข้อผิดพลาดระหว่างการแปลง |

## วิธีใช้การแปลงตารางเป็น CSV ด้วย SDK

### ข้อมูลกำกับการแปลงตารางเป็น CSV

[ข้อมูลกำกับ API การแปลงตารางเป็น CSV](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToCsv) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้สาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งในบรรทัดคำสั่งเพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}

{< tab tabNum="1" >}

```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/convert/table/csv?worksheet={worksheet}&tableName={tableName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&AutoRowsFit={AutoRowsFit}&AutoColumnsFit={AutoColumnsFit}&region={region}&password={password}" \
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
  "file": "สตรีมไบนารีของไฟล์ CSV ที่สร้างขึ้น"
}
```

{< /tab >}

{< /tabs >}

### ใช้ Aspose Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK จะซ่อนรายละเอียดระดับต่ำ ช่วยให้คุณมุ่งเน้นไปที่งานของโครงการได้ โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้เว็บเซอร์วิสของ Aspose.Cells Cloud ผ่าน SDK ต่างๆ:
`[TBD]`
---