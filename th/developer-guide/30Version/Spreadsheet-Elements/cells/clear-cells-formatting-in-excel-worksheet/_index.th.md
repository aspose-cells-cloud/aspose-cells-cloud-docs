---
title: "ล้างรูปแบบเซลล์ในสมุดงาน Excel"
type: docs
url: /clear-cells-formatting-in-excel-worksheet/
weight: 100
keywords: "Aspose.Cells Cloud, Excel, ล้างรูปแบบเซลล์, REST API, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "ใช้ Aspose.Cells Cloud REST API เพื่อล้างรูปแบบเซลล์ในสมุดงาน Excel ประกอบด้วยรายละเอียดคำขอ ตัวอย่าง cURL และตัวอย่างโค้ด SDK สำหรับหลายภาษา"
ArticleTitle: "ล้างรูปแบบเซลล์ในสมุดงาน Excel - Aspose.Cells Cloud API"
---

**หมายเหตุ:** การเรียกใช้ Aspose.Cells Cloud API ทั้งหมดต้องดำเนินการผ่าน **HTTPS** เท่านั้น เส้นทาง endpoints แบบ HTTP ถูกเลิกใช้งานแล้ว และอาจถูกบล็อกโดยเบราว์เซอร์

- **เมธอด:** POST  
- **endpoint:** `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearformats`

REST API นี้ใช้ล้างรูปแบบเซลล์ในไฟล์ Excel และเป็นส่วนหนึ่งของชุด Aspose.Cells Cloud สำหรับล้างรูปแบบเซลล์ในworksheet Excel

## PostClearFormats API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearformats
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### **การตอบกลับ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**โครงสร้างข้อมูลการตอบกลับ**

| ฟิลด์ | ประเภท | คำอธิบาย |
|--------|---------|-----------------------------------------------|
| Code   | integer | รหัสสถานะ HTTP ที่ส่งคืนโดย API (เช่น 200) |
| Status | string  | ผลลัพธ์ของการดำเนินการ (`OK` สำหรับความสำเร็จ) |

**รหัสสถานะ HTTP**

| รหัส | ความหมาย | คำอธิบาย |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK | ใช้ตัวกรองสำเร็จ; การตอบกลับประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | Bad Request | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401  | Unauthorized | JWT token ไม่ถูกต้องหรือขาดหาย |
| 413  | Payload Too Large | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | Internal Server Error | เกิดข้อผิดพลาดภายในเซิร์ฟเวอร์ที่ไม่คาดคิด |

## วิธีใช้ PostClearFormats API ร่วมกับ SDKs

### ข้อกำหนด PostClearFormats API

<a href="https://apireference.aspose.cloud/cells/#/Cells/PostClearFormats" rel="noopener noreferrer">OpenAPI Specification</a> กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้แบบเปิดเผย และช่วยให้คุณสามารถโต้ตอบกับ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งใน command-line เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/clearformats?range=a1%3Aa10&startRow=1&startColumn=1&endRow=10&endColumn=10" \
  -X POST \
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

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ดังนั้นคุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บ Aspose.Cells ด้วย SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostClearFormats.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostClearFormats.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostClearFormats.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostClearFormats.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostClearFormats.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostClearFormats.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostClearFormats.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostClearFormats.go" >}}

{{< /tab >}}

{{< /tabs >}}

**ดูเพิ่มเติม**

- [ล้างเนื้อหาและรูปแบบของเซลล์](https://docs.aspose.cloud/cells/clear-contents-and-styles)  
- [ตั้งค่ารูปแบบเซลล์](https://docs.aspose.cloud/cells/set-cell-style)
---