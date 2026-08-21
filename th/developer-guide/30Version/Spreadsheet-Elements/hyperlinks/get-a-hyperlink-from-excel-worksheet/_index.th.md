---
title: "รับลิงก์ไฮเปอร์เท็กซ์ของเวิร์กชีต"
type: docs
url: /hyperlinks/get/
keywords: "Aspose.Cells Cloud, Get Worksheet Hyperlink, Excel hyperlink API, REST, JWT authentication, Excel worksheet, API endpoint"
description: "ดึงลิงก์ไฮเปอร์เท็กซ์ที่ระบุจากเวิร์กชีต Excel โดยใช้ Aspose.Cells Cloud API (v3.0) ประกอบด้วย endpoint, พารามิเตอร์, ตัวอย่าง cURL, รายละเอียดการยืนยันตัวตน, การจัดการข้อผิดพลาด และตัวอย่างโค้ด SDK"
weight: 10
ArticleTitle: "Aspose.Cells Cloud API – รับลิงก์ไฮเปอร์เท็กซ์ของเวิร์กชีต"
---

REST API นี้ใช้เพื่อดึง **ลิงก์ไฮเปอร์เท็กซ์** ของเวิร์กชีตผ่าน **Aspose.Cells Get Hyperlink API**

## ความปลอดภัยและการยืนยันตัวตน

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้การยืนยันตัวตนแบบ [JWT token‑based](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
ก่อนเรียก endpoint คุณต้องได้รับ JWT access token โดยใช้ client ID และ secret ของคุณ แล้วแนบ token นี้ใน header `Authorization: Bearer <jwt token>`

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

### พารามิเตอร์ของ Request

| ชื่อพารามิเตอร์ | ประเภท    | ตำแหน่ง | คำอธิบาย                                             |
| ---------------- | --------- | -------- | ---------------------------------------------------- |
| name             | string    | path     | ชื่อไฟล์ Excel                                       |
| sheetName        | string    | path     | ชื่อเวิร์กชีตที่มีลิงก์                              |
| hyperlinkIndex   | integer   | path     | ดัชนีแบบ zero‑based ของลิงก์ไฮเปอร์เท็กซ์ที่ต้องการดึง |
| folder           | string    | query    | โฟลเดอร์ที่เอกสารถูกจัดเก็บ                         |
| storageName      | string    | query    | ชื่อของบริการจัดเก็บข้อมูล                           |

### คำตอบข้อผิดพลาด

| HTTP Code | เหตุผล                                               | ตัวอย่าง Body                                                        |
| --------- | ----------------------------------------------------- | -------------------------------------------------------------------- |
| **400**   | Bad Request – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง        | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**   | Unauthorized – ขาดหายหรือ JWT token ไม่ถูกต้อง       | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | Not Found – สมุดงานหรือเวิร์กชีตไม่มีอยู่จริง        | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**   | Internal Server Error – เกิดข้อผิดพลาดที่ไม่คาดคิด   | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlink) กำหนด programming interface ที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST interaction ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่าน command line เพื่อเข้าถึง Aspose.Cells web services ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlink": {
    "Address": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "Area": {
      "EndColumn": 0,
      "EndRow": 1,
      "StartColumn": 0,
      "StartRow": 1
    },
    "ScreenTip": null,
    "TextToDisplay": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/hyperlinks/1",
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

## ครอบครัว SDK สำหรับ Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ช่วยให้คุณโฟกัสไปที่งานในโครงการของคุณ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียก Aspose.Cells web services โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}