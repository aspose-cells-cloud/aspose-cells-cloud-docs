---
title: "การเปลี่ยนชื่อแผ่นงาน Excel"
second_title: "เอกสาร"
linktype: "เปลี่ยนชื่อ"
type: docs
url: /th/worksheets/rename/
aliases: [  /th/rename-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, การเปลี่ยนชื่อแผ่นงาน Excel, REST API, ชุดพัฒนาซอฟต์แวร์สเปรดชีต, เปลี่ยนชื่อแผ่นงาน, พื้นที่จัดเก็บบนคลาวด์"
description: "เปลี่ยนชื่อแผ่นงานในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API มีชุดพัฒนาซอฟต์แวร์ (SDK) ให้ใช้งานสำหรับ Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby และ Swift"
weight: 20
---

REST API นี้ใช้ในการเปลี่ยนชื่อแผ่นงานในสมุดงาน Excel

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/rename
```

### **พารามิเตอร์ของคำขอ**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                      |
| ---------------- | -------- | -------- | --------------------------------------------- |
| name             | string   | path     | ชื่อของไฟล์ Excel                             |
| sheetName        | string   | path     | ชื่อปัจจุบันของแผ่นงานที่ต้องการเปลี่ยนชื่อ   |
| newname          | string   | query    | ชื่อใหม่ที่ต้องการตั้งให้กับแผ่นงาน           |
| folder           | string   | query    | พาธของโฟลเดอร์ในพื้นที่จัดเก็บ (ไม่บังคับ)     |
| storageName      | string   | query    | ชื่อของพื้นที่จัดเก็บ (ไม่บังคับ)              |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostRenameWorksheet) กำหนด API สำหรับการเข้าถึงแบบเปิดเผยซึ่งช่วยให้คุณสามารถสื่อสารผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="คำตอบ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/rename?newname=newSheet" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
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

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับล่างให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่าง ๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostRenameWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-RenameWorksheet-rename-excel-worksheeet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostRenameWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-rename_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "RenameExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-RenameWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-RenameWorksheet-rename-excel-worksheeet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-RenameWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "accf2723cfaa2a328d3dea355156e4d9" >}}

{{< /tab >}}

{{< /tabs >}}