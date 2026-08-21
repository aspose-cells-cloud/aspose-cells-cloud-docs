---
title: "Excel ไป CSV"
second: "เอกสาร"
linktitle: "Excel ไป CSV"
type: docs
url: /thconvert-excel-file-to-CSV-file/
aliases:
  - /convert-excel-file-to-CSV-in-cloud/
  - /convert/excel-to-csv/
  - /convert-excel-file-to-CSV-file/
keywords: "Excel ไป CSV, Aspose.Cells Cloud, REST API, การแปลงสเปรดชีต, ไฟล์ CSV, การแปลงไฟล์"
description: "แปลงสเปรดชีต Excel เป็น CSV โดยใช้ Aspose.Cells Cloud REST API มีการสนับสนุน SDK และภาษาโปรแกรมต่างๆ มากมายเพื่อการผสานรวมที่ง่ายดาย"
weight: 90
---

REST API นี้แปลงไฟล์สเปรดชีตเป็นไฟล์รูปแบบ CSV

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/csv
```

### **ความปลอดภัยและการรับรองความถูกต้อง**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การรับรองความถูกต้องด้วยโทเคน JWT</a>

### พารามิเตอร์ Query

| ชื่อพารามิเตอร์        | ชนิด   | คำอธิบาย                                                                          |
| ----------------------- | ------ | --------------------------------------------------------------------------------- |
| `password`              | string | รหัสผ่านที่จำเป็นสำหรับการเปิดไฟล์ Excel                                          |
| `storageName`           | string | ชื่อของ storage ที่ไฟล์อยู่                                                       |
| `checkExcelRestriction` | bool   | กำหนดว่าจะตรวจสอบข้อจำกัดของไฟล์ Excel เมื่อผู้ใช้แก้ไขวัตถุที่เกี่ยวข้องกับเซลล์ |

### พารามิเตอร์ Request Body

| ชื่อพารามิเตอร์ | ชนิด      | คำอธิบาย                                                       |
| -------------- | --------- | -------------------------------------------------------------- |
| `datafile`     | data file | ไฟล์ข้อมูลที่รวมอยู่ในส่วนแรกของ request body แบบ multipart |

### การตอบกลับ

API จะส่งกลับวัตถุ **FileInfo** ที่มีไฟล์ CSV ที่สร้างขึ้น

| ฟิลด์           | ชนิด   | คำอธิบาย                                     |
| --------------- | ------ | -------------------------------------------- |
| **Filename**    | string | ชื่อไฟล์ CSV (เช่น `example.csv`)           |
| **FileSize**    | int    | ขนาดไฟล์เป็นไบต์                            |
| **FileContent** | string | เนื้อหาไฟล์ CSV ที่เข้ารหัสแบบ Base64        |

[FileInfo](/cells/file-info/)

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                      | คำอธิบาย                                                  |
|------|-------------------------------|-----------------------------------------------------------|
| 200  | สำเร็จ (OK)                   | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของ оперATION |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)   |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)| โทเคน JWT ไม่ถูกต้องหรือขาดหาย                            |
| 413  | ข้อมูลส่งมอบใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                    |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) | ข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด             |

## วิธีใช้ PostConvertWorkbookToCSV API ด้วย SDK

### ข้อมูลจำเพาะของ PostConvertWorkbookToCSV API

[ข้อมูลจำเพาะ OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToCSV) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถโต้ตอบกับ REST ผ่านเบราว์เซอร์เว็บได้โดยตรง

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ API บนคลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/csv" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.CSV",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่โครงการของคุณ ดู [repository บน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPDF.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPDF.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPDF.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPDF.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPDF.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPDF.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPDF.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPDF.go" >}}

{{< /tab >}}

{{< /tabs >}}