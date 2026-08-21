---
---
title: "Aspose.Cells Cloud – ผสาน แยก และนำเข้าข้อมูลสเปรดชีต"
second title: "เอกสาร"
ArticleTitle: "การประมวลผลข้อมูลสเปรดชีต – ผสาน แยก และนำเข้า"
linktitle: "การประมวลผลข้อมูล"
type: docs
url: /data-processing/
keywords: "Aspose.Cells Cloud, การประมวลผลข้อมูลสเปรดชีต, การผสาน Excel, การแยก Excel, การนำเข้า CSV, การนำเข้า JSON, API"
description: "คู่มือโดยละเอียดสำหรับการนำเข้าข้อมูล CSV/JSON, การผสานสมุดงาน Excel ระยะไกล และการแยกสเปรดชีตขนาดใหญ่โดยใช้ Aspose.Cells Cloud REST API พร้อมตัวอย่างคำขอและคำตอบ"
weight: 30
---

**Aspose.Cells Cloud** – บริการแบบ RESTful ที่ช่วยให้คุณสามารถจัดการไฟล์ Excel ผ่านระบบคลาวด์ได้อย่างเป็นโปรแกรม รองรับการนำเข้าข้อมูลจากรูปแบบต่างๆ การผสานสมุดงาน และการแยกสเปรดชีตขนาดใหญ่

ส่วน **การประมวลผลข้อมูล** ของ API Aspose.Cells Cloud ช่วยให้คุณสามารถนำเข้า ผสาน และแยกข้อมูลสเปรดชีตได้อย่างเป็นโปรแกรม โดยใช้จุดปลาย (endpoints) ด้านล่างนี้เพื่อจัดการการนำเข้า CSV/JSON การรวมสมุดงาน หรือการแยกไฟล์ขนาดใหญ่เป็นชิ้นส่วนที่จัดการได้ง่ายขึ้น

## การนำเข้าและจัดการข้อมูล

- **[นำเข้าข้อมูล CSV, JSON, XML ลงในไฟล์ Excel](https://docs.aspose.cloud/cells/import-data-into-spreadsheet/)**  

การดำเนินการนำเข้าจะรับข้อมูล JSON, CSV หรือ XML และสร้างแผ่นงานใหม่ (หรืออัปเดตแผ่นงานที่มีอยู่) ในสมุดงานเป้าหมาย

**รายละเอียดจุดปลาย**

| วิธี HTTP | จุดปลาย | เนื้อหาคำขอ | คำตอบที่สำเร็จ |
|-----------|---------|-------------|----------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/import` | `application/json` หรือ `text/csv` (ขึ้นอยู่กับรูปแบบ) | `200 OK` พร้อม JSON ที่มีข้อมูลเมตาของสมุดงานที่อัปเดตแล้ว |
| GET | `https://api.aspose.cloud/v3.0/cells/{fileName}?format=excel` | *ไม่มี* | ส่งคืนไฟล์สมุดงานที่ประมวลผลแล้ว |

**ตัวอย่างคำขอ cURL (การนำเข้า CSV)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/import" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: text/csv" \
     --data-binary @data.csv
```

**ตัวอย่างคำตอบ JSON**

```json
{
  "Code": 200,
  "Status": "OK",
  "Workbook": {
    "FileName": "MyWorkbook.xlsx",
    "Worksheets": 3
  }
}
```

> **ข้อกำหนดเบื้องต้น**: จำเป็นต้องมีโทเคนการเข้าถึง OAuth2 ไฟล์ต้นทางต้องอยู่ในพื้นที่จัดเก็บของ Aspose Cloud หรือต้องส่งผ่านการอัปโหลดแบบมัลติพาร์ท

## การดำเนินการผสานไฟล์

- **[ผสานไฟล์ Excel ระยะไกลลงในสมุดงานที่ระบุ](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)**
- **[ผสานไฟล์ Excel หลายไฟล์ลงในสมุดงานเดียว](https://docs.aspose.cloud/cells/merge-spreadsheets/)**
- **[ผสานไฟล์ Excel ที่ตรงกับรูปแบบในโฟลเดอร์ระยะไกล](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)**  

การผสานจะรวมสมุดงานสองสมุดขึ้นไปเข้าเป็นสมุดงานเป้าหมายเดียว API รองรับทั้งการระบุรายชื่อไฟล์อย่างชัดเจน และการผสานตามรูปแบบภายในโฟลเดอร์พื้นที่จัดเก็บ

**รายละเอียดจุดปลาย**

| วิธี HTTP | จุดปลาย | พารามิเตอร์ | คำตอบที่สำเร็จ |
|-----------|---------|-------------|----------------|
| POST | `https://api.aspose.cloud/v3.0/cells/merge` | `files` (อาเรย์ของชื่อไฟล์), `target` (ชื่อสมุดงานเป้าหมาย ไม่บังคับ) | `200 OK` พร้อม JSON ที่บรรยายสมุดงานที่ผสานแล้ว |
| POST | `https://api.aspose.cloud/v3.0/cells/merge/remote` | `sourceFolder`, `pattern`, `target` | `200 OK` พร้อมข้อมูลเมตาของสมุดงานที่ผสานแล้ว |

**ตัวอย่างคำขอ cURL (ผสานรายชื่ออย่างชัดเจน)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/merge" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "files": ["Book1.xlsx", "Book2.xlsx"],
           "target": "Combined.xlsx"
         }'
