---
title: "อัปเดตข้อมูลเมตา"
second_title: "เอกสาร"
linktype: "อัปเดตโดยไม่ใช้ที่จัดเก็บข้อมูล"
type: docs
url: /metadata/update/
keywords: "metadata, Excel, Aspose.Cells Cloud, REST API, update, spreadsheet"
description: "Aspose.Cells Cloud REST API ช่วยให้สามารถอัปเดตข้อมูลเมตาในไฟล์ Excel ได้ โดยรองรับ SDK หลายภาษา (เช่น C#, Java, Python, Ruby, Go เป็นต้น) เพื่อการรวมระบบอย่างราบรื่นบนภาษาโปรแกรมต่างๆ"
weight: 35
ArticleTitle: "อัปเดตข้อมูลเมตา – เอกสารประกอบ API ของ Aspose.Cells Cloud"
---

REST API นี้ใช้สำหรับอัปเดต **ข้อมูลเมตา** ในไฟล์ Excel หลายไฟล์

**ข้อกำหนดเบื้องต้น:** บัญชี Aspose Cloud ที่ยังไม่หมดอายุ, โทเคน JWT ที่ใช้งานได้ และไฟล์ Excel ที่ต้องการอัปโหลด

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/metadata/update
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์   | ชนิดข้อมูล | ตำแหน่ง         | คำอธิบาย                                      |
| ------------------ | -------- | ---------------- | ---------------------------------------------- |
| file               | ไฟล์    | formData         | ไฟล์ Excel ที่ต้องการอัปโหลด                   |
| DocumentProperties | ออบเจกต์ | HTTP body (JSON) | คุณสมบัติของเอกสารที่จะตั้งค่าให้กับไฟล์ Excel |

**หมายเหตุ:** สามารถอัปโหลดไฟล์ได้สูงสุด 10 ไฟล์ต่อคำขอละครั้ง รูปแบบที่รองรับ ได้แก่ `.xlsx`, `.xls` และ `.csv` โดยขนาดรวมของคำขอจะต้องไม่เกิน 100 MB

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PostMetadata) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST interaction ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่าน command-line เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="คำตอบ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/metadata/update" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'xxxxx1=@xxxx1.xlsx' \
  -F 'xxxxx2=@xxxx2.xlsx' \
  -d '[{ "name": "test", "value": "test" }]'
```

คำขอนี้ต้องมี header **Authorization** พร้อม JWT token แบบ Bearer โปรดตรวจสอบให้แน่ใจว่า token ถูกสร้างขึ้นโดยใช้ข้อมูลประจำตัวของลูกค้า Aspose Cloud ของคุณ

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้ ช่วยให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}

**ดูเพิ่มเติม:**  
- [รับข้อมูลเมตา](/metadata/get/)  
- [ลบข้อมูลเมตา](/metadata/delete/)  
---