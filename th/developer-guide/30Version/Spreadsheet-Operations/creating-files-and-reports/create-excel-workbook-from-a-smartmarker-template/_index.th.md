---
title: "สร้างรายงาน Excel ด้วยเทมเพลต Smart Marker"
second_title: "เอกสาร"
linktype: "SmartMarker"
type: docs
url: /build-report-with-smart-marker/
aliases:
  - /create-excel-workbook-from-a-smartmarker-template/
  - /workbook/smartmarker/
  - /workbook/create/smartmarker/
keywords: "Excel, Smart Marker, Aspose.Cells Cloud, REST API, สมุดงาน, SDK, API, การสร้างรายงาน"
description: "เรียนรู้วิธีการสร้างสมุดงาน Excel จากเทมเพลต Smart Marker โดยใช้ Aspose.Cells Cloud REST API พร้อมรายละเอียดคำขอ/การตอบกลับ ตัวอย่าง cURL ข้อกำหนดเบื้องต้น หมายเหตุ และตัวอย่างโค้ด SDK"
weight: 40
ArticleTitle: "สร้างรายงาน Excel ด้วยเทมเพลต Smart Marker – คู่มือ API Aspose.Cells Cloud"
---

REST API นี้สร้างสมุดงานโดยใช้เทมเพลต Smart Marker

## API สมุดงาน SmartMarker

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/smartmarker
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

### **Smart Marker คืออะไร?**

Smart Marker เป็นไวยากรณ์แบบตัวยึดตำแหน่งที่แมปฟิลด์ข้อมูลในไฟล์ XML (หรือ JSON) กับเซลล์ในเทมเพลต Excel เมื่อรันโปรแกรม Aspose.Cells จะแทนที่ตัวยึดตำแหน่งด้วยข้อมูลที่สอดคล้องกัน ช่วยให้คุณสร้างรายงานที่เต็มไปด้วยข้อมูลได้โดยอัตโนมัติผ่านโค้ด

### **พารามิเตอร์ Query**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย                                      |
| ---------------- | ---------- | --------------------------------------------- |
| outPath          | string     | เส้นทางปลายทางที่จะบันทึกสมุดงานที่สร้างขึ้น |
| folder           | string     | โฟลเดอร์ที่เก็บสมุดงานต้นฉบับ                |
| storageName      | string     | ชื่อของบริการจัดเก็บข้อมูลที่จะใช้           |

### **พารามิเตอร์ Request Body**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย                                      |
| ---------------- | ---------- | --------------------------------------------- |
| xmlFile          | file       | ไฟล์ข้อมูล XML ของ Smart Marker ที่อัปโหลดพร้อมคำขอนี้ |

### **การตอบกลับ**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**หมายเหตุ / ข้อจำกัด:**  
- API รองรับไฟล์ Excel ขนาดสูงสุด **50 เมกะไบต์**  
- รูปแบบที่รองรับมีเพียง **.xlsx**, **.xlsm** และ **.xlsb** เท่านั้น  
- มีการจำกัดอัตราการใช้งานที่ **20 คำขอต่อวินาที** ต่อบัญชี

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                | คำอธิบาย                                            |
| ---- | ------------------------ | --------------------------------------------------- |
| 200  | สำเร็จ (OK)             | ประมวลผลสำเร็จ; การตอบกลับมีรายละเอียดของคำสั่ง |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น รูปแบบไฟล์ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | JWT token ไม่ถูกต้องหรือขาดหาย                     |
| 413  | ข้อมูลส่งมายังใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                 |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดภายในเซิร์ฟเวอร์       |

## วิธีการใช้งาน API สมุดงาน SmartMarker

### ข้อกำหนด API สมุดงาน SmartMarker

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookGetSmartMarkerResult) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ใช้ SDK ของ Aspose.Cells Cloud

คุณสามารถใช้เครื่องมือ **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ผ่าน cURL

**ตัวอย่างแบบสั้นกระชับ**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/{name}/smartmarker?outPath={outPath}" -H "Authorization: Bearer {access_token}" -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/newworkbook_14.xlsx/smartmarker?outPath=GeneratedReport.xlsx" \
    -H "accept: multipart/form-data" \
    -H "x-aspose-client: Containerize.Swagger" \
    -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
HTTP/1.1 200 OK
Content-Type: application/json

{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### **การจัดการข้อผิดพลาด**

| สถานะ HTTP | คำอธิบาย             | สาเหตุที่พบบ่อย                                 |
| ----------- | -------------------- | ------------------------------------------------ |
| 400         | คำขอไม่ถูกต้อง (Bad Request) | เทมเพลตขาดหาย XML ผิดรูปแบบ หรือพารามิเตอร์ไม่ถูกต้อง |
| 401         | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็นการยืนยันตัวตนไม่ถูกต้องหรือขาดหาย       |
| 404         | ไม่พบ (Not Found)    | สมุดงานหรือตำแหน่งที่ตั้งของพื้นที่จัดเก็บที่ระบุไม่มีอยู่จริง |
| 500         | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดภายในเซิร์ฟเวอร์     |

**ตัวอย่างการตอบกลับข้อผิดพลาด (400)**

```json
{
  "Code": 400,
  "Message": "ไฟล์ข้อมูล XML ขาดหายหรือผิดรูปแบบ"
}
```

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งกระบวนการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreate.go" >}}

{{< /tab >}}

{{< /tabs >}}