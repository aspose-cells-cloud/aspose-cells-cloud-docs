---
---
title: "Aspose.Cells Cloud Web API - แปลงข้อมูลตารางในไฟล์ Excel ท้องถิ่นเป็นไฟล์ PDF - เครื่องมือออนไลน์ฟรี"
second_title: "เอกสาร"
ArticleTitle: "วิธีแปลงข้อมูลตารางในไฟล์สเปรดชีตท้องถิ่นเป็นไฟล์ PDF: คู่มือแบบทีละขั้นตอน"
linktype: "แปลงตารางเป็น PDF"
type: docs
url: /convert-table-to-pdf/
keywords: "Aspose.Cells, Excel ไป PDF, การแปลงตาราง, Cloud API"
description: "แปลงตาราง Excel ท้องถิ่นเป็นไฟล์ PDF อย่างรวดเร็วด้วย Aspose.Cells Cloud REST API"
weight: 100
---

ส่งออกข้อมูลตารางจากไฟล์ Excel ท้องถิ่นไปยังไฟล์ PDF โดยใช้ Cloud API

## **Convert Table to PDF API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์ด้วย JWT token</a>

### **พารามิเตอร์คำขอ:**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | Path/Query String/HTTPBody | คำอธิบาย                                                                 |
| :------------- | :----- | :------------------------- | :---------------------------------------------------------------------- |
| Spreadsheet    | ไฟล์   | FormData                   | อัปโหลดไฟล์สเปรดชีตที่ต้องการแปลง                                        |
| worksheet      | สตริง | Query                      | ชื่อแผ่นงานของสเปรดชีต                                                    |
| tableName      | สตริง | Query                      | ชื่อตารางที่ต้องการแปลง                                                    |
| outPath        | สตริง | Query                      | (ไม่บังคับ) เส้นทางโฟลเดอร์ที่จะบันทึกไฟล์ PDF ที่แปลงแล้ว ค่าเริ่มต้นคือ null |
| outStorageName | สตริง | Query                      | ระบุชื่อของพื้นที่จัดเก็บไฟล์ผลลัพธ์                                        |
| fontsLocation  | สตริง | Query                      | ใช้ฟอนต์ที่กำหนดเองสำหรับ PDF                                              |
| region         | สตริง | Query                      | ระบุการตั้งค่าภูมิภาคสำหรับสเปรดชีต                                        |
| password       | สตริง | Query                      | รหัสผ่านสำหรับการเข้าถึงไฟล์สเปรดชีต                                       |

### **การตอบกลับ**

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

**ตัวอย่างส่วนหัวของการตอบกลับ**

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="ConvertedTable.pdf"
Content-Length: 124578
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย               | คำอธิบาย                                                           |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | สำเร็จ (OK)           | ใช้ตัวกรองสำเร็จ; การตอบกลับประกอบด้วยรายละเอียดของคำสั่งทำงาน      |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)                |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | JWT token ไม่ถูกต้องหรือขาดหาย                                       |
| 413  | ข้อมูลร้องขอใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด                              |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดภายในเซิร์ฟเวอร์                              |

## **คุณควรใช้ Convert Table to PDF API ในกรณีใด?**

- **งบการเงิน**: แปลงสมุดบัญชีดุล, งบกำไรขาดทุน (ตารางเฉพาะ) เป็น PDF เพื่อสร้างเอกสารสำหรับการตรวจสอบ
- **รายงานการขาย**: แปลงแดชบอร์ดการขายหรือการคำนวณค่าคอมมิชชันเป็นไฟล์ PDF ที่สามารถส่งต่อได้
- **ตัวชี้วัดการดำเนินงาน**: ส่งออกตาราง KPI และตัวชี้วัดประสิทธิภาพเป็นรายงาน PDF ทางการ
- **ข้อมูลสัญญา**: ส่งออกตารางราคาและข้อตกลงระดับบริการจากสเปรดชีตเป็นไฟล์แนบ PDF
- **บันทึกการตรวจสอบ**: รักษาข้อมูลตารางการเงินไว้ในรูปแบบ PDF ที่แก้ไขไม่ได้เพื่อใช้เป็นหลักฐาน
- **สรุปพอร์ตโฟลิโอ**: ส่งออกตารางประสิทธิภาพการลงทุนเป็นรายงาน PDF สำหรับลูกค้า
- **รายงานการควบคุมคุณภาพ**: ส่งออกตารางข้อมูลการตรวจสอบเป็นไฟล์ PDF เพื่อบันทึกไว้เพื่อการตรวจสอบความสอดคล้อง
- **สรุปสต๊อกสินค้า**: แปลงตารางระดับสต๊อกเป็น PDF เพื่อใช้ในการทบทวนโดยผู้บริหาร

## **เหตุใดคุณจึงควรใช้ Convert Table to PDF API?**

- **เป็นมิตรกับนักพัฒนา**: Aspose.Cells Cloud มีไลบรารี SDK รองรับหลายภาษา ช่วยให้พัฒนาได้อย่างรวดเร็ว และมาพร้อมเอกสารประกอบที่ครบถ้วน เมื่อเทียบกับการสร้างโซลูชันการเรนเดอร์กราฟิกแบบกำหนดเอง ซึ่งช่วยลดภาระงานพัฒนาอย่างมาก
- **ประหยัดต้นทุน**: คุณสามารถแปลงข้อมูลตารางได้โดยไม่ต้องอัปโหลดสมุดงานก่อน ซึ่งช่วยประหยัดพื้นที่จัดเก็บและลดค่าใช้จ่าย
- **รักษาการจัดรูปแบบ Excel ที่ซับซ้อน** ในรูปแบบ PDF ที่เข้าถึงได้ทั่วโลก

## **วิธีใช้ Convert Table to PDF API ร่วมกับ SDK?**

### ข้อมูลจำเพาะของ Convert Table to PDF API

[ข้อมูลจำเพาะของ Convert Table to PDF API](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPDF) ให้อินเทอร์เฟซโปรแกรมที่เข้าถึงได้สาธารณะสำหรับการเรียกใช้งาน REST จากเบราว์เซอร์เว็บโดยตรง
คุณสามารถใช้เครื่องมือ cURL บรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.pdf
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

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เพราะช่วยซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถแปลงข้อมูลตารางในสเปรดชีตเป็นไฟล์ PDF ได้ด้วยโค้ดเพียงเล็กน้อย กรุณาดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) สำหรับรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}