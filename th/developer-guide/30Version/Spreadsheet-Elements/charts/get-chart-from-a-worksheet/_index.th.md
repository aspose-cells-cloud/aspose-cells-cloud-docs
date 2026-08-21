---
title: "ดึงข้อมูลแผนภูมิจากแผ่นงาน"
type: docs
url: /charts/get/
aliases: [/get-chart-from-a-worksheet/]
weight: 10
keywords: "Aspose.Cells Cloud, Get Chart, Worksheet, REST API, Excel, Chart API, chart retrieval, Excel chart"
description: "ดึงข้อมูลแผนภูมิ รวมถึง metadata และรูปแบบการส่งออก จากแผ่นงานโดยใช้ Aspose.Cells Cloud REST API"
ArticleTitle: "ดึงข้อมูลแผนภูมิจากแผ่นงาน – Aspose.Cells Cloud API"
---

API นี้จะดึงข้อมูลแผนภูมิ

**ข้อกำหนดเบื้องต้น** – เพื่อเรียกใช้จุดปลายทางนี้ คุณต้องมีบัญชี Aspose.Cells Cloud ที่ถูกต้อง มีพื้นที่จัดเก็บข้อมูลที่ใช้งานได้ และมีโทเคน JWT เพื่อใช้ในการยืนยันตัวตน โปรดรับโทเคนดังกล่าวโดยทำตามคำแนะนำในคู่มือการยืนยันตัวตนก่อนที่จะส่งคำขอ API ใดๆ

## GetWorksheetChart API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartNumber}
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและบังคับใช้การยืนยันตัวตนแบบใช้โทเคน <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>

### พารามิเตอร์คำขอ

| พารามิเตอร์ | ประเภทข้อมูล | ตำแหน่ง | คำอธิบาย |
| -------------- | ------- | -------- | ------------------------------------------- |
| name           | string  | path     | ชื่อไฟล์ Excel |
| sheetName      | string  | path     | ชื่อแผ่นงานที่มีแผนภูมิ |
| chartNumber    | integer | path     | ดัชนีของแผนภูมิที่ต้องการดึงข้อมูล (เริ่มต้นที่ 0) |
| format         | string  | query    | รูปแบบการส่งออกที่ต้องการ (เช่น png, jpeg) |
| folder         | string  | query    | ตำแหน่งโฟลเดอร์ที่เก็บเอกสารไว้ |
| storageName    | string  | query    | ชื่อของบริการจัดเก็บข้อมูล |

### **การตอบกลับ**

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Name": "Chart 1",
    "Type": "Bar",
    "Top": 50,
    "Left": 100,
    "Width": 400,
    "Height": 300,
    "DataRange": "A1:B5",
    "ShowLegend": true,
    "Format": "png"
  }
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | คำอธิบาย                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | ประมวลผลสำเร็จ; การตอบกลับประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | Bad Request                 | พารามิเตอร์ไม่ครบหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401  | Unauthorized                | โทเคน JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | Payload Too Large           | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด |
| 500  | Internal Server Error       | ข้อผิดพลาดภายในเซิร์ฟเวอร์ที่ไม่คาดคิด |

## วิธีใช้ GetWorksheetChart API ผ่าน SDK

### ข้อมูลจำเพาะของ GetWorksheetChart API

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChart) กำหนด API แบบเปิดที่สามารถเข้าถึงได้จากภายนอก และช่วยให้คุณสามารถโต้ตอบกับ REST API ผ่านเว็บเบราว์เซอร์ได้โดยตรง

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API ผ่าน cURL:

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Name": "Chart 1",
    "Type": "Bar",
    "Top": 50,
    "Left": 100,
    "Width": 400,
    "Height": 300,
    "DataRange": "A1:B5",
    "ShowLegend": true,
    "Format": "png"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งกระบวนการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ โดยที่คุณสามารถมุ่งเน้นไปที่งานหลักของโครงการได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChart-get-chart-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_worksheet_charts_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetChartAreaFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChart-get-chart-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "6fbcaeac3bd9fe1d22319418799757bd" >}}

{{< /tab >}}

{{< /tabs >}}
---