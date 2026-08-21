---
title: "การแปลง Excel เป็น Markdown"
second_title: "เอกสาร"
linktype: "Excel เป็น Markdown"
type: docs
url: /convert-excel-file-to-markdown-file/
keywords: "Excel, Markdown, การแปลง, Aspose.Cells Cloud, REST API, การแปลง Excel เป็น Markdown, Aspose Cells Markdown API, การส่งออก Excel เป็น Markdown"
description: "แปลงเวิร์กชีต Excel เป็น Markdown โดยใช้ Aspose.Cells Cloud REST API – ประกอบด้วยตัวอย่าง cURL, โค้ดตัวอย่าง SDK, พารามิเตอร์ที่จำเป็น และรายละเอียดการตรวจสอบสิทธิ์"
weight: 100
ArticleTitle: "แปลง Excel เป็น Markdown – เอกสารประกอบ API ของ Aspose.Cells Cloud"
---

REST API นี้แปลงไฟล์สเปรดชีตเป็นไฟล์รูปแบบ Markdown

## ความปลอดภัยและการตรวจสอบสิทธิ์
API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้การตรวจสอบสิทธิ์แบบ JWT token ดูรายละเอียดได้ที่ [การตรวจสอบสิทธิ์คำขอ REST API](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/markdown
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้การตรวจสอบสิทธิ์แบบ JWT token ดูรายละเอียดได้ที่ [การตรวจสอบสิทธิ์คำขอ REST API](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

### พารามิเตอร์ใน Query String


| ชื่อพารามิเตอร์       | ประเภท | ตำแหน่ง | คำอธิบาย                                                                                       |
| --------------------- | ------ | -------- | ------------------------------------------------------------------------------------------------- |
| password              | string | query    | รหัสผ่านที่จำเป็นสำหรับการเปิดไฟล์ Excel                                                         |
| storageName           | string | query    | ชื่อของพื้นที่จัดเก็บ (storage) ที่ไฟล์นั้นตั้งอยู่                                                    |
| checkExcelRestriction | bool   | query    | ระบุว่าจะบังคับข้อจำกัดเฉพาะของ Excel ขณะแก้ไขเซลล์หรือวัตถุที่เกี่ยวข้องหรือไม่ |
| datafile              | file   | body     | ไฟล์ Excel ที่จะอัปโหลดเป็นส่วนแรกของเนื้อหาแบบ multipart                                      |

### การตอบกลับ

API จะส่งกลับ JSON object ประเภท **FileInfo**:

- **FileInfo** – วัตถุที่บรรจุชื่อ ขนาด และเนื้อหาที่เข้ารหัส base64 ของไฟล์ Markdown ที่สร้างขึ้น

```json
{
  "Filename": "example.md",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

### การตอบกลับข้อผิดพลาด

| HTTP Code | คำอธิบาย                                                           | ตัวอย่าง JSON Body                             |
| --------- | ----------------------------------------------------------------- | ----------------------------------------------- |
| 401       | ไม่ได้รับอนุญาต – ไม่มี token หรือ token ไม่ถูกต้อง                          | `{"error":"Invalid access token."}`             |
| 400       | คำขอไม่ถูกต้อง – พารามิเตอร์ที่จำเป็นขาดหาย หรือรูปแบบไฟล์ไม่ถูกต้อง | `{"error":"The 'datafile' field is required."}` |
| 500       | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – ปัญหาที่ไม่คาดคิดของเซิร์ฟเวอร์                | `{"error":"An unexpected error occurred."}`     |



## วิธีใช้ API PostConvertWorkbookToMarkdown พร้อม SDK

### ข้อมูลจำเพาะ API PostConvertWorkbookToMarkdown

[OpenAPI Specification](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToMarkdown) นิยามอินเทอร์เฟซการโปรแกรมที่เข้าถึงได้จากภายนอก และช่วยให้คุณสามารถเรียกใช้ REST API ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างด้านล่างแสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```shell
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/markdown" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "File=@your_excel_file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.md",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณ ดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมดได้ที่ [GitHub repository](https://github.com/aspose-cells-cloud)

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToMarkdown.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToMarkdown.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToMarkdown.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToMarkdown.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToMarkdown.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToMarkdown.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToMarkdown.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToMarkdown.go" >}}

{{< /tab >}}

{{< /tabs >}}

## API อื่นๆ ที่ใช้ฟังก์ชันนี้

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – บันทึกไฟล์ Excel เป็น HTML พร้อมการตั้งค่าเพิ่มเติม และจัดเก็บผลลัพธ์
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – แปลงไฟล์ Excel เป็น HTML พร้อมตัวเลือกเพิ่มเติม และส่งกลับผลลัพธ์ในส่วนการตอบกลับ
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – ดึงข้อมูลไฟล์ Excel และสามารถแปลงเป็น HTML ได้พร้อมการตั้งค่าแบบเลือกได้
---