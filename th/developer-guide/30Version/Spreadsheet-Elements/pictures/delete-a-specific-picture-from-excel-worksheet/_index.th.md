---
title: "การลบรูปภาพออกจากแผ่นงาน Excel – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktitle: "ลบ"
type: docs
url: /pictures/delete/
aliases: [/delete-a-specific-picture-from-excel-worksheet/]
keywords: "Aspose.Cells, Cloud API, ลบรูปภาพ, แผ่นงาน Excel, REST"
description: "ลบรูปภาพออกจากแผ่นงาน Excel โดยใช้ REST API ของ Aspose.Cells Cloud ศึกษาเกี่ยวกับ endpoint แบบ DELETE พารามิเตอร์ที่จำเป็น การตรวจสอบสิทธิ์ รหัสข้อผิดพลาด และโค้ดตัวอย่าง"
weight: 50
ArticleTitle: "การลบรูปภาพออกจากแผ่นงาน Excel – Aspose.Cells Cloud API"
---

REST API นี้ใช้ลบรูปภาพออกจากแผ่นงาน Excel

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์แบบใช้โทเค็น JWT</a>

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | จำเป็น | คำอธิบาย                                     |
|------------------|--------|----------|--------|---------------------------------------------|
| name             | string | path     | ใช่    | ชื่อไฟล์สมุดงาน                             |
| sheetName        | string | path     | ใช่    | ชื่อของแผ่นงานที่มีรูปภาพ                   |
| pictureIndex     | integer | path    | ใช่    | ดัชนีแบบเริ่มต้นที่ 0 ของรูปภาพที่จะลบ     |
| folder           | string | query    | ไม่บังคับ | โฟลเดอร์ที่เก็บสมุดงาน                     |
| storageName      | string | query    | ไม่บังคับ | ชื่อของบริการจัดเก็บข้อมูล (ไม่บังคับ)      |

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งในบรรทัดคำสั่งเพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/0" \
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

**หัวเรื่องของการตอบกลับตัวอย่าง**

| หัวเรื่อง         | ค่า                           |
|------------------|------------------------------|
| Content-Type     | application/json             |
| Content-Length   | (แปรผัน)                     |
| Date             | (วันที่เซิร์ฟเวอร์)           |

{{< /tab >}}

{{< /tabs >}}

### การจัดการข้อผิดพลาด

| โค้ด HTTP | ความหมาย                                              | โครงสร้างข้อผิดพลาดตัวอย่าง                                        |
|-----------|--------------------------------------------------------|--------------------------------------------------------------------|
| 200       | ลบรูปภาพเรียบร้อยแล้ว                                | `{ "Code": 200, "Status": "OK" }`                                  |
| 400       | คำขอไม่ถูกต้อง – พารามิเตอร์ไม่ถูกต้อง               | `{ "Code": 400, "Message": "Invalid pictureIndex." }`             |
| 401       | ไม่ได้รับอนุญาต – โทเค็นหายไปหรือไม่ถูกต้อง          | `{ "Code": 401, "Message": "Access token is missing or invalid." }` |
| 404       | ไม่พบ – สมุดงาน แผ่นงาน หรือรูปภาพไม่มีอยู่จริง      | `{ "Code": 404, "Message": "Resource not found." }`               |
| 500       | ข้อผิดพลาดภายในเซิร์ฟเวอร์                            | `{ "Code": 500, "Message": "Unexpected server error." }`          |

## ครอบครัว SDK สำหรับคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่โครงการของคุณได้ โปรดดูที่ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้เว็บเซอร์วิสของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}