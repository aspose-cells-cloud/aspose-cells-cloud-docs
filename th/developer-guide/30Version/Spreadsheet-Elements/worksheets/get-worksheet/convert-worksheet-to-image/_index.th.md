---
title: "แปลงสมุดงานเป็น PDF, PNG, CSV และอื่นๆ – API ของ Aspose.Cells Cloud"
second_title: "เอกสาร"
linktype: "แปลงสมุดงาน"
type: docs
url: /th/worksheets/conversion/
aliases:
  - /convert-worksheet-to-image/
  - /worksheets/to-image/
keywords: "Aspose.Cells, การแปลงสมุดงาน, REST API, cURL, SDK, PDF, PNG, CSV"
description: "เรียนรู้วิธีการแปลงชีตเดียวจากสมุดงาน Excel เป็น PDF, PNG, CSV และรูปแบบอื่นๆ อีกกว่า 15 รูปแบบ โดยใช้ Aspose.Cells Cloud REST API รวมถึงตัวอย่าง cURL, ตัวอย่างโค้ด SDK และเอกสารอ้างอิงพารามิเตอร์แบบเต็ม"
weight: 130
ArticleTitle: "แปลงสมุดงานเป็น PDF, PNG, CSV และอื่นๆ – API ของ Aspose.Cells Cloud"
---

**API สำหรับแปลงสมุดงาน** – เอนด์พอยต์ `GET /cells/{name}/worksheets/{sheetName}` ใช้สำหรับแปลงชีตเดียว (แผ่นงานภายในสมุดงาน Excel) เป็นรูปแบบไฟล์อื่น

> **ข้อกำหนดเบื้องต้น:** คุณต้องมีโทเค็น JWT ที่ถูกต้อง และสมุดงานต้องถูกจัดเก็บไว้ในพื้นที่จัดเก็บของ Aspose Cloud ที่รองรับก่อนที่จะเรียกใช้เอนด์พอยต์นี้

รูปแบบที่รองรับสำหรับ **การนำเข้า** (สามารถอ่านสมุดงานได้):

- XLS, XLSX, XLSB, CSV, TSV, XLSM, ODS, TXT

รูปแบบที่รองรับสำหรับ **การส่งออกเท่านั้น** (สามารถบันทึกเป็น):

- PDF, OTS, XPS, DIF, PNG, JPEG, BMP, SVG, TIFF, EMF, NUMBERS, FODS

## API ของ REST

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat) อธิบายอินเทอร์เฟซที่เข้าถึงได้จากภายนอก

### **พารามิเตอร์ของคำขอ**

| พารามิเตอร์              | ชนิดข้อมูล | จำเป็น | ค่าเริ่มต้น | ค่าที่อนุญาต                                                          | คำอธิบาย                                         |
| ------------------------ | ---------- | ------ | ---------- | -------------------------------------------------------------------- | ------------------------------------------------ |
| **format**               | สตริง      | ใช่    | –          | pdf, png, jpeg, bmp, svg, tiff, emf, csv, txt, … (ดูรายการที่รองรับ) | รูปแบบผลลัพธ์ที่ต้องการ                          |
| **verticalResolution**   | จำนวนเต็ม  | ไม่    | 96         | 72‑600                                                              | ความละเอียดแนวตั้งสำหรับผลลัพธ์ภาพ             |
| **horizontalResolution** | จำนวนเต็ม  | ไม่    | 96         | 72‑600                                                              | ความละเอียดแนวนอนสำหรับผลลัพธ์ภาพ              |
| **password**             | สตริง      | ไม่    | –          | –                                                                   | รหัสผ่านสำหรับเปิดสมุดงานที่มีการป้องกัน        |
| **folder**               | สตริง      | ไม่    | –          | –                                                                   | โฟลเดอร์คลาวด์ที่เก็บสมุดงานต้นฉบับไว้          |
| **storage**              | สตริง      | ไม่    | –          | –                                                                   | ชื่อของพื้นที่จัดเก็บ (เช่น “Default”)          |

### การตอบกลับ

| รหัสสถานะ | คำอธิบาย                                                           | ชนิดข้อมูลที่ส่งคืน        |
| ---------- | ------------------------------------------------------------------ | -------------------------- |
| **200**    | การแปลงสำเร็จ; สตรีมไบนารีของไฟล์ที่แปลงแล้วถูกส่งคืน              | `application/octet-stream` |
| **400**    | คำขอไม่ถูกต้อง – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง                 | วัตถุข้อผิดพลาด JSON       |
| **401**    | ไม่ได้รับอนุญาต – โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                | วัตถุข้อผิดพลาด JSON       |
| **404**    | ไม่พบ – สมุดงานหรือชีตไม่มีอยู่                                   | วัตถุข้อผิดพลาด JSON       |
| **500**    | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – ความล้มเหลวที่ไม่คาดคิด             | วัตถุข้อผิดพลาด JSON       |

#### ตัวอย่างคำขอ (cURL)

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=png&verticalResolution=96&horizontalResolution=96" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### ตัวอย่างการตอบกลับ

```
ภาพที่แปลงแล้ว (สตรีมไบนารี)
```

## ครอบครัว SDK สำหรับคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นไปที่โครงการของคุณได้ กรุณาตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud แบบครบถ้วน

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}
---