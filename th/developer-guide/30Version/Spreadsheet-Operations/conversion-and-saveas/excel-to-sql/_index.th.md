---
title: "การแปลง Excel เป็น SQL"
second_title: "เอกสาร"
linktype: "Excel to SQL"
type: docs
url: /convert-excel-file-to-sql-file/
keywords: "Aspose.Cells, Excel to SQL, API บนคลาวด์, การแปลงสเปรดชีต, REST"
description: "ใช้ Aspose.Cells Cloud REST API เพื่อแปลงไฟล์สเปรดชีต Excel ให้อยู่ในรูปแบบไฟล์ SQL รองรับ SDK และภาษาโปรแกรมต่างๆ เพื่อการผสานรวมอย่างราบรื่นลงในแอปพลิเคชันของคุณ"
weight: 100
ArticleTitle: "แปลง Excel เป็น SQL – Aspose.Cells Cloud API"
---

REST API นี้จะแปลงไฟล์สเปรดชีตให้อยู่ในรูปแบบไฟล์ SQL

**ข้อกำหนดเบื้องต้น**  
ในการใช้งานจุดสิ้นสุด (endpoint) นี้ คุณต้องมีโทเคน JWT ที่ถูกต้องซึ่งสร้างขึ้นตามคำแนะนำในคู่มือการ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">ยืนยันตัวตนด้วยโทเคน JWT</a> API นี้รองรับไฟล์ Excelที่มีขนาดไม่เกินข้อจำกัดที่ระบุไว้ในเอกสารบริการ และสามารถจัดการสมุดงานที่มีการป้องกันด้วยรหัสผ่านได้เมื่อระบุพารามิเตอร์คิวรี `password`

## API PostConvertWorkbookToSQL

```http
POST https://api.aspose.cloud/v3.0/cells/convert/sql
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัย และต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบใช้โทเคน JWT</a>

### **พารามิเตอร์คิวรี**

| ชื่อพารามิเตอร์      | ชนิดข้อมูล | คำอธิบาย                                                                 |
| --------------------- | --------- | ----------------------------------------------------------------------- |
| password              | string    | รหัสผ่านที่จำเป็นสำหรับการเปิดไฟล์ Excel                               |
| storageName           | string    | ชื่อของพื้นที่จัดเก็บที่ไฟล์ถูกจัดเก็บไว้                              |
| checkExcelRestriction | bool      | ระบุว่าจะตรวจสอบข้อจำกัดของไฟล์ Excel เมื่อดัดแปลงวัตถุที่เกี่ยวข้องกับเซลล์หรือไม่ |

### **พารามิเตอร์เนื้อหาคำขอ (Request Body Parameter)**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล   | คำอธิบาย                                                             |
| -------------- | ----------- | ------------------------------------------------------------------- |
| datafile       | data file   | ไฟล์สเปรดชีตที่ต้องการแปลง ซึ่งรวมอยู่เป็นส่วนแรกของคำขอ (request) |

### การตอบกลับ (Response)

API จะส่งกลับวัตถุ **FileInfo** ซึ่งมีข้อมูลเกี่ยวกับไฟล์ sql ที่ถูกสร้างขึ้น

| ฟิลด์           | ชนิดข้อมูล | คำอธิบาย                                       |
| --------------- | --------- | --------------------------------------------- |
| **Filename**    | string    | ชื่อไฟล์ sql (เช่น `example.sql`)            |
| **FileSize**    | int       | ขนาดไฟล์เป็นไบต์                              |
| **FileContent** | string    | เนื้อหาของไฟล์ sql ที่ถูกเข้ารหัสแบบ Base64 |

[FileInfo](/cells/file-info/)

**รหัสสถานะ HTTP (HTTP Status Codes)**

| รหัส | ความหมาย                   | คำอธิบาย                                         |
|------|----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                | ประมวลผลตัวกรองเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของปฏิบัติการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                     |
| 413  | ข้อมูลในคำขอใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินข้อจำกัดที่กำหนด          |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์           |

## วิธีใช้ API PostConvertWorkbookToSQL ร่วมกับ SDK

### ข้อมูลจำเพาะของ API PostConvertWorkbookToSQL

<a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSQL" rel="noopener noreferrer">ข้อมูลจำเพาะ OpenAPI</a> กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้จากภายนอก และช่วยให้คุณสามารถดำเนินการโต้ตอบแบบ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/sql" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.sql",
  "FileSize": 1024,
  "FileContent": "base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณ โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บ GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToSQL.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToSQL.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToSQL.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToSQL.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToSQL.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToSQL.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToSQL.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToSQL.go" >}}

{{< /tab >}}

{{< /tabs >}}

## API อื่นที่ใช้ฟังก์ชันนี้

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – บันทึกสมุดงานในรูปแบบอื่น และจัดเก็บผลลัพธ์ไว้ในพื้นที่จัดเก็บที่ระบุ

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – แปลงสมุดงานเป็นรูปแบบอื่นพร้อมการตั้งค่าแบบเลือกได้ และส่งกลับผลลัพธ์ในการตอบกลับ

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – เรียกคืนสมุดงานพร้อมการตั้งค่าการแปลงแบบเลือกได้

**หมายเหตุ**  
- เมื่อแปลงไฟล์ Excel ที่มีการป้องกันด้วยรหัสผ่าน ให้แน่ใจว่าได้ระบุพารามิเตอร์คิวรี `password` มิเช่นนั้นการแปลงจะล้มเหลวโดยแสดงข้อผิดพลาดรหัส 400  
- บริการจะส่งเนื้อหาไฟล์ SQL กลับมาในรูปแบบ Base64 คุณควรถอดรหัสก่อนบันทึกเป็นไฟล์ `.sql`  

**ไฟล์ตัวอย่าง**  
ดาวน์โหลดสมุดงาน Excel ตัวอย่าง [ที่นี่](https://example.com/sample.xlsx) และผลลัพธ์ SQL ที่สร้างไว้ล่วงหน้า [ที่นี่](https://example.com/sample.sql) เพื่อทดสอบ API ได้อย่างรวดเร็ว
---