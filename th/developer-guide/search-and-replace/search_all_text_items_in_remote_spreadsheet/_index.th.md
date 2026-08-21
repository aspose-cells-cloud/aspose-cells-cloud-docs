---
title: "SearchAllTextItemsInRemoteSpreadsheet"
ArticleTitle: "SearchAllTextItemsInRemoteSpreadsheet – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktype: "SearchAllTextItemsInRemoteSpreadsheet"
type: docs
url: /th/cells/{name}/search/content/all-textitems
aliases: []
keywords: "ค้นหา, รายการข้อความ, Aspose.Cells"
description: "ค้นหาทุกรายการข้อความในสเปรดชีตระยะไกลโดยใช้ Aspose.Cells Cloud"
weight: 100
---

## SearchAllTextItemsInRemoteSpreadsheet ของ Aspose.Cells Cloud Web Services

เมทอดนี้ค้นหารายการข้อความทั้งหมดภายในไฟล์สเปรดชีตระยะไกล โดยรองรับการค้นหาในทุกชีตและเซลล์ของสมุดงาน ระบุตำแหน่งที่พบคำค้นหา การดำเนินการนี้ทำบนคลาวด์ ไม่ต้องใช้พื้นที่จัดเก็บในเครื่อง ตรวจสอบให้แน่ใจว่าคุณมีสิทธิ์อ่านไฟล์ต้นทางที่จำเป็น หากไม่สามารถเข้าถึงไฟล์ต้นทางหรือเกิดข้อผิดพลาดในระหว่างกระบวนการค้นหา (เช่น รูปแบบไฟล์ที่ไม่รองรับ) จะเกิดข้อยกเว้นที่เหมาะสมขึ้น เมทอดอาจส่งคืนตำแหน่งของผลลัพธ์ที่ตรงกัน (เช่น ชื่อชีต พิกัดเซลล์) ขึ้นอยู่กับรายละเอียดการปรับใช้งาน

### จุดสิ้นสุดของเว็บ API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์ด้วย JWT token</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | Path/Query String/HTTP Body | คำอธิบาย |
|----------------|--------|-----------------------------|-------------|
| name           | string | Path                        | ชื่อไฟล์สมุดงาน |
| folder         | string | Query                       | เส้นทางโฟลเดอร์ที่เก็บสมุดงานไว้ |
| storageName    | string | Query                       | (ไม่บังคับ) ชื่อของพื้นที่จัดเก็บ หากใช้คลาวด์สตอเรจแบบกำหนดเอง ใช้พื้นที่จัดเก็บเริ่มต้นหากไม่ระบุ |
| region         | string | Query                       | การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) มีผลต่อการจัดรูปแบบตัวเลข การแยกวิเคราะห์วันที่ และพฤติกรรมเฉพาะภูมิภาค |
| password       | string | Query                       | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต |

### พารามิเตอร์เนื้อหาคำขอ (Request Body Parameter)

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย |
| -------------- | ---- | ----------- |
| [TBD]          |      | [TBD] |

### **การตอบกลับ (Response)**

```json
{
  "TextItems": [
    {
      "SheetName": "string",
      "CellAddress": "string",
      "Text": "string"
    }
  ],
  "TotalCount": 0
}
```

**โค้ดสถานะการตอบกลับ**

| โค้ด | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | สำเร็จ (OK) | คำขอสำเร็จ และการตอบกลับมีรายการข้อความทั้งหมดที่พบในสเปรดชีต |
| 400 | คำขอไม่ถูกต้อง (Bad Request) | URL หรือพารามิเตอร์คำขอไม่ถูกต้อง |
| 401 | ไม่ได้รับอนุญาต (Unauthorized) | การตรวจสอบสิทธิ์ล้มเหลว หรือไม่ได้ระบุข้อมูลประจำตัว |
| 404 | ไม่พบ (Not Found) | ไม่สามารถเข้าถึงไฟล์ต้นทางได้ |
| 413 | ข้อมูลในคำขอมีขนาดใหญ่เกินไป (Payload Too Large) | ขนาดเนื้อหาในคำขอเกินขนาดที่อนุญาต |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | สมุดงานเกิดข้อผิดพลาดในการรับข้อมูล |

## วิธีใช้ SearchAllTextItemsInRemoteSpreadsheet ด้วย SDK

### ข้อกำหนด SearchAllTextItemsInRemoteSpreadsheet

[ข้อกำหนด API SearchAllTextItemsInRemoteSpreadsheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchAllTextItemsInRemoteSpreadsheet) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้สาธารณะ และให้คุณดำเนินการ REST interactions โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึง Aspose.Cells web services ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียก Cloud API โดยใช้ cURL

{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}

{< tab tabNum="1" >}

```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "TextItems": [
    {
      "SheetName": "Sheet1",
      "CellAddress": "A1",
      "Text": "Sample text"
    }
  ],
  "TotalCount": 1
}
```

{< /tab >}

{< /tabs >}

### ใช้ Aspose Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK ซ่อนรายละเอียดระดับต่ำไว้ ช่วยให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud อย่างสมบูรณ์

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียก Aspose Cells Cloud web services โดยใช้ SDK ต่างๆ:
`[TBD]`
---