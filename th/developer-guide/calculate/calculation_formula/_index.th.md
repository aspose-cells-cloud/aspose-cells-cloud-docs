---
title: "สูตรการคำนวณ"
ArticleTitle: "สูตรการคำนวณ – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktitle: "สูตรการคำนวณ"
type: docs
url: /th/cells/calculate/formula
aliases: []
keywords: "Aspose Cells, สูตรการคำนวณ, สเปรดชีต, API"
description: "คำนวณสูตรในสเปรดชีตโดยใช้ Aspose.Cells Cloud API"
weight: 100
---

## สูตรการคำนวณของเว็บเซอร์วิส Aspose.Cells Cloud

คำนวณสูตรที่ระบุในแผ่นงานที่กำหนดของไฟล์สเปรดชีตที่อัปโหลด และส่งคืนไฟล์สเปรดชีตที่ได้เป็นสตรีมไบนารี การดำเนินการนี้รองรับการประมวลผลตามการตั้งค่าภูมิภาคผ่านพารามิเตอร์ **region** และสามารถเปิดไฟล์ที่มีการป้องกันด้วยรหัสผ่านได้

### จุดสิ้นสุดของเว็บ API

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/formula
```

### **ความปลอดภัยและการพิสูจน์ตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การพิสูจน์ตัวตนแบบ JWT token</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | Path/Query String/HTTP Body | คำอธิบาย |
|----------------|--------|-----------------------------|-------------|
| Spreadsheet    | ไฟล์   | FormData                    | อัปโหลดไฟล์สเปรดชีต |
| worksheet      | สตริง | Query                       | ชื่อของแผ่นงานที่มีสูตร |
| formula        | สตริง | Query                       | สูตรที่ต้องการคำนวณ (เช่น `=SUM(A1:B2)`) |
| region         | สตริง | Query                       | การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) มีผลต่อการจัดรูปแบบตัวเลข การแปลงวันที่ และพฤติกรรมเฉพาะภูมิภาค |
| password       | สตริง | Query                       | รหัสผ่านสำหรับการเปิดไฟล์สเปรดชีต |

### พารามิเตอร์ของเนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **การตอบกลับ**

```json
{
  "File": "<สตรีมไบนารีของไฟล์สเปรดชีตที่ได้>"
}
```

**โค้ดสถานะการตอบกลับ**

| โค้ด | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | สำเร็จ | การคำนวณสำเร็จ; ส่งคืนไฟล์สเปรดชีตที่ได้ |
| 400 | คำขอไม่ถูกต้อง | พารามิเตอร์คำขอมีค่าว่างหรือไม่ถูกต้องหนึ่งพารามิเตอร์ขึ้นไป |
| 401 | ไม่ได้รับอนุญาต | การพิสูจน์ตัวตนล้มเหลวหรือ JWT token ขาดหาย/ไม่ถูกต้อง |
| 413 | ข้อมูลส่งออกมีขนาดใหญ่เกินไป | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่อนุญาต |
| 500 | เกิดข้อผิดพลาดภายในเซิร์ฟเวอร์ | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

## วิธีการใช้สูตรการคำนวณด้วย SDK

### คุณสมบัติของสูตรการคำนวณ

[สเปคของ Calculate Formula API](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/CalculationFormula) นิยามอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถโต้ตอบกับ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งเชลล์เพื่อเข้าถึงเว็บเซอร์วิสของ Aspose Cells Cloud ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ผ่าน cURL

{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}

{< tab tabNum="1" >}

```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/calculate/formula?worksheet=Sheet1&formula=%3DSUM(A1%3AB2)&region=en-US&password=MyPassword" \
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
  "File": "<สตรีมไบนารีของไฟล์สเปรดชีตที่ได้>"
}
```

{< /tab >}

{< /tabs >}

### ใช้ SDK ของ Aspose Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK ซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่งานของโครงการได้ โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บ GitHub</a> เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้เว็บเซอร์วิสของ Aspose Cells Cloud ผ่าน SDK ต่างๆ:
 `[TBD]`
---