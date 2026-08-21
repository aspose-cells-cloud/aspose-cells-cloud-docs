---
title: "ย้ายแผ่นงาน Excel – Aspose.Cells Cloud API (v3.0)"
second_title: "เอกสาร"
linktitle: "ย้าย"
type: docs
url: /th/worksheets/move/
aliases: [  /th/move-excel-worksheets/ ]
keywords: "Aspose.Cells Cloud, ย้ายแผ่นงาน, Excel, REST API, SDK, C#, Java, Python, Node.js, PHP, Ruby, Go, Android, Swift, Perl, v3.0"
description: "เรียนรู้วิธีการย้ายแผ่นงาน Excel ไปยังตำแหน่งใหม่โดยใช้ Aspose.Cells Cloud API (v3.0) รวมถึง endpoint, พารามิเตอร์ที่จำเป็น, ตัวอย่าง cURL และโค้ด SDK สำหรับ C#, Java, Python และอื่นๆ"
weight: 20
ArticleTitle: "วิธีการย้ายแผ่นงาน Excel ด้วย Aspose.Cells Cloud API v3.0"
---

REST API นี้ใช้ย้ายแผ่นงานภายในสมุดงาน Excel

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/position
```

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย |
| ---------------- | ------ | -------- | ------------------------------------------------------- |
| name             | string | path     | ชื่อไฟล์ Excel |
| sheetName        | string | path     | ชื่อของแผ่นงานที่จะย้าย |
| moving           | object | body     | ออบเจกต์ JSON ที่ระบุแผ่นงานปลายทาง (`DestinationWorksheet`) และตำแหน่งสัมพัทธ์ (`Position`) |
| folder           | string | query    | เส้นทางโฟลเดอร์ที่เก็บสมุดงานไว้ |
| storageName      | string | query    | ชื่อของบริการจัดเก็บข้อมูล |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostMoveWorksheet) นิยามอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถเรียกใช้การสื่อสารผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเรียกใช้บริการเว็บของ Aspose.Cells ตัวอย่างต่อไปนี้แสดงวิธีย้ายแผ่นงานด้วยคำข้อเพียงคำสั่งเดียว

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="คำตอบ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/position" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"DestinationWorksheet":"Sheet5","Position":"after"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                    | คำอธิบาย |
|------|------------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                  | ใช้ตัวกรองเรียบร้อยแล้ว; คำตอบประกอบด้วยรายละเอียดของคำสั่ง |
| 400  | คำขอผิด (Bad Request)       | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | เอกสารรับรอง JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | ข้อมูลส่งไปมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

**ตัวอย่างข้อมูลข้อผิดพลาด**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "พารามิเตอร์ที่จำเป็น 'moving' ขาดหาย"
}
```

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ผ่าน SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostMoveWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostMoveWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-move_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "MoveExcelWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-MoveWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-MoveWorksheet-move-excel-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-MoveWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "1f9b294ef1cfb23e3775c193f15ff660" >}}

{{< /tab >}}

{{< /tabs >}}