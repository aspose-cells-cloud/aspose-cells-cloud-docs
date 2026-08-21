---
title: "ยกเลิกการรวมเซลล์ในช่วงข้อมูล"  
second_title: "เอกสาร"  
linktitle: "ยกเลิกการรวม"  
type: docs  
url: /ranges/unmerge/  
aliases: [/unmerge-merged-cells-of-the-range/]  
keywords: "Aspose.Cells Cloud, ยกเลิกการรวมเซลล์, Excel API, ช่วงข้อมูลในแผ่นงาน, REST API"  
description: "เรียนรู้วิธีใช้ Aspose.Cells Cloud API เพื่อยกเลิกการรวมเซลล์ที่ถูกรวมไว้ในช่วงข้อมูลเฉพาะของแผ่นงาน Excel ซึ่งรวมถึง endpoint, พารามิเตอร์, ตัวอย่าง cURL และโค้ดตัวอย่าง SDK สำหรับ C#, Java, Python และอื่นๆ อีกมากมาย"  
weight: 20  
---  

REST API นี้ใช้ยกเลิกการรวมเซลล์ที่ถูกรวมไว้ภายในช่วงข้อมูลที่ระบุบนแผ่นงาน Excel

## REST API  

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/unmerge
```  

พารามิเตอร์ของคำขอมีดังนี้:

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | จำเป็น | คำอธิบาย                                      |
|----------------|--------|----------|--------|-----------------------------------------------|
| name           | string | path     | ใช่    | ชื่อสมุดงาน                                  |
| sheetName      | string | path     | ใช่    | ชื่อแผ่นงาน                                   |
| range          | object | body     | ใช่    | อ็อบเจกต์ช่วงข้อมูลที่กำหนดเซลล์ที่จะยกเลิกการรวม |
| folder         | string | query    | ไม่ใช่ | โฟลเดอร์ที่เก็บสมุดงาน                       |
| storageName    | string | query    | ไม่ใช่ | ชื่อพื้นที่จัดเก็บ                           |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeUnmerge) กำหนด API สำหรับการใช้งานผ่านเว็บที่สามารถเข้าถึงได้โดยทั่วไป และช่วยให้คุณดำเนินการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่ง command-line เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/unmerge" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
    "ColumnCount": 7,
    "ColumnWidth": 19,
    "FirstColumn": 0,
    "FirstRow": 9,
    "Name": "string",
    "RefersTo": "string",
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

## ครอบครัว SDK บนคลาวด์  

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา โดย SDK จะจัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeUnMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeUnMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeUnMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeUnMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeUnMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeUnMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeUnMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeUnMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}