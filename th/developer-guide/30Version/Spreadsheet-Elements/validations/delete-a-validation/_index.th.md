---
title: "การลบการตรวจสอบค่าในWorksheets – Aspose.Cells Cloud"
second title: "เอกสาร"
link title: "ลบ"
type: docs
url: /th/validations/delete/
keywords: "ลบ, การตรวจสอบค่าใน worksheet, Aspose.Cells Cloud, Excel API"
description: "เรียนรู้วิธีการลบการตรวจสอบค่าใน worksheet จากไฟล์ Excel โดยใช้ Aspose.Cells Cloud REST API ซึ่งประกอบด้วย endpoint, พารามิเตอร์, รายละเอียดการยืนยันตัวตน, ตัวอย่าง cURL, การจัดการข้อผิดพลาด และตัวอย่างโค้ด SDK"
weight: 10
---

API REST นี้จะลบการตรวจสอบค่าใน worksheet โดยใช้ดัชนีแบบ zero‑based บน worksheet ในไฟล์ Excel

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                            |
| ----------------- | --------- | -------- | ----------------------------------------------------- |
| name              | string    | path     | ชื่อของไฟล์ Excel                                     |
| sheetName         | string    | path     | ชื่อของ worksheet                                     |
| validationIndex   | integer   | path     | ดัชนีแบบ zero‑based ของการตรวจสอบค่าที่ต้องการลบ     |
| folder            | string    | query    | โฟลเดอร์ที่เก็บเอกสาร                                 |
| storageName       | string    | query    | ชื่อของบริการพื้นที่จัดเก็บข้อมูล                     |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation) กำหนด API ที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเรียกใช้บริการเว็บ Aspose.Cells ตัวอย่างต่อไปนี้แสดงวิธีการลบการตรวจสอบค่าโดยใช้ cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="คำตอบ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
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

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                    | คำอธิบาย                                                         |
|------|------------------------------|------------------------------------------------------------------|
| 200  | OK                           | ใช้ตัวกรองเรียบร้อยแล้ว; คำตอบประกอบด้วยรายละเอียดการดำเนินการ |
| 400  | Bad Request                  | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)          |
| 401  | Unauthorized                 | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                                   |
| 413  | Payload Too Large            | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                |
| 500  | Internal Server Error        | เกิดข้อผิดพลาดภายในเซิร์ฟเวอร์โดยไม่คาดคิด                      |

## ครอบครัว SDK สำหรับคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการผสานรวมการดำเนินการนี้เข้ากับแอปพลิเคชันของคุณ SDK จะจัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นที่ตรรกะเชิงธุรกิจได้ สำหรับรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud)

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการลบการตรวจสอบค่าใน worksheet โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}