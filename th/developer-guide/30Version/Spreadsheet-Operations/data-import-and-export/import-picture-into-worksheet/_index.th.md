---
title: "นำรูปภาพเข้าสู่แผ่นงาน Excel"
ArticleTitle: "นำรูปภาพเข้าสู่แผ่นงาน Excel – คู่มือ API ของ Aspose.Cells Cloud"
second_title: "เอกสาร"
linktitle: "นำรูปภาพเข้า"
type: docs
url: /import-picture-into-excel-worksheet/
aliases:
  - /import-picture-into-worksheet/
  - /import-data/picture/
  - /import/picture/
keywords: "นำรูปภาพเข้า, Excel, Aspose.Cells Cloud, REST API, v3.0"
description: "เรียนรู้วิธีการนำรูปภาพเข้าสู่แผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API v3.0 รวมตัวอย่างคำขอแบบมัลติพาร์ต ตัวอย่างโค้ด SDK และคำแนะนำการจัดการข้อผิดพลาด เริ่มต้นใช้งานได้อย่างรวดเร็วด้วยขั้นตอนที่ชัดเจน"
weight: 19
---

การนำรูปภาพเข้าสู่แผ่นงาน Excel ช่วยให้คุณเพิ่มเนื้อหาภาพ เช่น โลโก้ แผนภูมิ หรือไดอะแกรม เพื่อเสริมความสมบูรณ์ให้กับสมุดคำนวณ คู่มือนี้แสดงวิธีใช้การดำเนินการ **ImportPicture** ของ Aspose.Cells Cloud รูปแบบคำขอที่จำเป็น และวิธีจัดการกับการตอบกลับ

**ข้อกำหนดเบื้องต้น:** คุณต้องมีโทเค็น JWT สำหรับการยืนยันตัวตนที่ถูกต้อง และมีสมุดงานที่จัดเก็บไว้ใน Aspose Cloud Storage ก่อนเรียกใช้การดำเนินการนำเข้า

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### **พารามิเตอร์ของคำขอ**

คำขอเป็น HTTP **POST** ที่มีเนื้อหาแบบ **multipart/related** (ดูที่ [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) หรือ [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html))

- **ส่วนแรก** ประกอบด้วยออบเจกต์ JSON ชื่อ **ImportPictureOption** ซึ่งอธิบายตำแหน่งและวิธีการวางรูปภาพ
- **ส่วนที่สอง** นำส่งไฟล์รูปภาพ (หรือข้อมูลที่เข้ารหัส Base64 ของรูปภาพ)

### ImportPictureOption – คำนิยาม

```json
{
  "UpperLeftRow": 0,
  "UpperLeftColumn": 0,
  "LowerRightRow": 10,
  "LowerRightColumn": 5,
  "Filename": "logo.png",
  "Data": "iVBORw0KGgoAAAANSUhEUgAA...",
  "DestinationWorksheet": "Sheet1",
  "IsInsert": true,
  "ImportDataType": "Picture",
  "Source": { "FileSource": "Storage" }
}
```

_`IsInsert` เป็น **boolean** – `true` หมายถึงการแทรกรูปภาพใหม่ `false` หมายถึงการแทนที่รูปภาพที่มีอยู่_

### พารามิเตอร์สำคัญ

**ImportPictureOption**

| ชื่อพารามิเตอร์     | ชนิดข้อมูล | คำอธิบาย                                                                                                                                                               |
| ------------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| UpperLeftRow        | int        | ดัชนีแถวของมุมบนซ้ายที่จะวางรูปภาพ                                                                                                                                    |
| UpperLeftColumn     | int        | ดัชนีคอลัมน์ของมุมบนซ้ายที่จะวางรูปภาพ                                                                                                                               |
| LowerRightRow       | int        | ดัชนีแถวของมุมล่างขวาที่กำหนดขอบเขตของรูปภาพ                                                                                                                        |
| LowerRightColumn    | int        | ดัชนีคอลัมน์ของมุมล่างขวาที่กำหนดขอบเขตของรูปภาพ                                                                                                                   |
| Filename            | string     | ชื่อไฟล์รูปภาพ                                                                                                                                                         |
| Data                | string     | ข้อมูลไบนารีของรูปภาพที่เข้ารหัสแบบ Base64 (ไม่บังคับหากส่งไฟล์เป็นส่วนที่สอง)                                                                                        |
| DestinationWorksheet| string     | ชื่อของแผ่นงานที่จะแทรกรูปภาพ                                                                                                                                         |
| **IsInsert**        | **boolean**| `true` สำหรับการแทรกรูปภาพใหม่ `false` สำหรับการแทนที่รูปภาพที่มีอยู่                                                                                                |
| ImportDataType      | string     | ประเภทของข้อมูลที่นำเข้า (เช่น `Picture`, `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`) |
| Source              | FileSource | ระบุตำแหน่งของไฟล์ข้อมูลเมื่อพารามิเตอร์ `BatchData` เป็นค่าว่าง                                                                                                       |

### การตอบกลับ

คำขอที่ประสบความสำเร็จจะส่งกลับ **HTTP 200** พร้อมข้อมูล JSON ที่มีลักษณะดังนี้:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

รหัสสถานะที่เป็นไปได้:

| รหัส | ความหมาย                                            |
| ---- | ---------------------------------------------------- |
| 200  | การนำเข้าสำเร็จ                                      |
| 400  | คำขอไม่ถูกต้อง – ข้อมูลขาดหายหรือไม่ถูกต้อง        |
| 401  | ไม่มีสิทธิ์ – โทเค็นไม่ถูกต้องหรือขาดหาย            |
| 500  | ข้อผิดพลาดภายในของเซิร์ฟเวอร์                         |


## วิธีใช้ API PostImportData ด้วย SDK

### ข้อมูลจำเพาะของ API PostImportData

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้สาธารณะ และช่วยให้คุณสามารถดำเนินการโต้ตอบ REST ได้โดยตรงจากเบราว์เซอร์เว็บ

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ ให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud แบบครบถ้วน

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บ Aspose.Cells โดยใช้ SDK ต่างๆ:

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