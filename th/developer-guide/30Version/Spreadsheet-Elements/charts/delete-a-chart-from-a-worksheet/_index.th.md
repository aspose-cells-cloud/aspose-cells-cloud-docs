---
title: "การลบแผนภูมิออกจากแผ่นงาน"
type: docs
url: /th/charts/delete/
aliases: [  /th/delete-a-chart-from-a-worksheet/ ]
weight: 40
keywords:
  - "Aspose.Cells"
  - "REST API"
  - "Delete Chart"
  - "Worksheet"
  - "Excel"
  - "Cloud SDK"
  - "Chart Deletion"
  - "API Reference"
description: "ลบแผนภูมิออกจากแผ่นงานโดยใช้ดัชนีแบบเริ่มต้นที่ 0 ผ่าน Aspose.Cells Cloud REST API"
ArticleTitle: "การลบแผนภูมิออกจากแผ่นงานโดยใช้ Aspose.Cells Cloud REST API"
---

REST API นี้จะลบแผนภูมิออกจากแผ่นงานตามดัชนีของแผนภูมินั้น

สำหรับการดำเนินการที่เกี่ยวข้อง โปรดดูที่หน้า **[เพิ่มแผนภูมิ](#)** และ **[ดึงข้อมูลแผนภูมิ](#)**

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
```

### การรักษาความปลอดภัยและการพิสูจน์ตัวตน

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ [การพิสูจน์ตัวตนแบบใช้โทเคน JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

### พารามิเตอร์คำขอ

| พารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                     |
|-------------|-----------|----------|----------------------------------------------|
| name        | string    | path     | ชื่อสมุดงาน                                  |
| sheetName   | string    | path     | ชื่อแผ่นงาน                                   |
| chartIndex  | integer   | path     | ดัชนีแบบเริ่มต้นที่ 0 ของแผนภูมิที่ต้องการลบ    |
| folder      | string    | query    | โฟลเดอร์ที่เก็บสมุดงาน                         |
| storageName | string    | query    | ชื่อของพื้นที่จัดเก็บที่ต้องการใช้              |


### **การตอบกลับ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                      | คำอธิบาย                                             |
|------|-------------------------------|------------------------------------------------------|
| 200  | สำเร็จ (OK)                   | กรองข้อมูลเสร็จสิ้น; การตอบกลับประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ไม่ครบหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหายไป                         |
| 413  | ข้อมูลในเนื้อหาใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                        |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                   |

## วิธีใช้ PutWorksheetAddChart API ผ่าน SDK

### ข้อกำหนด PutWorksheetAddChart API

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetDeleteChart) กำหนดอินเทอร์เฟซการโปรแกรมที่สามารถเข้าถึงได้จากภายนอก และช่วยให้คุณสามารถโต้ตอบกับ REST API ผ่านเบราว์เซอร์เว็บได้โดยตรง

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ผ่าน cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0" \
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

API จะคืนค่าโค้ดสถานะต่อไปนี้:

| โค้ด | คำอธิบาย                                    |
|-----|---------------------------------------------|
| 200 | ลบแผนภูมิเสร็จสิ้น                           |
| 400 | คำขอไม่ถูกต้อง (เช่น ดัชนีไม่ถูกต้อง)         |
| 401 | ไม่ได้รับอนุญาต (โทเคน JWT ขาดหายหรือไม่ถูกต้อง) |
| 404 | ไม่พบสมุดงาน แผ่นงาน หรือแผนภูมิ            |
| 500 | ข้อผิดพลาดของเซิร์ฟเวอร์                      |

**การจัดการข้อผิดพลาด:** สำหรับข้อมูลข้อผิดพลาดโดยละเอียด โปรดอ้างอิงที่รูปแบบข้อผิดพลาดทั่วไปในข้อกำหนด OpenAPI

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK ซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโปรเจกต์ของคุณได้ โปรดตรวจสอบ [repository บน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ผ่าน SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteOneChart-delete-single-chart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetDeleteChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-delete_worksheet_chart_by_index-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteChartExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteOneChart-delete-single-chart.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b858c32efd7b745ebb75d61898ec50e0" >}}

{{< /tab >}}

{{< /tabs >}}