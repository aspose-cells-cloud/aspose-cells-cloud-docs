---
title: "อัปเดตคุณสมบัติของแผนภูมิ"
type: docs
url: /charts/properties/update/
aliases: [/update-chart-properties/]
weight: 160
keywords: "Aspose.Cells, แผนภูมิ, อัปเดต, Excel, REST API, SDK"
description: "เรียนรู้วิธีการอัปเดตคุณสมบัติของแผนภูมิ (ประเภท ชื่อ คำอธิบายประกอบ เป็นต้น) ในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API (เวอร์ชัน 3.0) รวมถึง endpoint, พารามิเตอร์, ตัวอย่าง cURL และตัวอย่างโค้ด SDK สำหรับ C#, Java, PHP, Ruby, Node.js, Perl และ Go"
ArticleTitle: "อัปเดตคุณสมบัติของแผนภูมิ – Aspose.Cells Cloud REST API"
---

REST API นี้ใช้สำหรับอัปเดตคุณสมบัติของแผนภูมิ

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

## API PostWorksheetChart

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
```

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | Path/Query String/HTTPBody | คำอธิบาย |
| ---------------- | ---------- | -------------------------- | ------------------------------------------------------------- |
| name             | string     | path                       | ชื่อไฟล์ Excel |
| sheetName        | string     | path                       | ชื่อของแผ่นงานที่มีแผนภูมิ |
| chartIndex       | integer    | path                       | ดัชนีเริ่มต้นที่ศูนย์ของแผนภูมิที่ต้องการอัปเดต |
| chart            | object     | body                       | วัตถุ JSON ที่กำหนดคุณสมบัติของแผนภูมิที่ต้องการแก้ไข |
| folder           | string     | query                      | โฟลเดอร์ในพื้นที่จัดเก็บที่ไฟล์ตั้งอยู่ |
| storageName      | string     | query                      | ชื่อของบริการพื้นที่จัดเก็บ |

### โครงสร้างเนื้อหาคำขอ

วัตถุ **`chart`** ประกอบด้วยคุณสมบัติที่คุณสามารถแก้ไขได้ ด้านล่างคือตัวอย่าง JSON ที่แสดงคุณสมบัติที่ใช้บ่อยบางส่วน:

```json
{
  "Title": {
    "Text": "ยอดขายรายไตรมาส"
  },
  "ShowLegend": true,
  "Type": "Line",
  "DataLabels": {
    "ShowValue": true,
    "ShowPercentage": false
  },
  "ChartArea": {
    "BorderColor": "Blue",
    "FillColor": "White"
  }
}
```

> **หมายเหตุ:** คุณจำเป็นต้องส่งเฉพาะฟิลด์ที่ต้องการเปลี่ยนแปลงเท่านั้น คุณสมบัติที่ไม่ได้ระบุจะยังคงค่าเดิมไว้

<a href="https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChart" target="_blank" rel="noopener noreferrer">ข้อกำหนด OpenAPI</a> กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบเปิดเผย และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ผ่าน cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet4/charts/1" \
-d '{"Type": "line"}' \
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

## การตอบกลับ

API จะส่งคืนวัตถุ JSON ที่ระบุผลลัพธ์ของการดำเนินการ การอัปเดตที่สำเร็จจะให้ผลลัพธ์ดังนี้:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**รหัสสถานะสำเร็จ**

| สถานะ HTTP | คำอธิบาย |
| ----------- | ----------- |
| 200         | OK – อัปเดตคุณสมบัติของแผนภูมิสำเร็จ |

**หัวเรื่องการตอบกลับ**

| หัวเรื่อง | คำอธิบาย |
| --------- | ----------- |
| `Content-Type` | `application/json` – ระบุว่าเนื้อหาการตอบกลับอยู่ในรูปแบบ JSON |
| `X-RequestId` | ตัวระบุที่ไม่ซ้ำสำหรับคำขอ (มีประโยชน์สำหรับการแก้ไขข้อขัดข้อง) |

การตอบกลับที่เป็นไปได้ในกรณีเกิดข้อผิดพลาดมีดังนี้:

| สถานะ HTTP | คำอธิบาย |
| ----------- | ----------------------------------------------- |
| 400         | Bad Request – พารามิเตอร์หรือเนื้อหาคำขอไม่ถูกต้อง |
| 401         | Unauthorized – ขาดหรือโทเค็นไม่ถูกต้อง |
| 404         | Not Found – ไม่พบไฟล์ แผ่นงาน หรือแผนภูมิ |
| 500         | Internal Server Error |

สำหรับการดำเนินการอื่นๆ ที่เกี่ยวข้องกับแผนภูมิ โปรดดูหัวข้อที่เกี่ยวข้อง เช่น [อัปเดตชื่อแผนภูมิ](/charts/title/update/) และ [อัปเดตคำอธิบายประกอบของแผนภูมิ](/charts/legend/update/)

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ และช่วยให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">ที่เก็บ GitHub</a> เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" tabName6="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Charts-UpdateChartProperties-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-CellsChartsPostWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-cells_charts_post_worksheet_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "d554e51920e174943a60f4343a97e203" >}}

{{< /tab >}}

{{< /tabs >}}