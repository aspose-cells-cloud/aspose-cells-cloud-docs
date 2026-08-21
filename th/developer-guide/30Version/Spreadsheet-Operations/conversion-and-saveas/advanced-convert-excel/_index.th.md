---
title: "การแปลงไฟล์ Excel ขั้นสูง"
second_title: "เอกสาร"
linktype: "Advanced Convert"
type: docs
url: /advanced-convert-excel/
keywords: "Aspose.Cells, การแปลง Excel, Cloud API, SDK"
description: "Aspose.Cells Cloud REST API มีฟีเจอร์ที่ทรงพลังสำหรับการแปลงสมุดงาน Excel ไปยังรูปแบบต่างๆ อย่างกว้างขวาง รวมถึงการกำหนดค่าการตั้งค่าหน้ากระดาษ ตัวเลือกการบันทึก และการตั้งค่าการพิมพ์ SDK มีให้ใช้งานสำหรับ Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby และ Swift ช่วยให้การผสานรวมเป็นไปอย่างราบรื่นบนแพลตฟอร์มต่างๆ"
weight: 50
ArticleTitle: "การแปลงไฟล์ Excel ขั้นสูง – คู่มือ Aspose.Cells Cloud API"
---

## API บนคลาวด์ขั้นสูงสำหรับการแปลง Excel

การดำเนินการแปลงขั้นสูง (Advanced Convert) ช่วยให้คุณสามารถแปลงสมุดงาน Excel ไปยังรูปแบบผลลัพธ์ต่างๆ (เช่น PDF, HTML, CSV เป็นต้น) พร้อมทั้งควบคุมรายละเอียดของการตั้งค่าหน้ากระดาษ ตัวเลือกการบันทึก และการตั้งค่าการพิมพ์ได้อย่างแม่นยำ  

**ข้อกำหนดเบื้องต้น / การยืนยันตัวตน**  
ในการใช้งานจุดปลายทางนี้ คุณต้องได้รับโทเคนการเข้าถึงจาก Aspose.Cells Cloud และใส่ไว้ในส่วนหัว `Authorization` ด้วยรูปแบบ Bearer token  

**การอ้างอิง API**  
- **เมธอด:** `PUT`  
- **จุดปลายทาง (Endpoint):** `/cells/convert`  
- **พารามิเตอร์:**  
  - `format` (string, จำเป็น) – รูปแบบผลลัพธ์ที่ต้องการ (เช่น `pdf`, `html`)  
  - `outPath` (string, ไม่บังคับ) – ตำแหน่งในพื้นที่เก็บข้อมูลบนคลาวด์ที่จะบันทึกไฟล์ที่แปลงแล้ว  
  - `options` (object, ไม่บังคับ) – ออบเจกต์ JSON ที่มีตัวเลือกการแปลงขั้นสูง เช่น `pageSetup`, `saveOptions` และ `printSettings`  
- **ตัวอย่างเนื้อหาคำขอ (Request Body):**  
  ```json
  {
    "format": "pdf",
    "outPath": "output/converted.pdf",
    "options": {
      "pageSetup": {
        "orientation": "Landscape",
        "paperSize": "A4"
      },
      "saveOptions": {
        "compress": true
      },
      "printSettings": {
        "printHeadings": false
      }
    }
  }
  ```  
- **การตอบกลับ (Response):**  
  - `200 OK` – การแปลงสำเร็จ; การตอบกลับจะมีสตรีมของไฟล์ที่แปลงแล้วหรือข้อมูลอ้างอิงไปยังไฟล์ที่บันทึกไว้  
  - `400 Bad Request` – พารามิเตอร์ไม่ถูกต้องหรือเนื้อหาคำขอผิดรูปแบบ  
  - `401 Unauthorized` – การยืนยันตัวตนล้มเหลวหรือไม่มีโทเคน  
  - `500 Internal Server Error` – เกิดข้อผิดพลาดด้านเซิร์ฟเวอร์ระหว่างการแปลง  

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                      | คำอธิบาย                                        |
|------|-------------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                   | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับจะมีรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ไม่ครบหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)| โทเคน JWT ไม่ถูกต้องหรือไม่มีโทเคน             |
| 413  | ขนาดข้อมูลใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

**หมายเหตุ**  
* รูปแบบผลลัพธ์บางรูปแบบมีข้อจำกัดเฉพาะ (เช่น การแปลงเป็น HTML จะไม่รักษาแมโครไว้) กรุณาตรวจสอบเอกสารเฉพาะรูปแบบเพิ่มเติมสำหรับรายละเอียด  

### ความสามารถในการโหลดไฟล์สเปรดชีตจากแหล่งข้อมูลหลายรูปแบบ

### ตั้งค่าการตั้งค่าหน้ากระดาษและตัวเลือกการบันทึก

## ครอบครัว SDK บนคลาวด์

การใช้ SDK ช่วยเร่งกระบวนการพัฒนาโดยจัดการรายละเอียดระดับต่ำให้ ทำให้คุณสามารถมุ่งเน้นไปที่งานหลักของโครงการได้ กรุณาตรวจสอบ <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer"> khoหลักข้อมูลบน GitHub</a> เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

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

<script type="application/ld+json">
{
  "@context":"https://schema.org",
  "@type":"WebAPI",
  "name":"Aspose.Cells Cloud Advanced Convert",
  "description":"แปลงสมุดงาน Excel เป็น PDF/HTML/CSV พร้อมตัวเลือกขั้นสูง",
  "url":"https://api.aspose.cloud/v3.0/cells/convert",
  "documentation":"https://docs.aspose.cloud/cells/advanced-convert-excel/",
  "endpointDescription":"PUT /cells/convert",
  "input":{
    "@type":"PropertyValueSpecification",
    "valueRequired":true,
    "valueName":"format",
    "description":"รูปแบบผลลัพธ์ที่ต้องการ (pdf, html, csv, …)"
  },
  "target":{
    "@type":"EntryPoint",
    "urlTemplate":"https://api.aspose.cloud/v3.0/cells/convert?format={format}",
    "httpMethod":"PUT"
  }
}
</script>
---