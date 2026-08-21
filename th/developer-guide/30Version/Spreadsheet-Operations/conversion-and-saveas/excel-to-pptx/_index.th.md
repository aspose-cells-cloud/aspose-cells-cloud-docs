---
title: "การแปลงไฟล์ Excel เป็น PPTX ด้วย Aspose.Cells Cloud API เวอร์ชัน 3.0"
second_title: "เอกสาร"
linktitle: "Excel เป็น PPTX"
type: docs
url: /convert-excel-file-to-pptx/
keywords: "Aspose, Cells, Excel, PPTX, การแปลง, REST API, คลาวด์"
description: "เรียนรู้วิธีการแปลงสมุดงาน Excel เป็นพรีเซนเทชัน PPTX ด้วย Aspose.Cells Cloud REST API เวอร์ชัน 3.0 ประกอบด้วยตัวอย่างคำขอ cURL โค้ดตัวอย่าง SDK การยืนยันตัวตน และการจัดการข้อผิดพลาด"
weight: 90
ArticleTitle: "การแปลงไฟล์ Excel เป็น PPTX ด้วย Aspose.Cells Cloud API เวอร์ชัน 3.0"
---

REST API นี้ใช้แปลงไฟล์สเปรดชีตเป็นรูปแบบ PPTX

## API PostConvertWorkbookToPptx

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pptx
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### พารามิเตอร์ Query

| ชื่อพารามิเตอร์        | ประเภท | คำอธิบาย                                                                                  |
| ----------------------- | ------ | ----------------------------------------------------------------------------------------- |
| `password`              | string | รหัสผ่านที่จำเป็นสำหรับการเปิดสมุดงาน Excel                                               |
| `storageName`           | string | ชื่อของพื้นที่จัดเก็บที่ไฟล์ต้นฉบับอยู่                                                    |
| `checkExcelRestriction` | bool   | ระบุว่าจะบังคับข้อจำกัดของไฟล์ Excel เมื่อแก้ไขวัตถุที่เกี่ยวข้องกับเซลล์หรือไม่         |

### พารามิเตอร์ Request Body

| ชื่อพารามิเตอร์ | ประเภท      | คำอธิบาย                                                           |
| -------------- | --------- | ------------------------------------------------------------------ |
| `datafile`     | data file | ไฟล์ Excel ที่อยู่ในส่วนแรกของ Request Body แบบมัลติพาร์ท         |

**ตัวอย่าง Request Body แบบมัลติพาร์ท (อย่างย่อ):**

```
--boundary
Content-Disposition: form-data; name="File"; filename="input.xlsx"
Content-Type: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet

<เนื้อหาไบนารีของ input.xlsx>
--boundary
Content-Disposition: form-data; name="password"

MyPwd
--boundary--
```

### Response

API จะส่งคืนวัตถุ **FileInfo** ซึ่งมีไฟล์ pptx ที่ถูกสร้างขึ้น

| ฟิลด์           | ประเภท | คำอธิบาย                                         |
| --------------- | ------ | ------------------------------------------------ |
| **Filename**    | string | ชื่อไฟล์ pptx (เช่น `example.pptx`)              |
| **FileSize**    | int    | ขนาดไฟล์เป็นไบต์                                 |
| **FileContent** | string | เนื้อหาของไฟล์ pptx ที่เข้ารหัสแบบ Base64         |

[FileInfo](/cells/file-info/)

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย                                                                 |
|------|-----------------------------|--------------------------------------------------------------------------|
| 200  | สำเร็จ (OK)                 | กรองถูกใช้งานสำเร็จ; Response ประกอบด้วยรายละเอียดของการดำเนินการ     |
| 400  | คำขอไม่ถูกต้อง (Bad Request)| พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)                 |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)| โทเคน JWT ไม่ถูกต้องหรือขาดหาย                                           |
| 413  | Payload ใหญ่เกินไป (Payload Too Large)| ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                        |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error)| ข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์                                   |

*หมายเหตุ:* จุดปลายทางนี้รองรับรูปแบบ Excel ทั่วไป (`.xlsx`, `.xls`, `.xlsm`) ขนาดไฟล์สูงสุดจำกัดอยู่ที่ 50 MB การแปลงอาจถูกจำกัดสำหรับสมุดงานที่มีมาโครหรือแผ่นงานที่ได้รับการป้องกัน เว้นแต่จะระบุพารามิเตอร์ที่เหมาะสม

## วิธีใช้งาน API PostConvertWorkbookToPptx ด้วย SDK

### ข้อมูลจำเพาะ API PostConvertWorkbookToPptx

<a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPptx" rel="noopener noreferrer">ข้อมูลจำเพาะ OpenAPI</a> นิยามอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการโต้ตอบ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างด้านล่างแสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pptx?storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/path/to/input.xlsx" \
     -F "password=MyPwd"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.pptx",
  "FileSize": 123456,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้งาน SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK ซ่อนรายละเอียดระดับต่ำไว้ ช่วยให้คุณมุ่งเน้นไปที่โปรเจกต์ของคุณ ดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมดได้ที่ [GitHub repository](https://github.com/aspose-cells-cloud" rel="noopener noreferrer")

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPptx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPptx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPptx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPptx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPptx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1c" "Example_PostConvertWorkbookToPptx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPptx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPptx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## API อื่นที่ดำเนินฟังก์ชันนี้

- **[POST /cells/convert/pdf](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPdf)** – แปลงไฟล์ Excel เป็น PDF
- **[POST /cells/convert/png](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPng)** – แปลงไฟล์ Excel เป็นภาพ PNG
- **[POST /cells/convert/svg](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSvg)** – แปลงไฟล์ Excel เป็นรูปแบบ SVG
---