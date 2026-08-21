---
title: "รับการแบ่งหน้าแนวนอน"
second_title: "เอกสาร"
linktitle: "รับการแบ่งหน้าแนวนอน"
type: docs
url: /th/page-breaks/get-horizontal-page-breaks/
aliases: [  /th/get-horizontal-page-breaks-inside-worksheet/ ]
keywords: "การแบ่งหน้าแนวนอน, Aspose.Cells Cloud, REST API, สมุดงาน Excel, SDK"
description: "ดึงการแบ่งหน้าแนวนอนจากสมุดงาน Excel ผ่าน Aspose.Cells Cloud API รวมถึง endpoint, พารามิเตอร์, ตัวอย่าง cURL, รูปแบบการตอบกลับ และตัวอย่างโค้ด SDK สำหรับ C#, Java, Python และอื่นๆ"
ArticleTitle: "รับการแบ่งหน้าแนวนอน - เอกสารประกอบ API Aspose.Cells Cloud"
weight: 10
---

**การแบ่งหน้าแนวนอน** – การแบ่งที่อยู่บนพื้นฐานของแถว ซึ่งบังคับให้สมุดงานเริ่มหน้าพิมพ์ใหม่หลังจากแถวที่ระบุ API นี้เป็น REST API ที่ใช้ดึงการแบ่งหน้าแนวนอนเหล่านี้

## ความปลอดภัยและการยืนยันตัวตน

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ [การยืนยันตัวตนแบบใช้โทเค็น JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
```

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                       |
| ---------------- | --------- | -------- | -------------------------------------------------------------- |
| name             | string    | path     | ชื่อไฟล์ Excel                                                 |
| sheetName        | string    | path     | ชื่อของworksheet                                               |
| folder           | string    | query    | เส้นทางโฟลเดอร์ในพื้นที่จัดเก็บที่ไฟล์อยู่ _(ไม่บังคับ)_         |
| storageName      | string    | query    | ชื่อของพื้นที่จัดเก็บ _(ไม่บังคับ)_                             |

<a href="https://apireference.aspose.cloud/cells/#/PageBreaks/GetHorizontalPageBreaks" rel="noopener" title="สเปค OpenAPI สำหรับ GetHorizontalPageBreaks">สเปค OpenAPI</a> กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้สาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งในบรรทัดคำสั่งเพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ผ่าน cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "HorizontalPageBreaks": {
    "HorizontalPageBreakList": [
      {
        "Row": 6,
        "EndColumn": 16383,
        "StartColumn": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/HorizontalPageBreaks",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## การจัดการข้อผิดพลาด

| HTTP Status | คำอธิบาย                                                   | ตัวอย่าง JSON                                         |
| ----------- | ---------------------------------------------------------- | ----------------------------------------------------- |
| 400         | คำขอไม่ถูกต้อง – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง         | `{ "Code": 400, "Message": "Invalid parameter." }`    |
| 401         | ไม่ได้รับอนุญาต – โทเค็น JWT ขาดหายหรือไม่ถูกต้อง         | `{ "Code": 401, "Message": "Authentication failed." }` |
| 404         | ไม่พบ – ไฟล์หรือ worksheet ที่ระบุไม่มีอยู่                 | `{ "Code": 404, "Message": "Resource not found." }`   |
| 500         | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เงื่อนไขที่ไม่คาดคิดบนเซิร์ฟเวอร์ | `{ "Code": 500, "Message": "Server error." }`         |

## ครอบครัว SDK ของ Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณ โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้เว็บเซอร์วิสของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetHorizontalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetHorizontalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetHorizontalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetHorizontalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetHorizontalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetHorizontalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetHorizontalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetHorizontalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}