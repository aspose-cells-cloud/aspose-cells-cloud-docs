---
title: "แก้ไขการ.pivot ของตาราง"
ArticleTitle: "แก้ไขการ.pivot ของตาราง – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktype: "docs"
url: /cells/unpivot/table
aliases: []
keywords: "Aspose.Cells, Unpivot, Transform"
description: "สลับแถวและคอลัมน์ในสเปรดชีต"
weight: 1
---

## การแก้ไขการ.pivot ของตารางด้วย Aspose.Cells Cloud Web Services

สลับแถวและคอลัมน์ในสเปรดชีต

### จุดสิ้นสุดของ Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/table
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### พารามิเตอร์ของ Request

| ชื่อพารามิเตอร์ | ประเภทข้อมูล | Path/Query String/HTTP Body | คำอธิบาย |
|------------------|---------|-----------------------------|------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | ไฟล์    | FormData                    | อัปโหลดไฟล์สเปรดชีต |
| worksheet        | สตริง  | Query                       | ชื่อเวิร์กชีต |
| index            | จำนวนเต็ม | Query                       | ช่วงข้อมูลที่ระบุ |
| skipEmptyValue   | ค่าบูลีน | Query                       | ข้ามค่าว่าง (ค่าเริ่มต้น: true) |
| outPath          | สตริง  | Query                       | (ไม่บังคับ) พาธของโฟลเดอร์ที่จัดเก็บเวิร์กบุ๊ก ค่าเริ่มต้นคือ null |
| outStorageName   | สตริง  | Query                       | ชื่อ Storage สำหรับไฟล์ที่ส่งออก |
| region           | สตริง  | Query                       | การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) ซึ่งมีผลต่อการจัดรูปแบบตัวเลข การแปลงวันที่ และพฤติกรรมเฉพาะของแต่ละภูมิภาค |
| password         | สตริง  | Query                       | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต |

### พารามิเตอร์ของ Request Body

| ชื่อพารามิเตอร์ | ประเภทข้อมูล | คำอธิบาย |
| -------------- | ---- | ----------- |
| N/A            | N/A  | ไม่มีพารามิเตอร์ในส่วนของ Request Body |

### **Response**

```json
{
  "File": "ข้อมูลแบบ binary stream ของสเปรดชีตที่ผ่านการแก้ไขการ.pivot แล้ว"
}
```

**รหัสสถานะของ Response**

| รหัส | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | สำเร็จ (OK) | ส่งคืนไฟล์สเปรดชีตที่ผ่านการแก้ไขการ.pivot แล้ว |
| 400 | Request ไม่ถูกต้อง (Bad Request) | พารามิเตอร์ของ Request ไม่ถูกต้อง |
| 401 | ไม่ได้รับอนุญาต (Unauthorized) | การยืนยันตัวตนล้มเหลว หรือ JWT token ไม่ถูกต้อง/ไม่มี |
| 413 | Payload ใหญ่เกินไป (Payload Too Large) | ขนาดไฟล์ที่อัปโหลดเกินขีดจำกัดที่อนุญาต |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดภายในเซิร์ฟเวอร์ |

## วิธีการใช้งานการแก้ไขการ.pivot ของตารางด้วย SDKs

### ข้อกำหนดของการแก้ไขการ.pivot ของตาราง

[ข้อกำหนดของ API การแก้ไขการ.pivot ของตาราง](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4# /Transform/UnpivotTable) กำหนด API ที่สามารถเข้าถึงได้แบบสาธารณะ ช่วยให้คุณดำเนินการ REST interactions ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึง Aspose.Cells web services ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก Cloud API ด้วย cURL

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/table?worksheet={worksheet}&index={index}&skipEmptyValue={skipEmptyValue}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}" \
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
  "File": "ข้อมูลแบบ binary stream ของสเปรดชีตที่ผ่านการแก้ไขการ.pivot แล้ว"
}
```

{< /tab >}

{< /tabs >}

### ใช้งาน Aspose Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK ทำหน้าที่ซ่อนรายละเอียดระดับต่ำ ช่วยให้คุณมุ่งเน้นไปที่งานของโครงการได้ โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้ Aspose Cells Cloud web services โดยใช้ SDK ต่าง ๆ:
 `[TBD]`
---