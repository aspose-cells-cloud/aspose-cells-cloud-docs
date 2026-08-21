---
title: "เพิ่มลายน้ำลงในไฟล์ Excel"
second_title: "เอกสาร"
linktype: "เพิ่มลายน้ำลงในไฟล์ Excel"
type: docs
url: /th/add-watermark-into-excel-files/
aliases: [  /th/watermark/ ]
keywords: "เพิ่มลายน้ำลงใน Excel, Aspose.Cells Cloud, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "เรียนรู้วิธีการเพิ่มลายน้ำข้อความลงในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API (เวอร์ชัน 3.0) รวมถึงตัวอย่าง cURL พารามิเตอร์ที่จำเป็น และรายละเอียดการตอบกลับ"
weight: 39
ArticleTitle: "เพิ่มลายน้ำลงในไฟล์ Excel – เอกสารประกอบ Aspose.Cells Cloud"
---

REST API นี้จะเพิ่ม **ลายน้ำ** ลงในไฟล์ Excel

**ข้อกำหนดเบื้องต้น:** คุณต้องได้รับโทเค็น JWT ที่ถูกต้อง และไฟล์ Excel ต้องอยู่ในรูปแบบที่รองรับ (เช่น `.xlsx`, `.xls`)  
**พื้นฐาน:** ลายน้ำคือข้อความแบบโปร่งแสงครึ่งหนึ่งที่ถูกวางทับบนแต่ละแผ่นงาน เพื่อระบุความเป็นเจ้าของหรือความลับ

## API PostWatermark

```http
POST https://api.aspose.cloud/v3.0/cells/watermark
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/th/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์แบบใช้โทเค็น JWT</a>

### **พารามิเตอร์ของคำขอ**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง                     | คำอธิบาย                                                     |
| ---------------- | ---------- | ---------------------------- | ------------------------------------------------------------ |
| `file`           | ไฟล์       | formData (เนื้อหาแบบ multipart) | ไฟล์ Excel ที่จะใส่ลายน้ำ                                   |
| `text`           | สตริง       | query                        | ข้อความลายน้ำที่จะแสดง                                      |
| `color`          | สตริง       | query                        | สีของลายน้ำในรูปแบบเลขฐานสิบหกแบบ ARGB (เช่น `004433ff`) |

### **การตอบกลับ**

การตอบกลับแบบ JSON จะมีอาร์เรย์ **Files** ซึ่งแต่ละออบเจกต์ไฟล์จะมีข้อมูลดังนี้:

- **Filename** – ชื่อของสมุดงานที่ประมวลผลแล้ว  
- **FileSize** – ขนาดไฟล์เป็นไบต์  
- **FileContent** – เนื้อหาของไฟล์ Excel ที่ใส่ลายน้ำแล้วที่ถูกเข้ารหัสแบบ Base64; คุณต้องถอดรหัสเพื่อให้ได้ไฟล์จริง

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Files": [
        {
            "Filename" : "[ชื่อไฟล์1]",
            "Filesize" : [ขนาดไฟล์],
            "FileContent" : "[Base64String]"
        },        {
            "Filename" : "[ชื่อไฟล์2]",
            "Filesize" : [ขนาดไฟล์],
            "FileContent" : "[Base64String]"
        },        {
            "Filename" : "[ชื่อไฟล์3]",
            "Filesize" : [ขนาดไฟล์],
            "FileContent" : "[Base64String]"
        }
    ]
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                   | คำอธิบาย                                                |
|------|-----------------------------|---------------------------------------------------------|
| 200  | สำเร็จ (OK)                | ลายน้ำถูกใส่เรียบร้อยแล้ว การตอบกลับมีรายละเอียดของคำสั่ง |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                             |
| 413  | ข้อมูลที่ส่งมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                           |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                    |

## วิธีการใช้ API PostWatermark ร่วมกับ SDK

### ข้อมูลเฉพาะของ API PostWatermark

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostWatermark) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้จากภายนอก และช่วยให้คุณสามารถสื่อสารผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ **cURL** ที่อยู่ในรูปแบบคำสั่งเพื่อเรียกใช้บริการเว็บของ Aspose.Cells ตัวอย่างต่อไปนี้แสดงคำขอที่สมบูรณ์ รวมถึงส่วนหัวการตรวจสอบสิทธิ์ที่จำเป็น แทนที่ `<your-jwt-token>` ด้วยโทเค็น JWT ที่ถูกต้องที่ได้รับจากปลายทางการตรวจสอบสิทธิ์ของ Aspose

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/watermark?text=aspose.cells.cloud&color=004433ff" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample_watermarked.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK ช่วยซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณได้ โปรดตรวจสอบ [คลังข้อมูล GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWatermark.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWatermark.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWatermark.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWatermark.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWatermark.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWatermark.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWatermark.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWatermark.go" >}}

{{< /tab >}}

{{< /tabs >}}