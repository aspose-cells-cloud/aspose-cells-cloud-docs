---
title: "การเพิ่มกราฟลงในแผ่นงาน"
type: docs
url: /charts/add/
aliases: [/add-a-chart-in-a-worksheet/]
weight: 20
description: "เรียนรู้วิธีการเพิ่มกราฟลงในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud API เวอร์ชัน 3.0 ซึ่งรวมถึง endpoint, พารามิเตอร์, ตัวอย่าง cURL และตัวอย่าง SDK"
keywords:
  - "add chart Aspose.Cells"
  - "Aspose.Cells add chart API"
  - "chart API REST"
  - "Aspose.Cells SDK examples"
ArticleTitle: "การเพิ่มกราฟลงในแผ่นงาน – คู่มือ Aspose.Cells Cloud API"
---

REST API นี้จะเพิ่มกราฟใหม่ลงในแผ่นงาน

**ข้อกำหนดเบื้องต้น**  
ก่อนเรียกใช้การดำเนินการนี้ คุณต้องได้รับโทเค็น JWT ที่ถูกต้องและตรวจสอบให้แน่ใจว่าสมุดงานเป้าหมายถูกจัดเก็บไว้ในโฟลเดอร์หรือตำแหน่งที่เก็บข้อมูลที่ระบุ

## PutWorksheetAddChart API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์         | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                                                                                                                              |
| ----------------------- | -------- | -------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**                | string   | path     | ชื่อสมุดงาน                                                                                                                                                                           |
| **sheetName**           | string   | path     | ชื่อแผ่นงาน                                                                                                                                                                          |
| **chartType**           | string   | query    | ประเภทของกราฟ (ดูคุณสมบัติ **Type** ในทรัพยากรกราฟ) ประเภทกราฟที่รองรับ ได้แก่ **Bar**, **Column**, **Line**, **Pie**, **Scatter**, **Area**, **Doughnut**, **Radar** เป็นต้น |
| **upperLeftRow**        | integer  | query    | ดัชนีแถวบนซ้ายของพื้นที่กราฟ (เริ่มต้นที่ 0)                                                                                                                                        |
| **upperLeftColumn**     | integer  | query    | ดัชนีคอลัมน์บนซ้ายของพื้นที่กราฟ (เริ่มต้นที่ 0)                                                                                                                                     |
| **lowerRightRow**       | integer  | query    | ดัชนีแถวล่างขวาของพื้นที่กราฟ (เริ่มต้นที่ 0)                                                                                                                                       |
| **lowerRightColumn**    | integer  | query    | ดัชนีคอลัมน์ล่างขวาของพื้นที่กราฟ (เริ่มต้นที่ 0)                                                                                                                                    |
| **area**                | string   | query    | ช่วงข้อมูลที่ใช้เป็นค่าสำหรับกราฟ (เช่น `A1:B5`)                                                                                                                                  |
| **isVertical**          | boolean  | query    | ระบุว่าทิศทางของกราฟเป็นแนวตั้งหรือไม่                                                                                                                                     |
| **categoryData**        | string   | query    | ช่วงของค่าแกนหมวดหมู่ (เช่น `D1:E10`)                                                                                                                                          |
| **isAutoGetSerialName** | boolean  | query    | หากเป็น **true** จะสร้างชื่อซีรีส์โดยอัตโนมัติ                                                                                                                                   |
| **title**               | string   | query    | หัวเรื่องของกราฟ                                                                                                                                                                      |
| **folder**              | string   | query    | โฟลเดอร์ที่เก็บสมุดงาน                                                                                                                                                       |
| **storageName**         | string   | query    | ชื่อของพื้นที่จัดเก็บ                                                                                                                                                                     |
| **dataLabels**          | boolean  | query    | แสดงป้ายกำกับข้อมูลเมื่อเป็น **true**                                                                                                                                                          |
| **dataLabelsPosition**  | string   | query    | ตำแหน่งของป้ายกำกับข้อมูล (เช่น `Above`)                                                                                                                                                 |
| **pivotTableSheet**     | string   | query    | ชื่อของแผ่นงานที่มีตารางไขว้                                                                                                                                                         |
| **pivotTableName**      | string   | query    | ชื่อของตารางไขว้                                                                                                                                                                 |

### **การตอบกลับ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | กรองถูกใช้งานเรียบร้อยแล้ว; การตอบกลับประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | Bad Request                 | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | Unauthorized                | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | Payload Too Large           | ไฟล์ที่อัปโหลดเกินขีดจำกัดขนาด |
| 500  | Internal Server Error       | เกิดข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด |

## วิธีการใช้ PutWorksheetAddChart API ร่วมกับ SDK

### ข้อมูลจำเพาะ PutWorksheetAddChart API

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetAddChart) กำหนด API ที่สามารถเข้าถึงได้แบบเปิดเผย และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งใน command-line เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts?chartType=Bar&area=B1:F2&title=SalesState" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
# การดำเนินการนี้ไม่จำเป็นต้องมีเนื้อหาคำขอ (request body)
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

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะซ่อนรายละเอียดระดับต่ำไว้ และช่วยให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Perl" tabName9="Android" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-AddChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-AddChart-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetAddChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_new_chart_to_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddChartToWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-AddChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-AddChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-chart-AddChart-AddChart.jave" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "7fa79c30fca0c594c18c0f3937b6bcc9" >}}

{{< /tab >}}

{{< /tabs >}}