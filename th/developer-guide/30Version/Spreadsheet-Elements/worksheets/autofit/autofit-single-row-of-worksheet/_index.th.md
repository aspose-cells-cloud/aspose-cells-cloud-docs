---
title: "ปรับขนาดแถวให้พอดีในสมุดงาน Excel"
second_title: "เอกสาร"
linktitle: "แถว"
type: docs
url: /worksheets/autofit/row/
aliases: [/autofit-single-row-of-worksheet/]
description: "เรียนรู้วิธีใช้ Aspose.Cells Cloud REST API เพื่อปรับขนาดแถวให้พอดีในสมุดงาน Excel รวมถึง endpoint, พารามิเตอร์, การรับรองความถูกต้อง, การจัดการข้อผิดพลาด, คำสั่ง cURL และตัวอย่าง SDK"
keywords: "ปรับขนาดแถวให้พอดี, Aspose.Cells Cloud, Excel API, REST, สมุดงาน, SDK, สเปรดชีต, API บนคลาวด์"
weight: 30
ArticleTitle: "ปรับขนาดแถวในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud API"
---

REST API นี้ **ปรับขนาดแถวให้พอดี** ในสมุดงาน Excel

## ความปลอดภัยและการรับรองความถูกต้อง
API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ [การรับรองความถูกต้องแบบใช้โทเคน JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrow
```

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์   | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                                                                                                                                          |
| ----------------- | --------- | -------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name              | string    | path     | ชื่อไฟล์ Excel                                                                                                                                                                                    |
| sheetName         | string    | path     | ชื่อของสมุดงาน                                                                                                                                                                                    |
| rowIndex          | integer   | query    | ดัชนีเริ่มต้นด้วยศูนย์ของแถวที่ต้องการปรับขนาดให้พอดี                                                                                                                                            |
| firstColumn       | integer   | query    | ดัชนีของคอลัมน์แรกที่รวมอยู่ในการดำเนินการ                                                                                                                                                        |
| lastColumn        | integer   | query    | ดัชนีของคอลัมน์สุดท้ายที่รวมอยู่ในการดำเนินการ                                                                                                                                                   |
| autoFitterOptions | object    | body     | ออบเจกต์ที่ควบคุมพฤติกรรมการปรับขนาดให้พอดี (เช่น ควรพิจารณาเซลล์ที่ถูกผนวกหรือข้อความที่ขึ้นบรรทัดใหม่หรือไม่) ดูเพิ่มเติมที่ [AutoFitterOptions](/cells/auto-fitter-options){:rel="noopener" title="ควบคุมพฤติกรรมการปรับขนาดให้พอดี"} |
| folder            | string    | query    | โฟลเดอร์ที่เก็บไฟล์ไว้                                                                                                                                                                            |
| storageName       | string    | query    | ชื่อของพื้นที่จัดเก็บ                                                                                                                                                                             |

**ตัวอย่างเนื้อหา JSON ของ `autoFitterOptions`**

```json
{
  "IsMergedCells": true,
  "IsWrapped": false,
  "AutoFitMergedCells": true,
  "AutoFitWrappedCells": false
}
```

### นิยามของเอนทิตี

| เอนทิตี              | คำอธิบาย                                                                                  |
| -------------------- | ----------------------------------------------------------------------------------------- |
| `rowIndex`           | ดัชนีเริ่มต้นด้วยศูนย์ของแถวเป้าหมาย                                                     |
| `firstColumn`        | คอลัมน์เริ่มต้นสำหรับการดำเนินการปรับขนาดให้พอดี                                       |
| `lastColumn`         | คอลัมน์สิ้นสุดสำหรับการดำเนินการปรับขนาดให้พอดี                                        |
| `autoFitterOptions`  | การตั้งค่าแบบทางเลือกที่มีผลต่อวิธีการปรับขนาดให้พอดีของแถว (เซลล์ที่ผนวก, ข้อความที่ขึ้นบรรทัดใหม่ เป็นต้น) |

[สเปค OpenAPI](/cells/#/Worksheets/PostAutofitWorksheetRow) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้สาธารณะ และอนุญาตให้คุณดำเนินการโต้ตอบ REST โดยตรงผ่านเบราว์เซอร์เว็บ

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียก API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrow?rowIndex=2&firstColumn=1&lastColumn=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

| ฟิลด์  | คำอธิบาย                                   |
| ------ | ------------------------------------------ |
| Code   | `200` – คำขอสำเร็จ                         |
| Status | `"OK"` – ปรับขนาดแถวให้พอดีเรียบร้อยแล้ว |

{{< /tab >}}

{{< /tabs >}}

## การจัดการข้อผิดพลาด

API จะคืนค่าโค้ดสถานะ HTTP มาตรฐาน ตัวอย่างคำสั่งตอบกลับข้อผิดพลาดทั่วไปสำหรับ endpoint นี้มีดังนี้:

| โค้ด HTTP | ตัวอย่างข้อมูลโหลด (payload)                               | ความหมาย                                                                                  |
| --------- | --------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| 400       | `{ "Code": 400, "Message": "Row index out of range." }`   | ค่า `rowIndex` ที่ระบุไม่มีอยู่ในสมุดงาน                                                   |
| 401       | `{ "Code": 401, "Message": "Invalid or expired token." }` | การรับรองความถูกต้องล้มเหลว – ตรวจสอบโทเคน JWT และให้แน่ใจว่าคำขอมีการส่งผ่าน HTTPS     |
| 404       | `{ "Code": 404, "Message": "File not found." }`           | ไม่สามารถหาไฟล์ Excel หรือสมุดงานที่ระบุได้                                               |
| 500       | `{ "Code": 500, "Message": "Internal server error." }`    | เกิดปัญหาที่ไม่คาดคิดในฝั่งเซิร์ฟเวอร์                                                   |

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะซ่อนรายละเอียดระดับต่ำ ช่วยให้คุณมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณ ดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud ได้ที่ [GitHub repository](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"}

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRow.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRow.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRow.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRow.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2c4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRow.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRow.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRow.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRow.go" >}}
{{< /tab >}}

{{< /tabs >}}

**ดูเพิ่มเติม:** [ปรับขนาดคอลัมน์ให้พอดี](/worksheets/autofit/column/), [ปรับขนาดแถวให้พอดี](/worksheets/autofit/rows/), [AutoFitterOptions](/cells/auto-fitter-options).