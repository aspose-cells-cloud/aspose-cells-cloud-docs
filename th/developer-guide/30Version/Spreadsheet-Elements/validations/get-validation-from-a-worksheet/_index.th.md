---
title: "รับค่าการตรวจสอบความถูกต้องของแผ่นงานโดยใช้ดัชนีจากแผ่นงาน Excel"
second_title: "เอกสาร"
linktype: "รับ"
type: docs
url: /th/validations/get/
aliases: [  /th/get-validation-from-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, API การตรวจสอบความถูกต้องของแผ่นงาน, รับการตรวจสอบความถูกต้องโดยใช้ดัชนี, Excel REST API, Aspose.Cells SDK"
description: "ดึงข้อมูลการตรวจสอบความถูกต้องของแผ่นงานโดยใช้ดัชนีแบบ zero‑based จากสมุดงาน Excel โดยใช้ Aspose.Cells Cloud API (เวอร์ชัน 3.0) มีตัวอย่าง cURL แผนผังการตอบกลับ รหัสข้อผิดพลาด และตัวอย่าง SDK สำหรับ C#, Java, Python และอื่นๆ"
weight: 10
---

API นี้ของ REST ใช้ดึงข้อมูลการตรวจสอบความถูกต้องของแผ่นงานโดยใช้ดัชนีจากแผ่นงาน Excel  
ก่อนเรียกใช้ปลายทาง (endpoint) ให้รับโทเค็น JWT จากปลายทาง `/connect/token` และใส่ในส่วนหัว `Authorization` ในรูปแบบ `Bearer <jwt token>`

## API ของ REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย                                            |
| ---------------- | -------- | -------- | ----------------------------------------------------- |
| name             | string   | path     | ชื่อไฟล์สมุดงาน                                     |
| sheetName        | string   | path     | ชื่อแผ่นงาน                                         |
| validationIndex  | integer  | path     | ดัชนีแบบ zero‑based ของการตรวจสอบความถูกต้องที่ต้องการดึงข้อมูล |
| folder           | string   | query    | โฟลเดอร์ที่เก็บสมุดงาน                              |
| storageName      | string   | query    | ชื่อของบริการจัดเก็บข้อมูล                           |

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidation) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Validation": {
    "AlertStyle": "Stop",
    "AreaList": [
      {
        "EndColumn": 0,
        "EndRow": 0,
        "StartColumn": 0,
        "StartRow": 0
      },
      {
        "EndColumn": 27,
        "EndRow": 0,
        "StartColumn": 26,
        "StartRow": 0
      }
    ],
    "IgnoreBlank": false,
    "InCellDropDown": false,
    "Operator": "None",
    "ShowError": false,
    "ShowInput": false,
    "Type": "AnyValue",
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/Validations/0",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**แผนผังการตอบกลับ**

| ฟิลด์          | ประเภท   | คำอธิบาย                                                                 |
| -------------- | -------- | -------------------------------------------------------------------------- |
| AlertStyle     | string   | รูปแบบของข้อความแจ้งเตือนที่แสดงต่อผู้ใช้ (Stop, Warning, Information)    |
| AreaList       | array    | คอลเลกชันของช่วงเซลล์ที่การตรวจสอบความถูกต้องนำไปใช้                    |
| IgnoreBlank    | boolean  | หากเป็น `true` เซลล์ที่ว่างจะถูกละเว้นระหว่างการตรวจสอบความถูกต้อง       |
| InCellDropDown | boolean  | หากเป็น `true` กล่องแบบเลือกลดจะปรากฏในเซลล์                            |
| Operator       | string   | ตัวดำเนินการเปรียบเทียบที่ใช้ในการตรวจสอบความถูกต้อง (เช่น `None`, `Between`) |
| ShowError      | boolean  | กำหนดว่าจะแสดงข้อความข้อผิดพลาดเมื่อการตรวจสอบความถูกต้องล้มเหลวหรือไม่ |
| ShowInput      | boolean  | กำหนดว่าจะแสดงข้อความป้อนข้อมูลเมื่อเลือกเซลล์หรือไม่                   |
| Type           | string   | ประเภทของการตรวจสอบความถูกต้อง (เช่น `AnyValue`, `WholeNumber`, `Decimal` เป็นต้น) |
| link.Href      | string   | URL อ้างอิงตนเองไปยังทรัพยากรการตรวจสอบความถูกต้อง                      |
| link.Rel       | string   | ประเภทความสัมพันธ์ (มีค่าเป็น `self` เสมอ)                               |

**รหัสข้อผิดพลาดที่เป็นไปได้**

| สถานะ HTTP | ความหมาย                                                                 |
| ----------- | ------------------------------------------------------------------------ |
| 200         | ดึงข้อมูลการตรวจสอบความถูกต้องเรียบร้อย                                 |
| 400         | คำขอผิดพลาด – พารามิเตอร์ไม่ครบหรือไม่ถูกต้อง                          |
| 401         | ไม่ได้รับอนุญาต – โทเค็น JWT ไม่ถูกต้องหรือไม่มี                         |
| 404         | ไม่พบ – สมุดงาน แผ่นงาน หรือดัชนีการตรวจสอบความถูกต้องไม่มีอยู่         |
| 500         | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เงื่อนไขที่ไม่คาดคิด                        |

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนาสำหรับ Aspose.Cells Cloud SDK จะช่วยซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณ ตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}