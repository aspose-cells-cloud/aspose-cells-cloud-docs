---
title: "การแบ่งไฟล์เป็นชุด"
second_title: "เอกสาร"
type: docs
url: /batch/split
keywords: "การแบ่งไฟล์เป็นชุด, Aspose.Cells Cloud, REST API, Excel, PDF, CSV, JSON, สเปรดชีต, Cloud SDK"
description: "เอกสารประกอบสำหรับ API การแบ่งไฟล์เป็นชุดของ Aspose.Cells Cloud ซึ่งช่วยแบ่งไฟล์สเปรดชีตออกเป็นหลายรูปแบบ เช่น PDF, CSV หรือ JSON ประกอบด้วยรายละเอียดคำขอ ตัวอย่างคำสั่ง cURL และวิธีการใช้งาน SDK บนภาษาโปรแกรมต่างๆ"
weight: 100
---

API นี้เป็น REST API ที่ดำเนินการ **การแบ่งไฟล์เป็นชุด** สำหรับไฟล์ที่มีคุณสมบัติเหมาะสม

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/split
```

### **การรักษาความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล         | Path/Query/String/HTTPBody | คำอธิบาย                                     |
|------------------|--------------------|----------------------------|-----------------------------------------------|
| BatchSplitRequest| BatchSplitRequest  | body                       | เนื้อหาคำขอที่มีตัวเลือกการแบ่งไฟล์         |

### **คุณสมบัติของ BatchSplitRequest**

| ชื่อคุณสมบัติ   | ชนิดข้อมูล          | คำอธิบาย                                  | หมายเหตุ   |
|----------------|---------------------|-------------------------------------------|------------|
| SourceFolder   | string              | โฟลเดอร์ที่มีไฟล์ต้นทาง                   | [ไม่บังคับ] |
| SourceStorage  | string              | ชื่อพื้นที่จัดเก็บที่ไฟล์ต้นทางอยู่        | [ไม่บังคับ] |
| MatchCondition | MatchConditionRequest| เงื่อนไขที่ใช้เลือกไฟล์สำหรับการแบ่งไฟล์    | [ไม่บังคับ] |
| Format         | string              | รูปแบบเอาต์พุตที่ต้องการ (เช่น pdf, csv)   | [ไม่บังคับ] |
| FromIndex      | integer             | ดัชนีเริ่มต้นของหน้าที่จะแบ่ง              | [ไม่บังคับ] |
| ToIndex        | integer             | ดัชนีสิ้นสุดของหน้าที่จะแบ่ง               | [ไม่บังคับ] |
| OutFolder      | string              | โฟลเดอร์ปลายทางสำหรับไฟล์ที่แบ่งแล้ว       | [ไม่บังคับ] |
| SaveOptions    | SaveOptions         | ตัวเลือกเพิ่มเติมสำหรับการบันทึกผลลัพธ์     | [ไม่บังคับ] |

### **คุณสมบัติของ MatchConditionRequest**

| ชื่อคุณสมบัติ       | ชนิดข้อมูล | คำอธิบาย                                  | หมายเหตุ   |
|--------------------|------------|-------------------------------------------|------------|
| RegexPattern       | string     | รูปแบบนิพจน์ทั่วไป (Regular Expression) สำหรับจับคู่ชื่อไฟล์ | [ไม่บังคับ] |
| FullMatchConditions| string[]   | รายการเงื่อนไขการจับคู่แบบตรงกันทุกประการ | [ไม่บังคับ] |

### พารามิเตอร์ในเนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย                                      |
| -------------- | --------- | --------------------------------------------- |
| data           | file      | เนื้อหาแบบไบนารีของไฟล์สมุดงานที่ต้องการสร้าง |

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

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | เกิดขึ้นเมื่อ                             |
|------|-----------------------------|-----------------------------------------|
| 200 OK | สร้างสมุดงานเรียบร้อยแล้ว    | กรณีการทำงานปกติ                         |
| 201 Created | สร้างสมุดงานเรียบร้อยแล้ว (การตอบกลับทางเลือก) | เมื่อ API ส่งคืนสถานะสร้างเสร็จสิ้น |
| 400 Bad Request | พารามิเตอร์ไม่ถูกต้อง | ข้อผิดพลาดฝั่งไคลเอนต์                   |
| 401 Unauthorized | ไม่มีโทเคนหรือโทเคนไม่ถูกต้อง | ข้อผิดพลาดด้านการยืนยันตัวตน           |
| 409 Conflict | ไฟล์มีอยู่แล้วและ `isWriteOver=false` | ขัดแย้งกับไฟล์ที่มีอยู่แล้ว             |


## วิธีใช้ API PostBatchSplit ด้วย SDK

### ข้อมูลจำเพาะ API PostBatchSplit

[ข้อมูลจำเพาะ OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchSplit) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบเปิดเผย ช่วยให้คุณสามารถโต้ตอบกับ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์โดยใช้ cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/split" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\"}"
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

### การใช้งาน SDK ของ Aspose.Cells Cloud

การใช้งาน SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ และให้คุณมุ่งเน้นไปที่งานการแบ่งไฟล์ของคุณ โปรดดูที่ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js"  tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}