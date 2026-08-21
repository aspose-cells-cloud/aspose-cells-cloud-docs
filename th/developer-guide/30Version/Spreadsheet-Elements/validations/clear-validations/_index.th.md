---
title: "ลบการตรวจสอบข้อมูลทั้งหมดของแผ่นงาน – Aspose.Cells Cloud API"
second_title: "เอกสารประกอบ"
linktitle: "ลบ"
type: docs
url: /th/validations/clear/
keywords: "Aspose.Cells Cloud, ลบการตรวจสอบข้อมูลของแผ่นงาน, Excel, REST API, การตรวจสอบสเปรดชีต, API"
description: "ลบกฎการตรวจสอบข้อมูลทั้งหมดออกจากแผ่นงานในไฟล์ Excel โดยใช้ Aspose.Cells Cloud REST API รวมถึงขั้นตอนการตรวจสอบสิทธิ์ รายละเอียดคำขอ ตัวอย่าง cURL โครงสร้างการตอบกลับ การจัดการข้อผิดพลาด และตัวอย่างโค้ด SDK"
weight: 10
---

**ข้อกำหนดเบื้องต้น**

- บัญชี Aspose Cloud ที่ถูกต้อง
- โทเคน JWT ที่ได้รับผ่าน API การตรวจสอบสิทธิ์ของ Aspose Cloud (`/connect/token`)
- สมุดงานต้องถูกจัดเก็บไว้ในพื้นที่จัดเก็บของ Aspose Cloud (หรือต้องระบุพารามิเตอร์คิวรี `folder` และ `storageName` ตามที่จำเป็น)

REST API นี้จะลบการตรวจสอบข้อมูลทั้งหมดของแผ่นงานในไฟล์ Excel

## REST API

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                |
| ---------------- | ---------- | -------- | -------------------------------------------------------- |
| name             | string     | path     | ชื่อของเอกสาร Excel                                      |
| sheetName        | string     | path     | ชื่อของแผ่นงานที่มีการตรวจสอบข้อมูล                    |
| folder           | string     | query    | โฟลเดอร์ที่เก็บเอกสารไว้                                |
| storageName      | string     | query    | ชื่อของบริการพื้นที่จัดเก็บ                            |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation) นิยามอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และอนุญาตให้คุณดำเนินการโต้ตอบ REST ผ่านเว็บเบราว์เซอร์โดยตรง

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียก API ด้วย cURL หลังจากได้รับโทเคน JWT แล้ว

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
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

### การจัดการข้อผิดพลาด

| สถานะ HTTP | ความหมาย               | คำอธิบาย                                                |
| ----------- | ---------------------- | -------------------------------------------------------- |
| 400         | คำขอผิดรูปแบบ (Bad Request) | คำขอไม่ถูกต้องหรือขาดพารามิเตอร์ที่จำเป็น               |
| 401         | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ขาดหาย ไม่ถูกต้อง หรือหมดอายุแล้ว            |
| 404         | ไม่พบ (Not Found)       | สมุดงานหรือแผ่นงานที่ระบุไม่มีอยู่จริง                  |
| 500         | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนฝั่งเซิร์ฟเวอร์              |

พายโหลดของข้อผิดพลาดจะมีโครงสร้าง JSON เหมือนกัน โดยมีฟิลด์ `Code` และ `Message` ตัวอย่างเช่น:

```json
{
  "Code": 401,
  "Message": "Invalid or expired token."
}
```

## ครอบครัว SDK สำหรับคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK ช่วยซ่อนรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจได้ โปรดตรวจสอบ[ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกเว็บเซอร์วิสของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}