---
title: "การลบตัวกรองวันที่ – Aspose.Cells Cloud"
second_title: "เอกสาร"
linktitle: "ลบตัวกรองวันที่"
type: docs
url: /th/autofilter/delete-date-filter/
aliases:
  - /remove-a-date-filter/
  - /autofilter/delete-a-date-filter/
weight: 100
keywords: "Aspose.Cells, ลบตัวกรองวันที่, Excel AutoFilter, REST API, SDK"
description: "เรียนรู้วิธีการลบตัวกรองวันที่จากแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API ซึ่งรวมถึง endpoint, พารามิเตอร์, ตัวอย่าง HTTPS cURL, โครงสร้างข้อมูลการตอบกลับ และตัวอย่างโค้ด SDK"
ArticleTitle: "การลบตัวกรองวันที่ – เอกสารประกอบ API Aspose.Cells Cloud"
---

API นี้จะลบตัวกรองวันที่ออกจากแผ่นงาน Excel

**ข้อกำหนดเบื้องต้น:** คุณต้องมีโทเคน JWT ที่ถูกต้อง ไฟล์สมุดงานต้องถูกจัดเก็บไว้ในพื้นที่จัดเก็บของ Aspose Cloud และคุณต้องมีสิทธิ์ที่เหมาะสมในการแก้ไขแผ่นงาน

## DeleteWorksheetDateFilter API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบใช้โทเคน JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์       | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                                     |
|----------------------|-----------|---------|----------------------------------------------------------------------------------------------|
| name                 | string    | path    | ชื่อไฟล์ Excel                                                                               |
| sheetName            | string    | path    | ชื่อแผ่นงาน                                                                                  |
| fieldIndex           | integer   | query   | ดัชนีแบบเริ่มต้นที่ 0 ของคอลัมน์ที่จะใช้ตัวกรอง                                              |
| dateTimeGroupingType | string    | query   | ประเภทการจัดกลุ่มของตัวกรองวันที่ (เช่น Year, Month, Day)                                     |
| year                 | integer   | query   | ส่วนประกอบปีของตัวกรอง (ค่าเริ่มต้นคือ 0)                                                     |
| month                | integer   | query   | ส่วนประกอบเดือนของตัวกรอง (ค่าเริ่มต้นคือ 0)                                                  |
| day                  | integer   | query   | ส่วนประกอบวันของตัวกรอง (ค่าเริ่มต้นคือ 0)                                                    |
| hour                 | integer   | query   | ส่วนประกอบชั่วโมงของตัวกรอง (ค่าเริ่มต้นคือ 0)                                                |
| minute               | integer   | query   | ส่วนประกอบนาทีของตัวกรอง (ค่าเริ่มต้นคือ 0)                                                   |
| second               | integer   | query   | ส่วนประกอบวินาทีของตัวกรอง (ค่าเริ่มต้นคือ 0)                                                 |
| folder               | string    | query   | เส้นทางโฟลเดอร์ในพื้นที่จัดเก็บที่ไฟล์ตั้งอยู่                                                 |
| storageName          | string    | query   | ชื่อของพื้นที่จัดเก็บ Aspose Cloud                                                            |

### **การตอบกลับ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย                                                                 |
|-----|------------------------------|--------------------------------------------------------------------------|
| 200 | OK                           | ตั้งค่าตัวกรองเรียบร้อยแล้ว; การตอบกลับประกอบด้วยรายละเอียดของคำสั่ง |
| 400 | Bad Request                  | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)                |
| 401 | Unauthorized                 | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                                          |
| 413 | Payload Too Large            | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                        |
| 500 | Internal Server Error        | เกิดข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด                                |

API จะคืนค่าโค้ดสถานะ HTTP มาตรฐานเพื่อบ่งบอกผลลัพธ์ของการลบตัวกรอง

| โค้ด | ความหมาย | คำอธิบาย                                                                 |
|-----|----------|--------------------------------------------------------------------------|
| 200 | OK       | ลบตัวกรองวันที่เรียบร้อยแล้ว; การตอบกลับประกอบด้วยสถานะของคำสั่ง     |
| 400 | Bad Request | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)                |
| 401 | Unauthorized | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                                          |
| 413 | Payload Too Large | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                        |
| 500 | Internal Server Error | เกิดข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด                                |

## วิธีใช้ DeleteWorksheetDateFilter API ผ่าน SDK

### ข้อมูลจำเพาะ API DeleteWorksheetDateFilter

<a href="https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetDateFilter" rel="noopener noreferrer">ข้อมูลจำเพาะ OpenAPI</a> กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้สาธารณะ และอนุญาตให้คุณดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ผ่าน cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?fieldIndex=0&dateTimeGroupingType=Year&year=1920" \
  -X DELETE \
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

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานโครงการของคุณได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บ GitHub</a> เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}