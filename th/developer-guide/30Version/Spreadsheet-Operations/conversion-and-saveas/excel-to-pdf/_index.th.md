---
title: "แปลง Excel เป็น PDF – Aspose.Cells Cloud API"
ArticleTitle: "แปลง Excel เป็น PDF – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktype: "แปลง Excel เป็น PDF"
type: docs
url: /convert-excel-file-to-pdf-file/
aliases: [/convert-excel-file-to-pdf-in-cloud/, /convert/excel-to-pdf/]
keywords: "Aspose, Cells, Excel, PDF, การแปลง, Cloud API"
description: "เรียนรู้วิธีการแปลงสมุดงาน Excel เป็น PDF ด้วย Aspose.Cells Cloud REST API รวมถึงตัวอย่าง cURL, SDK (C#, Java, Python) และคู่มือการตรวจสอบสิทธิ์"
weight: 80
---

API นี้สำหรับ REST ใช้สำหรับแปลงไฟล์สเปรดชีตให้อยู่ในรูปแบบไฟล์ PDF **ข้อกำหนดเบื้องต้น:** ต้องมี JWT access token ที่ถูกต้อง ไฟล์ Excel ต้นทางต้องถูกจัดเก็บไว้ในพื้นที่จัดเก็บที่รองรับ และต้องมีสิทธิ์ที่เหมาะสมในการเรียกใช้จุดปลายทางการแปลง

## API PostConvertWorkbookToPDF

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pdf
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์ด้วยโทเค็น JWT</a>

### **พารามิเตอร์แบบ Query**

| ชื่อพารามิเตอร์      | ประเภท | คำอธิบาย                                                                             |
| :-------------------- | :----- | :------------------------------------------------------------------------------------ |
| password              | string | รหัสผ่านสำหรับเปิดไฟล์ Excel                                                         |
| storageName           | string | ชื่อของพื้นที่จัดเก็บที่ไฟล์อยู่                                                     |
| checkExcelRestriction | bool   | กำหนดว่าจะบังคับข้อจำกัดของไฟล์ Excel เมื่อแก้ไขวัตถุที่เกี่ยวข้องกับเซลล์หรือไม่ |

ค่าเริ่มต้นของ `checkExcelRestriction` คือ `false` หากไม่ระบุ

### **พารามิเตอร์ใน Request Body**

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย                                                        |
| :------------- | :----- | :--------------------------------------------------------------- |
| datafile       | file   | ไฟล์ข้อมูลที่บันทึกเป็นส่วนแรกของเนื้อหาแบบ multipart            |

### **Response**

[FileInfo](/cells/file-info/)

Response จะส่งคืน JSON object ที่มี metadata ของไฟล์ โดยสามารถดาวน์โหลดไฟล์ PDF ได้โดยใช้ `FileContent` (base64) หรือผ่านลิงก์จาก `FileInfo` API จะส่งคืน JSON object ประเภท **FileInfo** ดังนี้:

- **FileInfo** – วัตถุที่มีชื่อไฟล์ ขนาด และเนื้อหา (base64-encoded) ของไฟล์ **PDF** ที่ถูกสร้างขึ้น

```json
{
  "Filename": "example.pdf",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                   | คำอธิบาย                                                       |
|------|-----------------------------|----------------------------------------------------------------|
| 200  | OK                          | ใช้ตัวกรองสำเร็จ; response มีรายละเอียดของ оперation         |
| 400  | Bad Request                 | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ไม่รองรับ)          |
| 401  | Unauthorized                | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                               |
| 413  | Payload Too Large           | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                             |
| 500  | Internal Server Error       | ข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์                          |

## วิธีใช้ API PostConvertWorkbookToPDF ด้วย SDK

### ข้อมูลจำเพาะของ API PostConvertWorkbookToPDF

[OpenAPI Specification](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPDF) กำหนด API ที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการ REST interaction ได้โดยตรงจากเว็บเบราว์เซอร์

**Request Headers**

| Header        | ประเภท | คำอธิบาย                                                           |
| :------------ | :----- | :------------------------------------------------------------------ |
| Authorization | string | Bearer token ที่ได้รับจากการตรวจสอบสิทธิ์ด้วย JWT                 |
| Content-Type  | string | ต้องเป็น `multipart/form-data` สำหรับการอัปโหลดไฟล์               |
| Accept        | string | `application/json` เพื่อรับ metadata ของ response                  |

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย โดยใส่ access token ใน header `Authorization` แล้วเรียกใช้คำสั่งด้านล่าง

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pdf" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "datafile=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}


### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK ช่วยให้การพัฒนาเป็นไปอย่างง่ายดาย เนื่องจากจัดการรายละเอียดระดับล่างให้โดยอัตโนมัติ โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:
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

## API อื่นที่มีฟังก์ชันนี้

| **API**        | **ประเภท** | **คำอธิบาย**                                                     | **ลิงก์ Swagger**                                                                           |
| :------------- | :--------- | :--------------------------------------------------------------- | :------------------------------------------------------------------------------------------ |
| /cells/convert | PUT        | แปลงสมุดงานจากเนื้อหาใน request ให้อยู่ในรูปแบบที่กำหนด      | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |

API [POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) ช่วยให้คุณบันทึกไฟล์ MS Excel ในรูปแบบ PDF พร้อมการตั้งค่าเพิ่มเติม และจัดเก็บผลลัพธ์ไว้ในพื้นที่จัดเก็บ

API REST นี้ใช้สำหรับแปลงไฟล์ Excel เป็น PDF

API [PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) ช่วยให้คุณแปลงไฟล์ MS Excel เป็น PDF พร้อมการตั้งค่าเพิ่มเติม และส่งคืนผลลัพธ์ใน response

API [GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) ช่วยให้คุณแปลงไฟล์ MS Excel เป็น PDF พร้อมการตั้งค่าเพิ่มเติม และส่งคืนผลลัพธ์ใน response

API ทั้งสามแบบ [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook), [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) และ [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) นิยาม API ที่เข้าถึงได้แบบสาธารณะ และอนุญาตให้คุณดำเนินการ REST interaction ได้โดยตรงจากเว็บเบราว์เซอร์

สำหรับตัวเลือกการแปลงเพิ่มเติม โปรดดูที่หน้า [Save Options](/cells/save-options/)