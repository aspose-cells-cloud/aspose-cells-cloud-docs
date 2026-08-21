---
title: "การป้องกันไฟล์ Excel แบบเป็นกลุ่ม"
second_title: "เอกสาร"
type: docs
url: /batch/protect
keywords: "การป้องกันไฟล์ Excel แบบเป็นกลุ่ม, Aspose Cells Cloud, REST API, การป้องกัน Excel, การป้องกันแบบเป็นกลุ่ม"
description: "เรียนรู้วิธีใช้ Aspose.Cells Cloud REST API ในการป้องกันไฟล์ Excel หลายไฟล์พร้อมกันแบบเป็นกลุ่ม รวมถึงรายละเอียดคำขอ ตัวอย่าง cURL และตัวอย่างโค้ด SDK สำหรับภาษาต่างๆ"
weight: 100
---

REST API นี้ช่วยให้คุณสามารถ **ป้องกันไฟล์ Excel ที่ผ่านการตรวจสอบแล้วแบบเป็นกลุ่ม** ได้

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/protect
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์      | ประเภท                | ตำแหน่ง | คำอธิบาย                                                                                              |
|-----------------------|---------------------|----------|----------------------------------------------------------------------------------------------------------|
| batchProtectRequest   | BatchProtectRequest | body     | JSON payload ที่ระบุโฟลเดอร์ต้นทาง เงื่อนไขการค้นหา ประเภทการป้องกัน รหัสผ่าน และโฟลเดอร์ปลายทาง |

### คุณสมบัติของ BatchProtectRequest

| ชื่อ            | ประเภท                     | คำอธิบาย                                                                                 | หมายเหตุ |
|-----------------|--------------------------|---------------------------------------------------------------------------------------------|-------|
| SourceFolder    | string                   | โฟลเดอร์ที่เก็บไฟล์ Excel ต้นทาง                                                           | ไม่บังคับ |
| MatchCondition  | MatchConditionRequest   | เกณฑ์ที่ใช้ในการเลือกไฟล์เพื่อป้องกัน                                                    | ไม่บังคับ |
| ProtectionType  | string                   | ประเภทการป้องกันที่จะใช้ (เช่น `All`, `ReadOnly`)                                           | ไม่บังคับ |
| Password        | string                   | รหัสผ่านที่จะตั้งให้กับไฟล์ที่ถูกป้องกัน                                                    | ไม่บังคับ |
| OutFolder       | string                   | โฟลเดอร์ปลายทางสำหรับไฟล์ที่ถูกป้องกัน                                                     | ไม่บังคับ |

### คุณสมบัติของ MatchConditionRequest

| ชื่อ                | ประเภท       | คำอธิบาย                                   | หมายเหตุ |
|---------------------|------------|-----------------------------------------------|-------|
| RegexPattern        | string     | นิพจน์ทั่วไป (Regular expression) ที่ใช้ค้นหาชื่อไฟล์ | ไม่บังคับ |
| FullMatchConditions | string[]   | รายการเงื่อนไขชื่อไฟล์แบบตรงกันทุกประการ          | ไม่บังคับ |

### พารามิเตอร์ใน Request Body

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย                                    |
| -------------- | ---- | ---------------------------------------------- |
| data           | file | เนื้อหาแบบไบนารีของไฟล์สมุดบันทึกที่ต้องการสร้าง |

  
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
**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | เกิดขึ้นเมื่อ                           |
|------|-----------------------------|-----------------------------------------|
| 200 OK | สร้างสมุดบันทึกเรียบร้อยแล้ว | กรณีการทำงานตามปกติ                              |
| 201 Created | สร้างสมุดบันทึกแล้ว (การตอบกลับทางเลือก) | เมื่อ API ส่งคืนสถานะ 'created' |
| 400 Bad Request | พารามิเตอร์ไม่ถูกต้อง | ข้อผิดพลาดฝั่งไคลเอ็นต์                        |
| 401 Unauthorized | ไม่มีหรือ token ไม่ถูกต้อง | ข้อผิดพลาดด้านการยืนยันตัวตน                    |
| 409 Conflict | ไฟล์มีอยู่แล้วและ `isWriteOver=false` | เกิดความขัดแย้งกับไฟล์ที่มีอยู่แล้ว    

## วิธีใช้ PostProtectConvert API ด้วย SDKs

### ข้อมูลเฉพาะของ PostProtectConvert API

[ข้อมูลเฉพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/PostProtectConvert) กำหนด API แบบเปิดที่เข้าถึงได้จากภายนอก และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/protect" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\",\"ProtectionType\":\"All\"}"
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

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ และช่วยให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ กรุณาตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ที่สมบูรณ์

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้เว็บเซอร์วิสของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}