---
title: "การลบฟิลเตอร์ออกจากแผ่นงาน Excel – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktitle: "ลบฟิลเตอร์"
type: docs
url: /delete-filter/
aliases: [/delete-a-filter-for-a-filter-column/, /delete-auto-filter/]
keywords: "Aspose.Cells Cloud ลบฟิลเตอร์, Excel, REST API, SDK"
description: "เรียนรู้วิธีการลบ AutoFilter ออกจากแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API, cURL และ SDK (C#, Java, Python เป็นต้น) รวมถึง endpoint, พารามิเตอร์, การยืนยันตัวตน และตัวอย่างโค้ด"
weight: 100
---

## REST API

REST API นี้ใช้ลบ **AutoFilter** ออกจากแผ่นงาน Excel

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์         | ชนิดข้อมูล | ตำแหน่ง | จำเป็น? | คำอธิบาย                                                                                   |
| ------------------------ | ---------- | -------- | ------- | ------------------------------------------------------------------------------------------ |
| **name**                 | string     | Path     | ใช่     | ชื่อสมุดงาน                                                                               |
| **sheetName**            | string     | Path     | ใช่     | ชื่อแผ่นงาน                                                                               |
| **range**                | string     | Query    | ไม่ใช่  | ช่วงเซลล์ที่ฟิลเตอร์ใช้ (เช่น `A1:C10`)                                                   |
| **fieldIndex**           | integer    | Query    | ใช่     | ดัชนีแบบเริ่มต้นที่ 0 ของคอลัมน์ที่ใช้ฟิลเตอร์                                             |
| **dateTimeGroupingType** | string     | Query    | ไม่ใช่  | วิธีการจัดกลุ่มค่าวันที่/เวลา: `Day`, `Hour`, `Minute`, `Month`, `Second` หรือ `Year`    |
| **year**                 | integer    | Query    | ไม่ใช่  | ส่วนปีสำหรับการจัดกลุ่มวันที่                                                               |
| **month**                | integer    | Query    | ไม่ใช่  | ส่วนเดือนสำหรับการจัดกลุ่มวันที่                                                             |
| **day**                  | integer    | Query    | ไม่ใช่  | ส่วนวันสำหรับการจัดกลุ่มวันที่                                                               |
| **hour**                 | integer    | Query    | ไม่ใช่  | ส่วนชั่วโมงสำหรับการจัดกลุ่มวันที่                                                           |
| **minute**               | integer    | Query    | ไม่ใช่  | ส่วนนาทีสำหรับการจัดกลุ่มวันที่                                                              |
| **second**               | integer    | Query    | ไม่ใช่  | ส่วนวินาทีสำหรับการจัดกลุ่มวันที่                                                            |
| **matchBlanks**          | boolean    | Query    | ไม่ใช่  | `true` / `false` – ระบุว่าจะรวมเซลล์ว่างในฟิลเตอร์หรือไม่                                 |
| **refresh**              | boolean    | Query    | ไม่ใช่  | `true` / `false` – ระบุว่าจะรีเฟรชแผ่นงานหลังการลบหรือไม่                                 |
| **folder**               | string     | Query    | ไม่ใช่  | โฟลเดอร์เดิมของสมุดงาน                                                                      |
| **storageName**          | string     | Query    | ไม่ใช่  | ชื่อพื้นที่จัดเก็บ                                                                         |

### **การตอบกลับ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                   | คำอธิบาย                                                                 |
|------|----------------------------|--------------------------------------------------------------------------|
| 200  | OK                         | ใช้งานฟิลเตอร์สำเร็จ; การตอบกลับมีรายละเอียดของการดำเนินการ             |
| 400  | Bad Request                | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ)            |
| 401  | Unauthorized               | JWT token ไม่ถูกต้องหรือขาดหาย                                             |
| 413  | Payload Too Large          | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                         |
| 500  | Internal Server Error      | เกิดข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด                                 |

## วิธีใช้ DeleteWorksheetFilter API ด้วย SDK

### ข้อกำหนดการใช้งาน DeleteWorksheetFilter API

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetFilter) กำหนด programming interface ที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่าน command-line เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ผ่าน cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?fieldIndex=0&dateTimeGroupingType=Year" \
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

### ใช้งาน Aspose.Cells Cloud SDK

การใช้ SDK เป็นวิธีที่มีประสิทธิภาพที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโปรเจกต์ของคุณได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ผ่าน SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}