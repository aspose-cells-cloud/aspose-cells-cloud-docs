---
title: "เพิ่มรูปภาพพื้นหลังให้กับสมุดงาน"
second_title: "เอกสาร"
linktype: "เพิ่ม"
type: docs
url: /add-background-in-excel-file/
aliases:
  - /add-background-in-workbook/
  - /workbook/add-background/
  - /workbook/background/add/
keywords: "Aspose.Cells, เพิ่มรูปภาพพื้นหลัง, Excel API, REST, cloud SDK, cURL, พื้นหลังสมุดงาน"
description: "เรียนรู้วิธีการเพิ่มรูปภาพพื้นหลังให้กับสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API รวมถึงพารามิเตอร์ที่จำเป็น รายละเอียดการยืนยันตัวตน ตัวอย่าง cURL แบบสมบูรณ์ และข้อมูลการจัดการข้อผิดพลาด"
weight: 160
---

## REST API

REST API นี้จะเพิ่ม **รูปภาพพื้นหลัง** ให้กับสมุดงาน Excel

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/background
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

### พารามิเตอร์ใน Query String

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย                                             |
| ---------------- | ------ | ----------------------------------------------------- |
| `picPath`        | string | เส้นทางไปยังไฟล์รูปภาพที่จะใช้เป็นพื้นหลัง           |
| `folder`         | string | โฟลเดอร์ที่เก็บสมุดงานต้นฉบับ                        |
| `storageName`    | string | ชื่อของ storage ที่ไฟล์นั้นๆ ถูกเก็บไว้                |

### พารามิเตอร์ใน Request Body

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย                                                |
| ---------------- | ------ | -------------------------------------------------------- |
| `datafile`       | file   | ไฟล์สมุดงานที่จะนำไปใช้รูปภาพพื้นหลัง                   |

**พารามิเตอร์ใน Path** – `{name}` ใน URL แทน **ชื่อไฟล์สมุดงาน** (เช่น `Book1.xlsx`)

### **คำตอบ (Response)**

```json
{
    "Status" : "OK",
    "Code" : 200
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                   | คำอธิบาย                                                                 |
|-----|----------------------------|--------------------------------------------------------------------------|
| 200 | OK                         | ใช้งานตัวกรองสำเร็จ; คำตอบประกอบด้วยรายละเอียดของการดำเนินการ         |
| 400 | Bad Request                | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ)           |
| 401 | Unauthorized               | JWT token ไม่ถูกต้องหรือขาดหาย                                           |
| 413 | Payload Too Large          | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                        |
| 500 | Internal Server Error      | เกิดข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด                                 |

## วิธีใช้ PutWorkbookBackground API ผ่าน SDK

### ข้อมูลการกำหนดค่า PutWorkbookBackground API

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground) นิยาม API ที่สามารถเข้าถึงได้แบบสาธารณะ ซึ่งช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงคำขอแบบสมบูรณ์ รวมถึงฟลา็กการอัปโหลดไฟล์แบบ multipart และ header ที่จำเป็นสำหรับการยืนยันตัวตน

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="คำตอบ" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/background?picPath=DotnetFiles%2FWaterMark.png&folder=DotnetFiles" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "datafile=@/path/to/Book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะซ่อนรายละเอียดระดับต่ำไว้ ช่วยให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณได้ ดูรายชื่อ SDK ของ Aspose.Cells Cloud แบบเต็มได้ที่ [GitHub repository](https://github.com/aspose-cells-cloud)

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}