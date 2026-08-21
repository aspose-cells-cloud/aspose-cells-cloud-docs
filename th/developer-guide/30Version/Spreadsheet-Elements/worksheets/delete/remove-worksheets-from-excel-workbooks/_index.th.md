---
title: "ลบวORKSHEET"
second_title: "Document"
linktype: "หนึ่งworksheet"
type: docs
url: /worksheets/delete-worksheet/
aliases: [/remove-worksheets-from-excel-workbooks/]
keywords: "Aspose.Cells Cloud, Delete Worksheet, Excel, Spreadsheet, REST API"
description: "ลบworksheet จากสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API รองรับ SDK สำหรับ C#, Java, PHP, Ruby, Node.js, Python, Perl, Go และ cURL"
weight: 20
ArticleTitle: "ลบWorksheet – Aspose.Cells Cloud API"
---

REST API นี้ใช้ลบ worksheet  
ข้อกำหนดเบื้องต้น: เพื่อเรียกใช้ API นี้ คุณต้องระบุโทเค็นการรับรองความถูกต้อง JWT ที่ถูกต้องในส่วนหัว **Authorization** และต้องมีสิทธิ์เข้าถึงตำแหน่งที่จัดเก็บสมุดงานที่เกี่ยวข้อง

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

*หมายเหตุ: API ใช้เวอร์ชัน **v3.0** ซึ่งเป็นเวอร์ชันที่เสถียรในปัจจุบัน การเปลี่ยนแปลงเวอร์ชันในอนาคตจะมีการประกาศไว้ในบันทึกการเผยแพร่*

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
| -------------- | ------ | -------- | ------------------- |
| name           | string | path     | ชื่อเอกสาร |
| sheetName      | string | path     | ชื่อ worksheet |
| folder         | string | query    | โฟลเดอร์ของเอกสาร |
| storageName    | string | query    | ชื่อที่เก็บข้อมูล |

การตอบกลับ HTTP ที่เป็นไปได้:

| โค้ดสถานะ | คำอธิบาย |
| ----------- | ----------- |
| 200 OK | ลบ worksheet สำเร็จ |
| 400 Bad Request | พารามิเตอร์คำขอไม่ถูกต้อง |
| 401 Unauthorized | การรับรองความถูกต้องล้มเหลวหรือไม่มีโทเค็น |
| 404 Not Found | สมุดงานหรือ worksheet ที่ระบุไม่มีอยู่จริง |
| 500 Internal Server Error | ข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheet) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้จากสาธารณะ และช่วยให้คุณดำเนินการเชื่อมต่อ REST ผ่านเว็บเบราว์เซอร์ได้โดยตรง

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ผ่าน cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet3" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*คำขอทั้งหมดต้องดำเนินการผ่าน HTTPS; API ไม่รองรับการเชื่อมต่อที่ไม่ใช่ TLS*

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

## ครอบครัว Cloud SDK

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วในการพัฒนา SDK จัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ผ่าน SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}