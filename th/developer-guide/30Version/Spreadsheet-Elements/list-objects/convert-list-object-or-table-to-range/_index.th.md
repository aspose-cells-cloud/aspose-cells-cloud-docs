---
title: "แปลง List Object ให้เป็น Range – Aspose.Cells Cloud API"
ArticleTitle: "แปลง List Object ให้เป็น Range โดยใช้ Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktitle: "การแปลง"
type: docs
url: /th/list-objects/to-range/
aliases:
  - /convert-list-object-or-table-to-range/
  - /tables/to-range/
keywords: "Aspose Cells API, แปลง list object ให้เป็น range, Excel REST API"
description: "เรียนรู้วิธีการแปลง ListObject (ตาราง) ใน Excel ให้เป็น Range โดยใช้ Aspose.Cells Cloud REST API รวมถึงไวยากรณ์คำขอ พารามิเตอร์ ตัวอย่าง cURL โครงสร้างคำตอบ รายละเอียดการยืนยันตัวตน รหัสข้อผิดพลาด และตัวอย่าง SDK"
weight: 30
---

REST API นี้แปลง **ListObject (ตาราง)** ให้เป็น **Range** ภายในแผ่นงาน Excel

**ข้อกำหนดเบื้องต้น:**  
ก่อนเรียกใช้จุดปลายทาง (endpoint) ให้แน่ใจว่าสมุดงานถูกอัปโหลดลงในที่เก็บข้อมูล Aspose Cloud ของคุณ แผ่นงานมี ListObject เป้าหมาย และคุณกำลังใช้รูปแบบไฟล์ที่รองรับ (เช่น .xlsx, .xlsm)

## REST API

**การยืนยันตัวตน**  
ในการเรียกใช้การดำเนินการนี้ คุณต้องใส่โทเค็น JWT ที่ถูกต้องในส่วนหัว `Authorization` รับโทเค็นโดยส่งคำขอ POST ไปยังจุดปลายทาง OAuth 2.0 ด้วย client ID และ client secret ของคุณ โทเค็นต้องมีขอบเขต `Cells.ReadWrite` และมีผลใช้งานตามระยะเวลาที่บริการโทเค็นกำหนด

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/ConvertToRange
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### พารามิเตอร์คำขอ

| ชื่อ                | ชนิดข้อมูล | ตำแหน่ง | จำเป็น | ค่าเริ่มต้น | คำอธิบาย                                                 |
| ------------------- | --------- | -------- | ------ | ---------- | --------------------------------------------------------- |
| **name**            | สตริง      | path     | ใช่    | –          | ชื่อไฟล์ Excel                                             |
| **sheetName**       | สตริง      | path     | ใช่    | –          | ชื่อแผ่นงานที่มี ListObject                                               |
| **listObjectIndex** | จำนวนเต็ม  | path     | ใช่    | –          | ดัชนีแบบเริ่มต้นที่ 0 ของ ListObject (ตาราง) ที่จะแปลง         |
| **folder**          | สตริง      | query    | ไม่บังคับ | –          | เส้นทางโฟลเดอร์ที่เก็บไฟล์                                        |
| **storageName**     | สตริง      | query    | ไม่บังคับ | –          | ชื่อบริการที่เก็บข้อมูล                                           |

> **หมายเหตุ:** การดำเนินการนี้ใช้ได้กับรูปแบบ Excel สมัยใหม่เท่านั้น เช่น **.xlsx** และ **.xlsm** ListObject ต้องไม่ได้รับการป้องกัน สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ ListObjects โปรดดูที่ [ภาพรวม ListObjects](/list-objects/) สำหรับรายละเอียดเกี่ยวกับการใช้งาน Range โปรดดูที่ [เอกสาร Range](/ranges/)

### ตัวอย่าง cURL (คำขอ)

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="คำตอบ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0/ConvertToRange" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>"
```

{{< /tab >}}

#### โครงสร้างคำตอบ

API จะส่งคำตอบ **200 OK** พร้อมรายละเอียดของ range ที่สร้างใหม่

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

| ฟิลด์           | ชนิดข้อมูล | คำอธิบาย                                         |
| --------------- | --------- | ------------------------------------------------- |
| **Code**        | จำนวนเต็ม  | รหัสสถานะแบบ HTTP (200 หมายถึงสำเร็จ)             |
| **Status**      | สตริง       | ข้อความสถานะในรูปแบบข้อความ                           |
| **RangeName**   | สตริง       | ชื่อที่กำหนดให้กับ range ที่สร้างขึ้น                    |
| **Address**     | สตริง       | ที่อยู่เต็มของ range รวมถึงชื่อแผ่นงาน                    |
| **FirstRow**    | จำนวนเต็ม   | ดัชนีแบบเริ่มต้นที่ 0 ของแถวแรกใน range                  |
| **FirstColumn** | จำนวนเต็ม   | ดัชนีแบบเริ่มต้นที่ 0 ของคอลัมน์แรกใน range               |
| **RowCount**    | จำนวนเต็ม   | จำนวนแถวใน range                                 |
| **ColumnCount** | จำนวนเต็ม   | จำนวนคอลัมน์ใน range                               |

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                    | คำอธิบาย                                           |
|-----|----------------------------|---------------------------------------------------|
| 200 | OK                         | ใช้ตัวกรองเรียบร้อยแล้ว; คำตอบประกอบด้วยรายละเอียดของการดำเนินการ |
| 400 | Bad Request                | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น รูปแบบไฟล์ที่ไม่รองรับ)    |
| 401 | Unauthorized               | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                             |
| 413 | Payload Too Large          | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                             |
| 500 | Internal Server Error      | ข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์                           |

**โครงสร้างคำตอบข้อผิดพลาด (ตัวอย่าง):**

```json
{
  "Code": 400,
  "Message": "listObjectIndex ไม่ถูกต้อง ดัชนีต้องอยู่ระหว่าง 0 ถึง 5"
}
```

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK สำหรับคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จัดการรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบที่ [คลังข้อมูล GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectConvertToRange.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectConvertToRange.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectConvertToRange.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectConvertToRange.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectConvertToRange.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectConvertToRange.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectConvertToRange.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectConvertToRange.go" >}}

{{< /tab >}}

{{< /tabs >}}