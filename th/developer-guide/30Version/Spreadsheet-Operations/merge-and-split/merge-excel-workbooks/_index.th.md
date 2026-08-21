---
title: "ผสานสมุดงาน Excel หนึ่งสมุดเข้ากับอีกสมุดงานหนึ่ง"
second_title: "เอกสาร"
linktitle: "ผสานสมุดงาน Excel เข้ากับสมุดงานอื่น"
type: docs
url: /th/merge-an-excel-file-into-the-excel-file/
aliases: [  /th/merge-excel-workbooks/ , /th/workbook/merge/ ]
keywords: "การผสาน Excel, Aspose.Cells Cloud, API สมุดงาน, REST API, การผสานสเปรดชีต, SDK บนคลาวด์, การยืนยันตัวตน, mergeWith, ตัวอย่าง cURL"
description: "คู่มือแบบทีละขั้นตอนสำหรับการผสานสมุดงาน Excel หนึ่งสมุดเข้ากับอีกสมุดหนึ่งโดยใช้ Aspose.Cells Cloud REST API (เวอร์ชัน 3.0) ประกอบด้วยการยืนยันตัวตน พารามิเตอร์ mergeWith ที่จำเป็น ตัวอย่าง cURL และตัวอย่างโค้ด SDK"
ArticleTitle: "ผสานสมุดงาน Excel เข้ากับสมุดงานอื่นโดยใช้ Aspose.Cells Cloud API"
weight: 50
---

## REST API

REST API นี้ใช้ผสาน **สมุดงาน** Excel หนึ่งสมุดเข้ากับอีกสมุดงานหนึ่ง

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/merge
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### **พารามิเตอร์ Query**

| ชื่อพารามิเตอร์ | ประเภท   | คำอธิบาย                                                |
| ---------------- | -------- | --------------------------------------------------------- |
| folder           | string   | โฟลเดอร์ที่มีสมุดงานต้นฉบับอยู่                         |
| storageName      | string   | ชื่อพื้นที่จัดเก็บ                                       |
| **mergeWith**    | string   | ชื่อสมุดงานที่จะถูกผสานเข้ากับสมุดงานเป้าหมาย           |

### **การตอบกลับ (Response)**

```json
{
    "Status":"OK",
    "Code":200,
      "Workbook": {
    "FileName": "test.xlsx",
    "Links": [
      {
        "Href": "/test.xlsx",
        "Rel": "self",
        "Title": null,
        "Type": null
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "ดาวน์โหลดเป็น CSV",
        "Type": "text/csv"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "ดาวน์โหลดเป็น HTML",
        "Type": "text/html"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "ดาวน์โหลดเป็น ODS",
        "Type": "application/vnd.oasis.opendocument.spreadsheet"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "ดาวน์โหลดเป็น PDF",
        "Type": "application/pdf"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "ดาวน์โหลดเป็นรูปแบบข้อความคั่นด้วยตาราง",
        "Type": "text/plain"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "ดาวน์โหลดเป็น TIFF",
        "Type": "image/tiff"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "ดาวน์โหลดเป็น Microsoft Excel 2003",
        "Type": "application/vnd.ms-excel"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "ดาวน์โหลดเป็น Microsoft Excel 2007",
        "Type": "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "ดาวน์โหลดเป็น XPS",
        "Type": "application/vnd.ms-xpsdocument"
      }
    ],
    "Worksheets": {
      "link": {
        "Href": "/worksheets",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "DefaultStyle": {
      "link": {
        "Href": "/defaultstyle",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "DocumentProperties": {
      "link": {
        "Href": "/documentproperties",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Names": {
      "link": {
        "Href": "/names",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Settings": {
      "link": {
        "Href": "/settings",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "IsWriteProtected": "False",
    "IsProtected": "False",
    "IsEncryption": "false",
    "Password": null
  }
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                  | คำอธิบาย                                                |
|-----|---------------------------|---------------------------------------------------------|
| 200 | สำเร็จ (OK)               | กรองข้อมูลสำเร็จ; การตอบกลับมีรายละเอียดของปฏิบัติการ |
| 400 | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401 | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                          |
| 413 | ข้อมูลส่งไปมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                         |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                  |

## วิธีใช้ API PostWorkbooksMerge ร่วมกับ SDK

### 仕样的 API PostWorkbooksMerge

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbooksMerge) กำหนดอินเทอร์เฟซการโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้ API สามารถดำเนินการปฏิสัมพันธ์ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ API บนคลาวด์ด้วย cURL รวมถึงส่วนหัวการยืนยันตัวตนที่จำเป็น

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
# ผสาน test2.xlsx เข้ากับ test.xlsx
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/merge?mergeWith=test2.xlsx" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access-token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Workbook": {
    "FileName": "test.xlsx",
    "Links": [
      {
        "Href": "/test.xlsx",
        "Rel": "self",
        "Title": null,
        "Type": null
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "ดาวน์โหลดเป็น CSV",
        "Type": "text/csv"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "ดาวน์โหลดเป็น HTML",
        "Type": "text/html"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "ดาวน์โหลดเป็น ODS",
        "Type": "application/vnd.oasis.opendocument.spreadsheet"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "ดาวน์โหลดเป็น PDF",
        "Type": "application/pdf"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "ดาวน์โหลดเป็นรูปแบบข้อความคั่นด้วยตาราง",
        "Type": "text/plain"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "ดาวน์โหลดเป็น TIFF",
        "Type": "image/tiff"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "ดาวน์โหลดเป็น Microsoft Excel 2003",
        "Type": "application/vnd.ms-excel"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "ดาวน์โหลดเป็น Microsoft Excel 2007",
        "Type": "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "ดาวน์โหลดเป็น XPS",
        "Type": "application/vnd.ms-xpsdocument"
      }
    ],
    "Worksheets": {
      "link": {
        "Href": "/worksheets",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "DefaultStyle": {
      "link": {
        "Href": "/defaultstyle",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "DocumentProperties": {
      "link": {
        "Href": "/documentproperties",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Names": {
      "link": {
        "Href": "/names",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Settings": {
      "link": {
        "Href": "/settings",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "IsWriteProtected": "False",
    "IsProtected": "False",
    "IsEncryption": "false",
    "Password": null
  },
  "Code": 200,
  "Status": "OK"
}
```

การตอบกลับจะส่งกลับวัตถุ `Workbook` ซึ่งมีข้อมูลเมตาเกี่ยวกับสมุดงานที่ผสานแล้ว รวมถึงลิงก์สำหรับดาวน์โหลดผลลัพธ์ในรูปแบบต่างๆ (CSV, PDF, HTML เป็นต้น)

ส่วนหัวการตอบกลับ

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK ซ่อนรายละเอียดระดับต่ำและช่วยให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ [GitHub Repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbooksMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbooksMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbooksMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbooksMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbooksMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbooksMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbooksMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbooksMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}