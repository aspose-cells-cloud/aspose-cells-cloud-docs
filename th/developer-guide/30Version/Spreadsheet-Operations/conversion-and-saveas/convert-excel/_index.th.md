---
title: "การแปลงไฟล์ Excel ไปยังรูปแบบต่างๆ"
ArticleTitle: "การแปลงไฟล์ Excel ไปยังรูปแบบต่างๆ"
second_title: "เอกสาร"
linktype: "แปลง Excel"
type: docs
url: /convert-an-excel-file-to-different-formats/
aliases:
  [
    "/convert-excel-workbook-to-different-file-formats/",
    "/convert/excel-to-different-formats/",
  ]
keywords: "Aspose.Cells Cloud, การแปลง Excel, การแปลงรูปแบบไฟล์, REST API, SDK, CSV, PDF, HTML, JSON, Markdown"
description: "แปลงสมุดงาน Excel ไปยังรูปแบบต่างๆ เช่น CSV, PDF, HTML, JSON, Markdown และอื่นๆ โดยใช้ Aspose.Cells Cloud REST API"
weight: 10
---

ก่อนเรียกใช้จุดปลายทางนี้ คุณต้องตรวจสอบให้แน่ใจว่าได้รับโทเค็น JWT ที่ถูกต้องแล้ว และสมุดงานต้นทางถูกเก็บไว้ในตำแหน่งที่จัดเก็บที่รองรับ (เช่น Aspose Cloud Storage) รวมโทเค็นไว้ในส่วนหัว `Authorization` และหากจำเป็น ให้ระบุพารามิเตอร์คิวรี `storageName`

REST API นี้แปลงไฟล์ Excel ไปยังรูปแบบเอาต์พุตต่างๆ

## PutConvertWorkBook API

```http
PUT https://api.aspose.cloud/v3.0/cells/convert
```

คำขอคือ HTTP **PUT** ที่มีเนื้อหาแบบมัลติพาร์ท (ดู [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) หรือ [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html))  
ส่วนแรกของเนื้อหาแบบมัลติพาร์ตประกอบด้วย **ไฟล์ข้อมูล** และส่วนที่สองประกอบด้วย **ตัวเลือกการบันทึก**

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### พารามิเตอร์คิวรี

| ชื่อพารามิเตอร์        | ชนิดข้อมูล | คำอธิบาย                                                                                                                          |
| ----------------------- | --------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| `format`                | สตริง     | รูปแบบไฟล์เป้าหมาย (เช่น CSV, XLS, HTML, PDF, XML, TXT, TIFF, PNG, JPG, GIF, EMF, BMP, MD, Numbers, WMF, SVG เป็นต้น)               |
| `password`              | สตริง     | รหัสผ่านที่จำเป็นในการเปิดไฟล์ Excel ต้นทาง                                                                                       |
| `outPath`               | สตริง     | พาธแบบเต็ม (รวมชื่อไฟล์และส่วนขยาย) สำหรับไฟล์เอาต์พุตเดี่ยว หรือพาธโฟลเดอร์เมื่อมีการสร้างไฟล์หลายไฟล์                             |
| `storageName`           | สตริง     | ชื่อของพื้นที่จัดเก็บที่ไฟล์ต้นทางอยู่                                                                                             |
| `checkExcelRestriction` | บูลีน     | เมื่อตั้งค่าเป็น **true** จะตรวจสอบข้อจำกัดของ Excel ก่อนแก้ไขเซลล์หรือออบเจกต์ที่เกี่ยวข้อง                                        |
| `streamFormat`          | สตริง     | รูปแบบสตรีมของไฟล์ต้นทาง                                                                                                          |
| `region`                | สตริง     | การตั้งค่าภูมิภาคที่ใช้กับสมุดงาน                                                                                                  |
| `pageWideFitOnPerSheet` | บูลีน     | ปรับความกว้างของหน้าให้พอดีกับแต่ละแผ่นงานเมื่อแปลงเป็น PDF                                                                       |
| `pageTallFitOnPerSheet` | บูลีน     | ปรับความสูงของหน้าให้พอดีกับแต่ละแผ่นงานเมื่อแปลงเป็น PDF                                                                         |
| `sheetName`             | สตริง     | ชื่อของแผ่นงานที่จะแปลง                                                                                                           |
| `pageIndex`             | สตริง     | ดัชนีของหน้าที่จะแปลง (ต้องระบุ `sheetName`)                                                                                       |
| `onePagePerSheet`       | บูลีน     | เมื่อตั้งค่าเป็น **true** จะสร้างหน้า PDF หน้าเดียวต่อหนึ่งแผ่นงาน                                                                  |
| `AutoRowsFit`           | บูลีน     | ปรับขนาดแถวให้พอดีอัตโนมัติในสมุดงาน                                                                                             |
| `AutoColumnsFit`        | บูลีน     | ปรับความกว้างคอลัมน์ให้พอดีอัตโนมัติในสมุดงาน                                                                                     |

### พารามิเตอร์เนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย                                                     |
| ---------------- | --------- | ------------------------------------------------------------- |
| `datafile`       | ไฟล์ข้อมูล | ไฟล์ Excel ที่ใส่ไว้ในส่วนแรกของเนื้อหาแบบมัลติพาร์ต          |
| `SaveOptions`    | ออบเจกต์  | ตัวเลือกการบันทึกที่ใส่ไว้ในส่วนที่สองของเนื้อหาแบบมัลติพาร์ต |

### **การตอบกลับ**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย                                                                 |
|------|------------------------------|--------------------------------------------------------------------------|
| 200  | คำขอสำเร็จ (OK)             | กรองถูกนำไปใช้สำเร็จ; การตอบกลับประกอบด้วยรายละเอียดการดำเนินการ      |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น รูปแบบไฟล์ที่ไม่รองรับ)            |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                                          |
| 413  | เนื้อหาข้อมูลมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด                               |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                                 |

## วิธีใช้ PutConvertWorkBook API ร่วมกับ SDK

### ข้อกำหนด PutConvertWorkBook API

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) นิยามอินเทอร์เฟซที่เข้าถึงได้สาธารณะ ซึ่งช่วยให้สามารถโต้ตอบกับ REST โดยตรงจากเว็บเบราว์เซอร์ได้

### ตัวอย่าง cURL

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=html" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK จะเร่งความเร็วการพัฒนาได้โดยจัดการรายละเอียดระดับต่ำให้ ช่วยให้คุณมุ่งเน้นไปที่ตรรกะของธุรกิจ ดู [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บ Aspose.Cells ด้วย SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "ExamplePutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "ExamplePutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "ExamplePutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ExamplePutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "ExamplePutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "ExamplePutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}