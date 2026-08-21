---
title: "รับการตรวจสอบความถูกต้องของworksheet ทั้งหมดจาก Excel worksheet"
second_title: "เอกสาร"
linktitle: "รับทั้งหมด"
type: docs
url: /th/validations/get-all/
keywords: "Aspose.Cells Cloud, Excel, worksheet validations, REST API, Get all validations, SDKs"
description: "ดึงข้อมูลการตรวจสอบความถูกต้องของ worksheet ทั้งหมดจาก Excel worksheet โดยใช้ Aspose.Cells Cloud REST API รองรับ SDK หลายภาษา (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) เพื่อการผสานรวมอย่างรวดเร็ว"
weight: 10
---

การตรวจสอบความถูกต้องของ worksheet ช่วยให้คุณกำหนดกฎเพื่อจำกัดประเภทหรือช่วงของข้อมูลที่สามารถป้อนลงในเซลล์ได้ โดยทั่วไปจะใช้เพื่อบังคับใช้ความสมบูรณ์ของข้อมูล เช่น การจำกัดข้อมูลให้อยู่ในรายการค่าที่กำหนด วันที่ภายในช่วงที่ระบุ หรือขีดจำกัดทางตัวเลข

API นี้จะดึงข้อมูลการตรวจสอบความถูกต้องของ worksheet ทั้งหมดจาก Excel worksheet

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                               |
| -------------- | ------ | -------- | ----------------------------------------- |
| name           | string | path     | ชื่อของเอกสาร Excel                      |
| sheetName      | string | path     | ชื่อของ worksheet                        |
| folder         | string | query    | เส้นทางโฟลเดอร์ที่เก็บเอกสารไว้         |
| storageName    | string | query    | ชื่อของบริการจัดเก็บข้อมูล               |

**รหัสสถานะของคำตอบ**

| รหัส | คำอธิบาย                                |
|------|------------------------------------------|
| 200  | คำขอสำเร็จ – รายการการตรวจสอบความถูกต้อง |
| 401  | ไม่ได้รับอนุญาต – เอกสาร JWT ไม่ถูกต้องหรือขาดหายไป |
| 404  | ไม่พบ – เอกสารหรือ worksheet ขาดหายไป |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์               |

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidations) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้จากภายนอก และช่วยให้คุณดำเนินการโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells Cloud ได้อย่างง่ายดาย **ข้อกำหนดเบื้องต้น:** คุณต้องใส่ JWT token ที่ถูกต้องไว้ในหัวข้อ `Authorization`

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="คำตอบ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "validations": [
    {
      "name": "Validation1",
      "type": "WholeNumber",
      "operator": "Between",
      "formula1": "1",
      "formula2": "100",
      "showErrorMessage": true,
      "errorMessage": "ค่าที่ป้อนต้องอยู่ระหว่าง 1 ถึง 100"
    },
    {
      "name": "Validation2",
      "type": "List",
      "formula1": "\"Option1,Option2,Option3\"",
      "showErrorMessage": true,
      "errorMessage": "เลือกค่าจากรายการ"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [ที่เก็บบน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกบริการเว็บของ Aspose.Cells ผ่าน SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}