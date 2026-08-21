---
title: "รีเฟรชตัวกรองอัตโนมัติในแผ่นงาน Excel"
second_title: "เอกสาร"
linktitle: "รีเฟรชตัวกรองอัตโนมัติ"
type: docs
url: /autofilter/refresh/
aliases: [/refresh-an-autofilter/]
weight: 100
keywords: "Aspose.Cells, AutoFilter, รีเฟรช, Excel, API, REST"
description: "รีเฟรชตัวกรองอัตโนมัติที่มีอยู่ในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API พร้อมตัวอย่าง cURL และ SDK สำหรับ C#, Java, Python และอื่นๆ"
ArticleTitle: "รีเฟรชตัวกรองอัตโนมัติในแผ่นงาน Excel"
---

### **รีเฟรช** ทำหน้าที่อะไร?

การเรียกใช้เอนด์พอยต์นี้จะนำเกณฑ์การกรองปัจจุบันไปใช้ใหม่หลังจากข้อมูลในแผ่นงานเปลี่ยนแปลง (เช่น เพิ่มหรือลบแถว) การดำเนินการนี้ไม่ได้แก้ไขคำนิยามของตัวกรอง แต่เพียงแค่ปรับปรุงมุมมองและส่งคืนการตอบกลับสถานะเท่านั้น

### REST API

REST API นี้รีเฟรชตัวกรองอัตโนมัติในแผ่นงาน Excel (เวอร์ชัน API **v3.0**)

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/refresh
```

### **ความปลอดภัยและการรับรองความถูกต้อง**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การรับรองความถูกต้องแบบ JWT token</a>

### **การตอบกลับ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                   | คำอธิบาย                                                                 |
|------|-----------------------------|--------------------------------------------------------------------------|
| 200  | สำเร็จ (OK)                 | ใช้งานตัวกรองสำเร็จ การตอบกลับประกอบด้วยรายละเอียดการดำเนินการ       |
| 400  | คำร้องขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์หายไปหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ)           |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)   | JWT token ไม่ถูกต้องหรือขาดหาย                                           |
| 413  | ข้อมูลร้องขอใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดสูงสุด                                  |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                                  |

*ตัวอย่างการตอบกลับข้อผิดพลาด*  

```json
// 400 Bad Request
{
    "Code": 400,
    "Message": "พารามิเตอร์ไม่ถูกต้อง: ไม่พบ sheetName"
}

// 401 Unauthorized
{
    "Code": 401,
    "Message": "การรับรองความถูกต้องล้มเหลว JWT token ขาดหายหรือไม่ถูกต้อง"
}

// 413 Payload Too Large
{
    "Code": 413,
    "Message": "ไฟล์ที่อัปโหลดมีขนาดเกินขนาดสูงสุดที่อนุญาต"
}

// 500 Internal Server Error
{
    "Code": 500,
    "Message": "เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์"
}
```

## วิธีใช้ API PostWorksheetAutoFilterRefresh ด้วย SDK

### ข้อมูลจำเพาะ API PostWorksheetAutoFilterRefresh

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetAutoFilterRefresh) กำหนดอินเทอร์เฟซโปรแกรมมิ่งที่เข้าถึงได้สาธารณะและอนุญาตให้คุณดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง cURL เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API คลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำร้องขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/refresh" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>"
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

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำและอนุญาตให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetAutoFilterRefresh.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetAutoFilterRefresh.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetAutoFilterRefresh.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetAutoFilterRefresh.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetAutoFilterRefresh.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetAutoFilterRefresh.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetAutoFilterRefresh.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetAutoFilterRefresh.go" >}}

{{< /tab >}}

{{< /tabs >}}