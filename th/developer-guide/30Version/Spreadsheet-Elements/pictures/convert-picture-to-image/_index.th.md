---
title: "Aspose.Cells Cloud API – ดึงภาพจากแผ่นงาน"
second_title: "เอกสาร"
linktype: "ดึง"
type: docs
url: /th/pictures/get/
aliases: [  /th/convert-picture-to-image/ ]
keywords: "Aspose.Cells, ดึงภาพ, API, Excel, Cloud, REST"
description: "ดึงภาพที่ระบุจากแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API ซึ่งรวมถึง endpoint, พารามิเตอร์, ขั้นตอนการยืนยันตัวตน, รหัสการตอบกลับ และตัวอย่างโค้ด"
weight: 10
ArticleTitle: "Aspose.Cells Cloud API – ดึงภาพจากแผ่นงาน"
---

REST API นี้ดึงภาพโดยใช้ดัชนีแบบเริ่มต้นที่ศูนย์ (zero-based index) จากแผ่นงาน Excel

## REST API

เพื่อเรียก endpoint นี้ คุณต้องใส่ JWT access token ที่ถูกต้องใน header **Authorization** token ได้รับจากกระบวนการยืนยันตัวตนของ Aspose.Cells Cloud และต้องมี scope ที่เหมาะสมสำหรับการเข้าถึงไฟล์ สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับการรับ token โปรดดูคู่มือ **Authentication** โดยรวม

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท    | ตำแหน่ง | คำอธิบาย                                                                                                         |
| ---------------- | --------- | -------- | ------------------------------------------------------------------------------------------------------------------- |
| name             | string    | path     | ชื่อเอกสาร Excel                                                                                                   |
| sheetName        | string    | path     | ชื่อแผ่นงาน                                                                                                        |
| pictureIndex     | integer   | path     | ดัชนีแบบเริ่มต้นที่ศูนย์ของภาพ                                                                                      |
| format           | string    | query    | รูปแบบการส่งออกที่ต้องการ (เช่น png, jpg, bmp, gif, tiff) หากไม่ระบุ ภาพจะถูกส่งกลับในรูปแบบดั้งเดิม                 |
| folder           | string    | query    | โฟลเดอร์ที่เก็บเอกสาร                                                                                               |
| storageName      | string    | query    | ชื่อของตำแหน่งจัดเก็บ                                                                                              |

### การตอบกลับข้อผิดพลาด

| HTTP Code | คำอธิบาย                                                                 |
| --------- | -------------------------------------------------------------------------- |
| 401       | ไม่ได้รับอนุญาต – ไม่มี token หรือ token ไม่ถูกต้อง                              |
| 404       | ไม่พบ – ไฟล์ แผ่นงาน หรือดัชนี page-break ที่ระบุไม่มีอยู่จริง                     |
| 400       | คำขอไม่ถูกต้อง – รูปแบบคำขอหรือพารามิเตอร์ไม่ถูกต้อง                              |
| 500       | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – พบเงื่อนไขที่ไม่คาดคิด                               |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPicture) กำหนด programming interface ที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการ REST interactions ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
# ข้อมูลภาพไบนารี (PNG) ที่ส่งกลับในส่วน body ของการตอบกลับ
# ตัวอย่าง: ข้อมูลย่อยที่เข้ารหัสแบบ base64
iVBORw0KGgoAAAANSUhEUgAA...
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นที่โปรเจกต์ของคุณได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPictureWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPictureWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPictureWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "ExampleGetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "ExampleGetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ExampleGetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "ExampleGetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "ExampleGetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}