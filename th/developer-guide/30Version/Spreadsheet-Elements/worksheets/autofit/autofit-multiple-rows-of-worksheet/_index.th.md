---
title: "ปรับขนาดอัตโนมัติสำหรับหลายแถวในสมุดงาน Excel"
second_title: "เอกสาร"
linktype: "แถว"
type: docs
url: /th/worksheets/autofit/rows/
aliases: [  /th/autofit-multiple-rows-of-worksheet/ ]
keywords: "ปรับขนาดอัตโนมัติแถว, Excel, Aspose.Cells Cloud, REST API, สมุดงาน, สเปรดชีต"
description: "เรียนรู้วิธีใช้ Aspose.Cells Cloud REST API เพื่อปรับขนาดอัตโนมัติหลายแถวในสมุดงาน Excel ประกอบด้วยไวยากรณ์คำขอ พารามิเตอร์ ตัวอย่าง cURL โค้ดตัวอย่าง SDK และการจัดการข้อผิดพลาด"
weight: 40
ArticleTitle: "ปรับขนาดอัตโนมัติหลายแถวในสมุดงาน Excel – เอกสารประกอบ API ของ Aspose.Cells Cloud"
---

REST API นี้จะปรับความสูงของแถวต่างๆ ในสมุดงาน Excel โดยอัตโนมัติ

## ความปลอดภัยและการยืนยันตัวตน
Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ [การยืนยันตัวตนด้วย JWT token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrows
```

### **พารามิเตอร์ของคำขอ**

| ชื่อพารามิเตอร์      | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                                                                         | จำเป็น |
| --------------------- | --------- | -------- | -------------------------------------------------------------------------------------------------------------------------------- | ------ |
| **name**              | string    | path     | ชื่อไฟล์ Excel                                                                                                                   | ✔      |
| **sheetName**         | string    | path     | ชื่อของสมุดงาน                                                                                                                   | ✔      |
| **autoFitterOptions** | object    | body     | ตัวเลือกที่ควบคุมวิธีการปรับขนาดอัตโนมัติของแถว (เช่น ไม่สนใจแถวที่ซ่อนอยู่) ดูรายละเอียดฟิลด์สั้นๆ ด้านล่าง                    | ✖      |
| **startRow**          | integer   | query    | แถวแรกที่จะปรับขนาดอัตโนมัติ (ดัชนีเริ่มต้นที่ 1)                                                                              | ✔      |
| **endRow**            | integer   | query    | แถวสุดท้ายที่จะปรับขนาดอัตโนมัติ (รวม)                                                                                          | ✔      |
| **onlyAuto**          | boolean   | query    | เมื่อตั้งค่าเป็น `true` API จะปรับขนาดเฉพาะแถวที่มีความสูงถูกคำนวณอัตโนมัติโดย Excel เท่านั้น เมื่อตั้งค่าเป็น `false` จะปรับขนาดทั้งหมด | ✖      |
| **folder**            | string    | query    | โฟลเดอร์ที่เก็บเอกสาร                                                                                                             | ✖      |
| **storageName**       | string    | query    | ชื่อของบริการจัดเก็บข้อมูล                                                                                                       | ✖      |

ฟิลด์ของ **autoFitterOptions** (ทั้งหมดเป็นทางเลือก):

- `AutoFitMergedCells` _(boolean)_ – เมื่อตั้งค่าเป็น `true` จะพิจารณาเซลล์ที่ถูกรวมไว้ด้วยเมื่อคำนวณความสูงของแถว
- `IgnoreHidden` _(boolean)_ – เมื่อตั้งค่าเป็น `true` จะไม่พิจารณาแถวที่ถูกซ่อนไว้ระหว่างกระบวนการปรับขนาดอัตโนมัติ
- `OnlyAuto` _(boolean)_ – สะท้อนค่าพารามิเตอร์ `onlyAuto` จาก query; เมื่อกำหนดค่าแล้ว จะแทนที่ค่าจาก query

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetRows) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และอนุญาตให้คุณดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งใน command-line เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrows?startRow=1&endRow=7" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": false}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

การตอบกลับข้อผิดพลาดทั่วไปประกอบด้วย:

- **400 Bad Request** – ค่าพารามิเตอร์ไม่ถูกต้องหรือ JSON body ผิดรูปแบบ
- **401 Unauthorized** – JWT token หายไปหรือไม่ถูกต้อง
- **404 Not Found** – ไฟล์หรือสมุดงานที่ระบุไม่มีอยู่
- **500 Internal Server Error** – เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย                                            |
|-----|-----------------------------|-----------------------------------------------------|
| 200 | OK                          | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของ operation |
| 400 | Bad Request                 | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401 | Unauthorized                | JWT token ไม่ถูกต้องหรือหายไป                        |
| 413 | Payload Too Large           | ไฟล์ที่อัปโหลดเกินขีดจำกัดขนาด                         |
| 500 | Internal Server Error       | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์               |

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณจึงสามารถมุ่งเน้นไปที่โครงการของคุณได้ โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}
---