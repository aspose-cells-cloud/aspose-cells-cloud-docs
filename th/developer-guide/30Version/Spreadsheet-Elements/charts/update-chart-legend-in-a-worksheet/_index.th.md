---
title: "อัปเดตคำอธิบายแผนภูมิในแผ่นงาน"
type: docs
url: /charts/legend/update/
aliases: [/update-chart-legend-in-a-worksheet/]
weight: 160
keywords: "Aspose.Cells, Cloud, Excel, Chart, Legend, REST API, Update, Worksheet, cURL, SDK"
description: "วิธีการอัปเดตคำอธิบายแผนภูมิในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API พร้อมตัวอย่างคำขอ cURL และโค้ดตัวอย่าง SDK สำหรับภาษาโปรแกรมต่างๆ"
ArticleTitle: "อัปเดตคำอธิบายแผนภูมิในแผ่นงาน – คู่มือ Aspose.Cells Cloud API"
---

REST API นี้ใช้สำหรับอัปเดตคำอธิบายแผนภูมิ (chart legend)

**ข้อกำหนดเบื้องต้น:** เพื่อใช้งานปลายทาง (endpoint) นี้ คุณต้องมีโทเคน JWT ที่ถูกต้องจาก Aspose Cloud และสมุดงานเป้าหมายต้องถูกจัดเก็บไว้ในตำแหน่งที่จัดเก็บที่รองรับ (ค่าเริ่มต้นคือพื้นที่จัดเก็บของ Aspose Cloud) ตรวจสอบให้แน่ใจว่าชื่อสมุดงาน ชื่อแผ่นงาน และดัชนีของแผนภูมิที่ต้องการแก้ไขนั้นถูกต้อง

คำอธิบายแผนภูมิ (chart legend) แสดงชื่อและสัญลักษณ์ของชุดข้อมูล (data series) ในแผนภูมิ การอัปเดตคำอธิบายแผนภูมิช่วยให้คุณปรับแต่งรูปลักษณ์ของมัน เช่น รูปแบบตัวอักษร สี และเงา

## PostWorksheetChartLegend API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### พารามิเตอร์ของ Request

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                     |
| ---------------- | --------- | -------- | -------------------------------------------- |
| name             | string    | path     | ชื่อสมุดงาน                                 |
| sheetName        | string    | path     | ชื่อแผ่นงาน                                  |
| chartIndex       | integer   | path     | ดัชนีของแผนภูมิที่ต้องการแก้ไข              |
| legend           | object    | body     | ออบเจกต์ JSON ที่กำหนดการตั้งค่าคำอธิบายแผนภูมิ |
| folder           | string    | query    | โฟลเดอร์ที่เก็บสมุดงาน                      |
| storageName      | string    | query    | ชื่อของพื้นที่จัดเก็บ                       |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChartLegend) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้โดยสาธารณะ และช่วยให้คุณสามารถดำเนินการโต้ตอบแบบ REST ผ่านเว็บเบราว์เซอร์ได้โดยตรง

คุณสามารถใช้เครื่องมือ cURL บนบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
-d '{"Font":{"Color":{"A":"1","R":"255","G":"0","B":"0"},"DoubleSize":10.0,"IsBold":true,"IsItalic":false,"IsStrikeout":false,"IsSubscript":false,"IsSuperscript":false,"Name":"Arial","Size":15,"Underline":"None"},"Shadow":true}' \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK ของ Cloud

การใช้ SDK จะช่วยเร่งกระบวนการพัฒนา เพราะ SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานของโครงการได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-UpdateChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-UpdateChartLegend-update-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PostWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-update_chart_legend-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateChartLegendInWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-UpdateChartLegend-update-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "74fffa317bc5ba65dc6536005e5bb683" >}}

{{< /tab >}}

{{< /tabs >}}