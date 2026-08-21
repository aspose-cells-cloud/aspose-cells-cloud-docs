---
---
title: "เพิ่มตัวกรองไอคอนลงในแผ่นงาน Excel"
second_title: "เอกสาร"
linktype: "เพิ่มตัวกรองไอคอน"
type: docs
url: /autofilter/add-icon-filter/
aliases: [/add-an-icon-filter/,/autofilter/add-an-icon-filter/]
keywords: "Aspose.Cells Cloud, Excel, ตัวกรองไอคอน, AutoFilter, REST API"
description: "เรียนรู้วิธีเพิ่มตัวกรองไอคอนลงในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API พร้อมรายละเอียดคำขอ ตัวอย่าง cURL ตัวอย่างโค้ด SDK และการจัดการข้อผิดพลาด"
weight: 65
ArticleTitle: "เพิ่มตัวกรองไอคอนลงในแผ่นงาน Excel – เอกสาร Aspose.Cells Cloud"
---

## REST API

This REST API เพิ่ม **ตัวกรองไอคอน** ลงในแผ่นงาน Excel โดยใช้ **Aspose.Cells Cloud REST API**

**พื้นหลัง:** ตัวกรองไอคอนจะใช้ชุดไอคอนแบบภาพกับเซลล์ตามค่าของเซลล์ ทำให้วิเคราะห์แนวโน้มข้อมูลได้อย่างรวดเร็วด้วยสายตา ตัวอย่างการใช้งานทั่วไป ได้แก่ การเน้นค่าตัวชี้วัดประสิทธิภาพ การแสดงตัวบ่งชี้สถานะ หรือจัดหมวดหมู่ค่าด้วยไอคอนไฟจราจรโดยตรงภายในแผ่นงาน Excel

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/iconFilter
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

### พารามิเตอร์คำขอ:

| พารามิเตอร์ | ประเภทข้อมูล | ตำแหน่ง | คำอธิบาย |
|----------------|---------|----------|-------------|
| name           | string  | Path     | ชื่อสมุดงาน |
| sheetName      | string  | Path     | ชื่อแผ่นงาน |
| range          | string  | Query    | ช่วงเซลล์ (เช่น `A1:B1`) ที่จะนำไปใช้ตัวกรอง |
| fieldIndex     | integer | Query    | ดัชนีตามลำดับของคอลัมน์ที่ตัวกรองมุ่งเป้าหมาย (เริ่มต้นที่ 0) |
| iconSetType    | string  | Query    | ชุดไอคอนที่จะใช้ ค่าที่อนุญาต: `Arrows3`, `ArrowsGray3`, `Flags3`, `Signs3`, `Symbols3`, `Symbols32`, `TrafficLights31`, `TrafficLights32`, `Arrows4`, `ArrowsGray4`, `Rating4`, `RedToBlack4`, `TrafficLights4`, `Arrows5`, `ArrowsGray5`, `Quarters5`, `Rating5`, `Stars3`, `Boxes5`, `Triangles3`, `None`, `CustomSet`, `Smilies3`, `ColorSmilies3` |
| iconId         | integer | Query    | ตัวระบุไอคอนเฉพาะภายในชุดไอคอนที่เลือก |
| matchBlanks    | boolean | Query    | ระบุว่าจะรวมเซลล์ว่าง (`true` หรือ `false`) หรือไม่ |
| refresh        | boolean | Query    | ระบุว่าจะรีเฟรชตัวกรองหลังจากนำไปใช้ (`true` หรือ `false`) หรือไม่ |
| folder         | string  | Query    | โฟลเดอร์ที่เก็บสมุดงานต้นฉบับ |
| storageName    | string  | Query    | ชื่อที่เก็บข้อมูลที่สมุดงานอยู่ |

### **การตอบกลับ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | คำอธิบาย                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                          | นำไปใช้ตัวกรองสำเร็จ; การตอบกลับมีรายละเอียดการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request)                 | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)                | JWT token ไม่ถูกต้องหรือขาดหาย |
| 413  | ข้อมูลส่งไปมีขนาดใหญ่เกินไป (Payload Too Large)           | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error)       | เกิดข้อผิดพลาดที่ไม่คาดคิดภายในเซิร์ฟเวอร์ |
## วิธีใช้ PutWorksheetIconFilter API ด้วย SDK

### ข้อมูลการกำหนดค่า PutWorksheetIconFilter API

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetIconFilter) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการโต้ตอบ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียก API บนคลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/iconFilter?range=A1:B1&fieldindex=0&iconsettype=ArrowsGray3&iconid=1" \
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

รหัสสถานะการตอบกลับที่เป็นไปได้:

| รหัส | คำอธิบาย |
|------|-------------|
| 200 | นำไปใช้ตัวกรองสำเร็จ |
| 400 | คำขอไม่ถูกต้อง – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง |
| 401 | ไม่ได้รับอนุญาต – โทเคนการยืนยันตัวตนไม่ถูกต้องหรือขาดหาย |
| 404 | ไม่พบสมุดงาน แผ่นงาน หรือช่วงที่ระบุ |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ |
{{< /tab >}}

{{< /tabs >}}

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานโครงการของคุณได้ โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetIconFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetIconFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetIconFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetIconFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetIconFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetIconFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetIconFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetIconFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

สำหรับความสามารถของ AutoFilter อื่นๆ โปรดดูที่เอกสาร **[เพิ่มตัวกรองสี](/autofilter/add-color-filter/)**, **[เพิ่มตัวกรองวันที่](/autofilter/add-date-filter/)** และ **[ล้าง AutoFilter](/autofilter/clear-autofilter/)**