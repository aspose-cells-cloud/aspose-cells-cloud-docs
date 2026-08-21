---
title: "การแปลง Excel เป็น TIFF"
second_title: "เอกสาร"
linketitle: "Excel to TIFF"
type: docs
url: /convert-excel-file-to-tiff-file/
aliases: [/convert-excel-file-to-tiff-in-cloud/, /convert/excel-to-tiff/]
keywords: "Aspose.Cells Cloud, การแปลง Excel เป็น TIFF, REST API, cURL, SDK, .NET, Java, Python, การส่งออกภาพ"
description: "เรียนรู้วิธีการแปลงสมุดงาน Excel เป็นภาพ TIFF คุณภาพสูงด้วย API ของ Aspose.Cells Cloud พร้อมตัวอย่างคำสั่ง cURL, SDK (C#, Java, Python, ฯลฯ), ขั้นตอนการตรวจสอบสิทธิ์ และการจัดการข้อผิดพลาด"
weight: 90
---

จุดปลายทาง **Convert**, **SaveAs**, และ **Export** ของ Aspose.Cells Cloud ช่วยให้คุณแปลงสมุดงาน Excel เป็นภาพ TIFF ได้  
คุณสามารถเรียกใช้จุดปลายทางเหล่านี้โดยตรงผ่าน **cURL** หรือผ่าน SDK ที่รองรับหนึ่งในนั้น

## REST API

| **API**                | **Method** | **วัตถุประสงค์**                                                                                   | **ลิงก์ Swagger**                                                                           |
| ---------------------- | ---------- | -------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `/cells/convert`       | PUT        | แปลงสมุดงานที่ส่งมาในเนื้อหาคำขอ (request body) เป็นรูปแบบที่ระบุ (TIFF)                         | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |
| `/cells/{name}`        | GET        | ส่งออกสมุดงานที่ระบุชื่อไปยังรูปแบบอื่น (TIFF) และส่งผลลัพธ์กลับมาในการตอบกลับ (response)         | [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)               |
| `/cells/{name}/saveAs` | POST       | บันทึกสมุดงานในรูปแบบที่เลือก (TIFF) และจัดเก็บผลลัพธ์ไว้ในพื้นที่จัดเก็บบนคลาวด์                 | [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)   |

จุดปลายทางเหล่านี้สามารถเข้าถึงได้แบบสาธารณะ และสามารถเรียกใช้งานได้โดยตรงจากเว็บเบราว์เซอร์หรือไคลเอนต์ HTTP ใดๆ

### ตัวอย่าง cURL

{{< tabs tabTotal="3" tabID="11" tabName11="convert" tabName12="saveas" tabName13="export">}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/convert?format=tiff" \
     -X PUT \
     -d '{"File":{"Name":"book1.xlsx","Data":"<เนื้อหา-base64>"},"SaveFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx/saveas?newfilename=book1.tiff" \
     -X POST \
     -d '{"SaveFormat":"tiff","ImageFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="13" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=tiff" \
     -X GET \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< /tabs >}}

> **หมายเหตุ:**
>
> - เนื้อหาคำขอ (request body) สำหรับ **Convert** ต้องมีไฟล์ (หรือข้อมูลอ้างอิงถึงไฟล์ที่จัดเก็บไว้) และ `SaveFormat` ที่ต้องการ
> - การส่งออก (Export) ไม่จำเป็นต้องมีเนื้อหาคำขอ (request body) โดยรูปแบบจะถูกระบุผ่าน query string (`format=tiff`)

## การจัดการข้อผิดพลาด

| **Status Code** | **ความหมาย**        | **สาเหตุทั่วไป**                            |
| --------------- | -------------------- | ------------------------------------------- |
| 200             | สำเร็จ              | ส่งคืนภาพ TIFF (สตรีมแบบไบนารี)             |
| 400             | คำขอไม่ถูกต้อง      | พารามิเตอร์ขาดหายหรือมีรูปแบบผิดพลาด      |
| 401             | ไม่ได้รับอนุญาต      | JWT token ไม่ถูกต้องหรือขาดหาย              |
| 404             | ไม่พบ                | สมุดงานที่ระบุไม่มีอยู่                     |
| 500             | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน | เงื่อนไขที่ไม่คาดคิดภายในเซิร์ฟเวอร์        |

เมื่อเกิดข้อผิดพลาด API จะส่งกลับ payload JSON ที่มี `Code`, `Message` และอาจมี `Description` ประกอบอยู่ด้วย

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา โดย SDK จะจัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นที่โครงการของคุณได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ผ่าน SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbookToTiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbookToTiff.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbookToTiff.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbookToTiff.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbookToTiff.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbookToTiff.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbookToTiff.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbookToTiff.go" >}}

{{< /tab >}}

{{< /tabs >}}