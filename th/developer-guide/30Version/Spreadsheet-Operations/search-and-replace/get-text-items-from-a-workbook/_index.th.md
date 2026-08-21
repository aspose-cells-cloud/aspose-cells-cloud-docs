---
title: "ดึงรายการข้อความจากสมุดงาน Excel"
ArticleTitle: "ดึงรายการข้อความจากสมุดงาน Excel โดยใช้ Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktype: "ได้ในสมุดงาน"
type: docs
url: /workbook/get-text-items/
aliases: [/get-text-items-from-a-workbook/]
weight: 10
keywords: "Excel, Aspose.Cells Cloud, REST API, สเปรดชีต, ดึงรายการข้อความ, สมุดงาน"
description: "ดึงรายการข้อความจากสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API ซึ่งรองรับผ่าน SDK สำหรับ C#, Java, Python, PHP, Ruby, Go, Node.js, Perl และ Swift"
---


## API แบบ REST

API แบบ REST นี้อ่าน **รายการข้อความ** ของสมุดงานในไฟล์ Excel

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/textItems
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>


### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย                                            |
| -------------- | ------ | -------- | ------------------------------------------------------ |
| name           | string | path     | ชื่อไฟล์สมุดงาน                                     |
| folder         | string | query    | ตำแหน่งโฟลเดอร์ในพื้นที่จัดเก็บที่สมุดงานตั้งอยู่   |
| storageName    | string | query    | ชื่อของบริการพื้นที่จัดเก็บ                         |

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
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                          | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request)                 | ขาดหรือค่าพารามิเตอร์ไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)                | โทเค็น JWT ไม่ถูกต้องหรือขาดหายไป |
| 413  | ข้อมูลส่งออกมีขนาดใหญ่เกินไป (Payload Too Large)           | ไฟล์ที่อัปโหลดเกินขีดจำกัดขนาด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error)       | เกิดข้อผิดพลาดที่ไม่คาดคิดในเซิร์ฟเวอร์ |
## วิธีใช้ API GetWorkbookTextItems ด้วย SDK

### ข้อกำหนด API GetWorkbookTextItems

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbookTextItems) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้สาธารณะ และช่วยให้คุณดำเนินการเชื่อมต่อ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งในบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/textItems" -H "accept: application/json"
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

โค้ดสถานะ HTTP ที่พบบ่อย:

| โค้ด | คำอธิบาย                                 |
|------|---------------------------------------------|
| 200  | คำขอสำเร็จ; คืนค่ารายการข้อความแล้ว |
| 401  | ไม่ได้รับอนุญาต – ขาดหรือโทเค็นไม่ถูกต้อง    |
| 403  | ถูกปฏิเสธ – สิทธิ์ไม่เพียงพอ                       |
| 404  | ไม่พบ – สมุดงานหรือทรัพยากรไม่พบ              |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – ล้มเหลวอย่างไม่คาดคิด |

### ใช้ SDK ของ Aspose.Cells Cloud

ตัวอย่างนี้ใช้เวอร์ชัน API **v3.0**; อ้างอิงบันทึกการเปลี่ยนแปลงสำหรับเวอร์ชันที่ใหม่กว่า การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำและช่วยให้คุณมุ่งเน้นไปที่งานโปรเจกต์ของคุณ โปรดตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbookTextItems.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbookTextItems.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbookTextItems.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbookTextItems.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbookTextItems.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbookTextItems.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbookTextItems.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbookTextItems.go" >}}

{{< /tab >}}

{{< /tabs >}}