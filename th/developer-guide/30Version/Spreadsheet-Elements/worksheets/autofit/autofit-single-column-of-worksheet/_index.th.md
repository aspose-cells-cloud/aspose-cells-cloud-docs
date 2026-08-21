---
title: "การปรับคอลัมน์ให้พอดีใน Excel ด้วย Aspose.Cells Cloud API – คู่มืออย่างย่อ"
second_title: "เอกสาร"
linktitle: "คอลัมน์"
type: docs
url: /th/worksheets/autofit/column/
aliases: [  /th/autofit-single-column-of-worksheet/ ]
keywords: "Aspose.Cells Cloud, autofit column, Excel API, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "เรียนรู้วิธีปรับขนาดคอลัมน์ (หรือช่วงคอลัมน์) ในแผ่นงาน Excel โดยอัตโนมัติด้วย Aspose.Cells Cloud REST API พร้อมตัวอย่าง cURL และ SDK (C#, Java, Python เป็นต้น) รวมรายละเอียดคำขอ/คำตอบแบบเต็มรูปแบบ"
weight: 10
---

บริการ REST API นี้ปรับความกว้างของคอลัมน์เดียวหรือช่วงคอลัมน์ที่อยู่ติดกันในแผ่นงาน Excel โดยอัตโนมัติ

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
| ----------------- | ------- | -------- | ------------------------------------------------------------------------------------------------ |
| name              | string  | path     | ชื่อไฟล์ Excel |
| sheetName         | string  | path     | ชื่อแผ่นงาน |
| firstColumn       | integer | query    | ดัชนีเริ่มต้นที่ 0 ของคอลัมน์แรกที่ต้องการปรับให้พอดี |
| lastColumn        | integer | query    | ดัชนีเริ่มต้นที่ 0 ของคอลัมน์สุดท้ายที่ต้องการปรับให้พอดี |
| autoFitterOptions | object  | body     | ตัวเลือกที่ควบคุมพฤติกรรมการปรับให้พอดี (ดูที่ [AutoFitterOptions](/cells/auto-filter-options)) |
| firstRow          | integer | query    | ดัชนีเริ่มต้นที่ 0 ของแถวแรกที่พิจารณาเมื่อคำนวณความกว้างคอลัมน์ |
| lastRow           | integer | query    | ดัชนีเริ่มต้นที่ 0 ของแถวสุดท้ายที่พิจารณาเมื่อคำนวณความกว้างคอลัมน์ |
| folder            | string  | query    | โฟลเดอร์ในพื้นที่จัดเก็บที่ไฟล์ตั้งอยู่ |
| storageName       | string  | query    | ชื่อของบริการพื้นที่จัดเก็บ |

### การตอบกลับข้อผิดพลาด

| สถานะ HTTP | ความหมาย | ตัวอย่าง JSON body |
| ----------- | ------------------------------------------- | ----------------------------------------------------------- |
| 400         | พารามิเตอร์ไม่ถูกต้อง | `{"Code":400,"Message":"Invalid parameter 'firstColumn'."}` |
| 401         | ไม่ได้รับอนุญาต – ไม่มีหรือโทเคน JWT ไม่ถูกต้อง | `{"Code":401,"Message":"Authorization failed."}` |
| 404         | ไม่พบไฟล์หรือแผ่นงาน | `{"Code":404,"Message":"Worksheet 'Sheet1' not found."}` |
| 500         | ข้อผิดพลาดภายในเซิร์ฟเวอร์ | `{"Code":500,"Message":"An unexpected error occurred."}` |

[สเปค OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการโต้ตอบกับ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเรียกใช้บริการ Aspose.Cells Cloud ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้จุดปลายทาง autofit-column

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?firstColumn=2&lastColumn=2" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": true}'
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

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการผนวก API เข้ากับแอปพลิเคชันของคุณ SDK จะจัดการรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจได้ ดูที่ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้จุดปลายทาง autofit-column ด้วย SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

---