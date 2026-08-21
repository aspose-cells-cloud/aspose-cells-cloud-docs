---
title: "Aspose.Cells Cloud – แปลงสมุดงาน Excel เป็น PDF, CSV, HTML และอื่นๆ (GET /cells/{name})"
second_title: "เอกสาร"
linktitle: "แปลง Excel"
type: docs
url: /th/get-different-formats-files/
aliases:
  - /export-excel-workbook-to-different-file-formats/
  - /export-different-formats/
keywords: "Aspose.Cells, การแปลง Excel, แปลง Excel, PDF, CSV, HTML, ODS, JSON, รูปแบบภาพ, การส่งออกสเปรดชีต, API, REST"
description: "เรียนรู้วิธีดึงสมุดงาน Excel ในรูปแบบต่างๆ (PDF, CSV, HTML, PNG เป็นต้น) โดยใช้ Aspose.Cells Cloud REST API ประกอบด้วยตัวอย่าง cURL, SDK, การตรวจสอบสิทธิ์ และรายละเอียดการตอบกลับ"
weight: 10
ArticleTitle: "Aspose.Cells Cloud – แปลงสมุดงาน Excel เป็น PDF, CSV, HTML และอื่นๆ (GET /cells/{name})"
---

REST API นี้ดึงสมุดงาน Excel ในรูปแบบอื่น

## API GetWorkBook

