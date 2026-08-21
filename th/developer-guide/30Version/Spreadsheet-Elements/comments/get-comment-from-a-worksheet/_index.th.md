---
title: "รับความคิดเห็นในแผ่นงาน – เอกสารประกอบ API ของ Aspose.Cells Cloud"
type: docs
url: /comments/get/
aliases: [/get-comment-from-a-worksheet/]
keywords: "Aspose.Cells, ความคิดเห็นในแผ่นงาน, API, GET, Excel"
description: "เรียนรู้วิธีการดึงความคิดเห็นในแผ่นงานโดยใช้ชื่อเซลล์ผ่าน Aspose.Cells Cloud API (เวอร์ชัน 3.0) รวมถึง URL คำขอ พารามิเตอร์ ตัวอย่าง cURL รายละเอียดการตอบกลับ และโค้ดตัวอย่าง SDK"
weight: 10
ArticleTitle: "รับความคิดเห็นในแผ่นงาน – เอกสารประกอบ API ของ Aspose.Cells Cloud"
---

REST API นี้ดึงความคิดเห็นในแผ่นงานโดยใช้ชื่อเซลล์ผ่าน **Aspose.Cells Cloud**

**ข้อกำหนดเบื้องต้น:** เพื่อเรียกใช้งานโอเปอเรชันนี้ คุณต้องใส่โทเค็น JWT ที่ถูกต้องใน header `Authorization` (รูปแบบ `Bearer <jwt token>`) โดยสามารถรับโทเค็นได้ผ่านขั้นตอนการยืนยันตัวตนของ Aspose.Cells Cloud ซึ่งอธิบายไว้ใน [คู่มือการยืนยันตัวตน](/cells/authentication/)

## API GetWorksheetComment

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและบังคับใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภทข้อมูล | ตำแหน่ง (เส้นทาง URL / สตริงค์คิวรี) | คำอธิบาย |
|------------------|-------------|--------------------------------------|--------------------------------------------------------|
| name             | string      | เส้นทาง URL                          | ชื่อไฟล์ Excel                                         |
| sheetName        | string      | เส้นทาง URL                          | ชื่อของแผ่นงานที่มีความคิดเห็น                        |
| cellName         | string      | เส้นทาง URL                          | ที่อยู่เซลล์ (เช่น **A1**) ที่ต้องการดึงความคิดเห็น   |
| folder           | string      | สตริงค์คิวรี                        | เส้นทางโฟลเดอร์ที่เก็บเอกสารไว้                      |
| storageName      | string      | สตริงค์คิวรี                        | ชื่อของบริการจัดเก็บข้อมูล                            |

<a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetComment" rel="noopener noreferrer">สเปค OpenAPI</a> กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และอนุญาตให้คุณดำเนินการ REST ผ่านเบราว์เซอร์เว็บได้โดยตรง

คุณสามารถใช้เครื่องมือ cURL ผ่าน command-line เพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ผ่าน cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Comment": {
    "CellName": "A1",
    "Author": "roy.wang",
    "HtmlNote": "",
    "Note": "Aspose.Cells Cloud.",
    "AutoSize": "True",
    "IsVisible": "True",
    "Width": 30,
    "Height": 10,
    "TextHorizontalAlignment": "Bottom",
    "TextOrientationType": "TopToBottom",
    "TextVerticalAlignment": "Bottom"
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**การตอบกลับ:** API จะส่งกลับวัตถุ JSON ที่มีวัตถุ `Comment` ซึ่งประกอบด้วยฟิลด์ดังนี้:

| ฟิลด์                      | ประเภทข้อมูล | คำอธิบาย                                                |
|----------------------------|-------------|----------------------------------------------------------|
| `CellName`                 | string      | ที่อยู่ของเซลล์ (เช่น **A1**)                          |
| `Author`                   | string      | ชื่อผู้เขียนความคิดเห็น                                 |
| `HtmlNote`                 | string      | เนื้อหาความคิดเห็นในรูปแบบ HTML (ถ้ามี)                |
| `Note`                     | string      | เนื้อหาความคิดเห็นในรูปแบบข้อความธรรมดา                |
| `AutoSize`                 | boolean     | ระบุว่ากล่องความคิดเห็นปรับขนาดอัตโนมัติหรือไม่         |
| `IsVisible`                | boolean     | ระบุว่าความคิดเห็นปรากฏให้เห็นหรือไม่                   |
| `Width`                    | integer     | ความกว้างของกล่องความคิดเห็น (หน่วยเป็นตัวอักษร)       |
| `Height`                   | integer     | ความสูงของกล่องความคิดเห็น (หน่วยเป็นตัวอักษร)          |
| `TextHorizontalAlignment` | string      | การจัดแนวแนวนอนของข้อความ (เช่น **Bottom**)           |
| `TextOrientationType`      | string      | ทิศทางของข้อความ (เช่น **TopToBottom**)               |
| `TextVerticalAlignment`    | string      | การจัดแนวแนวตั้งของข้อความ (เช่น **Bottom**)           |

## ข้อผิดพลาดทั่วไป

- **401 ไม่ได้รับอนุญาต (Unauthorized)** – ตรวจสอบว่าโทเค็น JWT ยังใช้งานได้ ไม่หมดอายุ และถูกใส่ไว้ใน header `Authorization` อย่างถูกต้อง
- **404 ไม่พบ (Not Found)** – ตรวจสอบให้แน่ใจว่าชื่อไฟล์ ชื่อแผ่นงาน และที่อยู่เซลล์ถูกต้อง และไฟล์มีอยู่ในโฟลเดอร์/พื้นที่จัดเก็บที่ระบุ
- **500 ข้อผิดพลาดภายในของเซิร์ฟเวอร์ (Internal Server Error)** – ตรวจสอบข้อมูลในคำขอว่ามีรูปแบบผิดหรือไม่ และยืนยันว่าบริการยังทำงานได้ปกติ

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                      | คำอธิบาย                                                       |
|------|-------------------------------|----------------------------------------------------------------|
| 200  | สำเร็จ (OK)                   | กรองข้อมูลสำเร็จ; การตอบกลับมีรายละเอียดของโอเปอเรชัน         |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ)  |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)| โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                               |
| 413  | ข้อมูลในคำขอใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด              |
| 500  | ข้อผิดพลาดภายในของเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดภายในเซิร์ฟเวอร์          |

## ครอบครัวของ SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโปรเจกต์ของคุณ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บ GitHub</a> เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้เว็บเซอร์วิสของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetComments.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetComments.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetComments.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetComments.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetComments.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetComments.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetComments.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetComments.go" >}}

{{< /tab >}}

{{< /tabs >}}