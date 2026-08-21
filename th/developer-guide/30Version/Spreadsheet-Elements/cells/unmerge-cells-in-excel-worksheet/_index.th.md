---
title: "ยกเลิกการผสานเซลล์ในสมุดงาน Excel"
type: docs
url: /th/unmerge-cells-in-excel-worksheet/
weight: 120
keywords: "Aspose.Cells, Excel, Unmerge Cells, REST API, Cloud SDK"
description: "เรียนรู้วิธีใช้ Aspose.Cells Cloud REST API เพื่อยกเลิกการผสานเซลล์ในสมุดงาน Excel พร้อมตัวอย่างคำขอ รูปแบบการตอบกลับ และตัวอย่างโค้ด SDK สำหรับภาษาโปรแกรมต่างๆ หลายภาษา"
ArticleTitle: "ยกเลิกการผสานเซลล์ในสมุดงาน Excel"
---

REST API นี้ใช้ยกเลิกการผสานเซลล์ในไฟล์ Excel

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/unmerge
```

## การรักษาความปลอดภัยและการยืนยันตัวตน

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ [การยืนยันตัวตนด้วยโทเค็น JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)


**พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย                                             |
|----------------|--------|----------|---------------------------------------------------------|
| name           | string | path     | ชื่อไฟล์สมุดงาน                                     |
| sheetName      | string | path     | ชื่อworksheet                                      |
| startRow       | integer | query    | ดัชนีของแถวแรกที่จะยกเลิกการผสาน (เริ่มนับจาก 0)           |
| startColumn    | integer | query    | ดัชนีของคอลัมน์แรกที่จะยกเลิกการผสาน (เริ่มนับจาก 0)        |
| totalRows      | integer | query    | จำนวนแถวที่รวมอยู่ในการดำเนินการยกเลิกการผสาน    |
| totalColumns   | integer | query    | จำนวนคอลัมน์ที่รวมอยู่ในการดำเนินการยกเลิกการผสาน |
| folder         | string | query    | เส้นทางโฟลเดอร์ที่เก็บสมุดงานไว้               |
| storageName    | string | query    | ชื่อของบริการจัดเก็บข้อมูล                            |

## **การตอบกลับ**

ส่งคืน CellCloudResponse

- **ภาพรวมฟิลด์ของการตอบกลับ**

| ฟิลด์           | ประเภท    | คำอธิบาย                                           |
| --------------- | ------- | ----------------------------------------------------- |
| `Status`          | string  |                    |
| `Code`           | integer | 200,400,401,500,...                                 |


```json
{
  "Status":"OK",
  "Code":200
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | คำอธิบาย                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                          | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request)                 | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ประเภทที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)                | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | ข้อมูลส่งไปมีขนาดใหญ่เกินไป (Payload Too Large)           | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error)       | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์ |
## วิธีใช้ PostWorksheetUnmerge API ด้วย SDKs

### ข้อกำหนด PostWorksheetUnmerge API

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetUnmerge) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถโต้ตอบกับ REST ผ่านเว็บเบราว์เซอร์ได้โดยตรง

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ผ่าน cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/unmerge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ และทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [คลังข้อมูลบน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetUnmerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetUnmerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetUnmerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetUnmerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetUnmerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetUnmerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetUnmerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetUnmerge.go" >}}

{{< /tab >}}

{{< /tabs >}}
---