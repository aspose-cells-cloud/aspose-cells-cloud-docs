---
title: "ค้นหาลิงก์ที่เสียในเวิร์กชีตระยะไกล"
ArticleTitle: "ค้นหาลิงก์ที่เสียในเวิร์กชีตระยะไกล – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktype: "docs"
url: /cells/{name}/worksheets/{worksheet}/search/broken-links
aliases: []
keywords: "Aspose.Cells, ค้นหาลิงก์ที่เสีย, เวิร์กชีตระยะไกล"
description: "ค้นหาลิงก์ที่เสียในเวิร์กชีตของไฟล์สเปรดชีตที่จัดเก็บในคลาวด์ระยะไกล"
weight: 100
---

## การค้นหาลิงก์ที่เสียในเวิร์กชีตระยะไกลของ Aspose.Cells Cloud Web Services

เมธอดนี้ใช้ค้นหาลิงก์ที่เสียภายในเวิร์กชีตของไฟล์สเปรดชีตที่จัดเก็บไว้ในพื้นที่จัดเก็บบนคลาวด์ระยะไกล โดยจะสแกนทุกชีตและเซลล์เพื่อระบุลิงก์ที่ไม่สามารถเชื่อมต่อไปยังปลายทางที่ถูกต้องได้อีกต่อไป เช่น URL ที่ไม่สามารถใช้งานได้หรือการอ้างอิงภายนอกที่หายไป การดำเนินการนี้จะดำเนินการจากระยะไกลภายในสภาพแวดล้อมคลาวด์ โดยไม่จำเป็นต้องดาวน์โหลดไฟล์มายังเครื่องของคุณ

### จุดสิ้นสุดของเว็บ API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | Path/Query String/HTTP Body | คำอธิบาย |
|----------------|------|-----------------------------|-------------|
| name | string | Path | ชื่อไฟล์สมุดบันทึกที่ต้องการค้นหา |
| worksheet | string | Path | ระบุเวิร์กชีตที่ต้องการค้นหา |
| folder | string | Query | พาธของโฟลเดอร์ที่จัดเก็บสมุดบันทึกไว้ (ไม่บังคับ) |
| storageName | string | Query | (ไม่บังคับ) ชื่อของพื้นที่จัดเก็บที่ใช้งานอยู่ หากใช้พื้นที่จัดเก็บคลาวด์แบบกำหนดเอง หากไม่ระบุจะใช้พื้นที่จัดเก็บเริ่มต้น |
| region | string | Query | การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) ส่งผลต่อการจัดรูปแบบตัวเลข การแยกวิเคราะห์วันที่ และพฤติกรรมเฉพาะของแต่ละภูมิภาค |
| password | string | Query | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต |

### พารามิเตอร์ของเนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย |
| -------------- | ---- | ----------- |
| — | — | ไม่จำเป็นต้องส่งเนื้อหาคำขอสำหรับการดำเนินการนี้ |

### **การตอบกลับ**

```json
{
  "Links": [
    {
      "SheetName": "Sheet1",
      "CellName": "A1",
      "Url": "http://invalid.example.com"
    }
  ],
  "Count": 1
}
```

**โค้ดสถานะของการตอบกลับ**

| โค้ด | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | สำเร็จ (OK) | ดึงรายการลิงก์ที่เสียได้สำเร็จ |
| 400 | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ของคำขอไม่ถูกต้องหรือ URL ผิดรูปแบบ |
| 401 | ไม่ได้รับอนุญาต (Unauthorized) | การยืนยันตัวตนล้มเหลว หรือไม่ได้ส่งข้อมูลรับรองใดๆ มา |
| 404 | ไม่พบ (Not Found) | ไม่สามารถเข้าถึงไฟล์ต้นฉบับได้ |
| 413 | ข้อมูลที่ส่งมามีขนาดใหญ่เกินไป (Payload Too Large) | ขนาดของ entity ในคำขอใหญ่เกินขีดจำกัด |
| 500 | เกิดข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | สมุดบันทึกเกิดข้อผิดพลาดในการดึงข้อมูล |

## วิธีใช้การค้นหาลิงก์ที่เสียในเวิร์กชีตระยะไกลด้วย SDKs

### ข้อมูลจำเพาะของการค้นหาลิงก์ที่เสียในเวิร์กชีตระยะไกล

[ข้อมูลจำเพาะของ API การค้นหาลิงก์ที่เสียในเวิร์กชีตระยะไกล](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteWorksheet) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้จากภายนอก และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งในบรรทัดคำสั่งเพื่อเข้าถึง Aspose.Cells web services ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}

{< tab tabNum="1" >}

```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Links": [
    {
      "SheetName": "Sheet1",
      "CellName": "A1",
      "Url": "http://invalid.example.com"
    }
  ],
  "Count": 1
}
```

{< /tab >}

{< /tabs >}

### ใช้ Aspose Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK จะซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่ภารกิจของโครงการได้ โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud แบบครบถ้วน

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้ Aspose Cells Cloud web services ผ่าน SDK ต่างๆ:
`[TBD]`
---