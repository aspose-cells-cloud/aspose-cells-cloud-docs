---
title: "รับลิงก์ทั้งหมด – Aspose.Cells Cloud REST API"
type: docs
url: /th/hyperlinks/get-all/
aliases:
  [/get-hyperlink-from-excel-worksheet/, /get-hyperlinks-from-excel-worksheet/]
keywords: "Aspose.Cells, รับลิงก์ทั้งหมด, Excel API, REST API, Cloud SDK, ตัวอย่าง cURL, ลิงก์ในสเปรดชีต"
description: "ดึงลิงก์ทั้งหมดจากชีตงานในไฟล์ Excel โดยใช้ Aspose.Cells Cloud REST API (เวอร์ชัน 3.0) รวมถึง endpoint HTTPS, พารามิเตอร์ที่จำเป็น, ตัวอย่าง cURL, โครงสร้างคำตอบ และตัวอย่างโค้ด SDK"
weight: 10
ArticleTitle: "รับลิงก์ทั้งหมด – เอกสารประกอบ Aspose.Cells Cloud REST API"
---

REST API นี้จะดึง **ลิงก์ทั้งหมด** จากชีตงานเฉพาะในสมุดงาน Excel

## ความปลอดภัยและการยืนยันตัวตน

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้การยืนยันตัวตนแบบ [JWT token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | จำเป็น | ค่าเริ่มต้น | คำอธิบาย                                   |
| ---------------- | ---------- | -------- | ------ | ----------- | ------------------------------------------ |
| name             | string     | path     | ใช่    | –           | ชื่อของเอกสาร Excel                        |
| sheetName        | string     | path     | ใช่    | –           | ชื่อของชีตงาน                             |
| folder           | string     | query    | ไม่ใช่ | –           | โฟลเดอร์ที่เก็บเอกสารไว้                  |
| storageName      | string     | query    | ไม่ใช่ | –           | ชื่อของบริการจัดเก็บข้อมูลที่จะใช้งาน     |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlinks) กำหนด API ที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งใน command-line เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างด้านล่างแสดงวิธีเรียก API ผ่าน cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="คำตอบ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlinks": {
    "Count": 4,
    "HyperlinkList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": null
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

คำตอบ JSON จะมีออบเจกต์ `Hyperlinks`

- **Count** – จำนวนลิงก์ทั้งหมดในชีตงาน
- **HyperlinkList** – อาเรย์ที่แต่ละรายการมีออบเจกต์ `link` โดยคุณสมบัติ `Href` จะเก็บที่อยู่ของลิงก์ ส่วน `Rel`, `Title`, และ `Type` ให้ข้อมูลเมตาเพิ่มเติม (มักเป็น `null` สำหรับลิงก์แบบง่าย)

### การตอบกลับข้อผิดพลาด

| HTTP Code | เหตุผล                                              | ตัวอย่างเนื้อหาคำตอบ                                               |
| --------- | ---------------------------------------------------- | ------------------------------------------------------------------ |
| **400**   | คำขอไม่ถูกต้อง – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง  | `{ "Code":"400", "Message":"Invalid parameter value." }`          |
| **401**   | ไม่ได้รับอนุญาต – JWT token ขาดหายหรือไม่ถูกต้อง | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | ไม่พบ – สมุดงานหรือชีตงานไม่มีอยู่                | `{ "Code":"404", "Message":"File not found." }`                   |
| **500**   | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เซิร์ฟเวอร์ล้มเหลวโดยไม่คาดคิด | `{ "Code":"500", "Message":"An unexpected error occurred." }`    |

## Cloud SDK Family

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการผสานรวมฟังก์ชันนี้ SDK จะจัดการรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณเองได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}