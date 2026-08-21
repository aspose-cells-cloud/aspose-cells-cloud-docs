---
title: "ลบหลายแถวจากแผ่นงาน Excel"
second_title: "เอกสาร"
linktitle: "แถว"
type: docs
url: /rows/delete/rows/
keywords: "Aspose.Cells Cloud, ลบแถว, ลบหลายแถว, แผ่นงาน Excel, REST API, SDK"
description: "เรียนรู้วิธีการลบแถวหนึ่งแถวหรือหลายแถวจากแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API ซึ่งรวมถึงรายละเอียดของปลายทาง (endpoint), พารามิเตอร์, ตัวอย่าง cURL และตัวอย่างโค้ด SDK สำหรับภาษาต่างๆ"
weight: 80
ArticleTitle: "ลบหลายแถวจากแผ่นงาน Excel ด้วย API ของ Aspose.Cells Cloud"
---

REST API นี้ใช้ลบหลายแถว **จาก** แผ่นงาน Excel

**ข้อกำหนดเบื้องต้น:** เพื่อเรียกใช้ปลายทางนี้ คุณต้องมีโทเค็น JWT ที่ถูกต้องซึ่งได้รับจากการยืนยันตัวตนของ Aspose Cloud และมีสิทธิ์การเข้าถึงที่เหมาะสมสำหรับสมุดงาน

## DeleteWorksheetRows API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### **พารามิเตอร์ของคำขอ**

| ชื่อพารามิเตอร์ | ประเภท | Path / Query String / HTTP Body | คำอธิบาย |
| --------------- | ------- | ------------------------------- | -------------------------------------------------------------------- |
| name            | string  | path                            | ชื่อสมุดงาน |
| sheetName       | string  | path                            | ชื่อแผ่นงาน |
| startrow        | integer | query                           | ดัชนีแบบ zero-based ของแถวแรกที่จะลบ (เช่น `0` หมายถึงแถวแรก) |
| totalRows       | integer | query                           | จำนวนแถวที่จะลบ |
| updateReference | boolean | query                           | กำหนดว่าจะอัปเดตการอ้างอิงหลังการลบหรือไม่ (`true`/`false`) |
| folder          | string  | query                           | โฟลเดอร์ของเอกสาร |
| storageName     | string  | query                           | ชื่อที่จัดเก็บ |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRows) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ที่อยู่ในรูปแบบคำสั่ง (command-line tool) เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ด้วย cURL **ปลายทางทั้งหมดต้องใช้ HTTPS; HTTP ถูกเลิกใช้งานแล้ว**

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="คำตอบ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
-X DELETE \
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

**รหัสคำตอบที่เป็นไปได้**

| สถานะ HTTP | คำอธิบาย |
|-------------|-------------|
| 200 | ลบแถวเรียบร้อยแล้ว |
| 400 | คำขอไม่ถูกต้อง – พารามิเตอร์ไม่ถูกต้อง |
| 401 | ไม่ได้รับอนุญาต – โทเค็น JWT หายไปหรือไม่ถูกต้อง |
| 404 | ไม่พบ – สมุดงานหรือแผ่นงานไม่มีอยู่จริง |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เงื่อนไขที่ไม่คาดคิด |

## Cloud SDK Family

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำและช่วยให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}