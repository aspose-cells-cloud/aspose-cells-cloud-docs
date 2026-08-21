---
title: "การลบหัวเรื่องของแผนภูมิในแผ่นงาน"
type: docs
url: /charts/delete-chart-title/
aliases: [/delete-chart-title-in-a-worksheet/]
weight: 150
keywords: "Aspose.Cells, Cloud API, ลบหัวเรื่องของแผนภูมิ, Excel, REST, SDK"
description: "เรียนรู้วิธีการลบหัวเรื่องของแผนภูมิออกจากแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API (เวอร์ชัน 4.0) รวมถึงตัวอย่าง cURL, SDK และการจัดการข้อผิดพลาด"
---

REST API นี้จะลบหัวเรื่องของแผนภูมิออก

## REST API

```bash
DELETE https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### ความปลอดภัยและการพิสูจน์ตัวตน

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้การพิสูจน์ตัวตนแบบ [ JWT token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                      |
|------------------|-----------|----------|-----------------------------------------------|
| name             | string    | path     | ชื่อไฟล์สมุดงาน                              |
| sheetName        | string    | path     | ชื่อแผ่นงาน                                  |
| chartIndex       | integer   | path     | ดัชนีของแผนภูมิ (เริ่มต้นที่ 0)               |
| folder           | string    | query    | โฟลเดอร์ที่เก็บสมุดงานไว้                    |
| storageName      | string    | query    | ชื่อของพื้นที่จัดเก็บข้อมูล                   |

### **การตอบกลับ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                      | คำอธิบาย                                                                 |
|------|-------------------------------|--------------------------------------------------------------------------|
| 200  | สำเร็จ (OK)                   | ตัวกรองถูกใช้งานเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของคำสั่งที่ดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request)  | พารามิเตอร์หายไปหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)                    |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | JWT token ไม่ถูกต้องหรือขาดหาย                                             |
| 413  | ข้อมูลในคำขอใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด                                      |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                                     |

## วิธีใช้ API DeleteWorksheetChartTitle ผ่าน SDK

### ข้อมูลจำเพาะ API DeleteWorksheetChartTitle

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetChartTitle) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้แบบเปิดเผย และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างด้านล่างแสดงวิธีการเรียกใช้งาน รวมถึง JWT token แบบ **Bearer** ซึ่งจำเป็นสำหรับการพิสูจน์ตัวตน

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
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

### การใช้งาน SDK ของ Aspose.Cells Cloud

การใช้งาน SDK เป็นวิธีที่ดีที่สุดในการเร่งกระบวนการพัฒนา โดย SDK จะจัดการรายละเอียดระดับต่ำให้คุณ และช่วยให้คุณสามารถมุ่งเน้นไปที่งานหลักของโครงการได้ โปรดตรวจสอบ [GitHub Repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteChartTitle-delete-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-hide_title_in_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteChartExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteChartTitle-delete-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3898d60ea8f7ea7bb460ffb5d7d29504" >}}

{{< /tab >}}

{{< /tabs >}}