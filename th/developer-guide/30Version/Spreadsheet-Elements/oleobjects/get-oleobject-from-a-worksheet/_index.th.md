---
---
title: "รับ OLE Object จากแผ่นงาน Excel – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktitle: "รับ"
type: docs
url: /th/oleobjects/get/
aliases: [/th/get-oleobject-from-a-worksheet/]
keywords: "aspose, cells, ole object, excel, worksheet, รับ ole object, rest api"
description: "ดึง OLE object (รูปภาพ, แผนภูมิ หรือไฟล์ที่ฝังไว้) จากแผ่นงานโดยใช้ Aspose.Cells Cloud REST API รวมถึง HTTPS endpoint, พารามิเตอร์ที่จำเป็น, ตัวอย่าง cURL และโค้ด SDK สำหรับหลายภาษา"
ArticleTitle: "รับ OLE Object จากแผ่นงาน Excel – Aspose.Cells Cloud API"
weight: 10
---

REST API นี้ใช้สำหรับการดึง **OLE object** จากแผ่นงาน Excel

## ความปลอดภัยและการยืนยันตัวตน
Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้การยืนยันตัวตนแบบ [JWT token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย                                                     |
| ---------------- | -------- | -------- | ------------------------------------------------------------ |
| name             | string   | path     | ชื่อเอกสาร                                                   |
| sheetName        | string   | path     | ชื่อแผ่นงาน                                                  |
| objectNumber     | integer  | path     | หมายเลข object ภายในแผ่นงาน                                 |
| format           | string   | query    | รูปแบบที่ต้องการส่งออก object (เช่น `png`, `jpeg`)           |
| folder           | string   | query    | โฟลเดอร์ที่เก็บเอกสารไว้                                     |
| storageName      | string   | query    | ชื่อ storage ที่ต้องการใช้งาน                                |

### ตัวเลือก Storage

- **folder** – ระบุโฟลเดอร์ย่อยใน storage เริ่มต้นที่สมุดงานอยู่
- **storageName** – แทนที่ชื่อ storage เริ่มต้นหากสมุดงานถูกเก็บไว้ในตำแหน่งอื่น

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject) กำหนด programming interface ที่สามารถเข้าถึงได้แบบสาธารณะ และอนุญาตให้คุณดำเนินการ REST interactions ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ command-line **cURL** เพื่อเรียกใช้ Aspose.Cells web service ตัวอย่างด้านล่างแสดงวิธีการขอ OLE object ในรูปแบบภาพ PNG

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

### การตอบกลับเป็นข้อมูลภาพไบนารี

เมื่อตั้งค่า `format` เป็นประเภทภาพ (เช่น `png`) API จะส่งข้อมูลภาพแบบไบนารีพร้อม header:

```
Content-Type: image/png
```

_(ไฟล์ภาพจะถูกส่งสตรีมโดยตรงไปยัง client)_

### การตอบกลับเป็น JSON สำหรับ metadata

หากไม่ได้ระบุ `format` หรือตั้งค่าเป็น `json` API จะส่ง JSON payload ซึ่งอธิบายรายละเอียดของ OLE object:

```json
{
  "Code": 200,
  "Status": "OK",
  "OLEObject": {
    "Name": "Object1",
    "Width": 200,
    "Height": 150,
    "Left": 10,
    "Top": 20,
    "IsLocked": false,
    "FileFormat": "png"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## การตอบกลับข้อผิดพลาด

| HTTP Status | Error Code   | คำอธิบาย                                      |
| ----------- | ------------ | --------------------------------------------- |
| 400         | BadRequest   | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง             |
| 401         | Unauthorized | JWT token ไม่ถูกต้องหรือขาดหาย               |
| 404         | NotFound     | ไม่พบสมุดงาน แผ่นงาน หรือ OLE object         |
| 500         | ServerError  | ข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด          |

**ตัวอย่างการตอบกลับ 404**

```json
{
  "Code": 404,
  "Status": "NotFound",
  "Message": "ไม่พบ OLE object ที่มีหมายเลข 0 ในแผ่นงาน 'Sheet1'"
}
```

## ครอบครัว Cloud SDK

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการผสานรวม API SDK จะจัดการรายละเอียดระดับล่างให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณ ดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud ได้ที่ [GitHub repository](https://github.com/aspose-cells-cloud)

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้ Aspose.Cells web services โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}