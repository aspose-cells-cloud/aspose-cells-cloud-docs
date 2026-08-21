---
title: "เพิ่มตัวกรองวันที่ลงในแผ่นงาน Excel"
second_title: "เอกสาร"
linktype: "เพิ่มตัวกรองวันที่"
type: docs
url: /autofilter/add-date-filter/
aliases:
  - /add-date-filter-in-a-worksheet/
  - /autofilter/add-a-date-filter/
description: "เรียนรู้วิธีเพิ่มตัวกรองวันที่ลงในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API (v3.0) รวมถึงตัวอย่าง cURL, ตัวอย่างโค้ด SDK (C#, Java, Python เป็นต้น), พารามิเตอร์ และการจัดการข้อผิดพลาด"
weight: 65
ArticleTitle: "เพิ่มตัวกรองวันที่ลงในแผ่นงาน Excel | Aspose.Cells Cloud API"
keywords: "Aspose.Cells, ตัวกรองวันที่ Excel, AutoFilter API, REST API, SDK บนคลาวด์, cURL, การทำให้สเปรดชีตอัตโนมัติ"
---

REST API นี้จะเพิ่ม **ตัวกรองวันที่** ลงในแผ่นงาน Excel

**ข้อกำหนดเบื้องต้น:** คุณต้องมีโทเค็น JWT ที่ถูกต้อง และสมุดงานเป้าหมายต้องมีอยู่แล้วในตำแหน่งที่จัดเก็บที่ระบุไว้ การร้องขอไม่จำเป็นต้องมีเนื้อหา JSON

## PutWorksheetDateFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### พารามิเตอร์ร้องขอ


| ชื่อพารามิเตอร์         | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                                                                                                                         |
| ------------------------ | --------- | -------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**                 | string    | Path     | ชื่อสมุดงาน                                                                                                                                                                       |
| **sheetName**            | string    | Path     | ชื่อแผ่นงาน                                                                                                                                                                       |
| **range**                | string    | Query    | ช่วงข้อมูลใน Excel ที่จะใช้ตัวกรอง (เช่น `A1:B1`)                                                                                                                                  |
| **fieldIndex**           | integer   | Query    | ดัชนีของคอลัมน์ที่จะกรอง (เริ่มนับจาก 0)                                                                                                                                           |
| **dateTimeGroupingType** | string    | Query    | ประเภทการจัดกลุ่มสำหรับตัวกรองวันที่/เวลา ค่าที่อนุญาตคือ `Day`, `Hour`, `Minute`, `Month`, `Second`, `Year` ค่าเหล่านี้แยกแยะตัวพิมพ์เล็ก-ใหญ่ และค่าเริ่มต้นคือ `Day`               |
| **year**                 | integer   | Query    | ส่วนประกอบของปีในค่าของตัวกรอง                                                                                                                                                      |
| **month**                | integer   | Query    | ส่วนประกอบของเดือนในค่าของตัวกรอง                                                                                                                                                   |
| **day**                  | integer   | Query    | ส่วนประกอบของวันในค่าของตัวกรอง                                                                                                                                                     |
| **hour**                 | integer   | Query    | ส่วนประกอบของชั่วโมงในค่าของตัวกรอง                                                                                                                                                 |
| **minute**               | integer   | Query    | ส่วนประกอบของนาทีในค่าของตัวกรอง                                                                                                                                                   |
| **second**               | integer   | Query    | ส่วนประกอบของวินาทีในค่าของตัวกรอง                                                                                                                                                  |
| **matchBlanks**          | boolean   | Query    | รวมเซลล์ว่าง (`true` หรือ `false`)                                                                                                                                                 |
| **refresh**              | boolean   | Query    | อัปเดตตัวกรองหลังจากนำไปใช้ (`true` หรือ `false`)                                                                                                                                  |
| **folder**               | string    | Query    | เส้นทางโฟลเดอร์ของสมุดงานต้นฉบับ                                                                                                                                                   |
| **storageName**          | string    | Query    | ชื่อของบริการจัดเก็บข้อมูล                                                                                                                                                          |

*คำร้องแบบ PUT ไม่จำเป็นต้องมีเนื้อหาคำร้อง; พารามิเตอร์ทั้งหมดจะถูกส่งผ่าน query string*

### **การตอบกลับ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย                                                                 |
|------|-----------------------------|--------------------------------------------------------------------------|
| 200  | สำเร็จ (OK)                 | ใช้ตัวกรองสำเร็จ; การตอบกลับประกอบด้วยรายละเอียดของการดำเนินการ      |
| 400  | คำร้องขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ)            |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)    | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                                           |
| 413  | ข้อมูลส่งไปขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด                               |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดภายในเซิร์ฟเวอร์                              |
## วิธีใช้ PutWorksheetDateFilter API ร่วมกับ SDK

### ข้อมูลจำเพาะ PutWorksheetDateFilter API


<a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetDateFilter" rel="noopener noreferrer">ข้อมูลจำเพาะ OpenAPI</a> กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้โดยสาธารณะ และช่วยให้คุณสามารถดำเนินการโต้ตอบกับ REST API ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำร้องขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?range=A1:B1&fieldIndex=0&dateTimeGroupingType=Year&year=1920&refresh=true" \
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

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ จึงสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ กรุณาตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บ GitHub</a> เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}