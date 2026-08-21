---
title: "รับการแก้ไขทั้งหมด"
ArticleTitle: "รับการแก้ไขทั้งหมด – Aspose.Cells Cloud"
second_title: "เอกสาร"
linktype: "รับการแก้ไขทั้งหมด"
type: docs
url: /th/cells/spreadsheet/accept-all-revisions
aliases: []
keywords: "Aspose.Cells, AcceptAllRevisions, สเปรดชีต, การแก้ไข"
description: "รับการแก้ไขทั้งหมดในไฟล์สเปรดชีตโดยใช้ API ของ Aspose.Cells Cloud"
weight: 100
---

## การรับการแก้ไขทั้งหมด (AcceptAllRevisions) ของเว็บเซอร์วิส Aspose.Cells Cloud

รับการแก้ไขทั้งหมดในไฟล์สเปรดชีตที่อัปโหลด และส่งคืนเวิร์กบุ๊กที่ผ่านการประมวลผลแล้ว

### ปลายทาง API ของเว็บ

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/accept-all-revisions
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | เส้นทาง/สตริงของ Query/เนื้อหา HTTP | คำอธิบาย |
|----------------|--------|-----------------------------|-------------|
| Spreadsheet    | ไฟล์   | FormData (เนื้อหา HTTP)        | อัปโหลดไฟล์สเปรดชีต |
| outPath        | สตริง | Query                       | (ไม่บังคับ) เส้นทางของโฟลเดอร์ที่เก็บเวิร์กบุ๊กไว้ ค่าเริ่มต้นคือ null |
| outStorageName | สตริง | Query                       | ชื่อ Storage ที่ใช้เก็บไฟล์ผลลัพธ์ |
| fontsLocation  | สตริง | Query                       | ใช้ฟอนต์ที่กำหนดเอง |
| region         | สตริง | Query                       | การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) มีผลต่อการจัดรูปแบบตัวเลข การแปลงวันที่ และพฤติกรรมเฉพาะพื้นที่ |
| password       | สตริง | Query                       | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต |

### พารามิเตอร์ของเนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย |
| -------------- | ---- | ----------- |
| Spreadsheet    | ไฟล์ | อัปโหลดไฟล์สเปรดชีต |

### **การตอบกลับ**

```json
{
  "File": "สตรีมไบนารีของสเปรดชีตที่ผ่านการประมวลผลแล้ว"
}
```

**รหัสสถานะของการตอบกลับ**

| รหัส | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | สำเร็จ (OK) | การรับการแก้ไขสำเร็จ และส่งคืนไฟล์ที่ประมวลผลแล้ว |
| 400 | คำขอไม่ถูกต้อง (Bad Request) | คำขอไม่ถูกต้อง (เช่น ขาดไฟล์ที่จำเป็นหรือพารามิเตอร์ไม่ถูกต้อง) |
| 401 | ไม่ได้รับอนุญาต (Unauthorized) | การยืนยันตัวตนล้มเหลวหรือโทเค็น JWT ขาดหายหรือไม่ถูกต้อง |
| 413 | เนื้อหาขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่อนุญาต |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

## วิธีใช้ AcceptAllRevisions ร่วมกับ SDK

### ข้อมูลเฉพาะของ AcceptAllRevisions

[ข้อมูลเฉพาะของ API AcceptAllRevisions](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AcceptAllRevisions) นิยามอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการปฏิสัมพันธ์ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ที่รันผ่านคำสั่ง command-line เพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ผ่าน cURL

{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}

{< tab tabNum="1" >}

```bash
# ใช้ HTTPS เพื่อเชื่อมต่ออย่างปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/accept-all-revisions?outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/fonts&region=en-US&password=12345" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@sample.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "สตรีมไบนารีของสเปรดชีตที่ผ่านการประมวลผลแล้ว"
}
```

{< /tab >}

{< /tabs >}

### ใช้ SDK ของ Aspose Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK ช่วยซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ <a href="[TBD]" rel="noopener noreferrer">คลังข้อมูล GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้เว็บเซอร์วิสของ Aspose Cells Cloud ผ่าน SDK ต่างๆ:
 `[TBD]`
---