```

**ตัวอย่างคำตอบ JSON**

```json
{
  "Code": 200,
  "Status": "OK",
  "MergedWorkbook": {
    "FileName": "Combined.xlsx",
    "Worksheets": 10
  }
}
```

> **ข้อกำหนดเบื้องต้น**: สมุดงานต้นทางทั้งหมดต้องจัดเก็บไว้ในตำแหน่งพื้นที่จัดเก็บคลาวด์เดียวกัน และผู้เรียกต้องมีสิทธิ์อ่าน/เขียน

## การดำเนินการแยกไฟล์

- **[แยกไฟล์ Excel ออกเป็นหลายไฟล์ตามแผ่นงาน](https://docs.aspose.cloud/cells/split-remote-spreadsheet/)**
- **[แยกไฟล์ Excel ตามกฎที่กำหนดเอง](https://docs.aspose.cloud/cells/split-spreadsheet/)**  

การแยกจะดึงแผ่นงานแต่ละแผ่น หรือกลุ่มแถว/คอลัมน์ออกเป็นไฟล์สมุดงานแยกต่างหาก

**รายละเอียดจุดปลาย**

| วิธี HTTP | จุดปลาย | พารามิเตอร์ | คำตอบที่สำเร็จ |
|-----------|---------|-------------|----------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/split` | `splitBy` (เช่น `worksheet`), `outputFolder` | `200 OK` พร้อมรายการ URL ของไฟล์ที่สร้างขึ้น |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/split/custom` | JSON ของกฎที่กำหนดเอง (ขนาดหน้า, ช่วงแถว ฯลฯ) | `200 OK` พร้อมรายละเอียดของไฟล์ที่แยกแล้ว |

**ตัวอย่างคำขอ cURL (แยกตามแผ่นงาน)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/BigReport.xlsx/split" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "splitBy": "worksheet",
           "outputFolder": "Splits/"
         }'
```

**ตัวอย่างคำตอบ JSON**

```json
{
  "Code": 200,
  "Status": "OK",
  "Splits": [
    {"FileName": "BigReport_Sheet1.xlsx", "Url": "https://storage.aspose.cloud/..."},
    {"FileName": "BigReport_Sheet2.xlsx", "Url": "https://storage.aspose.cloud/..."}
  ]
}
```

> **ข้อกำหนดเบื้องต้น**: สมุดงานต้นทางต้องเข้าถึงได้ในพื้นที่จัดเก็บของ Aspose Cloud และผู้เรียกต้องมีสิทธิ์เขียนในโฟลเดอร์ปลายทาง