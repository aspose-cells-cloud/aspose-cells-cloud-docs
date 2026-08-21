---
title: "อัปเดตการตรวจสอบความถูกต้องของชีตงานในชีตงาน Excel"
second_title: "เอกสาร"
linktitle: "อัปเดต"
type: docs
url: /th/validations/update/
keywords: "Aspose.Cells Cloud, การอัปเดตการตรวจสอบความถูกต้องของ Excel, REST API, การตรวจสอบความถูกต้องของชีตงาน, Excel API"
description: "วิธีการอัปเดตการตรวจสอบความถูกต้องของชีตงานในไฟล์ Excel โดยใช้ Aspose.Cells Cloud REST API พร้อมตัวอย่าง cURL และโค้ด SDK สำหรับภาษาโปรแกรมต่างๆ"
weight: 10
ArticleTitle: "อัปเดตการตรวจสอบความถูกต้องของชีตงานโดยใช้ Aspose.Cells Cloud API"
---

REST API นี้อัปเดตการตรวจสอบความถูกต้องของชีตงานตามดัชนีที่ระบุ

ก่อนเรียกใช้เอนด์พอยต์นี้ คุณต้องได้รับโทเคน JWT ที่มีขอบเขตที่เหมาะสม (เช่น `Cells.ReadWrite`) และใส่โทเคนนี้ในส่วนหัว `Authorization` ดังที่แสดงในตัวอย่าง

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ประเภท    | ตำแหน่ง | คำอธิบาย                                                    |
| ---------------- | -------- | -------- | ----------------------------------------------------------- |
| name             | string   | path     | ชื่อไฟล์สมุดงาน                                             |
| sheetName        | string   | path     | ชื่อชีตงานที่มีการตรวจสอบความถูกต้องนี้                    |
| validationIndex  | integer  | path     | ดัชนีแบบ zero‑based ของการตรวจสอบความถูกต้องที่จะอัปเดต    |
| validation       | object   | body     | ออบเจกต์ JSON ที่กำหนดการตั้งค่าการตรวจสอบความถูกต้องที่อัปเดตแล้ว |
| folder           | string   | query    | โฟลเดอร์ในพื้นที่จัดเก็บบนคลาวด์ที่สมุดงานตั้งอยู่         |
| storageName      | string   | query    | ชื่อของบริการจัดเก็บ (หากใช้พื้นที่จัดเก็บแบบกำหนดเอง)      |

<a href="https://apireference.aspose.cloud/cells/#/WorksheetValidations/PostWorksheetValidation" target="_blank" rel="noopener noreferrer">ข้อกำหนด OpenAPI</a> กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบเปิดเผย และช่วยให้คุณดำเนินการโต้ตอบแบบ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดเพื่อเรียกใช้บริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="คำตอบ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{ "AlertStyle":"Warning" }'
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

**โค้ดสถานะ HTTP ที่เป็นไปได้**

| โค้ด | ความหมาย                                | คำอธิบาย |
|-----|------------------------------------------|---------|
| 200 | สำเร็จ (OK)                             | อัปเดตการตรวจสอบความถูกต้องเรียบร้อยแล้ว |
| 400 | คำขอไม่ถูกต้อง (Bad Request)            | คำขอมีรูปแบบผิดหรือขาดพารามิเตอร์ที่จำเป็น |
| 401 | ไม่ได้รับอนุญาต (Unauthorized)          | โทเคน JWT ไม่ถูกต้องหรือขาดหายไป |
| 403 | ถูกปฏิเสธการเข้าถึง (Forbidden)         | โทเคนไม่มีขอบเขตที่เพียงพอ |
| 404 | ไม่พบ (Not Found)                       | สมุดงาน ชีตงาน หรือดัชนีการตรวจสอบความถูกต้องที่ระบุไม่มีอยู่จริง |
| 500 | ข้อผิดพลาดภายในของเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับการจัดการข้อผิดพลาด โปรดดูที่ <a href="https://apireference.aspose.cloud/cells/#/Errors" target="_blank" rel="noopener noreferrer">เอกสารข้อผิดพลาดของ Aspose.Cells Cloud</a>

คุณอาจต้องการสำรวจการดำเนินการที่เกี่ยวข้องอื่นๆ เช่น การเพิ่มการตรวจสอบความถูกต้องใหม่ หรือการลบการตรวจสอบความถูกต้องที่มีอยู่:

- [เพิ่มการตรวจสอบความถูกต้องของชีตงาน](https://docs.aspose.cloud/cells/validations/add/)
- [ลบการตรวจสอบความถูกต้องของชีตงาน](https://docs.aspose.cloud/cells/validations/delete/)

## ครอบครัว SDK สำหรับคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK ช่วยซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณ โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">ที่เก็บ GitHub</a> เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}
---