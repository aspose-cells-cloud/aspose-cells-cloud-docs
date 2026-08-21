---
---
title: "การแปลงสมุดงาน – เอกสารประกอบ API ของ Aspose.Cells Cloud"
second title: "เอกสาร"
ArticleTitle: "วิธีแปลงข้อมูลสมุดงานในไฟล์ Excel ที่อยู่ในเครื่องเป็นไฟล์รูปภาพ: คู่มือแบบทีละขั้นตอน"
linktitle: "แปลงสมุดงานเป็นรูปภาพ"
type: docs
url: /convert-worksheet-to-image/
keywords: "Aspose.Cells Cloud, แปลงสมุดงานเป็นรูปภาพ, แปลงสมุดงานเป็นรูปภาพ, Excel เป็น PNG, Excel เป็น SVG, Excel เป็น TIFF, Excel เป็น JPEG, Excel เป็น BMP, API สำหรับแปลงรูปภาพ, REST API, การส่งออกสมุดงานเป็นรูปภาพ, ตัวอย่าง SDK"
description: "คู่มือแบบทีละขั้นตอนในการแปลงสมุดงาน Excel เป็นรูปแบบไฟล์รูปภาพ (PNG, SVG, TIFF, JPEG, BMP เป็นต้น) โดยใช้ API ของ Aspose.Cells Cloud ซึ่งประกอบด้วยพารามิเตอร์ของคำขอ, รายละเอียดของคำตอบ, โค้ดข้อผิดพลาด, สถานการณ์การใช้งาน และตัวอย่างโค้ด SDK"
weight: 100
---

ส่งออกข้อมูลจากสมุดงานในไฟล์ Excel ที่อยู่ในเครื่องไปยังไฟล์ [รูปภาพ](https://docs.fileformat.com/image/) โดยใช้ API ของ Aspose.Cells Cloud การดำเนินการนี้รองรับรูปแบบไฟล์รูปภาพหลายรูปแบบและเหมาะสำหรับการสร้างภาพสแนปช็อตของข้อมูลในสมุดงาน

**รูปแบบภาพที่รองรับ**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **API สำหรับแปลงสมุดงานเป็นรูปภาพ**

### **Web API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/worksheet/image
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### **พารามิเตอร์ของคำขอ**

| ชื่อพารามิเตอร์ | ประเภท | Path/Query String/HTTPBody | คำอธิบาย                                                                 |
| :------------- | :----- | :------------------------- | :----------------------------------------------------------------------- |
| Spreadsheet    | ไฟล์  | FormData                   | อัปโหลดไฟล์สมุดงาน                                                       |
| worksheet      | สตริง | Query                      | ชื่อของสมุดงานที่ต้องการแปลง                                            |
| format         | สตริง | Query                      | รูปแบบภาพที่ต้องการ (`svg`, `png`, `tiff`, `jpeg`, `bmp`, เป็นต้น)     |
| outPath        | สตริง | Query                      | _(ไม่บังคับ)_ ที่อยู่โฟลเดอร์ที่จะบันทึกไฟล์ภาพผลลัพธ์; ค่าเริ่มต้นคือ `null` |
| outStorageName | สตริง | Query                      | ชื่อของสถานที่จัดเก็บไฟล์ผลลัพธ์                                         |
| fontsLocation  | สตริง | Query                      | ที่อยู่โฟลเดอร์ฟอนต์ที่กำหนดเอง กรณีที่ต้องการใช้ฟอนต์ที่ไม่มีในเซิร์ฟเวอร์ |
| region         | สตริง | Query                      | การตั้งค่าภูมิภาคของสมุดงาน (เช่น `en-US`)                               |
| password       | สตริง | Query                      | รหัสผ่านที่จำเป็นสำหรับการเปิดไฟล์สมุดงานที่ได้รับการป้องกัน            |

### **คำตอบ**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย               | คำอธิบาย                                                             |
| ---- | --------------------- | ------------------------------------------------------------------- |
| 200  | สำเร็จ (OK)           | ประมวลผลคำขอสำเร็จ; คำตอบประกอบด้วยรายละเอียดของการดำเนินการ    |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ไม่ครบหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)            |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | JWT token ไม่ถูกต้องหรือไม่มี                                          |
| 413  | ข้อมูลในคำขอใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                   |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                            |

