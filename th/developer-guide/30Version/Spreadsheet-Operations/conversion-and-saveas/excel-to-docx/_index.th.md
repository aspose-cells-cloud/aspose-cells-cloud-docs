---
title: "Excel ไป Docx"
second_title: "เอกสาร"
linktitle: "Excel ไป Docx"
type: docs
url: /thconvert-excel-file-to-docx-file/
keywords: "การแปลง Excel เป็น Docx, Aspose.Cells Cloud, REST API, การแปลงสเปรดชีต, การสร้างเอกสาร"
description: "แปลงไฟล์สเปรดชีต Excel เป็นเอกสาร Docx โดยใช้ REST API ของ Aspose.Cells Cloud มี SDK และภาษาโปรแกรมต่างๆ รองรับมากมายเพื่อการผสานรวมที่ลื่นไหล"
weight: 90
---

REST API นี้แปลงไฟล์สเปรดชีตเป็นรูปแบบไฟล์ DOCX

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/docx
```

### **ความปลอดภัยและการรับรองความถูกต้อง**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การรับรองความถูกต้องแบบ JWT token</a>

**พารามิเตอร์ Query**

| ชื่อพารามิเตอร์       | ประเภท | คำอธิบาย                                                                                   |
| --------------------- | ------ | ------------------------------------------------------------------------------------------ |
| password              | string | รหัสผ่านที่จำเป็นสำหรับการเปิดไฟล์ Excel                                                   |
| storageName           | string | ชื่อของ storage ที่เก็บไฟล์ไว้                                                            |
| checkExcelRestriction | bool   | ระบุว่าจะตรวจสอบข้อจำกัดของไฟล์ Excel เมื่อผู้ใช้แก้ไขวัตถุที่เกี่ยวข้องกับเซลล์หรือไม่ |

**พารามิเตอร์ Request Body**

| ชื่อพารามิเตอร์ | ประเภท    | คำอธิบาย                                                  |
| --------------- | --------- | --------------------------------------------------------- |
| datafile        | data file | ไฟล์ข้อมูลที่บันทึกไว้ในส่วนแรกของ Request Body แบบ multipart |

**Response**

API จะส่งคืนวัตถุ **FileInfo** ซึ่งมีข้อมูลของไฟล์ Word ที่สร้างขึ้น

| ฟิลด์           | ประเภท | คำอธิบาย                                      |
| --------------- | ------ | --------------------------------------------- |
| **Filename**    | string | ชื่อไฟล์ Word (เช่น `example.docx`)           |
| **FileSize**    | int    | ขนาดไฟล์เป็นหน่วยไบต์                        |
| **FileContent** | string | เนื้อหาไฟล์ Word ที่เข้ารหัสด้วย Base64      |


[FileInfo](/cells/file-info/)

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                   | คำอธิบาย                                                   |
|------|----------------------------|------------------------------------------------------------|
| 200  | OK                         | ใช้ตัวกรองสำเร็จ; response มีรายละเอียดของOPERATION       |
| 400  | Bad Request                | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)    |
| 401  | Unauthorized               | JWT token ไม่ถูกต้องหรือขาดหาย                              |
| 413  | Payload Too Large          | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                          |
| 500  | Internal Server Error      | ข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด                        |

## วิธีใช้ PostConvertWorkbookToDocx API ด้วย SDK

### ข้อมูลจำเพาะ PostConvertWorkbookToDocx API

[OpenAPI Specification](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToDocx) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ **cURL** ผ่าน command-line เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บน Cloud ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/docx" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.docx",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณจดจ่อกับงานของโปรเจกต์ โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToDocx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToDocx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToDocx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToDocx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToDocx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToDocx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToDocx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToDocx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## API อื่นๆ ที่ใช้ฟังก์ชันนี้

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – บันทึกไฟล์ Excel เป็นไฟล์ DOCX พร้อมการตั้งค่าเพิ่มเติม และจัดเก็บผลลัพธ์ไว้ใน storage ที่ระบุ

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – แปลงไฟล์ Excel เป็นไฟล์ DOCX พร้อมการตั้งค่าทางเลือก และส่งคืนผลลัพธ์ใน response

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – ดึงข้อมูลสมุดงาน Excel และแปลงเป็นไฟล์ DOCX พร้อมพารามิเตอร์ทางเลือก

---