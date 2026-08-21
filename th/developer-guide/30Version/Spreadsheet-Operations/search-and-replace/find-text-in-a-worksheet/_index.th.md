---
title: "ค้นหาข้อความในแผ่นงาน Excel"
second_title: "เอกสาร"
linktitle: "ค้นหาในแผ่นงาน"
type: docs
url: /th/worksheets/find-text/
aliases: [  /th/find-text-in-a-worksheet/ ]
weight: 40
keywords: "Excel, Aspose.Cells Cloud, REST API, ค้นหาข้อความ, แผ่นงาน, สเปรดชีต, ค้นหา"
description: "ใช้ Aspose.Cells Cloud REST API เพื่อค้นหาข้อความในแผ่นงาน Excel API นี้พร้อมใช้งานผ่าน SDK หลายตัวและภาษาการเขียนโปรแกรม"
---

REST API นี้ใช้ค้นหาข้อความในแผ่นงาน Excel

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/findText
```


### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>


### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย         |
| ---------------- | ---------- | -------- | ---------------- |
| name             | string     | path     | ชื่อเอกสาร       |
| sheetName        | string     | path     | ชื่อแผ่นงาน     |
| text             | string     | query    | ข้อความที่ต้องการค้นหา |
| folder           | string     | query    | โฟลเดอร์ของเอกสาร |
| storageName      | string     | query    | ชื่อพื้นที่จัดเก็บ |

### **การตอบกลับ**

```json
{
  "Status":"OK",
  "Code":200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย                                      |
|------|------------------------------|-----------------------------------------------|
| 200  | สำเร็จ (OK)                  | ใช้ตัวกรองสำเร็จ การตอบกลับมีรายละเอียดของ операция |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหายไป |
| 413  | ข้อมูลส่งไปใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

## วิธีใช้ PostWorksheetTextSearch API ด้วย SDK

### สเปคของ PostWorksheetTextSearch API

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetTextSearch) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถปฏิบัติการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างด้านล่างแสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/findText?text=a" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK ซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดดู [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetTextSearch.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetTextSearch.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetTextSearch.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetTextSearch.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetTextSearch.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetTextSearch.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetTextSearch.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetTextSearch.go" >}}

{{< /tab >}}

{{< /tabs >}}