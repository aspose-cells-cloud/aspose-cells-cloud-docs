---
title: "เพิ่มตัวกรองสีในแผ่นงาน Excel"
second_title: "เอกสาร"
linktitle: "เพิ่มตัวกรองสี"
type: docs
url: /autofilter/add-color-filter/
aliases: [/filter-a-list-using-a-color-filter/,/autofilter/add-a-color-filter/]
keywords: "Excel, ตัวกรองสี, Aspose.Cells Cloud, REST API, auto filter, การยืนยันตัวตนด้วย JWT"
description: "เรียนรู้วิธีใช้ Aspose.Cells Cloud API เพื่อประยุกต์ใช้ตัวกรองสีในแผ่นงาน Excel รวมถึง endpoint, พารามิเตอร์, ตัวอย่าง cURL, การจัดการข้อผิดพลาด และตัวอย่าง SDK"
weight: 65
ArticleTitle: "เพิ่มตัวกรองสีในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud API"
---

เรียนรู้วิธีเพิ่มตัวกรองสีในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud API คู่มือนี้ครอบคลุม endpoint ที่จำเป็น พารามิเตอร์ ข้อกำหนดเบื้องต้นสำหรับการยืนยันตัวตน ตัวอย่างคำสั่ง cURL ตัวอย่าง SDK และการจัดการการตอบกลับ

REST API นี้จะเพิ่ม **ตัวกรองสี** ลงในแผ่นงาน Excel

## PutWorksheetColorFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/colorFilter
```

### **การรักษาความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

### พารามิเตอร์คำขอ:


| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                 |
|----------------|---------|----------|-----------------------------------------------------------------------------|
| name           | string  | path     | ชื่อไฟล์ Excel                                                               |
| sheetName      | string  | path     | ชื่อของแผ่นงานที่มีข้อมูลที่ต้องการกรอง                                          |
| range          | string  | query    | ช่วงของเซลล์ที่ใช้ตัวกรอง (เช่น `A1:B10`)                                     |
| fieldIndex     | integer | query    | ดัชนีแบบเริ่มต้นที่เป็นศูนย์ของคอลัมน์ที่ใช้ตัวกรองสี                              |
| colorFilter    | object  | body     | ออบเจกต์ JSON ที่กำหนดสีพื้นหน้าและสีพื้นหลังที่ใช้กรอง                           |
| matchBlanks    | boolean | query    | ระบุว่าควรรวมแถวที่มีเซลล์ว่างในผลลัพธ์ของการกรองหรือไม่                         |
| refresh        | boolean | query    | หากเป็น `true` แผ่นงานจะถูกปรับปรุงใหม่หลังจากประยุกต์ตัวกรองแล้ว                     |
| folder         | string  | query    | โฟลเดอร์ในพื้นที่จัดเก็บที่ไฟล์ Excel อยู่                                       |
| storageName    | string  | query    | ชื่อของบริการพื้นที่จัดเก็บ (เช่น Aspose Cloud Storage)                            |

**โครงสร้าง JSON ของ `colorFilter`**

| คุณสมบัติ          | ชนิดข้อมูล | คำอธิบาย                                                                    | จำเป็น |
|-------------------|--------|--------------------------------------------------------------------------------|----------|
| Pattern           | string | รูปแบบการกรอง (เช่น `"Solid"`)                                             | ใช่      |
| ForegroundColor   | object | กำหนดสีพื้นหน้า มีคุณสมบัติย่อย เช่น `Color`, `ColorIndex`, `IsShapeColor`, `ThemeColor` และ `Type` | ไม่จำเป็น |
| BackgroundColor   | object | กำหนดสีพื้นหลัง มีคุณสมบัติย่อยเช่นเดียวกับ `ForegroundColor`               | ไม่จำเป็น |

### **การตอบกลับ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                 | ประยุกต์ตัวกรองสำเร็จ; การตอบกลับประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ไม่ครบหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | JWT token ไม่ถูกต้องหรือไม่ได้ส่งมา |
| 413  | ข้อมูลในคำขอใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดภายในเซิร์ฟเวอร์ |
## วิธีใช้ PutWorksheetColorFilter API ผ่าน SDK

### ข้อมูลกำกับ PutWorksheetColorFilter API

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetColorFilter) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบเปิดเผย และช่วยให้คุณดำเนินการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API ผ่าน cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/colorFilter?range=A1%3AB1&fieldIndex=0" \
-X PUT \
-d "{ \"Pattern\": \"Solid\", \"ForegroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 1 }, \"Type\": \"Automatic\" }, \"BackgroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 0 }, \"Type\": \"Automatic\" }}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells ผ่าน SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetColorFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetColorFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetColorFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetColorFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetColorFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetColorFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetColorFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetColorFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

**ดูเพิ่มเติม:** [เพิ่มตัวกรองแบบกำหนดเอง](https://docs.aspose.cloud/cells/autofilter/add-custom-filter/), [เพิ่มตัวกรองวันที่](https://docs.aspose.cloud/cells/autofilter/add-date-filter/), [ลบตัวกรองอัตโนมัติ](https://docs.aspose.cloud/cells/autofilter/remove-auto-filter/)