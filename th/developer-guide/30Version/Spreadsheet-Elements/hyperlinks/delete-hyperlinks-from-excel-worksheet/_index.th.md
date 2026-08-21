---
title: "ล้างลิงก์ไฮเปอร์"
type: docs
url: /th/hyperlinks/clear/
aliases: [  /th/add-hyperlinks-to-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, ล้างลิงก์ไฮเปอร์, ลบลิงก์ไฮเปอร์, REST API, แผ่นงาน, SDK"
description: "เรียนรู้วิธีการลบลิงก์ไฮเปอร์ทั้งหมดออกจากแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API หรือ SDK ใดก็ได้ที่รองรับ (C#, Java, Python, Node.js, Go, PHP, Ruby, Perl เป็นต้น)"
weight: 40
ArticleTitle: "ล้างลิงก์ไฮเปอร์ – เอกสารประกอบ API ของ Aspose.Cells Cloud"
---

REST API นี้จะลบ **ลิงก์ไฮเปอร์ทั้งหมด** ออกจากแผ่นงาน Excel

## ความปลอดภัยและการยืนยันตัวตน
API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ [การยืนยันตัวตนด้วยโทเค็น JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                      |
| ---------------- | ---------- | -------- | --------------------------------------------- |
| name             | string     | path     | ชื่อไฟล์ Excel                                |
| sheetName        | string     | path     | ชื่อของแผ่นงาน                               |
| folder           | string     | query    | โฟลเดอร์ที่เก็บเอกสารไว้                     |
| storageName      | string     | query    | ชื่อของบริการจัดเก็บข้อมูล (storage service) |

### การตอบกลับข้อผิดพลาด

| รหัส HTTP | เหตุผล                                                 | ตัวอย่างเนื้อหาตอบกลับ                                              |
| --------- | ------------------------------------------------------- | -------------------------------------------------------------------- |
| **400**   | คำขอไม่ถูกต้อง – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง      | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**   | ไม่ได้รับอนุญาต – โทเค็น JWT ขาดหายหรือไม่ถูกต้อง      | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | ไม่พบ – สมุดงานหรือแผ่นงานไม่มีอยู่                    | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**   | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เซิร์ฟเวอร์ล้มเหลวอย่างไม่คาดคิด | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlinks) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้จากภายนอก ซึ่งทำให้คุณสามารถเรียกใช้การโต้ตอบผ่าน REST API ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ **cURL** ผ่านคำสั่งใน command-line เพื่อเรียกใช้บริการเว็บของ Aspose.Cells ตัวอย่างต่อไปนี้แสดงวิธีการลบลิงก์ไฮเปอร์ทั้งหมดออกจากแผ่นงาน

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test1.xlsx/worksheets/Sheet1/hyperlinks" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK บนคลาวด์

การใช้ SDK จะช่วยเร่งความเร็วในการพัฒนา โดยจัดการรายละเอียดระดับต่ำให้คุณโดยอัตโนมัติ สำหรับรายการ SDK ทั้งหมดของ Aspose.Cells Cloud โปรดเยี่ยมชม [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud)

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการลบลิงก์ไฮเปอร์ของแผ่นงานโดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}