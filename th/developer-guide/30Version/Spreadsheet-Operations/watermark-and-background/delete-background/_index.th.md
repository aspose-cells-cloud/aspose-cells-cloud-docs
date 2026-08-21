---
title: "ลบพื้นหลังออกจากสมุดงาน Excel"
second_title: "เอกสาร"
linktitle: "ลบ"
type: docs
url: /th/delete-background-in-excel-file/
aliases:
  - /delete-background-in-workbook/
  - /workbook/delete-background/
  - /workbook/background/delete/
keywords: "Aspose Cells ลบพื้นหลัง, Excel API ลบพื้นหลัง, Aspose.Cells Cloud, DELETE /cells background"
description: "ลบภาพพื้นหลังออกจากสมุดงาน Excel โดยใช้ Aspose.Cells Cloud API เรียนรู้เกี่ยวกับ endpoint DELETE, พารามิเตอร์ที่จำเป็น, ตัวอย่าง cURL และโค้ด SDK ในภาษา C#, Java, Python และอื่นๆ"
weight: 170
ArticleTitle: "ลบภาพพื้นหลังออกจากสมุดงาน Excel โดยใช้ Aspose.Cells Cloud API"
---

REST API นี้จะลบภาพพื้นหลังของสมุดงาน Excel

## DeleteWorkbookBackground API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/background
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### **พารามิเตอร์แบบ Query**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย                               | จำเป็น |
| ---------------- | ---------- | --------------------------------------- | ------ |
| folder           | string     | โฟลเดอร์ที่เก็บสมุดงานต้นฉบับ          | ไม่จำเป็น |
| storageName      | string     | ชื่อของบริการจัดเก็บข้อมูลที่จะใช้      | ไม่จำเป็น |

### **การตอบกลับ**

```json
{
    "Status" : "OK",
    "Code" : 200
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                    | คำอธิบาย                                              |
|------|-----------------------------|-------------------------------------------------------|
| 200  | สำเร็จ (OK)                 | กรองถูกใช้งานเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                         |
| 413  | ข้อมูลที่ส่งมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                     |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์               |

## วิธีใช้ DeleteWorkbookBackground API ผ่าน SDK

### ข้อมูลจำเพาะของ DeleteWorkbookBackground API

<a href="https://apireference.aspose.cloud/cells/#/Workbook/DeleteWorkbookBackground" target="_blank" rel="noopener noreferrer">ข้อมูลจำเพาะ OpenAPI</a> กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ ซึ่งช่วยให้คุณสามารถโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงคำขอ DELETE แบบสมบูรณ์พร้อมส่วนหัวการยืนยันตัวตนที่จำเป็น ไม่จำเป็นต้องส่งเนื้อหาคำขอ (request body)

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/{name}/background?folder=DotnetFiles" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -H "x-aspose-client: Containerize.Swagger"
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

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">ที่เก็บบน GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4"
   tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby"
   tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}