---
title: "ล้างเนื้อหาและรูปแบบของเซลล์ในแผ่นงาน Excel"
type: docs
url: /th/clear-contents-and-styles-of-cells-in-excel-worksheet/
weight: 50
keywords:
  - Aspose.Cells
  - Excel API
  - clear cell contents
  - clear cell styles
  - cloud spreadsheet
  - REST API
description: "เรียนรู้วิธีใช้ Aspose.Cells Cloud REST API ในการล้างเนื้อหาและรูปแบบของเซลล์ในแผ่นงาน Excel พร้อมตัวอย่าง cURL และโค้ดตัวอย่าง SDK"
ArticleTitle: "ล้างเนื้อหาและรูปแบบของเซลล์ในแผ่นงาน Excel – Aspose.Cells Cloud API"
---

ก่อนใช้งานจุดปลายทาง **Clear Contents and Styles** คุณควรตรวจสอบให้แน่ใจว่าคุณมี:

* เทคโนโลยี **JWT token** ที่ได้รับจากกระบวนการยืนยันตัวตนของ Aspose.Cells Cloud  
* สมุดงานที่อัปโหลดไว้ยังที่จัดเก็บที่คุณเลือก (หรือเข้าถึงได้ผ่านพารามิเตอร์ `folder`)  
* รุ่น SDK ที่จำเป็นติดตั้งไว้แล้ว หากคุณต้องการใช้ไลบรารีไคลเอนต์ที่รองรับภาษาเฉพาะ

API นี้เป็น REST API ที่ใช้ในการล้างเนื้อหาของเซลล์ในไฟล์ Excel

## PostClearContents API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearcontents
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบใช้ JWT token</a>

### **การตอบกลับ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                    | คำอธิบาย                                       |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | ใช้ตัวกรองสำเร็จ; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400  | Bad Request                 | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | Unauthorized                | JWT token ไม่ถูกต้องหรือขาดหาย |
| 413  | Payload Too Large           | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | Internal Server Error       | เกิดข้อผิดพลาดภายในเซิร์ฟเวอร์ที่ไม่คาดคิด |

## วิธีใช้ PostClearContents API ผ่าน SDK

### ข้อมูลจำเพาะ PostClearContents API

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostClearContents) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ผ่าน cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/clearcontents?range=A2:C11" \
  -X POST \
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

### ใช้งาน Aspose.Cells Cloud SDK

การใช้งาน SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ และช่วยให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ [repository บน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ที่มีทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ผ่าน SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostClearContents.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostClearContents.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostClearContents.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostClearContents.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostClearContents.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostClearContents.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostClearContents.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostClearContents.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "ล้างเนื้อหาและรูปแบบของเซลล์ในแผ่นงาน Excel",
  "description": "วิธีใช้ Aspose.Cells Cloud REST API ในการล้างเนื้อหาและรูปแบบของเซลล์ในแผ่นงาน Excel",
  "url": "https://docs.aspose.cloud/cells/clear-contents-and-styles-of-cells-in-excel-worksheet/",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2023-07-08",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose",
    "logo": {
      "@type": "ImageObject",
      "url": "https://docs.aspose.cloud/cells/images/Aspose-image-for-open-graph.jpg",
      "caption": "Aspose.Cells Cloud – ล้างเนื้อหาและรูปแบบของเซลล์"
    }
  },
  "keywords": "Aspose.Cells, Excel API, clear cell contents, clear cell styles, REST API, cloud spreadsheet"
}
</script>