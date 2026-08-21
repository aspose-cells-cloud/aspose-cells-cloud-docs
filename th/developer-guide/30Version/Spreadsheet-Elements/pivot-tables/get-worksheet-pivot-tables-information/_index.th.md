---
title: "ดึงข้อมูลตารางไข่ข้าวทั้งหมดในแผ่นงาน Excel"
second_title: "เอกสาร"
linktitle: ดึงข้อมูลทั้งหมด
type: docs
url: /pivot-tables/get-all/
aliases: [/get-worksheet-pivot-tables-information/]
keywords: "ดึงข้อมูลตารางไข่ข้าวทั้งหมด, Aspose.Cells Cloud API, Excel PivotTable, REST API"
description: "ดึงข้อมูลตารางไข่ข้าวทุกตารางจากแผ่นงาน Excel ผ่าน Aspose.Cells Cloud API รวมถึง endpoint, พารามิเตอร์, ขั้นตอนการยืนยันตัวตน, cURL และตัวอย่าง SDK สำหรับ API ตารางไข่ข้าว"
weight: 20
ArticleTitle: "ดึงข้อมูลตารางไข่ข้าวทั้งหมดในแผ่นงาน Excel – Aspose.Cells Cloud API"
---

**ตารางไข่ข้าว (PivotTable)** คือเครื่องมือสรุปข้อมูลใน Excel ที่ช่วยให้คุณจัดเรียงและวิเคราะห์ชุดข้อมูลขนาดใหญ่ได้ REST API นี้จะดึงข้อมูลเกี่ยวกับ **ตารางไข่ข้าวทั้งหมด** ในแผ่นงานที่ระบุ

## ความปลอดภัยและการยืนยันตัวตน

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้การยืนยันตัวตนแบบ [โทเค็น JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                     |
| ---------------- | --------- | -------- | -------------------------------------------- |
| name             | string    | path     | ชื่อของเอกสาร Excel                         |
| sheetName        | string    | path     | ชื่อของแผ่นงาน                              |
| folder           | string    | query    | โฟลเดอร์ที่เก็บเอกสารไว้                    |
| storageName      | string    | query    | ชื่อของบริการจัดเก็บข้อมูล (storage service) |

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/GetWorksheetPivotTables) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และอนุญาตให้คุณดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

### คำขอ

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

### คำตอบ

{{< tab tabNum="2" >}}

```json
{
  "PivotTables": {
    "PivotTableList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self"
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### การตอบกลับข้อผิดพลาด

| โค้ด HTTP | คำอธิบาย                                                           | ตัวอย่าง JSON Payload                                         |
| --------- | ------------------------------------------------------------------ | ------------------------------------------------------------- |
| 400       | คำขอผิดรูปแบบ – พารามิเตอร์ที่จำเป็นขาดหายไป                     | `{ "Code": "400", "Message": "Missing required parameter." }` |
| 401       | ไม่ได้รับอนุญาต – โทเค็นไม่ถูกต้องหรือไม่มีโทเค็น                 | `{ "Code": "401", "Message": "Authentication failed." }`      |
| 404       | ไม่พบ – สมุดงาน แผ่นงาน หรือตารางไข่ข้าวไม่มีอยู่จริง            | `{ "Code": "404", "Message": "Resource not found." }`         |
| 500       | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เงื่อนไขที่ไม่คาดคิดบนเซิร์ฟเวอร์   | `{ "Code": "500", "Message": "Server error." }`               |

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่โปรเจกต์ของคุณได้ โปรดดูที่ [คลัง GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกบริการเว็บ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-GetWorksheetPivotTables-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-GetPivotTableWorksheet-GetPivotTableWorksheet-12345.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetWorksheetPivotTablesInformation.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-GetWorksheetPivotTables-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-GetPivotTableWorksheet-GetPivotTableWorksheet-12345.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-GetWorksheetPivotTables-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "6b30a17927feeb2899283e4dbe566c42" >}}
{{< /tab >}}

{{< /tabs >}}