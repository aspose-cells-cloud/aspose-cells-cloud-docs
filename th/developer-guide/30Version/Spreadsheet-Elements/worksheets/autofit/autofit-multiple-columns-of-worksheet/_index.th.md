---
title: "ปรับขนาดคอลัมน์หลายคอลัมน์ในสมุดงาน Excel"
second_title: "เอกสาร"
linktitle: "คอลัมน์"
type: docs
url: /th/worksheets/autofit/columns/
aliases: [  /th/autofit-multiple-columns-of-worksheet/ ]
keywords: "Aspose.Cells, ปรับขนาดคอลัมน์, Excel API, สเปรดชีตบนคลาวด์, REST"
description: "เรียนรู้วิธีการปรับขนาดคอลัมน์หลายคอลัมน์ในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API (เวอร์ชัน 3.0) ซึ่งรวมถึง endpoint, พารามิเตอร์, ตัวอย่าง cURL, การจัดการข้อผิดพลาด และตัวอย่างโค้ด SDK สำหรับ C#, Java, Python และอื่นๆ"
weight: 20
---

บริการ REST API นี้จะปรับขนาด **คอลัมน์หลายคอลัมน์** ในสมุดงาน Excel

## API ผ่าน REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์      | ประเภท    | ตำแหน่ง | คำอธิบาย                                                                                                                                 |
| ------------------- | ------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| name                | string  | path     | ชื่อไฟล์                                                                                                                              |
| sheetName           | string  | path     | ชื่อworksheet                                                                                                                         |
| firstColumn         | integer | query    | ดัชนีคอลัมน์เริ่มต้น                                                                                                                     |
| lastColumn          | integer | query    | ดัชนีคอลัมน์สิ้นสุด                                                                                                                       |
| autoFitterOptions\* | object  | body     | ตัวเลือก AutoFitter (ดูที่[ตัวเลือก Auto Fitter](/cells/auto-fitter-options/)) ซึ่งประกอบด้วย `AutoFitMergedCells`, `IgnoreHidden` และ `OnlyAuto` |
| firstRow            | integer | query    | ดัชนีแถวเริ่มต้นสำหรับการปรับขนาด (**ไม่บังคับ**)                                                                                             |
| lastRow             | integer | query    | ดัชนีแถวสิ้นสุดสำหรับการปรับขนาด (**ไม่บังคับ**)                                                                                               |
| folder              | string  | query    | เส้นทางโฟลเดอร์ใน storage (**ไม่บังคับ**)                                                                                                      |
| storageName         | string  | query    | ชื่อ storage (**ไม่บังคับ**)                                                                                                                |

\*ชื่อพารามิเตอร์แสดงเป็นลิงก์ไปยังเอกสารที่เกี่ยวข้อง

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่าน command-line เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?lastColumn=5&firstColumn=0" \
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

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโปรเจกต์ของคุณ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

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