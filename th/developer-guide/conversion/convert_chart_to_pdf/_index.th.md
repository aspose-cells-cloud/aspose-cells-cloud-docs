---
---
title: "การแปลงกราฟเป็น PDF"
ArticleTitle: "การแปลงกราฟเป็น PDF – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktitle: "ConvertChartToPdf"
type: docs
url: /cells/convert/chart/pdf
aliases: []
keywords: "ConvertChartToPdf, Aspose.Cells, PDF, การแปลงกราฟ"
description: "แปลงกราฟในไฟล์สเปรดชีตที่อยู่บนไดรฟ์ในเครื่องเป็น PDF"
weight: 100
---

## การแปลงกราฟเป็น PDF ด้วยเว็บเซอร์วิสของ Aspose.Cells Cloud

วิธีการนี้อ่านกราฟจากไฟล์สเปรดชีตที่อัปโหลดผ่านทางการอัปโหลดไฟล์ในเครื่อง แล้วแปลงกราฟดังกล่าวเป็นรูปแบบ PDF และส่งคืนผลลัพธ์ที่แปลงแล้ว กระบวนการนี้ดำเนินการทั้งหมดบนเซิร์ฟเวอร์คลาวด์ ดังนั้นจึงไม่จำเป็นต้องมีการจัดเก็บข้อมูลชั่วคราว คุณต้องระบุพาธไฟล์ต้นทางและรูปแบบเป้าหมายให้ถูกต้อง รวมทั้งต้องมีสิทธิ์ที่เหมาะสมในการอ่านไฟล์ต้นทาง หากเกิดข้อผิดพลาด เช่น ไฟล์ไม่พบ ปัญหาการเข้าถึง หรือความล้มเหลวในการแปลง จะส่งคืนการตอบกลับ HTTP ที่เหมาะสม

### จุดสิ้นสุดของเว็บ API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ประเภท | Path/Query String/HTTP Body | คำอธิบาย |
|------------------|--------|-----------------------------|-------------|
| Spreadsheet      | ไฟล์ | FormData                    | อัปโหลดไฟล์สเปรดชีต |
| worksheet        | สตริง | Query                       | ชื่อเวิร์กชีตของสเปรดชีต |
| chartIndex       | จำนวนเต็ม | Query                       | ดัชนีของกราฟในเวิร์กชีต |
| outPath          | สตริง | Query                       | (ไม่บังคับ) เส้นทางโฟลเดอร์ที่เก็บสมุดงาน ค่าเริ่มต้นคือ null |
| outStorageName   | สตริง | Query                       | ชื่อที่จัดเก็บไฟล์ผลลัพธ์ |
| fontsLocation    | สตริง | Query                       | ใช้ฟอนต์ที่กำหนดเอง |
| region           | สตริง | Query                       | การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) ซึ่งส่งผลต่อการจัดรูปแบบตัวเลข การประมวลผลวันที่ และพฤติกรรมที่ขึ้นกับภาษาท้องถิ่น |
| password         | สตริง | Query                       | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต |

### พารามิเตอร์ของเนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย |
| -------------- | ---- | ----------- |
| Spreadsheet    | ไฟล์ | อัปโหลดไฟล์สเปรดชีต |

### **การตอบกลับ**

```json
{
  "ResponseFile": "สตรีมไฟล์ PDF แบบไบนารี"
}
```

**โค้ดสถานะของการตอบกลับ**

| โค้ด | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | สำเร็จ | กราฟได้รับการแปลงเป็น PDF สำเร็จ และส่งคืนไฟล์ PDF แบบไบนารี |
| 400 | คำขอไม่ถูกต้อง | พารามิเตอร์คำขอไม่ถูกต้อง หรือ URL ผิดรูปแบบ |
| 401 | ไม่ได้รับอนุญาต | การยืนยันตัวตนล้มเหลว หรือไม่ได้ระบุข้อมูลประจำตัว |
| 404 | ไม่พบ | ไม่สามารถเข้าถึงไฟล์ต้นทาง |
| 413 | ขนาดข้อมูลในคำขอใหญ่เกินไป | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่อนุญาต |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ | เกิดข้อผิดพลาดขณะประมวลผลการแปลง |

## วิธีการใช้งานการแปลงกราฟเป็น PDF ด้วย SDK

### คุณสมบัติของการแปลงกราฟเป็น PDF

[สเปคของ API การแปลงกราฟเป็น PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToPdf) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และอนุญาตให้คุณดำเนินการ REST ผ่านเว็บเบราว์เซอร์โดยตรง

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}
{< tab tabNum="1" >}
```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/convert/chart/pdf?worksheet={worksheet}&chartIndex={chartIndex}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "ResponseFile": "สตรีมไฟล์ PDF แบบไบนารี"
}
```
{< /tab >}
{< /tabs >}

### ใช้ Aspose Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งพัฒนา SDK ช่วยซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository บน GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้เว็บเซอร์วิสของ Aspose Cells Cloud ด้วย SDK ต่างๆ:
`[TBD]`
---