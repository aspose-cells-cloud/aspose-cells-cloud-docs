---
title: "UnpivotRange"
ArticleTitle: "UnpivotRange – Aspose.Cells Cloud"
second_title: "เอกสาร"
linktype: "UnpivotRange"
type: docs
url: /th/cells/unpivot/range
aliases: []
keywords: "Aspose.Cells, UnpivotRange, API"
description: "สลับแถวและคอลัมน์ในสเปรดชีต"
weight: 10
---

## UnpivotRange ของ Aspose.Cells Cloud Web Services

สลับแถวและคอลัมน์ในสเปรดชีต

### ปลายทาง Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/range
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์ด้วย JWT token</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท | Path/Query String/HTTP Body | คำอธิบาย |
|------------------|--------|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | ไฟล์ | FormData                    | อัปโหลดไฟล์สเปรดชีต |
| worksheet        | สตริง | Query                       | ชื่อแผ่นงาน |
| cellArea         | สตริง | Query                       | ช่วงข้อมูลที่ระบุ |
| skipEmptyValue   | บูลีน | Query                       | หากเป็นค่า true จะข้ามค่าว่างค่าเริ่มต้นคือ true |
| outPath          | สตริง | Query                       | (ไม่บังคับ) ตำแหน่งโฟลเดอร์ที่จัดเก็บสมุดงาน ค่าเริ่มต้นคือ null |
| outStorageName   | สตริง | Query                       | ชื่อพื้นที่จัดเก็บไฟล์ผลลัพธ์ |
| region           | สตริง | Query                       | การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) ส่งผลต่อการจัดรูปแบบตัวเลข การแยกวิเคราะห์วันที่ และพฤติกรรมเฉพาะของแต่ละภูมิภาค |
| password         | สตริง | Query                       | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต |

### พารามิเตอร์เนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย |
|----------------|------|-------------|
| — | — | — |

### **การตอบกลับ**

```json
{
  "File": "สตรีมไบนารี"
}
```

**โค้ดสถานะการตอบกลับ**

| โค้ด | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | สำเร็จ (OK) | ส่งคืนไฟล์สเปรดชีตที่ผ่านการ unpivot แล้ว |
| 400 | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์คำขอไม่ถูกต้อง |
| 401 | ไม่ได้รับอนุญาต (Unauthorized) | การตรวจสอบสิทธิ์ล้มเหลว |
| 413 | ข้อมูลโหลดมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500 | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) | เซิร์ฟเวอร์พบสถานการณ์ที่ไม่คาดคิด |

## วิธีใช้ UnpivotRange ด้วย SDK

### ข้อมูลจำเพาะของ UnpivotRange

[ข้อมูลจำเพาะของ API UnpivotRange](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{UnpivotRange}) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้สาธารณะ และช่วยให้คุณดำเนินการโต้ตอบแบบ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells Cloud ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียก API บนคลาวด์ด้วย cURL

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/range?worksheet=Sheet1&cellArea=A1:C10&skipEmptyValue=true&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=yourPassword" -X PUT -H "Content-Type: multipart/form-data" -H "Accept: application/octet-stream" -H "Authorization: Bearer <jwt token>" -F 'Spreadsheet=@sample.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "FileUrl": "https://example.com/output/unpivoted.xlsx"
}
```

{< /tab >}

{< /tabs >}

### ใช้ SDK ของ Aspose Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK จะซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บ GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกบริการเว็บของ Aspose Cells Cloud โดยใช้ SDK ต่างๆ:
 `[TBD]`
---