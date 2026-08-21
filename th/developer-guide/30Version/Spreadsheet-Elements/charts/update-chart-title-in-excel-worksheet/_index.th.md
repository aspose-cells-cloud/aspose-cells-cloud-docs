---
title: "อัปเดตชื่อกราฟในแผ่นงาน Excel"
type: docs
url: /th/charts/title/update/
aliases: [  /th/update-chart-title-in-excel-worksheet/ ]
weight: 160
keywords: Excel, Aspose.Cells, REST API, ชื่อกราฟ, อัปเดต, Cloud SDK
description: เรียนรู้วิธีการอัปเดตชื่อกราฟในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API, cURL และ SDK ต่างๆ
ArticleTitle: "อัปเดตชื่อกราฟในแผ่นงาน Excel – เอกสารประกอบ Aspose.Cells Cloud"
---

REST API นี้ใช้อัปเดตชื่อกราฟ

**ข้อกำหนดเบื้องต้น:** คุณต้องมีบัญชี Aspose Cloud ที่ถูกต้องและโทเคน JWT สำหรับการตรวจสอบสิทธิ์ ขั้นตอนทั่วไปได้แก่:

- สมัครใช้งานบัญชี Aspose Cloud  
- สร้างโทเคน JWT ผ่านจุดปลายทางการตรวจสอบสิทธิ์  
- ตรวจสอบให้แน่ใจว่าสมุดงานเป้าหมายถูกจัดเก็บไว้ในพื้นที่จัดเก็บข้อมูลบนคลาวด์ที่รองรับ (ค่าเริ่มต้นหรือแบบกำหนดเอง)

## API PostWorksheetChartTitle

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

คำขอทั้งหมดต้องส่งผ่าน **HTTPS** เพื่อหลีกเลี่ยงคำเตือนเกี่ยวกับเนื้อหาแบบผสม

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์ด้วยโทเคน JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย |
| -------------- | ------- | -------- | ------------------------------ |
| name           | string  | path     | ชื่อสมุดงาน |
| sheetName      | string  | path     | ชื่อแผ่นงาน |
| chartIndex     | integer | path     | ดัชนีของกราฟ (เริ่มต้นที่ 0) |
| title          | string  | body     | ชื่อกราฟใหม่ |
| folder         | string  | query    | โฟลเดอร์ของสมุดงาน |
| storageName    | string  | query    | ชื่อพื้นที่จัดเก็บข้อมูล |

### รหัสสถานะของคำตอบ

| รหัส | คำอธิบาย |
| ---- | ---------------------------------------- |
| 200  | OK – อัปเดตชื่อกราฟเรียบร้อยแล้ว |
| 400  | Bad Request – พารามิเตอร์ไม่ครบหรือไม่ถูกต้อง |
| 401  | Unauthorized – โทเคน JWT ไม่ถูกต้องหรือไม่มี |
| 404  | Not Found – ไม่พบสมุดงาน แผ่นงาน หรือกราฟ |
| 500  | Internal Server Error – เงื่อนไขผิดปกติของเซิร์ฟเวอร์ |

**หมายเหตุ:** `chartIndex` เป็นการนับแบบเริ่มต้นที่ 0 กราฟแรกในแผ่นงานจะอ้างอิงด้วยค่า `0`

<a href="https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChartTitle" target="_blank" rel="noopener noreferrer">สเปค OpenAPI</a> กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้สาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL บนคำสั่งบรรทัดเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการส่งคำขอไปยัง Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v POST "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
-d '{"title":"Stock exchange"}' \
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

## ครอบครัว SDK สำหรับคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำและช่วยให้คุณมุ่งเน้นไปที่งานของโครงการ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository บน GitHub</a> เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการส่งคำขอไปยังบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-UpdateChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-UpdateChartTitle-update-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PostWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-update_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateChartTitleInExcelWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-UpdateChartTitle-update-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "aab21ae55930321e6eaa46ffe5b8e7bf" >}}

{{< /tab >}}

{{< /tabs >}}