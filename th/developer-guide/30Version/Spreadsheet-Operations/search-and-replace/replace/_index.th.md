---
title: "แทนที่ข้อความจากไฟล์ Excel"
second_title: "เอกสาร"
linktype: "แทนที่โดยไม่ใช้พื้นที่จัดเก็บ"
type: docs
url: /replace/
keywords: "แทนที่ข้อความใน Excel, Aspose.Cells Cloud, REST API, แทนที่ในสเปรดชีต, API, การแทนที่ข้อความในไฟล์ Excel"
description: "ใช้ Aspose.Cells Cloud REST API เพื่อแทนที่ข้อความที่มีอยู่ด้วยค่าใหม่ในไฟล์ Excel มี SDK รองรับสำหรับ C#, Java, Python, Node.js, PHP, Ruby, Go และ Perl"
weight: 80
---


## REST API

REST API นี้ใช้แทนที่ข้อมูลในไฟล์ Excel

```bash
POST https://api.aspose.cloud/v3.0/cells/replace
```

### ความปลอดภัยและการยืนยันตัวตน

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้การยืนยันตัวตนแบบ [โทเคน JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)


### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง              | คำอธิบาย                                      |
| ---------------- | ------ | --------------------- | --------------------------------------------- |
| **file**         | ไฟล์   | formData (multipart)  | ไฟล์ Excel ที่ต้องการประมวลผล               |
| **text**         | สายอักขระ | query             | ข้อความที่ต้องการแทนที่                     |
| **newtext**      | สายอักขระ | query             | ข้อความที่ใช้แทน                            |
| **password**     | สายอักขระ | query             | รหัสผ่านสำหรับสมุดงานที่มีการป้องกัน (ไม่บังคับ) |
| **sheetname**    | สายอักขระ | query             | ชื่อแผ่นงานที่ต้องการเป้าหมาย (ไม่บังคับ)     |

### **การตอบกลับ**

```json
{
  "Status":"OK",
  "Code":200,
  "Files": [
    {
      "Filename" : "[ชื่อไฟล์1]",
      "Filesize" : [ขนาดไฟล์],
      "FileContent" : "[Base64String]"
    },
    {
      "Filename" : "[ชื่อไฟล์2]",
      "Filesize" : [ขนาดไฟล์],
      "FileContent" : "[Base64String]"
    },
    {
      "Filename" : "[ชื่อไฟล์3]",
      "Filesize" : [ขนาดไฟล์],
      "FileContent" : "[Base64String]"
    }
  ]
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                    | คำอธิบาย                                         |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                 | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                |
| 413  | ข้อมูลส่งไปใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด             |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์       |
## วิธีใช้ PostReplace API ผ่าน SDK

### ข้อมูลจำเพาะ PostReplace API

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostReplace) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/replace?text=1&newtext=aspose.cells.cloud" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxx1",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "xxxx2",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK สำหรับคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการกับรายละเอียดระดับต่ำให้คุณ แล้วคุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [คลังเก็บบน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostReplace.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostReplace.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostReplace.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostReplace.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostReplace.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostReplace.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostReplace.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostReplace.go" >}}

{{< /tab >}}

{{< /tabs >}}