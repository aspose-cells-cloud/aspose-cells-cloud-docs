---
---
title: "การแปลงไฟล์ Excel ให้อยู่ในรูปแบบต่างๆ"
second_title: "เอกสาร"
linktitle: "แปลงสเปรดชีต"
type: docs
url: /convert-a-spread-file-to-different-formats/
keywords: "การแปลง Excel, การแปลงสเปรดชีต, Aspose.Cells Cloud, REST API, PDF, CSV, JSON, Markdown, การแปลงรูปแบบไฟล์"
description: "ใช้ REST API ของ Aspose.Cells Cloud เพื่อแปลงสมุดงาน Excel ให้อยู่ในรูปแบบต่างๆ เช่น PDF, CSV, JSON และ Markdown โดย API นี้รองรับ SDK หลายภาษา ได้แก่ C#, Java, Python และอื่นๆ อีกมากมาย"
weight: 10
ArticleTitle: "การแปลงไฟล์ Excel ให้อยู่ในรูปแบบต่างๆ – คู่มือ API ของ Aspose.Cells Cloud"
---

REST API นี้ใช้แปลงไฟล์ Excel ให้อยู่ในรูปแบบอื่น โดยรองรับรูปแบบผลลัพธ์หลากหลาย และอนุญาตให้ตั้งค่าการตั้งค่าหน้ากระดาษและตัวเลือกการบันทึกก่อนการแปลง

## API PostConvertWorkBook

```http
POST https://api.aspose.cloud/v3.0/cells/convert
```

ก่อนใช้ API นี้ คุณต้องมี JWT token ที่ถูกต้องและติดตั้ง SDK ของ Aspose.Cells Cloud ที่เหมาะสมสำหรับภาษาการเขียนโปรแกรมที่คุณใช้งาน

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบใช้ JWT token</a>

## วิธีใช้ API PostConvertWorkBook ร่วมกับ SDK

### ข้อมูลกำกับคุณสมบัติของ API PostConvertWorkBook

[ข้อมูลกำกับคุณสมบัติ OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostConvertWorkBook) กำหนด API ที่สามารถเข้าถึงได้แบบเปิดเผย ช่วยให้คุณสามารถโต้ตอบกับ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างด้านล่างแสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำร้องขอ" tabName12="คำตอบ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d {}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "filename",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา โดย SDK ทำหน้าที่ซ่อนรายละเอียดระดับต่ำ ให้คุณสามารถมุ่งเน้นไปที่โปรเจกต์ของคุณ ตรวจสอบ[ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud อย่างครบถ้วน

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}