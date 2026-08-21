---
title: "ย้ายช่วงที่ตั้งชื่อด้วยสมุดงาน Excel"
second_title: "เอกสาร"
linktitle: "ย้าย"
type: docs
url: /th/ranges/move/
aliases: [  /th/move-a-named-range-with-an-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, ย้ายช่วงที่ตั้งชื่อ, สมุดงาน Excel, REST API, ย้ายช่วง, ตัวอย่าง SDK"
description: "เรียนรู้วิธีย้ายช่วงที่ตั้งชื่อภายในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API เวอร์ชัน 3.0 พร้อมรายละเอียดปลายทาง (endpoint), การยืนยันตัวตน, ตัวอย่าง และโค้ดตัวอย่าง SDK"
weight: 20
ArticleTitle: "ย้ายช่วงที่ตั้งชื่อด้วยสมุดงาน Excel โดยใช้ Aspose.Cells Cloud API"
---

การย้ายช่วงที่ตั้งชื่อเป็นงานที่พบได้บ่อยเมื่อคุณต้องการจัดระเบียบข้อมูลใหม่ด้วยการเขียนโปรแกรม ส่วนนี้อธิบายวิธีย้ายช่วงที่กำหนดไว้ไปยังตำแหน่งใหม่ในเวิร์กชีตเดียวกันโดยใช้ Aspose.Cells Cloud REST API

REST API นี้จะย้ายช่วงที่ระบุไปยังช่วงปลายทางบนสมุดงาน Excel

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/moveto
```

### การยืนยันตัวตน (Authentication)
API นี้ต้องการ **โทเค็น JWT Bearer** ที่ได้มาจากการดำเนินการ OAuth ของ Aspose Cloud โดยใส่โทเค็นนี้ในส่วนหัว (header) `Authorization` ดังนี้:

```
Authorization: Bearer <jwt token>
```

โทเค็นนี้ต้องมีขอบเขต (scope) **Cells**

### ข้อกำหนดเบื้องต้น
- ต้องจัดเก็บสมุดงานไว้ในพื้นที่จัดเก็บของ Aspose Cloud  
- หากไฟล์ไม่อยู่ในไดเรกทอรีราก ให้ระบุชื่อพื้นที่จัดเก็บ (`storageName`) และเส้นทางโฟลเดอร์ (`folder`)  
- ใช้ SDK เวอร์ชันล่าสุดของ Aspose.Cells Cloud ที่รองรับ API เวอร์ชัน **v3.0**

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud API มีความปลอดภัยและต้องใช้การยืนยันตัวตนแบบใช้โทเค็น JWT ดูรายละเอียดเพิ่มเติมได้ที่ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนคำร้อง REST API</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย |
|----------------|--------|----------|-------------|
| **name**       | string | path     | ชื่อไฟล์สมุดงาน |
| **sheetName**  | string | path     | ชื่อเวิร์กชีต |
| **destRow**    | integer| query    | ดัชนีแถวเริ่มต้นของช่วงปลายทาง (เริ่มที่ 0) |
| **destColumn**| integer| query    | ดัชนีคอลัมน์เริ่มต้นของช่วงปลายทาง (เริ่มที่ 0) |
| **range**      | object | body     | คำนิยามของช่วงต้นทางที่จะย้าย |
| **folder**     | string | query    | เส้นทางโฟลเดอร์ที่จัดเก็บสมุดงานไว้ |
| **storageName**| string | query    | ชื่อของพื้นที่จัดเก็บ Aspose Cloud |

### เนื้อหาคำขอ (Request Body)

| ฟิลด์          | ประเภท   | จำเป็น | คำอธิบาย |
|----------------|--------|----------|-------------|
| **ColumnCount**| integer| ไม่จำเป็น | จำนวนคอลัมน์ในช่วงต้นทาง |
| **ColumnWidth**| integer| ไม่จำเป็น | ความกว้างของแต่ละคอลัมน์ (หน่วย: จุด) |
| **FirstColumn**| integer| ไม่จำเป็น | ดัชนีคอลัมน์แรกของช่วงต้นทาง (เริ่มที่ 0) |
| **FirstRow**   | integer| ไม่จำเป็น | ดัชนีแถวแรกของช่วงต้นทาง (เริ่มที่ 0) |
| **Name**       | string | ไม่จำเป็น | ชื่อของช่วง (หากเป็นช่วงที่ตั้งชื่อ) |
| **RefersTo**   | string | ไม่จำเป็น | การอ้างอิงรูปแบบ A1 ที่กำหนดช่วง |
| **RowCount**   | integer| ไม่จำเป็น | จำนวนแถวในช่วงต้นทาง |
| **RowHeight**  | integer| ไม่จำเป็น | ความสูงของแต่ละแถว (หน่วย: จุด) |
| **Worksheet**  | string | ไม่จำเป็น | เวิร์กชีตที่มีช่วงต้นทาง |

### ขั้นตอนการทำงาน

1. **อัปโหลด** สมุดงานไปยังพื้นที่จัดเก็บของ Aspose Cloud (หากยังไม่มีอยู่)  
2. **สร้าง** โทเค็น JWT โดยใช้ปลายทาง OAuth  
3. **สร้าง** พาเลย์โหลด JSON ที่อธิบายช่วงต้นทาง  
4. **เรียก** ปลายทาง `moveto` โดยระบุพารามิเตอร์ path, query และเนื้อหา JSON  
5. **ตรวจสอบ** การตอบกลับ; การเรียกที่สำเร็จจะส่งกลับสถานะ `200 OK`

### ตัวอย่างคำขอ / การตอบกลับ

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/moveto?destRow=20&destColumn=20" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{ 
  "ColumnCount": 7,
  "ColumnWidth": 19,
  "FirstColumn": 0,
  "FirstRow": 9,
  "Name": "MyRange",
  "RefersTo": "A10:G10",
  "RowCount": 1,
  "RowHeight": 15,
  "Worksheet": "Sheet1"
}'
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

เมื่อเกิดข้อผิดพลาด การตอบกลับจะประกอบด้วยฟิลด์ `ErrorMessage` ซึ่งเป็นทางเลือกที่ให้รายละเอียดเพิ่มเติมเกี่ยวกับข้อผิดพลาด

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | คำอธิบาย                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                          | ใช้ตัวกรองสำเร็จ; การตอบกลับมีรายละเอียดของคำสั่งดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request)                 | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)                | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | เนื้อหาคำขอใหญ่เกินไป (Payload Too Large)           | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error)       | ข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์ |

**โครงสร้างการตอบกลับ**

| ฟิลด์ | ประเภท   | คำอธิบาย |
|-------|--------|-------------|
| **Code** | integer | รหัสสถานะแบบ HTTP ที่ API ส่งกลับ (เช่น 200) |
| **Status** | string | คำอธิบายข้อความของผลลัพธ์ (เช่น "OK") |
| **ErrorMessage** | string (ทางเลือก) | รายละเอียดข้อผิดพลาดที่อ่านเข้าใจได้เมื่อการเรียกล้มเหลว |

## ครอบครัว SDK สำหรับคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นไปที่งานของโปรเจกต์ได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บ GitHub</a> เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMoveTo.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMoveTo.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMoveTo.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMoveTo.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMoveTo.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMoveTo.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMoveTo.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMoveTo.go" >}}

{{< /tab >}}

{{< /tabs >}}