---
title: "จับคู่เซลล์ที่ไม่ว่างเปล่าทั้งหมดในแผ่นงาน Excel"
second_title: "เอกสาร"
linktitle: "จับคู่เซลล์ที่ไม่ว่างเปล่าทั้งหมด"
type: docs
url: /th/autofilter/match-all-non-blank/
aliases: [  /th/match-all-non-blank-cells-in-the-list/ ]
keywords: "Aspose.Cells Cloud, จับคู่เซลล์ที่ไม่ว่างเปล่า, AutoFilter, Excel API"
description: "เรียนรู้วิธีใช้ Aspose.Cells Cloud REST API เพื่อจับคู่เซลล์ที่ไม่ว่างเปล่าทั้งหมดในรายการ AutoFilter บนแผ่นงาน Excel รวมถึง endpoint, พารามิเตอร์, การยืนยันตัวตน, โครงสร้างคำตอบ, รหัสข้อผิดพลาด และตัวอย่าง SDK"
ArticleTitle: "จับคู่เซลล์ที่ไม่ว่างเปล่าทั้งหมดในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud API"
weight: 100
---

**ภาพรวม**  
การดำเนินการ *จับคู่เซลล์ที่ไม่ว่างเปล่าทั้งหมด* จะใช้ AutoFilter กับแผ่นงานและส่งคืนเฉพาะแถวที่คอลัมน์ที่ระบุมีข้อมูล ไม่รวมเซลล์ว่างเปล่า การดำเนินการนี้มีประโยชน์ในการทำความสะอาดชุดข้อมูล สร้างรายงาน หรือเตรียมข้อมูลสำหรับการวิเคราะห์เพิ่มเติม

**ข้อกำหนดเบื้องต้น**  
- โทเคน JWT ที่ถูกต้องสำหรับการยืนยันตัวตนกับ Aspose.Cells Cloud  
- สมุดงานต้องถูกอัปโหลดลงในพื้นที่จัดเก็บของ Aspose Cloud  
- คุณต้องมีชื่อไฟล์ ชื่อแผ่นงาน และดัชนีคอลัมน์แบบเริ่มต้นที่ 0 (`fieldIndex`) ที่ต้องการกรอง

API REST นี้จะจับคู่เซลล์ที่ไม่ว่างเปล่าทั้งหมดในรายการ AutoFilter บนแผ่นงาน Excel

## API PostWorksheetMatchNonBlanks

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchNonBlanks
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบโทเคน JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย                                                     |
| ---------------- | -------- | -------- | ------------------------------------------------------------- |
| name             | สายอักขระ | path     | ชื่อไฟล์ Excel                                                |
| sheetName        | สายอักขระ | path     | ชื่อแผ่นงานที่มี AutoFilter                                  |
| fieldIndex       | จำนวนเต็ม | query    | ดัชนีคอลัมน์แบบเริ่มต้นที่ 0 ที่จะนำไปใช้ตัวกรอง             |
| folder           | สายอักขระ | query    | _(ไม่บังคับ)_ "path" ของโฟลเดอร์ที่เก็บไฟล์ไว้                 |
| storageName      | สายอักขระ | query    | _(ไม่บังคับ)_ ชื่อของบริการพื้นที่จัดเก็บที่จะใช้              |

### **คำตอบ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                      | คำอธิบาย                                               |
|------|-------------------------------|---------------------------------------------------------|
| 200  | สำเร็จ (OK)                   | ใช้ตัวกรองสำเร็จ; คำตอบประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                           |
| 413  | ข้อมูลส่งมอบมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                        |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์                  |

*ตัวอย่างคำตอบข้อผิดพลาด (400)*  

```json
{
  "Code": 400,
  "Message": "พารามิเตอร์ไม่ถูกต้อง: fieldIndex ต้องเป็นจำนวนเต็มที่ไม่ติดลบ"
}
```

## วิธีใช้ API PostWorksheetMatchNonBlanks ร่วมกับ SDK

### ข้อมูลจำเพาะ API PostWorksheetMatchNonBlanks

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchNonBlanks) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการโต้ตอบ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API ผ่าน cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="คำตอบ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchNonBlanks?fieldIndex=0" \
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

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับล่างให้คุณ และช่วยให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchNonBlanks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchNonBlanks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchNonBlanks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchNonBlanks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchNonBlanks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchNonBlanks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchNonBlanks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchNonBlanks.go" >}}

{{< /tab >}}

{{< /tabs >}}