```http
GET https://api.aspose.cloud/v3.0/cells/{name}
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์แบบใช้โทเค็น JWT</a>

### **พารามิเตอร์การสืบค้น**

| ชื่อพารามิเตอร์      | ชนิดข้อมูล | คำอธิบาย                                                                                                                                                                          | ค่าเริ่มต้น |
| --------------------- | ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- |
| format                | string     | รูปแบบไฟล์เป้าหมาย (เช่น CSV, XLS, HTML, MHTML, ODS, PDF, XML, TXT, TIFF, XLSB, XLSM, XLSX, XLTM, XLTX, XPS, PNG, JPG, GIF, EMF, BMP, MD, Numbers, WMF, SVG เป็นต้น)              | –          |
| password              | string     | รหัสผ่านที่จำเป็นในการเปิดไฟล์ Excel                                                                                                                                             | –          |
| isAutoFit             | bool       | ปรับความกว้างของแถวและคอลัมน์อัตโนมัติ                                                                                                                                          | false      |
| onlySaveTable         | bool       | เมื่อตั้งค่าเป็น **true** จะบันทึกเฉพาะข้อมูลตารางเท่านั้น รับค่า `true` หรือ `false`                                                                                              | false      |
| outPath               | string     | เส้นทางที่จะบันทึกผลลัพธ์ สำหรับไฟล์เดียวให้ระบุชื่อไฟล์และนามสกุล สำหรับหลายไฟล์ให้ระบุเฉพาะโฟลเดอร์                                                                           | –          |
| outStorageName        | string     | ชื่อพื้นที่จัดเก็บที่จะบันทึกไฟล์ผลลัพธ์                                                                                                                                         | –          |
| checkExcelRestriction | bool       | ตรวจสอบข้อจำกัดของ Excel เมื่อดัดแปลงเซลล์หรือออบเจกต์ที่เกี่ยวข้อง                                                                                                             | false      |
| region                | string     | การตั้งค่าภูมิภาคที่ใช้กับสมุดงาน                                                                                                                                                 | –          |
| pageWideFitOnPerSheet | bool       | ปรับความกว้างหน้ากระดาษให้พอดีกับแต่ละแผ่นงานเมื่อแปลงเป็น PDF                                                                                                                  | false      |
| pageTallFitOnPerSheet | bool       | ปรับความสูงหน้ากระดาษให้พอดีกับแต่ละแผ่นงานเมื่อแปลงเป็น PDF                                                                                                                    | false      |
| onePagePerSheet       | bool       | สร้างหน้า PDF หน้าเดียวต่อหนึ่งแผ่นงาน                                                                                                                                           | false      |
| folder                | string     | เส้นทางโฟลเดอร์ของสมุดงานต้นฉบับ                                                                                                                                                 | –          |
| storageName           | string     | ชื่อพื้นที่จัดเก็บที่เก็บไฟล์ต้นฉบับ                                                                                                                                              | –          |

### การตอบกลับ

**สำเร็จ (200)** 

- API จะส่งกลับออบเจกต์ **[Workbook](/cells/workbook/)** ซึ่งมีข้อมูลโครงสร้างสมุดงานเมื่อไม่ได้ระบุพารามิเตอร์การสืบค้น `format`

- API จะส่งกลับไฟล์ที่แปลงแล้วในรูปแบบที่ร้องขอเมื่อพารามิเตอร์การสืบค้น `format` ระบุประเภทไฟล์

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="book1.pdf"
Content-Length: 123456

(ข้อมูล PDF แบบไบนารี)
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                    | คำอธิบาย                                                                 |
|------|-----------------------------|--------------------------------------------------------------------------|
| 200  | สำเร็จ (OK)                 | ใช้ตัวกรองสำเร็จ; การตอบกลับประกอบด้วยรายละเอียดการดำเนินการ           |
| 400  | คำร้องขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น รูปแบบไฟล์ที่ไม่รองรับ)             |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                                            |
| 413  | ข้อมูลในคำร้องขามีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                          |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์                                  |

> **หมายเหตุ:**  
> - สมุดงานที่มีขนาดใหญ่อาจใช้เวลานานในการแปลง ควรเพิ่มเวลาหมดเขตของคำร้องขอ  
> - บางรูปแบบ (เช่น `ODS`) ไม่รองรับคุณสมบัติบางอย่างของ Excel เช่น แมโคร

## วิธีใช้ API GetWorkBook ร่วมกับ SDK

> **ข้อกำหนดเบื้องต้น:**  
> - โทเค็นการเข้าถึง JWT ที่ถูกต้องซึ่งได้มาจากการตรวจสอบสิทธิ์ของ Aspose.Cells  
> - สมุดงานต้นฉบับต้องจัดเก็บไว้ในพื้นที่จัดเก็บที่ Aspose รองรับ หรือส่งตรงในคำร้องขอ  
> - ตรวจสอบให้แน่ใจว่าเวอร์ชัน API (`v3.0`) ตรงกับเวอร์ชันที่เผยแพร่ล่าสุด

### ข้อมูลจำเพาะ API GetWorkBook

<a href="https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook" rel="noopener noreferrer">ข้อมูลจำเพาะ OpenAPI</a> กำหนดอินเทอร์เฟซการโปรแกรมที่เข้าถึงได้แบบสาธารณะและอนุญาตให้คุณดำเนินการ REST ผ่านเบราว์เซอร์เว็บได้โดยตรง

### ตัวอย่างคำร้องขอ

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ตัวอย่างต่อไปนี้แสดงคำร้องขอ GET ที่ถูกต้องพร้อมส่วนหัวการยืนยันตัวตนที่จำเป็น

{{< tabs tabTotal="1" tabID="11" tabName11="คำร้องขอ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger"
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK ซ่อนรายละเอียดระดับต่ำไว้ให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บ GitHub</a> สำหรับรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

**ดูเพิ่มเติม**

- <a href="https://apireference.aspose.cloud/cells/#/Workbook/ConvertWorkbook" rel="noopener noreferrer">แปลงสมุดงาน (POST)</a>  
- <a href="https://apireference.aspose.cloud/cells/#/Workbook/SaveAs" rel="noopener noreferrer">บันทึกเป็น (GET)</a>

---

_อัปเดตครั้งล่าสุด: 2024-12-01_

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Aspose.Cells Cloud – Convert Excel Workbook to PDF, CSV, HTML, and More (GET /cells/{name})",
  "description": "เอกสารประกอบสำหรับจุดสิ้นสุด GET /cells/{name} ของ Aspose.Cells Cloud ที่แปลงสมุดงาน Excel เป็นรูปแบบต่างๆ เช่น PDF, CSV, HTML และอื่นๆ",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2024-12-01",
  "keywords": "Aspose.Cells, การแปลง Excel, PDF, CSV, HTML, API, REST, คลาวด์",
  "url": "https://docs.aspose.cloud/cells/get-different-formats-files/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>