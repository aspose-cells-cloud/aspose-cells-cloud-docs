---
title: "TransposeData"
ArticleTitle: "TransposeData – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktype: "docs"
url: /th/cells/transpose
aliases: [  /th/cells/transpose ]
keywords: "TransposeData, Aspose.Cells, Cloud API, สเปรดชีต, transpose"
description: "สลับแถวและคอลัมน์ในสเปรดชีต"
weight: 1000
---

## TransposeData ของ Aspose.Cells Cloud Web Services

สลับแถวและคอลัมน์ในสเปรดชีต

### จุดสิ้นสุดของเว็บ API

```http
PUT https://api.aspose.cloud/v4.0/cells/transpose
```

### **ความปลอดภัยและการรับรองความถูกต้อง**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การรับรองความถูกต้องด้วยโทเคน JWT</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง (Path/Query String/HTTP Body) | คำอธิบาย |
|------------------|--------|-----------------------------|------------------------------------------------------------------------|
| Spreadsheet      | ไฟล์   | FormData                    | อัปโหลดไฟล์สเปรดชีต |
| worksheet        | สตริง | Query                       | ชื่อของเวิร์กชีต |
| cellArea         | สตริง | Query                       | ช่วงข้อมูลที่กำหนด |
| outPath          | สตริง | Query                       | (ไม่บังคับ) เส้นทางโฟลเดอร์ที่เก็บสมุดงาน ค่าเริ่มต้นคือ null |
| outStorageName   | สตริง | Query                       | ชื่อพื้นที่จัดเก็บสำหรับไฟล์ผลลัพธ์ |
| region           | สตริง | Query                       | การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) มีผลต่อรูปแบบตัวเลข การแยกวิเคราะห์วันที่ และพฤติกรรมเฉพาะของภูมิภาค |
| password         | สตริง | Query                       | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต |

### พารามิเตอร์ของเนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย |
| -------------- | ---- | ----------- |
| [TBD]          | [TBD]| [TBD]       |

### **คำตอบ**

```json
{
  "file": "สตรีมไบนารีของสเปรดชีตที่ถูก transpose แล้ว"
}
```

**รหัสสถานะของคำตอบ**

| รหัส | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | สำเร็จ (OK) | ส่งคืนไฟล์สเปรดชีตที่ถูก transpose แล้ว |
| 400 | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์อินพุตไม่ถูกต้องหรือคำขอผิดรูปแบบ |
| 401 | ไม่ได้รับอนุญาต (Unauthorized) | การรับรองความถูกต้องล้มเหลว หรือโทเคน JWT หายไป/ไม่ถูกต้อง |
| 413 | เนื้อหาที่ส่งมามีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดภายในเซิร์ฟเวอร์ |

## วิธีใช้ TransposeData ด้วย SDK

### ข้อมูลจำเพาะของ TransposeData

[ข้อมูลจำเพาะของTransposeData API](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{TransposeData}) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการโต้ตอบแบบ REST ผ่านเบราว์เซอร์เว็บได้โดยตรง

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึง Aspose Cells Cloud web services ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="คำตอบ" >}

{< tab tabNum="1" >}

```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/transpose?worksheet=Sheet1&cellArea=A1:C10&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=MyPassword" \
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
  "file": "สตรีมไบนารีของสเปรดชีตที่ถูก transpose แล้ว"
}
```

{< /tab >}

{< /tabs >}

### ใช้ Aspose Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK ซ่อนรายละเอียดระดับต่ำไว้ ช่วยให้คุณสามารถมุ่งเน้นไปที่งานในโปรเจกต์ของคุณได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บบน GitHub</a> เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้ Aspose Cells Cloud web services โดยใช้ SDK ต่างๆ:
`[TBD]`
---