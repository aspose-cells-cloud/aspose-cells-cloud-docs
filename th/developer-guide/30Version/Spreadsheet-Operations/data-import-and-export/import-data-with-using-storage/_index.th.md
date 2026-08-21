---
title: "การนำเข้าข้อมูลโดยใช้ที่จัดเก็บข้อมูล"
second_title: "เอกสาร"
linktype: "docs"
url: /th/import-data-with-using-storage/
aliases:
  - /import-data-into-excel-worksheet/
  - /import-data-into-worksheet/
  - /import-data-in-excel-worksheet/
  - /import-data/
  - /import/with-using-storage/
description: "การนำเข้าข้อมูลโดยใช้ที่จัดเก็บข้อมูล: นำเข้าข้อมูลลงในสมุดงาน Excel โดยใช้ API ของ Aspose.Cells Cloud จากแหล่งที่จัดเก็บข้อมูลต่างๆ รองรับรูปแบบ JSON, CSV และอื่นๆ ผ่าน HTTPS"
keywords: "Aspose.Cells Cloud, Excel, นำเข้าข้อมูล, REST API, Cloud Storage, JSON, CSV, PDF, Markdown, HTTPS"
weight: 10
ArticleTitle: "การนำเข้าข้อมูลโดยใช้ที่จัดเก็บข้อมูล - เอกสารประกอบ API ของ Aspose.Cells Cloud"
---

REST API นี้ใช้สำหรับนำเข้าข้อมูลลงในไฟล์ Excel

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **ความปลอดภัยและการพิสูจน์ตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การพิสูจน์ตัวตนด้วยโทเค็น JWT</a>

### พารามิเตอร์ของคำขอ

| พารามิเตอร์ | ประเภทข้อมูล | ตำแหน่ง | คำอธิบาย |
|-------------|-------------|----------|----------|
| name | string | path | ชื่อของไฟล์ Excel |
| folder | string | query | เส้นทางของโฟลเดอร์ในที่จัดเก็บข้อมูลที่ไฟล์นั้นอยู่ |
| storageName | string | query | ชื่อของบริการที่จัดเก็บข้อมูล |
| importData | object | body | ออบเจกต์ JSON ที่มีข้อมูลที่จะนำเข้า |

**พารามิเตอร์ตัวเลือกการนำเข้าข้อมูล** อธิบายไว้ใน [ลิงก์อ้างอิง](/cells/import/#import-data-option-parameter)

**ข้อกำหนดเบื้องต้น:** คุณต้องระบุโทเค็น JWT ที่ถูกต้องในส่วนหัว `Authorization` และต้องแน่ใจว่าสมุดงานเป้าหมายมีอยู่แล้วในตำแหน่งที่จัดเก็บข้อมูลที่ระบุ

### การตอบกลับ

```json
{
  "Status":"OK",
  "Code":200
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย | คำอธิบาย |
|------|----------|----------|
| 200 | OK | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับประกอบด้วยรายละเอียดของการดำเนินการ |
| 400 | Bad Request | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401 | Unauthorized | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย |
| 413 | Payload Too Large | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500 | Internal Server Error | ข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด |

## วิธีใช้ API PostImportData ร่วมกับ SDK

### ข้อกำหนดเฉพาะของ API PostImportData

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostImportData" rel="noopener noreferrer">ข้อกำหนด OpenAPI</a> กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถโต้ตอบกับ REST API ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งต่างๆ เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata" \
     -X POST \
     -d '{"Data":[1,2,4],"DestinationWorksheet":"Sheet1","FirstRow":1,"FirstColumn":2,"IsVertical":true,"IsInsert":true,"importDataType":"IntArray"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### การใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วในการพัฒนา SDK ช่วยซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณได้ โปรดตรวจสอบ [ที่เก็บบน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ภาษา PHP: