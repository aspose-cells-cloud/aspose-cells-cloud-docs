---
title: "Excel เป็น JSON"
second_title: "เอกสาร"
linktitle: "Excel เป็น JSON"
type: docs
url: /th/convert-excel-file-to-json-file/
keywords: "Aspose.Cells, Excel เป็น JSON, Cloud API, การแปลงสเปรดชีต, REST API"
description: "เรียนรู้วิธีการแปลงไฟล์สเปรดชีต Excel เป็นไฟล์ JSON ผ่าน Aspose.Cells Cloud REST API มีตัวอย่าง cURL, ชิ้นส่วนโค้ด SDK (C#, Java, Python), พารามิเตอร์ที่จำเป็น, การรับรองความถูกต้อง และรูปแบบการตอบกลับ"
weight: 100
ArticleTitle: "แปลง Excel เป็น JSON ด้วย Aspose.Cells Cloud API – คู่มืออย่างรวดเร็ว"
---


## API ของ REST

API นี้แปลงไฟล์สเปรดชีตให้อยู่ในรูปแบบไฟล์ JSON  


```http
POST https://api.aspose.cloud/v3.0/cells/convert/json
```

### การรักษาความปลอดภัยและการรับรองความถูกต้อง

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้การรับรองความถูกต้องแบบ [โทเค็น JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

### คำขอ

**พารามิเตอร์การคิวรี**

| ชื่อพารามิเตอร์        | ชนิดข้อมูล | คำอธิบาย                                                     |
| ----------------------- | ---------- | ------------------------------------------------------------ |
| `password`              | สายอักขระ   | รหัสผ่านที่จำเป็นสำหรับการเปิดไฟล์ Excel (ไม่บังคับ)            |
| `storageName`           | สายอักขระ   | ชื่อพื้นที่จัดเก็บที่ไฟล์ตั้งอยู่ (ไม่บังคับ)                   |
| `checkExcelRestriction` | ค่าตรรกะ     | บังคับใช้ข้อจำกัดเฉพาะของ Excel ขณะแก้ไขเซลล์ (ไม่บังคับ)       |

**พารามิเตอร์เนื้อหาคำขอ**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย                                                                         |
| -------------- | ---------- | -------------------------------------------------------------------------------- |
| `datafile`     | ไฟล์        | ไฟล์ Excel ที่จะอัปโหลด ต้องส่งเป็นส่วนแรกของคำขอแบบ `multipart/form-data` |

#### ตัวอย่างการเรียก cURL

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" \
     -H "Authorization: Bearer $ACCESS_TOKEN" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@myWorkbook.xlsx"
```

### การตอบกลับ

บริการจะส่งกลับวัตถุ **FileInfo** โดยฟิลด์สำคัญมีดังนี้:

| ฟิลด์         | ชนิดข้อมูล | คำอธิบาย                                                                       |
| ------------- | ---------- | ------------------------------------------------------------------------------ |
| `Filename`    | สายอักขระ   | ชื่อไฟล์ JSON ที่สร้างขึ้น (เช่น `myWorkbook.json`)                              |
| `FileSize`    | จำนวนเต็ม   | ขนาดของไฟล์ที่สร้างขึ้นเป็นไบต์                                                  |
| `FileContent` | สายอักขระ   | เนื้อหาไฟล์ JSON ที่เข้ารหัสแบบ Base64 ถอดรหัสเพื่อรับ JSON จริง               |

**ตัวอย่างการตอบกลับ**

```json
{
  "Filename": "myWorkbook.json",
  "FileSize": 8423,
  "FileContent": "eyJmb3JtYXR0ZWRfZGF0YSI6IH ... (base64 string) ..."
}
```

#### การจัดการข้อผิดพลาด

หากคำขอล้มเหลว API จะส่งกลับวัตถุข้อผิดพลาดที่มีโครงสร้างดังนี้:

| ฟิลด์     | ชนิดข้อมูล | คำอธิบาย                                    |
| --------- | ---------- | ------------------------------------------- |
| `Code`    | สายอักขระ   | ตัวระบุข้อผิดพลาดในรูปแบบอ่านโดยเครื่อง    |
| `Message` | สายอักขระ   | คำอธิบายข้อผิดพลาดในรูปแบบอ่านโดยมนุษย์    |

โค้ดสถานะ HTTP ที่พบบ่อย:

- **400** – คำขอไม่ถูกต้อง (เช่น ขาดไฟล์หรือพารามิเตอร์ไม่ถูกต้อง)
- **401** – ไม่ได้รับอนุญาต (โทเค็นการเข้าถึงไม่ถูกต้องหรือขาดหาย)
- **500** – ข้อผิดพลาดภายในเซิร์ฟเวอร์

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย                                               |
|------|------------------------------|--------------------------------------------------------|
| 200  | สำเร็จ                       | ตัวกรองใช้งานได้สำเร็จ การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง              | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต              | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                         |
| 413  | ข้อมูลส่งไปมีขนาดใหญ่เกินไป | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                        |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์   | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์                 |
## วิธีใช้ API PostConvertWorkbookToJson ด้วย SDK

### ข้อมูลจำเพาะของ API PostConvertWorkbookToJson


[ข้อมูลจำเพาะ OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToJson) นิยามอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบเปิดเผย และช่วยให้คุณใช้การโต้ตอบ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ผ่าน cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" \
     -H "Authorization: Bearer $ACCESS_TOKEN" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@myWorkbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "myWorkbook.json",
  "FileSize": 8423,
  "FileContent": "eyJmb3JtYXR0ZWRfZGF0YSI6IH... (base64 string)"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับล่างให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer" title="SDK ของ Aspose.Cells Cloud บน GitHub"> kho หลัก GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ที่สมบูรณ์

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells ผ่าน SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToJson.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToJson.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToJson.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToJson.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToJson.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToJson.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToJson.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToJson.go" >}}

{{< /tab >}}

{{< /tabs >}}

## API อื่นที่มีฟังก์ชันคล้ายกัน

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – บันทึกไฟล์ Excel เป็นไฟล์ HTML พร้อมการตั้งค่าเพิ่มเติม และจัดเก็บผลลัพธ์ไว้ในพื้นที่จัดเก็บที่ระบุ
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – แปลงไฟล์ Excel เป็นไฟล์ HTML พร้อมการตั้งค่าเพิ่มเติม และส่งกลับผลลัพธ์ในการตอบกลับ
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – ดึงไฟล์ Excel สามารถใช้ร่วมกับพารามิเตอร์คิวรีเพื่อรับไฟล์ในรูปแบบ HTML