---
title: "เพิ่มเกณฑ์ที่กำหนดเองในแผ่นงาน Excel"
second_title: "เอกสาร"
linktype: "เพิ่มตัวกรองแบบกำหนดเอง"
type: docs
url: /autofilter/add-custom-filter/
aliases: [/filter-a-list-with-a-custom-criteria/,/autofilter/add-a-custom-filter/]
keywords: "Excel, ตัวกรองแบบกำหนดเอง, Aspose.Cells Cloud, REST API, ตัวกรองอัตโนมัติ, แผ่นงาน, เกณฑ์ที่กำหนดเอง"
description: "เรียนรู้วิธีใช้ REST API ของ Aspose.Cells Cloud เพื่อเพิ่มตัวกรองแบบกำหนดเองในแผ่นงาน Excel พร้อมรายละเอียดคำขอ ตัวอย่าง cURL และโค้ดตัวอย่าง SDK สำหรับภาษาโปรแกรมต่างๆ"
weight: 65
ArticleTitle: "เพิ่มเกณฑ์ที่กำหนดเองในแผ่นงาน Excel – Aspose.Cells Cloud API"
---

REST API นี้ใช้กรองรายการโดยใช้ **เกณฑ์ที่กำหนดเอง**

## PutWorksheetCustomFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/custom
```

### **การรักษาความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

### พารามิเตอร์คำขอ:

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย |
|----------------|---------|------------------------------|-----------------------------------------------------------------------------|
| name | string | path | ชื่อไฟล์ Excel |
| sheetName | string | path | ชื่อแผ่นงานที่มีข้อมูลที่จะกรอง |
| range | string | query | ช่วงเซลล์ที่จะนำไปใช้ตัวกรอง (เช่น `A1:B1`) |
| fieldIndex | integer | query | ดัชนีแบบเริ่มต้นที่ศูนย์ของคอลัมน์ที่ใช้ตัวกรอง |
| operatorType1 | string | query | ตัวดำเนินการเปรียบเทียบตัวแรก (เช่น `LessOrEqual`, `Equal`) |
| criteria1 | string | query | ค่าหรือนิพจน์ของตัวกรองตัวแรก |
| isAnd | boolean | query | หากเป็น `true` จะรวมเกณฑ์ทั้งสองด้วย **AND** มิฉะนั้นจะใช้ **OR** |
| operatorType2 | string | query | ตัวดำเนินการเปรียบเทียบตัวที่สอง (ไม่บังคับ) |
| criteria2 | string | query | ค่าหรือนิพจน์ของตัวกรองตัวที่สอง (ไม่บังคับ) |
| matchBlanks | boolean | query | เมื่อตั้งค่าเป็น `true` จะรวมเซลล์ว่างในผลลัพธ์การกรอง |
| refresh | boolean | query | หากเป็น `true` จะบังคับให้แผ่นงานรีเฟรชหลังจากใช้ตัวกรอง |
| folder | string | query | เส้นทางโฟลเดอร์ในพื้นที่จัดเก็บที่ไฟล์ตั้งอยู่ |
| storageName | string | query | ชื่อของบริการพื้นที่จัดเก็บ |

### **การตอบกลับ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย | คำอธิบาย |
|------|-----------------------------|--------------------------------------------------|
| 200 | OK | ใช้ตัวกรองสำเร็จ; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400 | Bad Request | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401 | Unauthorized | JWT token ไม่ถูกต้องหรือขาดหาย |
| 413 | Payload Too Large | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500 | Internal Server Error | เกิดข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด |

## วิธีใช้ PutWorksheetCustomFilter API ผ่าน SDK

### ข้อมูลจำเพาะ PutWorksheetCustomFilter API

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetCustomFilter) กำหนด API ที่สามารถเข้าถึงได้แบบเปิดเผยและทำให้คุณสามารถโต้ตอบกับ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียก API บนคลาวด์ผ่าน cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/custom?range=A1:B1&fieldIndex=0&operatorType1=LessOrEqual&criteria1=1" \
  -X PUT \
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

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะจัดการรายละเอียดระดับล่างให้คุณสามารถมุ่งเน้นไปที่ตรรกะของโปรเจกต์ของคุณได้ โปรดดูที่ [repository บน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetCustomFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetCustomFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetCustomFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetCustomFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetCustomFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetCustomFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetCustomFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetCustomFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

สำหรับการดำเนินการ AutoFilter อื่นๆ เช่น การเพิ่มตัวกรองมาตรฐานหรือตัวกรองวันที่ โปรดดูที่หน้าเอกสารที่เกี่ยวข้องในส่วน AutoFilter