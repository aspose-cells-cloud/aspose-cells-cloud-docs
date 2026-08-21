---
title: "Aspose.Cells Cloud API – ตั้งค่าหัวเรื่องกราฟในแผ่นงาน Excel"
type: docs
url: /chart/title/add/
aliases: [/set-chart-title-in-excel-worksheet/]
weight: 30
keywords: "Aspose.Cells Cloud, API หัวเรื่องกราฟ, หัวเรื่องกราฟ Excel, REST API, ตัวอย่าง SDK"
description: "เรียนรู้วิธีการเพิ่มหรืออัปเดตหัวเรื่องกราฟในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API รวมถึงตัวอย่าง cURL, SDK, พารามิเตอร์ที่จำเป็น, ขั้นตอนการยืนยันตัวตน และการจัดการข้อผิดพลาด"
---

เพิ่มหัวเรื่องกราฟหรือทำให้หัวเรื่องที่มีอยู่แสดงผล

## PutWorksheetChartTitle API

```http
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### พารามิเตอร์ของคำขอ

| พารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                              |
|-------------|-----------|----------|---------------------------------------|
| name        | string    | path     | ชื่อสมุดงาน                          |
| sheetName   | string    | path     | ชื่อแผ่นงาน                          |
| chartIndex  | integer   | path     | ดัชนีของกราฟ                          |
| title       | string    | body     | ข้อความของหัวเรื่องกราฟ               |
| folder      | string    | query    | โฟลเดอร์ที่เก็บสมุดงาน               |
| storageName | string    | query    | ชื่อของพื้นที่เก็บข้อมูล (storage)    |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartTitle) กำหนด API ที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการ REST interactions ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL บน command-line เพื่อเข้าถึง Aspose.Cells web services ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
  -d '{"Text":"Sales Chart"}' \
  -X PUT \
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

**การตอบกลับข้อผิดพลาด**

| HTTP Code | ตัวอย่าง Payload                                                                      | คำอธิบาย                                                 |
|-----------|----------------------------------------------------------------------------------------|-----------------------------------------------------------|
| 400       | `{ "Code": "400", "Message": "Invalid request payload." }`                            | เนื้อหาคำขอไม่ถูกต้องหรือขาดพารามิเตอร์ที่จำเป็น         |
| 401       | `{ "Code": "401", "Message": "Authentication failed. Invalid or expired JWT token." }` | JWT token ขาดหาย ไม่ถูกต้อง หรือหมดอายุ                   |
| 404       | `{ "Code": "404", "Message": "Workbook, worksheet, or chart not found." }`            | ทรัพยากรที่ระบุไม่มีอยู่                                  |
| 500       | `{ "Code": "500", "Message": "Internal server error." }`                              | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                   |

## Cloud SDK Family

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK ซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ กรุณาตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้ Aspose.Cells web services ด้วย SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-SetChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetChartTitle.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-SetChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-SetChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "728d523e11f8751f5f601bafb04ab86f" >}}

{{< /tab >}}

{{< /tabs >}}