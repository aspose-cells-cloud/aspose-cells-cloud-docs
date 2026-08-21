---
title: "การลบวัตถุ OLE ในเวิร์กชีต Excel"
second_title: "เอกสาร"
linktitle: "ลบ"
type: docs
url: /th/oleobjects/delete/
aliases: [/delete-a-specific-oleobject-from-excel-worksheet/]
keywords: "Aspose.Cells, Cloud, ลบ, OLE, วัตถุ, Excel, เวิร์กชีต, REST, API, SDK"
description: "เรียนรู้วิธีการลบวัตถุ OLE จากเวิร์กชีต Excel โดยใช้ Aspose.Cells Cloud REST API (เวอร์ชัน 4.0) ซึ่งรวมถึง HTTPS endpoint, ขั้นตอนการยืนยันตัวตน, ตัวอย่าง cURL, ตัวอย่างโค้ด SDK, คำแนะนำการจัดการข้อผิดพลาด และลิงก์สำหรับขั้นตอนต่อไป"
weight: 50
ArticleTitle: "ลบวัตถุ OLE จากเวิร์กชีต Excel โดยใช้ Aspose.Cells Cloud API"
---

หน้านี้อธิบายวิธีการลบวัตถุ OLE ที่ระบุออกจากเวิร์กชีตในสมุดงาน Excel โดยใช้ **Aspose.Cells Cloud** วัตถุ OLE อาจเป็นภาพที่เชื่อมโยง แผนภูมิ หรือวัตถุที่ฝังไว้อื่นๆ ที่ Excel จัดเก็บเป็นหน่วยแยกต่างหาก

## ความปลอดภัยและการยืนยันตัวตน
Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ [การยืนยันตัวตนด้วย JWT token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## REST API

```bash
DELETE https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย                                           |
| ---------------- | -------- | -------- | --------------------------------------------------- |
| name             | string   | path     | ชื่อสมุดงาน                                        |
| sheetName        | string   | path     | ชื่อเวิร์กชีต                                       |
| oleObjectIndex   | integer  | path     | ดัชนีของวัตถุ OLE ที่ต้องการลบ                     |
| folder           | string   | query    | โฟลเดอร์ที่เก็บสมุดงาน (ไม่บังคับ)                 |
| storageName      | string   | query    | ชื่อของบริการจัดเก็บข้อมูล (ไม่บังคับ)             |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/OleObjects/DeleteWorksheetOleObject) กำหนด API สำหรับการใช้งานผ่านอินเทอร์เฟซที่เข้าถึงได้จากภายนอก และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้ **เครื่องมือ cURL ผ่าน command-line** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0" \
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

### รายละเอียดของคำตอบ

| สถานะ HTTP           | คำอธิบาย                                                                 | ตัวอย่าง JSON                                                       |
| -------------------- | ------------------------------------------------------------------------ | ------------------------------------------------------------------- |
| **200 OK**           | วัตถุ OLE ถูกลบเรียบร้อยแล้ว                                           | `{ "Code": 200, "Status": "OK" }`                                   |
| **401 Unauthorized** | ไม่มี JWT token หรือ token ไม่ถูกต้อง                                    | `{ "Code": 401, "Message": "Access token is missing or invalid." }` |
| **404 Not Found**    | สมุดงาน เวิร์กชีต หรือดัชนีของวัตถุ OLE ที่ระบุไม่มีอยู่จริง             | `{ "Code": 404, "Message": "OLE object index out of range." }`      |
| **400 Bad Request**  | พารามิเตอร์ที่จำเป็นขาดหายหรือรูปแบบไม่ถูกต้อง                         | `{ "Code": 400, "Message": "Invalid request parameters." }`         |

จัดการกับคำตอบเหล่านี้ในแอปพลิเคชันของคุณโดยตรวจสอบค่า status code และแสดงข้อความที่มาพร้อม

## Cloud SDK Family
การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วในการพัฒนา SDK จะจัดการกับรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}