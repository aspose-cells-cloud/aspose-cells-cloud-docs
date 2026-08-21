---
title: "ล็อกไฟล์ Excel แบบเป็นชุด"
second_title: "เอกสาร"
type: docs
url: /th/batch/lock
keywords: "ล็อกแบบเป็นชุด, Excel, Aspose.Cells, Cloud API, สเปรดชีต, การป้องกันไฟล์"
description: "Aspose.Cells Cloud API ช่วยให้สามารถล็อกไฟล์ Excel หลายไฟล์ในเวลาเดียวกันได้ โดยใช้ REST endpoint หรือ SDK ที่รองรับ (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go เป็นต้น) เพื่อล็อกไฟล์แบบเป็นชุด"
weight: 100
---

REST API นี้ช่วยให้สามารถ **ล็อกไฟล์ Excel แบบเป็นชุด** ได้

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/lock
```

### **ความปลอดภัยและการพิสูจน์ตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องการ<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การพิสูจน์ตัวตนด้วย JWT token</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย |
|------------------|--------------------|----------|---------------------------------------------|
| BatchLockRequest | BatchLockRequest   | body     | JSON body ที่มีพารามิเตอร์การล็อก |

#### คุณสมบัติของ **BatchLockRequest**

| ชื่อ | ประเภท | คำอธิบาย | หมายเหตุ |
|---------------|--------------------------|--------------------------------------------------------|----------|
| SourceFolder  | string                   | โฟลเดอร์ที่เก็บไฟล์ Excel ต้นทาง | optional |
| MatchCondition| MatchConditionRequest    | เงื่อนไขที่ใช้เลือกไฟล์ที่จะล็อก | optional |
| Password      | string                   | รหัสผ่านที่ใช้กับไฟล์ที่ล็อก | optional |
| OutFolder     | string                   | โฟลเดอร์ปลายทางสำหรับไฟล์ที่ล็อก | optional |

#### คุณสมบัติของ **MatchConditionRequest**

| ชื่อ | ประเภท | คำอธิบาย | หมายเหตุ |
|--------------------|-----------|------------------------------------------------------|----------|
| RegexPattern       | string    | รูปแบบ Regular expression สำหรับจับคู่ชื่อไฟล์ | optional |
| FullMatchConditions| string[]  | การจับคู่ชื่อไฟล์แบบตรงกันทุกประการเพื่อล็อก | optional |

### พารามิเตอร์ของ Request Body

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย |
| -------------- | ---- | ---------------------------------------------- |
| data           | file | เนื้อหาแบบไบนารีของไฟล์สมุดงานที่จะสร้าง |

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

| รหัส | ความหมาย | เกิดขึ้นเมื่อ |
|------|-----------------------------|-----------------------------------------|
| 200 OK | สร้างสมุดงานเรียบร้อยแล้ว | สถานการณ์ปกติ |
| 201 Created | สร้างสมุดงานแล้ว (การตอบกลับทางเลือก) | เมื่อ API ส่งคืนสถานะ creation |
| 400 Bad Request | พารามิเตอร์ไม่ถูกต้อง | ข้อผิดพลาดฝั่งไคลเอนต์ |
| 401 Unauthorized | ไม่มีหรือโทเค็นไม่ถูกต้อง | ข้อผิดพลาดการพิสูจน์ตัวตน |
| 409 Conflict | ไฟล์มีอยู่แล้วและ `isWriteOver=false` | ความขัดแย้งกับไฟล์ที่มีอยู่ |

## วิธีใช้ PostBatchLock API ด้วย SDK

### ข้อกำหนด PostBatchLock API

[ข้อกำหนด OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchLock) นิยามอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างด้านล่างแสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/lock" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\"}"
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

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา โดย SDK จะซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่งานล็อกของคุณได้ โปรดตรวจสอบ[ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud อย่างละเอียด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchLock.go" >}}

{{< /tab >}}

{{< /tabs >}}