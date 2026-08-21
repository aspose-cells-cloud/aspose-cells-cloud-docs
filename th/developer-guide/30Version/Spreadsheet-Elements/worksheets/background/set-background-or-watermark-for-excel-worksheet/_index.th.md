---
title: "ตั้งค่าพื้นหลังในแผ่นงาน Excel"
ArticleTitle: "ตั้งค่าพื้นหลังในแผ่นงาน Excel – คู่มือ API ของ Aspose.Cells Cloud"
second_title: "เอกสาร"
linktype: "เพิ่ม"
type: docs
url: /worksheets/background/add/
aliases: [/set-background-or-watermark-for-excel-worksheet/]
keywords: "Aspose.Cells, Excel, แผ่นงาน, พื้นหลัง, REST API, SDK, เพิ่มรูปภาพ"
description: "เรียนรู้วิธีเพิ่มรูปภาพพื้นหลัง (PNG, JPEG, BMP) ลงในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API ซึ่งรวมถึง endpoint, พารามิเตอร์ที่จำเป็น, ขั้นตอนการยืนยันตัวตน, ตัวอย่าง cURL และตัวอย่างโค้ด SDK"
weight: 180
---

REST API นี้จะเพิ่มรูปภาพพื้นหลังลงในแผ่นงาน

## ความปลอดภัยและการยืนยันตัวตน
API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ [การยืนยันตัวตนด้วยโทเค็น JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/background
```

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย                                                   |
| ---------------- | ------ | -------- | ----------------------------------------------------------- |
| name             | string | path     | ชื่อสมุดงาน Excel                                          |
| sheetName        | string | path     | ชื่อแผ่นงานที่จะนำรูปภาพไปใช้                             |
| imageFile        | file   | body     | ไฟล์รูปภาพแบบไบนารี (PNG, JPEG, BMP เป็นต้น) ที่จะตั้งเป็นพื้นหลัง |
| folder           | string | query    | โฟลเดอร์ในพื้นที่จัดเก็บที่สมุดงานตั้งอยู่                  |
| storageName      | string | query    | ชื่อของพื้นที่จัดเก็บ Aspose Cloud                         |

**รูปแบบที่รองรับและข้อจำกัด**

- นามสกุลภาพที่ยอมรับ: **PNG, JPEG, BMP, GIF**
- ขนาดไฟล์สูงสุด: **5 MB**
- รูปภาพจะถูกทำซ้ำ (tiled) เพื่อเติมพื้นหลังของแผ่นงานทั้งหมด

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetBackground) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการโต้ตอบ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งใน command-line เพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/background" \
  -X PUT \
  -F "imageFile=@Creative.jpg" \
  -H "Content-Type: multipart/form-data" \
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

*การตอบกลับข้อผิดพลาดที่เป็นไปได้*

| HTTP Code | คำอธิบาย                                           |
| --------- | --------------------------------------------------- |
| 400       | คำขอไม่ถูกต้อง – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง |
| 401       | ไม่ได้รับอนุญาต – โทเค็น JWT ไม่ถูกต้องหรือหมดอายุ |
| 404       | ไม่พบ – สมุดงานหรือแผ่นงานไม่มีอยู่จริง           |
| 500       | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เงื่อนไขที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ และช่วยให้คุณมุ่งเน้นไปที่งานโครงการของคุณ โปรดตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกเว็บเซอร์วิสของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}