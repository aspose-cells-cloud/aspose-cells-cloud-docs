---
title: "API นำเข้าข้อมูล Aspose.Cells Cloud – โซลูชันบนคลาวด์สำหรับการนำเข้าข้อมูล CSV, JSON และ XML ลงในสมุดงาน Excel โดยอัตโนมัติ"
second_title: "เอกสาร"
ArticleTitle: "แพลตฟอร์มการรวมข้อมูลจากหลายแหล่งสำหรับ Excel – API นำเข้าและแปลงข้อมูลอัตโนมัติ Aspose.Cells Cloud"
linktitle: "นำเข้าข้อมูลลงในสมุดงาน"
type: docs
url: /th/import-data-into-spreadsheet/
keywords: "Aspose Cells, API นำเข้าข้อมูล, CSV ไปยัง Excel, JSON ไปยัง Excel, XML ไปยัง Excel, สมุดงานบนคลาวด์, REST API"
description: "นำเข้าข้อมูล CSV, JSON หรือ XML ลงในสมุดงาน Excel ด้วย REST API ของ Aspose.Cells Cloud ศึกษาเกี่ยวกับรูปแบบคำขอ พารามิเตอร์ ตัวอย่างโค้ด SDK และการจัดการข้อผิดพลาด"
weight: 100
---

## คุณสมบัติหลัก

### การรองรับข้อมูลหลายรูปแบบ

- **<a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">CSV</a> นำเข้าข้อมูล**: รองรับตัวคั่นหลายรูปแบบและตรวจจับการเข้ารหัสอัตโนมัติ
- **<a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">JSON</a> การจัดการข้อมูล**: แบ่งโครงสร้าง JSON ที่ซับซ้อนออกเป็นตาราง Excel
- **<a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">XML</a> การแปลงไฟล์**: แมปข้อมูลโนดให้เป็นโครงสร้างแถวและคอลัมน์ใน Excel

## **คำอธิบาย API นำเข้าข้อมูลลงในสมุดงาน**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data
```

### **ความปลอดภัยและการรับรองความถูกต้อง**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การรับรองความถูกต้องด้วยโทเค็น JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย |
| ---------------- | ------ | -------- | ------------------------------------------------------------------------ |
| datafile | ไฟล์ | FormData | ไฟล์ข้อมูล (CSV, JSON หรือ XML) ที่จะนำเข้า |
| spreadsheet | ไฟล์ | FormData | สมุดงานเป้าหมายที่จะรับข้อมูลที่นำเข้า |
| worksheet | สายอักขระ | Query | ชื่อแผ่นงานที่จะวางข้อมูล |
| startCell | สายอักขระ | Query | ช่องซ้ายบน (เช่น `A1`) ที่กำหนดตำแหน่งเริ่มต้นสำหรับการนำเข้า |
| insert | บูลีน | Query | `true` สำหรับการแทรกแถว; `false` สำหรับการเขียนทับข้อมูลที่มีอยู่ |
| convertNumericData | บูลีน | Query | `true` สำหรับการแปลงสตริงตัวเลขให้เป็นตัวเลขระหว่างการนำเข้า |
| splitter | สายอักขระ | Query | ตัวคั่น CSV หนึ่งตัวอักษร (ค่าเริ่มต้นคือ `,`) |
| outPath | สายอักขระ | Query (ไม่บังคับ) | เส้นทางโฟลเดอร์ที่จะบันทึกสมุดงานที่อัปเดต |
| outStorageName | สายอักขระ | Query (ไม่บังคับ) | ชื่อตำแหน่งจัดเก็บสำหรับไฟล์ผลลัพธ์ |
| fontsLocation | สายอักขระ | Query (ไม่บังคับ) | เส้นทางไปยังโฟลเดอร์ฟอนต์ที่กำหนดเอง (ถ้าจำเป็น) |
| region | สายอักขระ | Query (ไม่บังคับ) | การกำหนดค่าภูมิภาคของสมุดงาน (เช่น `en-US`) |
| password | สายอักขระ | Query (ไม่บังคับ) | รหัสผ่านสำหรับเปิดสมุดงานที่มีการป้องกัน |

### คำตอบ

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
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200 | คำขอสำเร็จ | ใช้ตัวกรองเรียบร้อยแล้ว; คำตอบประกอบด้วยรายละเอียดการดำเนินการ |
| 400 | คำขอไม่ถูกต้อง | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401 | ไม่ได้รับอนุญาต | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย |
| 413 | ข้อมูลส่งไปมีขนาดใหญ่เกินไป | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ | ข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด |

## เหตุผลที่คุณควรใช้ API นี้

- **การโหลดข้อมูลที่มีประสิทธิภาพ** – ช่วยให้นำข้อมูลขนาดใหญ่เข้าสู่สมุดงานโดยตรงโดยไม่ต้องสร้างไฟล์ชั่วคราว
- **การรองรับ SDK อย่างกว้างขวาง** – มีไลบรารีไคลเอนต์สำหรับ .NET, Java, PHP, Ruby, Node.js, Python, Go และ Perl ทำให้ง่ายต่อการผสานรวม
- **การประมวลผลในหน่วยความจำ** – ดำเนินการแปลงในหน่วยความจำ ลดความต้องการพื้นที่จัดเก็บชั่วคราว

## วิธีใช้ API นำเข้าข้อมูลลงในสมุดงานด้วย SDK

**หมายเหตุ / ข้อจำกัด:** API รองรับสูงสุด 1,000,000 แถวต่อการนำเข้า ตัวคั่น CSV ค่าเริ่มต้นคือจุลภาคเท่านั้น ตัวคั่นอื่นๆ ที่เป็นอักขระเดี่ยวสามารถระบุผ่านพารามิเตอร์ `splitter` ไฟล์ XML ขนาดใหญ่อาจเพิ่มเวลาในการประมวลผล

สำหรับการดำเนินการที่เกี่ยวข้อง เช่น การส่งออกข้อมูลหรือการแปลงรูปแบบสมุดงาน ดูที่เอกสาร **การส่งออกข้อมูล** และ **การแปลงสมุดงาน**

### ข้อกำหนด API นำเข้าข้อมูลลงในสมุดงาน

<a href="https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet" rel="noopener noreferrer">ข้อกำหนด API นำเข้าข้อมูลลงในสมุดงาน</a> มีอินเทอร์เฟซโปรแกรมที่เข้าถึงได้สาธารณะ ช่วยให้คุณสามารถโต้ตอบกับ REST โดยตรงจากเว็บเบราว์เซอร์ของคุณ
คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง cURL เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียก API บนคลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="คำตอบ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/import/data?worksheet=Sheet1&startCell=A1&insert=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "datafile=@/path/to/data.csv" \
  -F "spreadsheet=@/path/to/workbook.xlsx"
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

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจากซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถนำข้อมูลลงในแผ่นงานของสมุดงานได้ด้วยโค้ดสั้นๆ โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บ GitHub</a> สำหรับรายชื่อ SDK ของ Aspose.Cells Cloud อย่างสมบูรณ์

---