---
---
title: "Aspose.Cells Cloud Web API – แปลงข้อมูลตารางในสมุดงานเป็นไฟล์ CSV – เครื่องมือออนไลน์ฟรี"
secondtitle: "เอกสาร"
ArticleTitle: "วิธีการแปลงข้อมูลตารางในสมุดงานเป็นไฟล์ CSV: คู่มือแบบทีละขั้นตอน"
linktype: "docs"
url: "/convert-table-to-csv/"
keywords: "Aspose.Cells Cloud, ตารางเป็น CSV, การแปลงสมุดงาน, Excel เป็น CSV, API, REST, การส่งออกข้อมูล"
description: "แปลงตารางจากสมุดงาน Excel เป็นไฟล์ CSV ได้อย่างรวดเร็วด้วย Aspose.Cells Cloud API"
weight: 100
---

ส่งออกข้อมูลตารางจากสมุดงาน Excel ที่อยู่ในเครื่องเป็นไฟล์ CSV โดยใช้ Cloud API

## **Convert Table to CSV API**

### Web API

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **การรักษาความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

```bash
-H "Authorization: Bearer {access_token}"
```

### **พารามิเตอร์คำขอ:**

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง (Path/Query String/HTTP Body) | คำอธิบาย |
|------------------|--------|----------------------------------------|----------|
| Spreadsheet | ไฟล์ | FormData | อัปโหลดไฟล์สมุดงาน |
| worksheet | สตริง | Query | ชื่อของแผ่นงานในสมุดงาน |
| tableName | สตริง | Query | ชื่อของตารางที่จะแปลง |
| outPath | สตริง | Query | (ไม่บังคับ) พาธของโฟลเดอร์ที่เก็บสมุดงาน (ค่าเริ่มต้นคือ null) |
| outStorageName | สตริง | Query | ชื่อของพื้นที่จัดเก็บสำหรับไฟล์ผลลัพธ์ |
| fontsLocation | สตริง | Query | พาธสำหรับใช้ฟอนต์ที่กำหนดเอง |
| region | สตริง | Query | การตั้งค่าภูมิภาค/ภาษาของสมุดงาน (เช่น `en-US`, `fr-FR`) มีผลต่อการจัดรูปแบบตัวเลข การแยกวิเคราะห์วันที่ และพฤติกรรมเฉพาะของภูมิภาค |
| password | สตริง | Query | รหัสผ่านสำหรับเปิดไฟล์สมุดงาน |

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

**รหัสสถานะ HTTP**

| รหัส | ความหมาย | คำอธิบาย |
|------|-----------|-----------|
| 200 | สำเร็จ (OK) | ใช้ตัวกรองเรียบร้อยแล้ว; ข้อมูลการตอบกลับประกอบด้วยรายละเอียดของการดำเนินการ |
| 400 | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401 | ไม่ได้รับอนุญาต (Unauthorized) | JWT token ไม่ถูกต้องหรือขาดหาย |
| 413 | ข้อมูลในคำขอใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

## **คุณควรใช้ Convert Table to CSV API ในกรณีใด?**

- **การย้ายฐานข้อมูล**: แปลงตารางจาก Excel เป็น CSV เพื่อนำเข้าเป็นชุดใหญ่เข้าสู่ฐานข้อมูล SQL (MySQL, PostgreSQL, SQL Server)
- **การโหลดข้อมูลลงคลังข้อมูล (Data Warehouse)**: แปลงตารางสำหรับการรายงานที่สร้างจาก Excel เป็น CSV เพื่อนำเข้าสู่ Snowflake, Redshift หรือ BigQuery
- **การส่งข้อมูลเป็นชุดผ่าน API**: แปลงข้อมูลตารางจาก Excel เป็น CSV เพื่ออัปโหลดเป็นชุดใหญ่ไปยังบริการ REST
- **การสื่อสารระหว่างบริการ (Service-to-Service Communication)**: ใช้ CSV เป็นรูปแบบการแลกเปลี่ยนข้อมูลแบบเบาสำหรับไมโครเซอร์วิส
- **การเตรียมข้อมูลสำหรับการเรียนรู้ของเครื่อง (Machine Learning Data Prep)**: แปลงตารางคุณลักษณะ (feature tables) จาก Excel เป็น CSV เพื่อนำไปใช้กับไลบรารีการเรียนรู้ของเครื่องใน Python/R
- **การวิเคราะห์เชิงสถิติ**: แปลงตารางข้อมูลการวิจัยเป็น CSV เพื่อนำเข้าสู่ SPSS, SAS หรือ Stata
- **การย้ายเนื้อหา**: ย้ายเนื้อหาที่มีโครงสร้างจาก Excel ไปยังระบบจัดการเนื้อหา (CMS) ผ่าน CSV

## เหตุใดคุณควรใช้ Convert Table to CSV API?

- **เป็นมิตรกับนักพัฒนา**: Aspose.Cells Cloud มี SDK รองรับหลายภาษา ช่วยให้การพัฒนาทำได้อย่างรวดเร็ว และมีเอกสารประกอบที่ครอบคลุม เมื่อเทียบกับการสร้างโซลูชันเอง ช่วยลดภาระงานพัฒนาได้อย่างมาก
- **ประหยัดต้นทุน**: คุณสามารถแปลงข้อมูลตารางโดยไม่จำเป็นต้องอัปโหลดสมุดงานก่อน ซึ่งช่วยประหยัดพื้นที่จัดเก็บและลดต้นทุน
- **ดึงข้อมูลอย่างบริสุทธิ์โดยไม่มีการจัดรูปแบบ**
- **CSV ได้รับการรองรับโดยเกือบทุกระบบ**:
  - ฐานข้อมูล (RDBMS หลักทั้งหมด)
  - ภาษาการเขียนโปรแกรม (มีตัวแยกวิเคราะห์ในตัวทั้งหมด)
  - เครื่องมือธุรกิจเชิงวิเคราะห์ (Tableau, Power BI, Looker)
  - โปรแกรมสมุดงาน (Excel, Google Sheets, LibreOffice)
  - เครื่องมือใน command-line (awk, sed, grep)

## วิธีใช้ Convert Table to CSV API พร้อม SDKs?

### ข้อมูลจำเพาะของ Convert Table to CSV API

[ข้อมูลจำเพาะของ Convert Table to CSV API](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToCSV) ให้อินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้จากสาธารณะ ช่วยให้คุณสามารถโต้ตอบกับ REST ผ่านเว็บเบราว์เซอร์โดยตรงได้
คุณสามารถใช้เครื่องมือ command-line cURL เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/csv?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.csv
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (เข้ารหัสแบบ Base64)",
  "contentType": "MIME type",
  "fileDownloadName": "ชื่อไฟล์ (ไม่บังคับ)"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจากซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถแปลงข้อมูลตารางในสมุดงานเป็นไฟล์ CSV ได้ด้วยโค้ดเพียงเล็กน้อย โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToCSV.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToCSV.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToCSV.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToCSV.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToCSV.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToCSV.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToCSV.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToCSV.go" >}}
{{</tab>}}
{{< /tabs >}}