---
title: "แปลง Excel เป็น PNG"
second_title: "เอกสาร"
linktitle: "Excel to PNG"
type: docs
url: convert-excel-file-to-png-file/
keywords: "Excel to PNG, Aspose.Cells Cloud, REST API, การแปลงสเปรดชีต, รูปแบบ PNG"
description: "แปลงไฟล์สเปรดชีต Excel เป็นภาพ PNG โดยใช้ REST API ของ Aspose.Cells Cloud มีการรองรับ SDK หลายตัวและมีตัวอย่างรายละเอียดสำหรับภาษาโปรแกรมต่างๆ"
weight: 90
---

REST API นี้ใช้แปลงไฟล์สเปรดชีตให้อยู่ในรูปแบบ PNG

## ข้อมูลเฉพาะของ REST API

```
POST https://api.aspose.cloud/v3.0/cells/convert/png
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### **พารามิเตอร์แบบ Query**

| ชื่อพารามิเตอร์      | ชนิดข้อมูล | คำอธิบาย                                                                                       |
| --------------------- | ---------- | ---------------------------------------------------------------------------------------------- |
| password              | string     | รหัสผ่านที่จำเป็นสำหรับการเปิดไฟล์ Excel                                                       |
| storageName           | string     | ชื่อของพื้นที่เก็บข้อมูลที่ไฟล์นั้นอยู่                                                         |
| checkExcelRestriction | bool       | กำหนดว่าจะตรวจสอบข้อจำกัดของไฟล์ Excel เมื่อมีการแก้ไขเซลล์หรือวัตถุที่เกี่ยวข้องหรือไม่       |

### **พารามิเตอร์ใน Request Body**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย                                                                 |
| ---------------- | ---------- | ------------------------------------------------------------------------ |
| datafile         | data file  | ไฟล์สเปรดชีตที่ส่งมาในส่วนแรกของ request แบบ multipart                   |

### **Response**

API จะส่งคืน **FileInfo** ซึ่งประกอบด้วยไฟล์ PNG ที่ถูกสร้างขึ้น

| ฟิลด์           | ชนิดข้อมูล | คำอธิบาย                                     |
| --------------- | ---------- | -------------------------------------------- |
| **Filename**    | string     | ชื่อไฟล์ PNG (เช่น `example.png`)            |
| **FileSize**    | int        | ขนาดไฟล์เป็นไบต์                             |
| **FileContent** | string     | เนื้อหาไฟล์ PNG ที่เข้ารหัสแบบ Base64         |

[FileInfo](/cells/file-info/)


**รหัสสถานะ HTTP**

| รหัส | ความหมาย                    | คำอธิบาย                                                    |
|------|-----------------------------|-------------------------------------------------------------|
| 200  | สำเร็จ (OK)                 | กรองข้อมูลสำเร็จ; response ประกอบด้วยรายละเอียดการดำเนินการ |
| 400  | Request ไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                              |
| 413  | Payload ใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                            |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดในเซิร์ฟเวอร์                      |

## วิธีใช้ PostConvertWorkbookToPNG API ร่วมกับ SDK

### ข้อมูลเฉพาะของ PostConvertWorkbookToPNG API

[OpenAPI Specification](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPNG) กำหนด API ที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถเรียกใช้การโต้ตอบ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/png" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d {"File":{}}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.png",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPNG.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPNG.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPNG.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPNG.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPNG.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPNG.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPNG.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPNG.go" >}}

{{< /tab >}}

{{< /tabs >}}

## API อื่นๆ ที่มีฟังก์ชันที่คล้ายกัน

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – บันทึกไฟล์ Excel ในรูปแบบ CSV (หรือรูปแบบอื่นๆ) พร้อมการตั้งค่าเพิ่มเติม และจัดเก็บผลลัพธ์
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – แปลงไฟล์ Excel เป็น CSV (หรือรูปแบบอื่นๆ) พร้อมพารามิเตอร์ทางเลือก และส่งคืนผลลัพธ์ใน response
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – ดึงไฟล์ Excel และสามารถแปลงเป็น CSV (หรือรูปแบบอื่นๆ) ได้ทันที

---