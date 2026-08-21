---
title: "Aspose.Cells Cloud Web API – แปลงแผ่นงาน Excel แบบโลคัลเป็นไฟล์ PDF – เครื่องมือออนไลน์ฟรี"
second_title: "เอกสาร"
ArticleTitle: "วิธีการแปลงแผ่นงานสมุดรายวันแบบโลคัลเป็นไฟล์ PDF: คู่มือแบบทีละขั้นตอน"
linktype: "แปลงแผ่นงานเป็น PDF"
type: docs
url: /convert-worksheet-to-pdf/
keywords: "Aspose.Cells, Excel เป็น PDF, การแปลงแผ่นงาน, REST API, การแปลงบนคลาวด์, PDF สมุดรายวัน, endpoint ของ API, การสร้าง PDF"
description: "ใช้ Aspose.Cells Cloud API แปลงแผ่นงานจากไฟล์ Excel แบบโลคัลเป็นเอกสาร PDF ได้อย่างรวดเร็วและปลอดภัย"
weight: 100
---

ส่งออกแผ่นงานจากไฟล์ Excel แบบโลคัลเป็นไฟล์ [PDF](https://docs.fileformat.com/pdf/) โดยใช้ Cloud API

## **API แปลงแผ่นงานเป็น PDF**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### **พารามิเตอร์คำขอ:**

| ชื่อพารามิเตอร์ | ประเภท | Path/Query String/HTTPBody | คำอธิบาย                                                                 |
| ---------------- | ------ | -------------------------- | ------------------------------------------------------------------------ |
| Spreadsheet      | ไฟล์   | FormData                   | อัปโหลดไฟล์สมุดรายวัน                                                    |
| worksheet        | ข้อความ | Query                      | ชื่อของแผ่นงานในสมุดรายวัน                                               |
| outPath          | ข้อความ | Query                      | (ไม่บังคับ) เส้นทางโฟลเดอร์ที่เก็บสมุดรายวัน; ค่าเริ่มต้นคือ null       |
| outStorageName   | ข้อความ | Query                      | ชื่อพื้นที่จัดเก็บไฟล์ผลลัพธ์                                             |
| fontsLocation    | ข้อความ | Query                      | ใช้ฟอนต์ที่กำหนดเองสำหรับ PDF                                             |
| region           | ข้อความ | Query                      | กำหนดการตั้งค่าภูมิภาคของสมุดรายวัน                                      |
| password         | ข้อความ | Query                      | รหัสผ่านที่ใช้เปิดไฟล์สมุดรายวัน                                          |

### **การตอบกลับ**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย              | คำอธิบาย                                                      |
| ---- | ---------------------- | ------------------------------------------------------------- |
| 200  | สำเร็จ (OK)           | กรองข้อมูลเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของ operation |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | JWT token ไม่ถูกต้องหรือขาดหาย                                |
| 413  | ข้อมูลในคำขอใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                            |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) | ข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์                         |

## **คุณควรใช้ API แปลงแผ่นงานเป็น PDF ในกรณีใด?**

- **งบการเงิน**: แปลงงบดุล งบกำไรขาดทุน (ตารางเฉพาะ) เป็น PDF เพื่อใช้เป็นเอกสารสำหรับการตรวจสอบ
- **รายงานการขาย**: แปลงแดชบอร์ดการขายหรือการคำนวณค่าคอมมิชชันเป็นไฟล์ PDF ที่สามารถแจกจ่ายได้
- **ตัวชี้วัดการดำเนินงาน**: ส่งออกตาราง KPI และตัวชี้วัดประสิทธิภาพเป็นรายงาน PDF ทางการ
- **ข้อมูลสัญญา**: ส่งออกตารางราคาและข้อตกลงระดับบริการจากสมุดรายวันเป็นไฟล์แนบ PDF
- **บันทึกการตรวจสอบ**: รักษาแผ่นงานการเงินไว้เป็นหลักฐาน PDF แบบแก้ไขไม่ได้
- **สรุปพอร์ตโฟลิโอ**: ส่งออกตารางประสิทธิภาพการลงทุนเป็นเอกสาร PDF พร้อมส่งให้ลูกค้า
- **รายงานควบคุมคุณภาพ**: ส่งออกแผ่นงานการตรวจสอบเป็น PDF เพื่อบันทึกไว้เพื่อการตรวจสอบการปฏิบัติตามข้อกำหนด
- **สรุปรายการสต๊อก**: แปลงแผ่นงานสต๊อกเป็น PDF เพื่อใช้ในการทบทวนโดยฝ่ายบริหาร

## **เหตุใดคุณจึงควรใช้ API แปลงแผ่นงานเป็น PDF?**

- **เป็นมิตรกับนักพัฒนา**: Aspose.Cells Cloud มี SDK สำหรับภาษาต่างๆ หลายภาษา ช่วยให้การพัฒนาเป็นไปอย่างรวดเร็ว และมาพร้อมกับเอกสารที่ครอบคลุม เมื่อเทียบกับการสร้างโซลูชันการเรนเดอร์กราฟิกแบบกำหนดเอง การใช้ API นี้ช่วยลดภาระงานพัฒนาได้อย่างมาก
- **คุ้มค่า**: คุณสามารถแปลงข้อมูลตารางได้โดยไม่จำเป็นต้องอัปโหลดสมุดรายวันก่อน ซึ่งช่วยประหยัดพื้นที่จัดเก็บและลดต้นทุน
- **รักษาการจัดรูปแบบ**: คงการจัดรูปแบบที่ซับซ้อนของ Excel ไว้ในรูปแบบ PDF ที่เข้าถึงได้ทั่วไป

## **วิธีใช้ API แปลงแผ่นงานเป็น PDF ร่วมกับ SDK?**

### ข้อมูลจำเพาะ API แปลงแผ่นงานเป็น PDF

[ข้อมูลจำเพาะ API แปลงแผ่นงานเป็น PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToPDF) ให้อินเทอร์เฟซโปรแกรมที่เข้าถึงได้สาธารณะ และช่วยให้คุณสามารถโต้ตอบกับ REST API ได้โดยตรงจากเบราว์เซอร์เว็บ

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/json?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (เข้ารหัส Base64)",
  "contentType": "MIME type",
  "fileDownloadName": "ชื่อไฟล์ (ไม่บังคับ)"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจากช่วยซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถแปลงข้อมูลตารางในสมุดรายวันเป็นไฟล์ PDF ได้ด้วยโค้ดน้อยที่สุด โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}