---
title: "ปลดล็อกแบบแบทช์"
second: "เอกสาร"
type: docs
url: /batch/unlock
keywords: "ปลดล็อกแบบแบทช์, Aspose.Cells Cloud, Excel, REST API, สเปรดชีต, cloud SDK"
description: "ปลดล็อกไฟล์ Excel หลายไฟล์แบบแบทช์โดยใช้ Aspose.Cells Cloud REST API รองรับ SDK สำหรับ C#, Java, Python และภาษาอื่นๆ"
weight: 100
---

REST API นี้ปลดล็อกไฟล์ Excel ที่มีสิทธิ์ปลดล็อกแบบแบทช์

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/unlock
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
|----------------|------|----------|-------------|
| **BatchLockRequest** |  | body | เนื้อหาคำขอที่มีการตั้งค่าการปลดล็อก |

### คุณสมบัติของ **BatchLockRequest**

| ชื่อ          | ชนิดข้อมูล                     | คำอธิบาย                                 | หมายเหตุ |
|---------------|--------------------------|---------------------------------------------|-------|
| SourceFolder  | string                   | โฟลเดอร์ที่มีไฟล์ Excel ต้นทาง           | [ไม่บังคับ] |
| MatchCondition| MatchConditionRequest    | เงื่อนไขที่ใช้คัดเลือกไฟล์สำหรับการปลดล็อก | [ไม่บังคับ] |
| Password      | string                   | รหัสผ่านที่ใช้กับสมุดงานที่ได้รับการป้องกัน | [ไม่บังคับ] |
| OutFolder     | string                   | โฟลเดอร์ปลายทางสำหรับไฟล์ที่ปลดล็อกแล้ว   | [ไม่บังคับ] |

### คุณสมบัติของ **MatchConditionRequest**

| ชื่อ               | ชนิดข้อมูล      | คำอธิบาย                                 | หมายเหตุ |
|--------------------|-----------|---------------------------------------------|-------|
| RegexPattern       | string    | รูปแบบนิพจน์ทั่วไป (Regular Expression) สำหรับจับคู่ชื่อไฟล์ | [ไม่บังคับ] |
| FullMatchConditions| string[]  | เงื่อนไขชื่อไฟล์แบบตรงกันทุกประการสำหรับการจับคู่ | [ไม่บังคับ] |

### พารามิเตอร์เนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย                                    |
| -------------- | ---- | ---------------------------------------------- |
| data           | file | เนื้อหาแบบไบนารีของไฟล์สมุดงานที่ต้องการสร้าง |

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
| 200 OK | สร้างสมุดงานเรียบร้อยแล้ว | กรณีการทำงานตามปกติ                              |
| 201 Created | สร้างสมุดงานเรียบร้อยแล้ว (การตอบกลับทางเลือก) | เมื่อ API ส่งคืนสถานะสร้างเสร็จสิ้น |
| 400 Bad Request | พารามิเตอร์ไม่ถูกต้อง | ข้อผิดพลาดฝั่งไคลเอนต์                        |
| 401 Unauthorized | ไม่มีโทเค็นหรือโทเค็นไม่ถูกต้อง | ข้อผิดพลาดด้านการยืนยันตัวตน                    |
| 409 Conflict | มีไฟล์อยู่แล้วและ `isWriteOver=false` | ขัดแย้งกับไฟล์ที่มีอยู่แล้ว    

## วิธีใช้ API PostBatchLock ด้วย SDK

### ข้อมูลจำเพาะ API PostBatchLock


[OpenAPI Specification](https://reference.aspose.cloud/cells/#/Batch/PostBatchUnlock) นิยามอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/unlock" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"SourceFolder":"CellsTests","OutFolder":"Output","MatchCondition":{"RegexPattern":"(^Book)(.+)(xlsx$)"},"Password":"123456"}'
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

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนาฟังก์ชันการปลดล็อก SDK จะซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud แบบครบถ้วน

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchUnlock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchUnlock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchUnlock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchUnlock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchUnlock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchUnlock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchUnlock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchUnlock.go" >}}

{{< /tab >}}

{{< /tabs >}}