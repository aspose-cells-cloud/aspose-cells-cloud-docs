---
title: "รับรูปทรงทั้งหมดบนแผ่นงาน Excel"
second_title: "เอกสาร"
linktitle: "get-all"
type: docs
url: /th/shapes/get-all/
aliases: [  /th/get-all-shapes-inside-the-worksheet/ ]
keywords: "Aspose.Cells, Cloud API, รูปทรง Excel, รับรูปทรง, REST, SDK"
description: "ดึงข้อมูลรูปทรงทั้งหมด (กราฟ รูปภาพ กล่องข้อความ) จากแผ่นงานโดยใช้ Aspose.Cells Cloud REST API พร้อมตัวอย่าง cURL โค้ดตัวอย่าง SDK ขั้นตอนการตรวจสอบสิทธิ์ และการจัดการข้อผิดพลาด"
ArticleTitle: "รับรูปทรงทั้งหมดบนแผ่นงาน Excel"
weight: 10
---

API REST นี้ช่วยให้สามารถดึงข้อมูลรูปทรงทั้งหมดบนแผ่นงาน Excel ได้

## ความปลอดภัยและการตรวจสอบสิทธิ์
API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้การตรวจสอบสิทธิ์แบบ [โทเค็น JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย |
| ---------------- | ------ | -------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| **name** | string | path | ชื่อไฟล์ Excel |
| **sheetName** | string | path | ชื่อแผ่นงาน |
| **folder** | string | query | โฟลเดอร์ที่เก็บเอกสารไว้ |
| **storageName** | string | query | ชื่อของบริการจัดเก็บข้อมูลที่ต้องการใช้ |
| **include** | string | query | ตั้งค่าเป็น `details` เพื่อส่งกลับคุณสมบัติของรูปทรงแบบเต็มรูปแบบ มิฉะนั้นจะส่งกลับเฉพาะวัตถุ `link` เท่านั้น |

> **ไม่บังคับ**: `folder`, `storageName` และ `include` สามารถละเว้นได้เมื่อไฟล์อยู่ในพื้นที่จัดเก็บหลัก (root storage)

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ตัวอย่างต่อไปนี้แสดงคำขอที่รวมพารามิเตอร์การคิวรีที่ไม่บังคับ

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?folder=Samples&storageName=MyStorage" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Shapes": {
    "ShapeList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes",
      "Rel": "self",
      "Type": null,
      "Title": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### ฟิลด์การตอบกลับ

วัตถุ `Shapes` มีรายการของวัตถุ `Shape` แต่ละรูปทรงประกอบด้วยคุณสมบัติต่อไปนี้ (เมื่อใช้ฟlag `include=details`; มิฉะนั้นจะส่งกลับเฉพาะวัตถุ `link` เท่านั้น)

| คุณสมบัติ | ประเภท | คำอธิบาย |
| --------- | ------ | -------------------------------------------------------------------- |
| **Name** | string | ชื่อที่กำหนดให้กับรูปทรง (เช่น “Chart 1”) |
| **Type** | string | ประเภทของรูปทรง (เช่น `Chart`, `Picture`, `TextBox`) |
| **Top** | number | ระยะห่าง (หน่วยเป็นจุด) จากขอบด้านบนของแผ่นงานถึงรูปทรง |
| **Left** | number | ระยะห่าง (หน่วยเป็นจุด) จากขอบด้านซ้ายของแผ่นงานถึงรูปทรง |
| **Width** | number | ความกว้างของรูปทรง (หน่วยเป็นจุด) |
| **Height** | number | ความสูงของรูปทรง (หน่วยเป็นจุด) |
| **Link** | object | ข้อมูลลิงก์ (Href, Rel, Type, Title) |

## การจัดการข้อผิดพลาด

| สถานะ HTTP | คำอธิบาย | ตัวอย่างเนื้อหาข้อผิดพลาด |
| ----------- | ------------------------------------------------- | ------------------------------------------------------------------- |
| **400** | คำขอไม่ถูกต้อง – พารามิเตอร์มีรูปแบบไม่ถูกต้อง | `{ "Code": 400, "Message": "Invalid parameter value." }` |
| **401** | ไม่ได้รับอนุญาต – ไม่มีหรือโทเค็นไม่ถูกต้อง | `{ "Code": 401, "Message": "Access token is missing or invalid." }` |
| **404** | ไม่พบ – สมุดงานหรือแผ่นงานไม่มีอยู่จริง | `{ "Code": 404, "Message": "File or worksheet not found." }` |
| **500** | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เงื่อนไขที่ไม่คาดคิด | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

คำขอที่สำเร็จจะส่งกลับ **HTTP 200** พร้อมกับวัตถุ `Shapes` ที่มีรายการของรูปทรงตามตัวอย่างการตอบกลับข้างต้น

API บังคับใช้ขีดจำกัดที่ **150 คำขอต่อนาทีต่อโทเค็น JWT** หากเกินขีดจำกัดนี้จะส่งกลับ **HTTP 429** พร้อมส่วนหัว `Retry-After` ที่ระบุเวลาที่ควรลองใหม่

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำและช่วยให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShapes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShapes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShapes.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShapes.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShapes.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShapes.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShapes.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShapes.go" >}}

{{< /tab >}}

{{< /tabs >}}