## **ควรใช้ API แปลงสมุดงานเป็นรูปภาพในกรณีใด?**

- **ภาพสแนปช็อตของรายงานคงที่** – แปลงตารางข้อมูลทางการเงิน การคำนวณ หรือข้อมูลอื่นๆ เป็นรูปภาพเพื่อใส่ลงในรายงาน PDF สไลด์ PowerPoint หรือเอกสารพิมพ์ที่ไม่จำเป็นต้องแก้ไขต่อ
- **การนำเสนอข้อมูลในรูปภาพสำหรับงานนำเสนอ** – แปลงตารางสมุดงานที่ซับซ้อน (รวมถึงการจัดรูปแบบตามเงื่อนไขหรือกราฟแบบง่าย) เป็นรูปภาพที่สามารถฝังลงในการนำเสนอ (PPTX, Google Slides)
- **เอกสารประกอบและสื่อการฝึกอบรม** – บันทึกตัวอย่างสมุดงาน แม่แบบ หรือแบบฟอร์มป้อนข้อมูลเป็นรูปภาพสำหรับคู่มือผู้ใช้ คู่มือการใช้งาน หรือบทความฐานความรู้
- **ภาพตัวอย่างขนาดย่อ (Thumbnail Previews)** – สร้างภาพขนาดย่อของส่วนสำคัญของสมุดงานสำหรับใช้ในเบราว์เซอร์ไฟล์ คลังเอกสาร หรือผลลัพธ์การค้นหา

## **ทำไมควรใช้ API แปลงสมุดงานเป็นรูปภาพ?**

- **เป็นมิตรกับนักพัฒนา** – Aspose.Cells Cloud มี SDK ในหลายภาษา ช่วยให้พัฒนาได้อย่างรวดเร็ว และมีเอกสารประกอบที่ครบถ้วน เมื่อเทียบกับการสร้างโซลูชันสำหรับการเรนเดอร์กราฟิกแบบกำหนดเอง สิ่งนี้ช่วยลดภาระงานพัฒนาอย่างมาก
- **ประหยัดต้นทุน** – คุณสามารถแปลงข้อมูลตารางโดยไม่จำเป็นต้องจัดเก็บสมุดงานไว้ถาวร ซึ่งช่วยประหยัดพื้นที่จัดเก็บและลดค่าใช้จ่าย
- **คงความสมบูรณ์แบบของพิกเซล** – จำลองลักษณะของ Excel ได้อย่างแม่นยำ รวมถึงการจัดรูปแบบเซลล์ สูตร (ในรูปแบบค่าที่แสดง) เส้นขอบ สี และการจัดรูปแบบตามเงื่อนไข ในภาพผลลัพธ์
- **ความเข้ากันได้ทั่วโลก** – รูปแบบไฟล์รูปภาพ (PNG, JPEG, TIFF, BMP, SVG และอื่นๆ) สามารถดูได้บนอุปกรณ์หรือแพลตฟอร์มใดก็ตามโดยไม่ต้องใช้ซอฟต์แวร์เฉพาะ ทำให้มีความเข้าถึงได้สูงสุด

## **วิธีใช้ API แปลงสมุดงานเป็นรูปภาพด้วย SDK?**

### **ข้อมูลเฉพาะของ API แปลงสมุดงานเป็นรูปภาพ**

[ข้อมูลเฉพาะของ API แปลงสมุดงานเป็นรูปภาพ](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToImage) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้จากภายนอก และอนุญาตให้โต้ตอบกับ REST API โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งในบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="คำตอบ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/image?format=png&worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.png
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "MIME type",
  "fileDownloadName": "optional file name"
}
```

{{< /tab >}}

{{< /tabs >}}

### **ใช้ SDK ของ Aspose.Cells Cloud**

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจาก SDK ซ่อนรายละเอียดระดับต่ำไว้และให้คุณแปลงข้อมูลสมุดงานเป็นรูปภาพด้วยโค้ดเพียงเล็กน้อย โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}