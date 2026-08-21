---
---
title: "เพิ่มตัวกรองในแผ่นงาน Excel"
second_title: "เอกสาร"
linktitle: "เพิ่มตัวกรอง"
type: docs
url: /autofilter/add-filter/
aliases: [/add-a-filter-for-a-filter-column/]
keywords: "Aspose.Cells, Cloud, Excel, AutoFilter, Add Filter, REST API, SDK"
description: "เรียนรู้วิธีการเพิ่มตัวกรองอัตโนมัติให้กับคอลัมน์ในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API ซึ่งประกอบด้วยตัวอย่าง cURL, SDK และคู่มือพารามิเตอร์"
weight: 60
ArticleTitle: "เพิ่มตัวกรองลงในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud"
---

**ข้อกำหนดเบื้องต้น:** ก่อนเรียกใช้ API นี้ คุณต้องได้รับโทเคน JWT ที่ถูกต้อง ตรวจสอบให้แน่ใจว่าสมุดงานเป้าหมายถูกอัปโหลดไปยังพื้นที่จัดเก็บที่ระบุ และมีสิทธิ์ที่จำเป็นในการเข้าถึงไฟล์นั้น ขอแนะนำให้ใช้เวอร์ชันของ cURL (7.68 หรือใหม่กว่า) สำหรับตัวอย่างในบรรทัดคำสั่ง

API นี้เป็น REST API ที่เพิ่มตัวกรองสำหรับคอลัมน์เฉพาะในแผ่นงาน Excel

## PutWorksheetFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### พารามิเตอร์สำหรับคำขอ

| พารามิเตอร์ | ประเภทข้อมูล | ตำแหน่ง | คำอธิบาย |
|-------------|-------------|----------|-----------|
| name        | string      | Path     | ชื่อสมุดงาน |
| sheetName   | string      | Path     | ชื่อแผ่นงาน |
| range       | string      | Query    | ช่วงเซลล์ที่มีตัวกรอง (เช่น `A1:B1`) |
| fieldIndex  | integer     | Query    | ดัชนีของคอลัมน์ (เริ่มต้นที่ 0) ที่ต้องการใช้ตัวกรอง |
| criteria    | string      | Query    | เงื่อนไขการกรอง (เช่น ค่าหรือนิพจน์) |
| matchBlanks | boolean     | Query    | ตั้งค่าเป็น `true` เพื่อรวมเซลล์ว่างในตัวกรอง มิฉะนั้นตั้งค่าเป็น `false` |
| refresh     | boolean     | Query    | ตั้งค่าเป็น `true` เพื่อรีเฟรชตัวกรองหลังจากใช้งาน มิฉะนั้นตั้งค่าเป็น `false` |
| folder      | string      | Query    | โฟลเดอร์ที่เก็บสมุดงานต้นฉบับไว้ |
| storageName | string      | Query    | ชื่อของบริการพื้นที่จัดเก็บ |

### **การตอบกลับ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | คำอธิบาย |
|-----|-------------------------------|-----------|
| 200 | OK                           | ใช้งานตัวกรองเรียบร้อยแล้ว; การตอบกลับประกอบด้วยรายละเอียดของการดำเนินการ |
| 400 | Bad Request                  | พารามิเตอร์ไม่ครบถ้วนหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401 | Unauthorized                 | โทเคน JWT ไม่ถูกต้องหรือไม่มี |
| 413 | Payload Too Large            | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500 | Internal Server Error        | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์ |

## วิธีการใช้ PutWorksheetFilter API ร่วมกับ SDKs

### ข้อมูลเฉพาะของ PutWorksheetFilter API

<a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilter" target="_blank" rel="noopener noreferrer">สเปค OpenAPI</a> นิยามอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และอนุญาตให้คุณดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?range=A1:B1&fieldIndex=0&criteria=Year" \
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

### ใช้ SDKs ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่โครงการของคุณได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">ที่เก็บบน GitHub</a> เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}