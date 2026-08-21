---
title: "ซ่อนคำอธิบายกราฟในแผ่นงาน Excel – API ของ Aspose.Cells Cloud"
type: docs
url: /charts/legend/hide/
aliases: [/hide-chart-legend-in-a-worksheet/]
weight: 110
keywords: "Aspose.Cells, Excel, ซ่อนคำอธิบายกราฟ, REST API, Cloud SDK, คำอธิบายกราฟ"
description: "เรียนรู้วิธีซ่อนคำอธิบายกราฟในแผ่นงาน Excel โดยใช้ REST API ของ Aspose.Cells Cloud ซึ่งรวมถึง HTTPS endpoint, การรับรองความถูกต้องที่จำเป็น, ไวยากรณ์คำขอ, รายละเอียดการตอบกลับ, การจัดการข้อผิดพลาด และตัวอย่าง SDK"
---

API นี้จะซ่อนคำอธิบายกราฟ (chart legend) ซึ่งคือกล่องที่ระบุชุดข้อมูล (data series) ที่ถูกวาดลงในกราฟ

API นี้ต้องใช้โทเคน JWT ที่ถูกต้องจาก Aspose Cloud, สมุดงานต้องถูกอัปโหลดลงในที่จัดเก็บบน Aspose Cloud และเวอร์ชัน API ที่ใช้คือ **v3.0**

## ความปลอดภัยและการรับรองความถูกต้อง
API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้การรับรองความถูกต้องแบบใช้โทเคน JWT [ดูรายละเอียดเพิ่มเติม](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## REST API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                        |
| ---------------- | --------- | -------- | ------------------------------- |
| **name**         | string    | path     | ชื่อสมุดงาน                    |
| **sheetName**    | string    | path     | ชื่อแผ่นงาน                    |
| **chartIndex**   | integer   | path     | ดัชนีของกราฟ                   |
| **folder**       | string    | query    | โฟลเดอร์ของสมุดงาน (ไม่บังคับ) |
| **storageName**  | string    | query    | ชื่อที่จัดเก็บ (ไม่บังคับ)      |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetChartLegend) นิยามอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้สาธารณะนี้

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเรียก API ได้อย่างง่ายดาย ตัวอย่างด้านล่างแสดงคำขอที่ซ่อนคำอธิบายกราฟตัวที่ 0 ในไฟล์ _Sample_Test_Book.xls_

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
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

## การตอบกลับ

| สถานะ HTTP                   | คำอธิบาย                                             | JSON ตัวอย่าง                                                |
| ---------------------------- | ---------------------------------------------------- | ----------------------------------------------------------- |
| **200 OK**                   | ซ่อนคำอธิบายกราฟเรียบร้อยแล้ว                      | `{ "Code": 200, "Status": "OK" }`                           |
| **401 Unauthorized**         | โทเคน JWT ขาดหายหรือไม่ถูกต้อง                     | `{ "Code": 401, "Message": "Invalid access token." }`       |
| **404 Not Found**            | สมุดงาน แผ่นงาน หรือกราฟไม่พบ                      | `{ "Code": 404, "Message": "Chart not found." }`            |
| **500 Internal Server Error**| เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์             | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## FAQ

**Q:** _วิธีซ่อนคำอธิบายกราฟโดยใช้ Aspose.Cells Cloud มีวิธีการอย่างไร?_  
**A:** ส่งคำขอแบบ `DELETE` ไปยัง `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend` โดยใส่โทเคน JWT ที่ถูกต้องในหัวข้อ `Authorization` การตอบกลับด้วยสถานะ `200 OK` แสดงว่าดำเนินการสำเร็จ

**Q:** _การรับรองความถูกต้องที่จำเป็นสำหรับ API ในการซ่อนคำอธิบายกราฟคืออะไร?_  
**A:** ต้องใส่หัวข้อ `Authorization: Bearer <jwt token>` คุณสามารถรับโทเคนผ่านกระบวนการ OAuth ของ Aspose Cloud

**Q:** _หากดัชนีกราฟไม่ถูกต้อง จะได้รับการตอบกลับข้อผิดพลาดแบบใด?_  
**A:** บริการจะตอบกลับด้วย `404 Not Found` พร้อม JSON body ที่มี `Code: 404` และข้อความอธิบายว่าไม่พบกราฟ

**Q:** _สามารถใช้ HTTP แทน HTTPS ได้หรือไม่?_  
**A:** ไม่ได้ เนื่องจากปลายทางทั้งหมดของ Aspose Cloud ต้องใช้ HTTPS เพื่อความปลอดภัย

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา โดย SDK จะซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานหลักของโครงการได้ กรุณาตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ที่มีทั้งหมด

ตัวอย่างโค้ดด้านล่างแสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-HideChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-hide_legend_in_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "HideChartLegendInWorkSheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-HideChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
**เร็วๆ นี้จะเปิดให้ใช้งาน** – ตัวอย่าง SDK สำหรับ Swift จะเพิ่มเข้ามาในเร็วๆ นี้  
{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-HideChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3eb15aa10e3d2cd8931e60f8d001fd1c" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebPage",
  "name": "ซ่อนคำอธิบายกราฟในแผ่นงาน Excel – API ของ Aspose.Cells Cloud",
  "description": "คู่มือทีละขั้นตอนสำหรับซ่อนคำอธิบายกราฟในแผ่นงาน Excel โดยใช้ REST API ของ Aspose.Cells Cloud ซึ่งประกอบด้วย HTTPS endpoint, การรับรองความถูกต้อง, ไวยากรณ์คำขอ, รายละเอียดการตอบกลับ, การจัดการข้อผิดพลาด และตัวอย่าง SDK",
  "breadcrumb": {
    "@type": "BreadcrumbList",
    "itemListElement": [
      { "@type": "ListItem", "position": 1, "name": "หน้าแรก", "item": "https://docs.aspose.cloud/" },
      { "@type": "ListItem", "position": 2, "name": "Cells", "item": "https://docs.aspose.cloud/cells/" },
      { "@type": "ListItem", "position": 3, "name": "Charts", "item": "https://docs.aspose.cloud/cells/charts/" },
      { "@type": "ListItem", "position": 4, "name": "ซ่อนคำอธิบายกราฟ", "item": "https://docs.aspose.cloud/cells/charts/legend/hide/" }
    ]
  },
  "about": "ซ่อนคำอธิบายกราฟโดยใช้ API ของ Aspose.Cells Cloud"
}
</script>