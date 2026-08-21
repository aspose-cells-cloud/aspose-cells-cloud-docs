---
title: "แสดงคำอธิบายกราฟในเวิร์กชีต"
type: docs
url: /charts/legend/show/
aliases: [/show-chart-legend-in-a-worksheet/]
weight: 100
keywords: "Aspose.Cells Cloud, API คำอธิบายกราฟ, คำอธิบายกราฟ Excel, REST PUT คำอธิบายกราฟ, Aspose API v3.0"
description: "เรียนรู้วิธีแสดงคำอธิบายกราฟในเวิร์กชีต Excel โดยใช้ Aspose.Cells Cloud REST API (v3.0) ซึ่งประกอบด้วยรายละเอียดของ endpoint, พารามิเตอร์, ตัวอย่าง cURL และตัวอย่างโค้ด SDK"
---

API REST นี้ช่วยให้คุณสามารถแสดง **คำอธิบายกราฟ (legend)** — กล่องคำอธิบายที่ระบุชุดข้อมูล — ที่อยู่ในกราฟซึ่งฝังอยู่ในเวิร์กชีตของสมุดงาน Excel

## API REST

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### พารามิเตอร์สำหรับคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                |
|------------------|------------|----------|------------------------------------------|
| name             | string     | path     | ชื่อไฟล์สมุดงาน                         |
| sheetName        | string     | path     | ชื่อเวิร์กชีตที่มีกราฟ                  |
| chartIndex       | integer    | path     | ดัชนีของกราฟ (เริ่มต้นที่ 0)             |
| folder           | string     | query    | โฟลเดอร์ที่เก็บสมุดงาน                 |
| storageName      | string     | query    | ชื่อของบริการจัดเก็บข้อมูล (storage service) |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartLegend) กำหนด API ที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการโต้ตอบแบบ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

การยืนยันตัวตนทำผ่านโทเคน Bearer JWT ที่ส่งไปใน header **Authorization**

คุณสามารถใช้เครื่องมือ cURL บนบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
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

API สามารถส่งกลับโค้ดสถานะ HTTP ต่อไปนี้:

- **200 OK** – แสดงคำอธิบายกราฟเรียบร้อยแล้ว
- **400 Bad Request** – พารามิเตอร์ไม่ถูกต้อง
- **401 Unauthorized** – การยืนยันตัวตนล้มเหลว
- **404 Not Found** – สมุดงาน เวิร์กชีต หรือกราฟที่ระบุไม่มีอยู่
- **500 Internal Server Error** – เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK สำหรับคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการกับรายละเอียดระดับต่ำให้ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่าง ๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-ShowChartLegend-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-ShowChartLegend-show-chart-legend.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartLegend-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-show_legend_in_chart-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ShowChartLegendInAWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-ShowChartLegend-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-ShowChartLegend-show-chart-legend.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-ShowChartLegend-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "f9f1d14e3b6985c0a44ec7acdd4f56b2" >}}
{{< /tab >}}

{{< /tabs >}}