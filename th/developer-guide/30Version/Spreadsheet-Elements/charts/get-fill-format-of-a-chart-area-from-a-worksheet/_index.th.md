---
title: "รับรูปแบบการเติมพื้นที่กราฟ – Aspose.Cells Cloud API (v3.0)"
type: docs
url: /th/charts/chart-area/fill-format/get/
aliases: [  /th/get-fill-format-of-a-chart-area-from-a-worksheet/ ]
weight: 70
keywords:
  - "Aspose.Cells"
  - "Chart Area"
  - "Fill Format"
  - "REST API"
  - "Excel"
description: "ดึงข้อมูลรูปแบบการเติม (สี รูปแบบพื้นผิว หรือไล่สี) ของพื้นที่กราฟในสมุดงาน Excel ผ่าน Aspose.Cells Cloud API พร้อมตัวอย่าง cURL โค้ดตัวอย่าง SDK ขั้นตอนการยืนยันตัวตน และรายละเอียดการตอบกลับ"
ArticleTitle: "รับรูปแบบการเติมพื้นที่กราฟ Aspose.Cells Cloud API v3.0"
---

REST API นี้จะดึงข้อมูลรูปแบบการเติมของ **พื้นที่กราฟ (Chart Area)**

**ข้อกำหนดเบื้องต้น**  
ในการเรียกใช้จุดปลายทางนี้ คุณต้องมีโทเคนการเข้าถึง OAuth/JWT ที่ถูกต้อง รับโทเคนโดยใช้ขั้นตอนการยืนยันตัวตนของ Aspose.Cells Cloud และใส่ในส่วนหัว `Authorization` ในรูปแบบ `Bearer <jwt token>` หากคุณใช้ SDK ใดๆ ให้แน่ใจว่า SDK ได้รับการตั้งค่าด้วย `client_id` และ `client_secret` ของคุณก่อนเรียกใช้เมธอด

## API GetChartAreaFillFormat

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/chartArea/fillFormat
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                |
| ---------------- | --------- | -------- | --------------------------------------- |
| name             | string    | path     | ชื่อสมุดงาน                             |
| sheetName        | string    | path     | ชื่อแผ่นงาน                             |
| chartIndex       | integer   | path     | ดัชนีของกราฟ                            |
| folder           | string    | query    | โฟลเดอร์ที่เก็บสมุดงาน                  |
| storageName      | string    | query    | ชื่อพื้นที่จัดเก็บ (storage)             |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ChartArea/GetChartAreaFillFormat) นิยามอินเทอร์เฟซโปรแกรมที่เข้าถึงได้จากสาธารณะ และอนุญาตให้คุณดำเนินการโต้ตอบ REST โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ตัวอย่างด้านล่างแสดงวิธีเรียกใช้ API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea/fillFormat" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "FillFormat": {
    "Type": "Automatic"
  },
  "Code": 200,
  "Status": "OK"
}
```

**หมายเหตุ**  
- การเรียกใช้งานที่สำเร็จจะส่งกลับ HTTP 200 พร้อมรายละเอียดรูปแบบการเติม  
- HTTP 401 แสดงว่าการยืนยันตัวตนล้มเหลว (โทเคนไม่ถูกต้องหรือไม่มี)  
- HTTP 404 จะถูกส่งกลับเมื่อสมุดงาน แผ่นงาน หรือดัชนีกราฟที่ระบุไม่มีอยู่  
- HTTP 500 แสดงข้อผิดพลาดฝั่งเซิร์ฟเวอร์ ลองเรียกใหม่หรือติดต่อฝ่ายสนับสนุนหากปัญหายังคงอยู่

| โค้ด | ความหมาย                                              |
|-----|-------------------------------------------------------|
| 200 | สำเร็จ – ส่งกลับรูปแบบการเติมแล้ว                   |
| 401 | ไม่ได้รับอนุญาต – โทเคนไม่ถูกต้องหรือไม่มี            |
| 404 | ไม่พบ – ไม่พบสมุดงาน แผ่นงาน หรือกราฟที่ระบุ         |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์                            |

สำหรับการดำเนินการที่เกี่ยวข้อง ดูที่จุดปลายทาง **Get Chart Area Border** และ **Get Chart Title**

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับล่างให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChartFillFormat-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetChartAreaFillFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_area_fill_format_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetFillFormatOfChartAreaFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChartFillFormat-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChartFillFormat-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "d9af13f9a5cf8dee333f8d5e26c32866" >}}

{{< /tab >}}

{{< /tabs >}}
---