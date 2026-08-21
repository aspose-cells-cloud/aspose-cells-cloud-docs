---
title: "เพิ่มรูปร่างลงในสมุดงาน Excel"
second_title: "เอกสาร"
linktitle: "เพิ่ม"
type: docs
url: /th/shapes/add/
aliases: [  /th/add-a-shape-inside-the-worksheet/ ]
keywords: "Aspose.Cells, เพิ่มรูปร่าง, Excel, REST API, คลาวด์ SDK, shapeDTO, ประเภทการวาดภาพ"
description: "เรียนรู้วิธีการเพิ่มรูปร่าง (เช่น โค้ง สาย รูปสี่เหลี่ยม เป็นต้น) ลงในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API เวอร์ชัน 3.0 ประกอบด้วยไวยากรณ์คำขอ พารามิเตอร์ที่จำเป็น ขั้นตอนการตรวจสอบสิทธิ์ และตัวอย่างโค้ด SDK"
weight: 30
ArticleTitle: "เพิ่มรูปร่างลงในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud API"
---

API REST นี้จะเพิ่มรูปร่างลงในสมุดงาน Excel  
จุดปลายทางนี้จัดอยู่ใน **เวอร์ชัน API v3.0**; ตรวจสอบให้แน่ใจว่าคุณใช้โทเค็น JWT ที่ได้รับจากขั้นตอน OAuth2 ของ Aspose Cloud (client-id/client-secret) และใส่ไว้ในส่วนหัว `Authorization: Bearer <token>`

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์ด้วยโทเค็น JWT</a>

## PutWorksheetShape API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### **พารามิเตอร์ของคำขอ**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
|------------------|-----------|---------|----------|
| name             | string    | path    | ชื่อเอกสาร |
| sheetName        | string    | path    | ชื่อชีตงาน |
| shapeDTO         | object    | body    | ออบเจกต์ JSON ที่อธิบายรูปร่างที่จะเพิ่ม (ดูข้อมูลจำเพาะ OpenAPI เพื่อดูโครงสร้างแบบเต็ม) |
| drawingType      | string    | query   | ชนิดของออบเจกต์รูปร่าง (เช่น `arc`, `line`, `rectangle`) |
| upperLeftRow     | integer   | query   | ดัชนีแถวบนซ้ายของรูปร่าง |
| upperLeftColumn  | integer   | query   | ดัชนีคอลัมน์บนซ้ายของรูปร่าง |
| top              | integer   | query   | ระยะห่างแนวตั้งจากขอบบนของรูปร่างเป็นพิกเซล |
| left             | integer   | query   | ระยะห่างแนวนอนจากขอบซ้ายของรูปร่างเป็นพิกเซล |
| width            | integer   | query   | ความกว้างของรูปร่างเป็นพิกเซล |
| height           | integer   | query   | ความสูงของรูปร่างเป็นพิกเซล |
| folder           | string    | query   | โฟลเดอร์ที่เก็บเอกสารไว้ |
| storageName      | string    | query   | ชื่อพื้นที่จัดเก็บ |

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Shapes/PutWorksheetShape) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการโต้ตอบ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง cURL เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API คลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?DrawingType=arc&upperLeftRow=1&upperLeftColumn=1&top=1&left=1&width=100&height=100" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "ShapeId": 5
}
```

_การตอบกลับที่สำเร็จจะส่งกลับโค้ดสถานะ HTTP ข้อความสถานะ และตัวระบุของรูปร่างที่สร้างขึ้นใหม่ (`ShapeId`)_

{{< /tab >}}

{{< /tabs >}}

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                   | คำอธิบาย |
|-----|-----------------------------|----------|
| 200 | OK (สำเร็จ)                | ตัวกรองถูกใช้งานเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของ operation |
| 400 | Bad Request (คำขอล้มเหลว)  | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401 | Unauthorized (ไม่ได้รับอนุญาต) | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย |
| 413 | Payload Too Large (ข้อมูลหนักเกินไป) | ไฟล์ที่อัปโหลดเกินขีดจำกัดขนาด |
| 500 | Internal Server Error (ข้อผิดพลาดภายในเซิร์ฟเวอร์) | เกิดข้อผิดพลาดที่ไม่คาดคิดในเซิร์ฟเวอร์ |

การตอบกลับข้อผิดพลาดทั่วไปประกอบด้วย:

- **400 Bad Request** – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง  
- **401 Unauthorized** – โทเค็น JWT ไม่ถูกต้องหรือขาดหาย  
- **404 Not Found** – ชีตงานหรือเอกสารที่ระบุไม่มีอยู่จริง

ข้อผิดพลาดแต่ละประเภทจะถูกส่งกลับในรูปแบบออบเจกต์ JSON ที่มีฟิลด์ `Code` และ `Message`

## ครอบครัว SDK สำหรับคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ ให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}