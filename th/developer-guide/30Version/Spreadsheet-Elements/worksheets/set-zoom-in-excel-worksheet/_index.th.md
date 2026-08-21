---
title: "ตั้งค่าการซูมสำหรับเวิร์กชีต Excel – Aspose.Cells Cloud API v3.0"
second_title: "เอกสาร"
linktitle: "การซูม"
type: docs
url: /th/worksheets/zoom/
aliases: [  /th/set-zoom-in-excel-worksheet/ ]
keywords: "Aspose.Cells, การซูม Excel, การซูมเวิร์กชีต, REST API, SDK บนคลาวด์, การประมวลผลอัตโนมัติ Excel"
description: "เรียนรู้วิธีตั้งค่าการซูมเวิร์กชีต (10–400%) โดยใช้ Aspose.Cells Cloud API v3.0 พร้อมตัวอย่าง cURL, SDK และการจัดการข้อผิดพลาด"
weight: 20
ArticleTitle: "ตั้งค่าการซูมสำหรับเวิร์กชีต Excel – Aspose.Cells Cloud API v3.0"
---

REST API นี้ใช้ตั้งค่าค่าการซูมของเวิร์กชีต Excel **จำเป็นต้องมีการยืนยันตัวตน**; ใส่โทเค็น JWT Bearer ที่ถูกต้องในส่วนหัว `Authorization` ของการร้องขอทุกครั้ง

## ความปลอดภัยและการยืนยันตัวตน
API ของ Aspose.Cells Cloud มีความปลอดภัยและจำเป็นต้องใช้ [การยืนยันตัวตนด้วยโทเค็น JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/zoom
```

### **พารามิเตอร์คำร้องขอ**

| พารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                             |
|-------------|-----------|----------|-----------------------------------------------------------------------|
| name        | สตริง      | เส้นทาง   | ชื่อไฟล์ Excel (สมุดงาน)                                            |
| sheetName   | สตริง      | เส้นทาง   | ชื่อเวิร์กชีตที่ต้องการแก้ไข                                        |
| value       | จำนวนเต็ม  | query    | เปอร์เซ็นต์การซูม (ช่วงที่อนุญาตคือ **10–400** เช่น `40` สำหรับ 40%) |
| folder      | สตริง      | query    | เส้นทางโฟลเดอร์ที่เก็บไฟล์ไว้                                       |
| storageName | สตริง      | query    | ชื่อของบริการจัดเก็บข้อมูล                                          |

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetZoom) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้สาธารณะ และอนุญาตให้คุณดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งในบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำร้องขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/zoom?value=40" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**ข้อมูลการตอบกลับข้อผิดพลาด**  
รหัสสถานะ HTTP ที่เป็นไปได้ ได้แก่:

- `400 Bad Request` – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง
- `401 Unauthorized` – โทเค็น JWT ขาดหายหรือไม่ถูกต้อง
- `404 Not Found` – ไฟล์หรือเวิร์กชีตที่ระบุไม่มีอยู่จริง
- `500 Internal Server Error` – ข้อผิดพลาดที่ไม่คาดคิดเกิดขึ้นที่เซิร์ฟเวอร์

การตอบกลับข้อผิดพลาดแต่ละครั้งจะส่งคืนเนื้อหา JSON ที่มี `Code` และ `Message` ซึ่งให้คำอธิบายโดยละเอียด

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ และช่วยให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}

{{< /tab >}}

{{< /tabs >}}