---
title: "แปลงไฟล์ Excel แบบเป็นชุด"
second_title: "เอกสาร"
type: docs
url: /th/batch/convert
keywords: "การแปลงแบบเป็นชุด, Excel, Aspose.Cells Cloud, REST API, PDF, CSV, JSON, Markdown, สเปรดชีต"
description: "เรียนรู้วิธีใช้ API Aspose.Cells Cloud เพื่อแปลงไฟล์ Excel หลายไฟล์เป็นรูปแบบต่างๆ เช่น PDF, CSV, JSON หรือ Markdown คู่มือนี้ประกอบด้วยรายละเอียดของ REST endpoint, พารามิเตอร์คำขอ, ตัวอย่าง cURL และตัวอย่างโค้ด SDK สำหรับภาษาต่างๆ"
weight: 100
---

API REST นี้ช่วยให้สามารถ **แปลงไฟล์แบบเป็นชุด** ได้

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/convert
```

### **การรักษาความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์     | ประเภท   | ตำแหน่ง | คำอธิบาย                                         |
|----------------------|----------|----------|--------------------------------------------------|
| **batchConvertRequest** | ออบเจกต์ | body     | เนื้อหาคำขอที่มีการตั้งค่าการแปลง                 |

#### คุณสมบัติของ BatchConvertRequest

| ชื่อ          | ประเภท                | คำอธิบาย                                           | หมายเหตุ |
|---------------|-----------------------|----------------------------------------------------|----------|
| **SourceFolder** | สตริง              | เส้นทางของโฟลเดอร์ที่มีไฟล์ Excel ต้นทาง         | [ไม่บังคับ] |
| **MatchCondition** | MatchConditionRequest | เงื่อนไขที่ใช้ในการเลือกไฟล์ที่จะแปลง           | [ไม่บังคับ] |
| **Format**        | สตริง              | รูปแบบเป้าหมายสำหรับการแปลง (เช่น `pdf`, `csv`) | [ไม่บังคับ] |
| **OutFolder**     | สตริง              | โฟลเดอร์ปลายทางที่จะบันทึกไฟล์ที่แปลงแล้ว       | [ไม่บังคับ] |
| **SaveOptions**   | SaveOptions         | ตัวเลือกเพิ่มเติมที่ควบคุมวิธีการบันทึกไฟล์       | [ไม่บังคับ] |

#### คุณสมบัติของ MatchConditionRequest

| ชื่อ               | ประเภท      | คำอธิบาย                                         | หมายเหตุ |
|--------------------|-------------|--------------------------------------------------|----------|
| **RegexPattern**   | สตริง        | นิพจน์ทั่วไปที่ใช้กรองชื่อไฟล์                  | [ไม่บังคับ] |
| **FullMatchConditions** | สตริง[] | รายการเงื่อนไขชื่อไฟล์แบบตรงกันทั้งหมดสำหรับการจับคู่ | [ไม่บังคับ] |


### พารามิเตอร์เนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย                                  |
| ---------------- | ------ | ------------------------------------------ |
| data             | ไฟล์   | เนื้อหาไบนารีของไฟล์สมุดงานที่ต้องการสร้าง |

### **การตอบกลับ**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | เกิดขึ้นเมื่อ                             |
|------|-------------------------------|------------------------------------------|
| 200 OK | สร้างสมุดงานเรียบร้อยแล้ว | กรณีการทำงานปกติ                         |
| 201 Created | สร้างสมุดงานแล้ว (การตอบกลับทางเลือก) | เมื่อ API คืนค่าสถานะสร้างแล้ว |
| 400 Bad Request | พารามิเตอร์ไม่ถูกต้อง | ข้อผิดพลาดฝั่งไคลเอนต์                   |
| 401 Unauthorized | ไม่มีหรือโทเค็นไม่ถูกต้อง | ข้อผิดพลาดด้านการยืนยันตัวตน          |
| 409 Conflict | ไฟล์มีอยู่แล้วและ `isWriteOver=false` | ขัดแย้งกับไฟล์ที่มีอยู่แล้ว          

## วิธีใช้ API PostBatchConvert ด้วย SDK

### ข้อมูลจำเพาะ API PostBatchConvert

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/PostBatchConvert) กำหนด API ที่สามารถเข้าถึงได้จากภายนอก และช่วยให้คุณดำเนินการ REST interaction โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/convert" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\",\"SaveOptions\":{\"SaveFormat\":\"pdf\",\"CalculateFormula\":true,\"EnableHTTPCompression\":true,\"OnePagePerSheet\":true,\"CreateDirectory\":false,\"Compliance\":\"None\"}}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ และช่วยให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ [repository บน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Batch-Convet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Batch-Convet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-Batch-Convet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Batch-Convet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Batch-Convet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Batch-Convet.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Batch-Convet.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d763dc80b0aff6275403dc1d82ad59a5" "Examples-Batch-Convet.go" >}}

{{< /tab >}}

{{< /tabs >}}
---