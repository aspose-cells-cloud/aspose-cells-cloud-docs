---
title: "ดึงชื่อจากสมุดงาน Excel"
second_title: "เอกสาร"
linktitle: "ชื่อ"
type: docs
url: /th/get-names-from-an-excel-file/
aliases:
  [
    "/get-names-count-from-excel-workbooks/",
    "/workbook/names/",
    "/workbook/get/names/",
  ]
keywords: "Aspose.Cells, Cloud, Excel, Workbook, Names, REST API, SDK"
description: "ดึงชื่อที่กำหนดไว้ทั้งหมดจากสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API ประกอบด้วยคำแนะนำการยืนยันตัวตน ตัวอย่าง cURL โครงสร้างการตอบกลับ การจัดการข้อผิดพลาด และตัวอย่าง SDK"
weight: 120
ArticleTitle: "ดึงชื่อจากสมุดงาน Excel – Aspose.Cells Cloud API"
---

REST API นี้จะดึงชื่อที่กำหนดไว้จากสมุดงาน Excel

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

## API GetWorkbookNames

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/names
```

พารามิเตอร์คำขอมีดังนี้:

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย                                    |
| ---------------- | -------- | -------- | ------------------------------------------- |
| name             | string   | path     | ชื่อไฟล์สมุดงาน                            |
| folder           | string   | query    | โฟลเดอร์ที่เก็บสมุดงานไว้                  |
| storageName      | string   | query    | ชื่อของพื้นที่จัดเก็บ (storage) ที่จะใช้งาน |

คำขอต้องมี HTTP headers ดังนี้:

| Header        | ประเภท   | คำอธิบาย                                       |
|---------------|----------|------------------------------------------------|
| Authorization | string   | Bearer JWT token (จำเป็นต้องมี)                |
| Accept        | string   | `application/json`                             |
| Content-Type  | string   | `application/json` (สำหรับคำขอที่มีเนื้อหา)   |

**การยืนยันตัวตน** – API นี้ต้องใช้ OAuth2/JWT bearer token คุณสามารถขอ token ได้จาก `https://api.aspose.cloud/connect/token` โดยใช้ client-id และ client-secret ของคุณ จากนั้นเพิ่ม header `Authorization: Bearer <jwt token>` ในทุกคำขอ

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbookNames) กำหนด programming interface ที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถสื่อสารผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL บน command-line เพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ตัวอย่างด้านล่างนี้แสดงวิธีเรียกใช้ Aspose.Cells Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/names" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "Names": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Count": 0,
    "NameList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        }
      }
    ]
  }
}
```

**ฟิลด์ในคำตอบ (Response fields)**

- **Status** _(string)_ – ข้อความสถานะการดำเนินการ
- **Names.link** _(object)_ – ข้อมูลลิงก์สำหรับคอลเลกชัน
- **Names.Count** _(integer)_ – จำนวนชื่อที่กำหนดไว้ทั้งหมดที่ส่งกลับมา
- **Names.NameList** _(array)_ – รายการของวัตถุชื่อ; แต่ละวัตถุมี object **link** ที่มีรายละเอียดการนำทาง

**การจัดการข้อผิดพลาด** – บริการอาจส่งกลับ HTTP status codes ต่อไปนี้:

| โค้ด | ความหมาย                | คำแนะนำการดำเนินการ                                        |
| ----- | ------------------------ | ------------------------------------------------------------ |
| 401   | ไม่ได้รับอนุญาต (Unauthorized) | ตรวจสอบให้แน่ใจว่าได้ระบุ JWT token ที่ถูกต้อง             |
| 404   | ไม่พบ (Not Found)        | ตรวจสอบให้แน่ใจว่าชื่อสมุดงาน โฟลเดอร์ และพื้นที่จัดเก็บถูกต้อง |
| 500   | เซิร์ฟเวอร์เกิดข้อผิดพลาดภายใน (Internal Server Error) | ลองใหม่อีกครั้งภายหลัง หรือติดต่อทีมสนับสนุนของ Aspose หากปัญหายังคงอยู่ |

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว Cloud SDK

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ช่วยให้คุณสามารถมุ่งเน้นไปที่โปรเจกต์ของคุณได้ โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้เว็บเซอร์วิสของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbookNames.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbookNames.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbookNames.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbookNames.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbookNames.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbookNames.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbookNames.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbookNames.go" >}}

{{< /tab >}}

{{< /tabs >}}