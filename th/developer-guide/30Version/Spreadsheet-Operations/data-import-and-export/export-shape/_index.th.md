---
---
title: "ส่งออกรูปร่าง"
second_title: "เอกสาร"
linktitle: "รูปร่าง"
type: docs
url: /export-excel-shape-to-different-formats/
aliases: [/export/excel-shape-to-different-formats/]
keywords: "การส่งออกชาร์ต, Aspose.Cells Cloud, การส่งออกชาร์ต Excel, รูปแบบภาพ, REST API, SDK"
description: "เรียนรู้วิธีการส่งออกชาร์ต Excel ไปยังรูปแบบภาพต่างๆ (PNG, GIF, JPEG, BMP, SVG, TIFF, EMF, WMF) โดยใช้ Aspose.Cells Cloud REST API และ SDK"
weight: 20
ArticleTitle: "ส่งออกชาร์ต – Aspose.Cells Cloud"
---

การส่งออกชาร์ตจาก Excel ช่วยให้คุณสามารถนำเนื้อหาแบบแผนภาพกลับมาใช้ใหม่ได้บนแพลตฟอร์มและแอปพลิเคชันต่างๆ **ข้อกำหนดเบื้องต้น:** ต้องมีโทเคน JWT ที่ถูกต้อง และไฟล์ Excel ต้นฉบับที่ต้องการอัปโหลด

คุณสามารถส่งออกชาร์ตไปยังรูปแบบต่อไปนี้: **PNG**, **GIF**, **JPEG**, **BMP**, **SVG**, **TIFF**, **EMF**, **WMF**

## API PostExport

```http
PUT https://api.aspose.cloud/v3.0/cells/export
```

### **การรักษาความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบใช้โทเคน JWT</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ประเภท   | เส้นทาง/สตริงคำสั่ง/เนื้อหา HTTP Body | จำเป็น | คำอธิบาย |
|----------------|--------|-----------------------------|----------|-------------|
| file           | ไฟล์   | formData                    | ใช่     | ไฟล์ที่ต้องการอัปโหลด |
| objectType     | สตริง | query                       | ใช่     | ประเภทของวัตถุที่ต้องการส่งออก สำหรับการส่งออกชาร์ตให้ใช้ `chart` ค่าที่ใช้ได้รวมถึง `shape`, `worksheet`, `picture` เป็นต้น |
| format         | สตริง | query                       | ใช่     | รูปแบบผลลัพธ์ที่ต้องการ ค่าที่รองรับ: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf` |

### **ตัวอย่างคำขอ**

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### คำตอบ

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1_Shapes_0.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    }
    // ... ออบเจกต์ไฟล์เพิ่มเติม ...
  ]
}
```

*เนื้อหาไฟล์ที่เข้ารหัสด้วย Base64 โดยทั่วไปมีขนาดตั้งแต่ไม่กี่ร้อยไบต์ไปจนถึงหลายเมกะไบต์ ขึ้นอยู่กับขนาดและรูปแบบของภาพ*

**รหัสสถานะ HTTP**

| รหัส | ความหมาย               | คำอธิบาย |
|------|-----------------------|-------------|
| 200  | สำเร็จ (OK)                    | ส่งออกชาร์ตเรียบร้อยแล้ว; คำตอบจะประกอบด้วยรายชื่อไฟล์ |
| 400  | คำขอไม่ถูกต้อง (Bad Request)           | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)          | โทเคนเข้าถึงไม่ถูกต้องหรือขาดหาย |
| 413  | เนื้อหาคำขอใหญ่เกินไป (Payload Too Large)     | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

## วิธีใช้ API PostExport ด้วย SDK

### ข้อมูลจำเพาะ API PostExport

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้จากภายนอก และช่วยให้คุณสามารถโต้ตอบกับ REST API ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ API บนคลาวด์ผ่าน cURL:

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนาแอปพลิเคชันที่ใช้ Aspose.Cells Cloud SDK ช่วยซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจได้ ดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud ได้ที่ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud)

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportShape.go" >}}

{{< /tab >}}

{{< /tabs >}}