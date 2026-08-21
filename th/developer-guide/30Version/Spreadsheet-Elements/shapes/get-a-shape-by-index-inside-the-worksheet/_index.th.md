---
title: "รับรูปร่างตามดัชนีในแผ่นงาน Excel"
second_title: "เอกสาร"
linktype: "รับ"
type: docs
url: /shapes/get/
aliases: [/get-a-shape-by-index-inside-the-worksheet/]
keywords: "Aspose.Cells Cloud, API รูปร่าง Excel, รับรูปร่างตามดัชนี, รูปร่างในแผ่นงาน, REST API, การดึงข้อมูลรูปร่าง, Aspose.Cells SDK"
description: "ดึงรูปร่างตามดัชนีจากแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API ซึ่งรวมถึงไวยากรณ์คำขอ พารามิเตอร์ รายละเอียดการตอบกลับ และตัวอย่าง SDK"
weight: 20
ArticleTitle: "รับรูปร่างตามดัชนีในแผ่นงาน Excel – เอกสารประกอบ Aspose.Cells Cloud"
---

REST API นี้จะดึงรูปร่าง (รวมถึงข้อมูลภาพหรือเมตาดาต้าของรูปร่าง) จากแผ่นงาน Excel

## API GetWorksheetShape

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

**ข้อกำหนดเบื้องต้น**  
- โทเคนการเข้าถึง Aspose Cloud ที่ถูกต้อง (Bearer JWT)  
- สมุดงานต้องถูกจัดเก็บไว้ในพื้นที่จัดเก็บของ Aspose Cloud หรือในโฟลเดอร์ที่ระบุ  

### **ความปลอดภัยและการพิสูจน์ตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การพิสูจน์ตัวตนด้วยโทเคน JWT</a>

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย |
| -------------- | ------- | -------- | --------------------------------------------------- |
| name           | string  | path     | ชื่อของเอกสาร Excel |
| sheetName      | string  | path     | ชื่อของแผ่นงานที่มีรูปร่าง |
| shapeindex     | integer | path     | ดัชนีของรูปร่าง (เริ่มต้นที่ 0) ในแผ่นงาน |
| folder         | string  | query    | เส้นทางโฟลเดอร์ที่เก็บเอกสารไว้ |
| storageName    | string  | query    | ชื่อของบริการจัดเก็บข้อมูล |

**หมายเหตุ:** `shapeindex` เป็นดัชนีแบบเริ่มต้นที่ 0 (zero-based) ดังนั้นรูปร่างแรกจะมีค่าดัชนีเป็น 0 โปรดตรวจสอบให้แน่ใจว่าสมุดงานถูกจัดเก็บไว้ใน `folder` และ `storageName` ที่ระบุไว้ หากคุณไม่ได้ใช้พื้นที่จัดเก็บเริ่มต้น

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/Shapes/GetWorksheetShape) กำหนดอินเทอร์เฟซการโปรแกรมที่สามารถเข้าถึงได้สาธารณะ และช่วยให้คุณสามารถดำเนินการโต้ตอบแบบ REST ผ่านเว็บเบราว์เซอร์ได้โดยตรง

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
# แก้ไข endpoint และ path ให้ถูกต้องแล้ว
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet4/shapes/1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "Shape": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Name": "string",
    "MsoDrawingType": "string",
    "AutoShapeType": "string",
    "Placement": "string",
    "UpperLeftRow": 0,
    "Top": 0,
    "UpperLeftColumn": 0,
    "Left": 0,
    "LowerRightRow": 0,
    "Bottom": 0,
    "LowerRightColumn": 0,
    "Right": 0,
    "Width": 0,
    "Height": 0,
    "X": 0,
    "Y": 0,
    "RotationAngle": 0,
    "HtmlText": "string",
    "Text": "string",
    "AlternativeText": "string",
    "TextHorizontalAlignment": "string",
    "TextHorizontalOverflow": "string",
    "TextOrientationType": "string",
    "TextVerticalAlignment": "string",
    "TextVerticalOverflow": "string",
    "IsGroup": true,
    "IsHidden": true,
    "IsLockAspectRatio": true,
    "IsLocked": true,
    "IsPrintable": true,
    "IsTextWrapped": true,
    "IsWordArt": true,
    "LinkedCell": "string",
    "ZOrderPosition": 0
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**โค้ดสถานะ HTTP ที่เป็นไปได้**

| โค้ด | คำอธิบาย |
|------|-------------|
| **200 OK** | ดึงข้อมูลรูปร่างสำเร็จ |
| **400 Bad Request** | คำขอผิดรูปแบบหรือขาดพารามิเตอร์ที่จำเป็น |
| **401 Unauthorized** | การพิสูจน์ตัวตนล้มเหลวหรือโทเคนไม่ถูกต้อง/หายไป |
| **404 Not Found** | สมุดงาน แผ่นงาน หรือดัชนีรูปร่างที่ระบุไม่มีอยู่จริง |
| **500 Internal Server Error** | เกิดข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด |

**ข้อผิดพลาดที่พบบ่อย:** การใช้โดเมนฐานที่ไม่ถูกต้อง (`api.aspose.com`) หรือส่วน `/autoshapes/` ที่ล้าสมัยจะทำให้เกิดข้อผิดพลาด 404 เสมอใช้ส่วน `/shapes/` ร่วมกับโดเมน `api.aspose.cloud`

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำและช่วยให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}

สำหรับการดำเนินการที่เกี่ยวข้อง โปรดดูเอกสารประกอบสำหรับ **[การเพิ่มรูปร่าง](/shapes/add/)** และ **[การอัปเดตรูปร่าง](/shapes/update/)**