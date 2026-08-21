---
title: "ป้องกันไฟล์ Excel"
second_title: "เอกสาร"
linktype: "เข้ารหัสไฟล์ Excel"
type: docs
url: /protect-excel-files/
aliases:
  [
    /protect/without-storage/,
    /protect/without-using-storage/,
    /protect/without-using-storage/,
  ]
keywords: "Aspose.Cells, API ป้องกัน Excel, เข้ารหัสสมุดงาน Excel, ความปลอดภัยของสเปรดชีตบนคลาวด์, REST API"
description: "ใช้ REST API ของ Aspose.Cells Cloud เพื่อป้องกันไฟล์ Excel คู่มือนี้แสดงวิธีการเข้ารหัสสมุดงานผ่าน HTTP POST, cURL และ SDK สำหรับภาษาโปรแกรมต่างๆ ณ ปี 2026"
weight: 40
---

REST API นี้ใช้ป้องกันไฟล์ Excel

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/protect
```

### ความปลอดภัยและการพิสูจน์ตัวตน

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ [การพิสูจน์ตัวตนด้วยโทเค็น JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย |
| -------------- | ------ | ------------------------- | ------------------------------------- |
| file           | ไฟล์   | formData (body)           | ไฟล์ที่จะอัปโหลด                      |
| password       | สตริง | สตริงคำสั่ง (`password`) | รหัสผ่านที่ใช้ป้องกันสมุดงาน          |

### การตอบกลับ


```json
{
  "Status":"OK",
  "Code":200,
  "Files": [
    {
      "Filename": "ชื่อไฟล์ที่ได้รับการป้องกัน: smaple1.xlsx",
      "FileSize": ขนาด,
      "FileContent": "-----Base64String ของ sample1-----"
    },
    {
      "Filename": "ชื่อไฟล์ที่ได้รับการป้องกัน: sample2.xlsx",
      "FileSize": ขนาด,
      "FileContent": "-----Base64String ของ sample2-----"
    }
  ]
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | คำอธิบาย                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                 | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ไม่ครบหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็น JWT ไม่ถูกต้องหรือไม่มี |
| 413  | ข้อมูลส่งไปมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์ |

## วิธีใช้ PostProtect API ผ่าน SDK

### ข้อมูลจำเพาะ PostProtect API

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostProtect) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถโต้ตอบกับ REST ผ่านเบราว์เซอร์เว็บได้โดยตรง

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียก API บนคลาวด์ผ่าน cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/protect?password=MySecretPwd" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@sample1.xlsx' \
  -F 'file2=@sample2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "sample1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String ของ sample1-----"
    },
    {
      "Filename": "sample2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String ของ sample2-----"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### **การจัดการข้อผิดพลาด**

– API สามารถส่งรหัสสถานะต่อไปนี้กลับมาได้:

| รหัส HTTP | ความหมาย                                 | ตัวอย่างข้อมูล JSON แสดงข้อผิดพลาด |
| --------- | --------------------------------------- | --------------------------------------------------- |
| 400       | คำขอไม่ถูกต้อง (เช่น ไฟล์ไม่ได้ส่งมา)        | `{"Code":400,"Message":"จำเป็นต้องมีไฟล์"}`        |
| 401       | ไม่ได้รับอนุญาต (โทเค็นไม่ถูกต้องหรือไม่มี) | `{"Code":401,"Message":"โทเค็นการเข้าถึงไม่ถูกต้อง"}`    |
| 403       | ถูกปฏิเสธการเข้าถึง (สิทธิ์ไม่เพียงพอ)    | `{"Code":403,"Message":"การเข้าถึงถูกปฏิเสธ"}`           |
| 500       | ข้อผิดพลาดภายในเซิร์ฟเวอร์                   | `{"Code":500,"Message":"เกิดข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด"}` |

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ดังนั้นคุณสามารถมุ่งเน้นไปที่งานโครงการของคุณได้ โปรดดูที่ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกบริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}