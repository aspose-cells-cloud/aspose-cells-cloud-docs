---
title: "ส่งออกชีตงาน – API ของ Aspose.Cells Cloud v4 (PDF, PNG, SVG, CSV)"
second_title: "เอกสาร"
ArticleTitle: "วิธีการส่งออกชีตงานสเปรดชีตแบบรีโมทไปยังรูปแบบอื่น: คู่มือแบบทีละขั้นตอน"
linktype: "ส่งออกชีตงาน"
type: docs
url: /export-worksheet-as-format/
keywords: "Aspose Cells, ส่งออกชีตงาน, API คลาวด์, PDF, PNG, CSV, การแปลง Excel"
description: "แปลงชีตงานที่จัดเก็บไว้ใน Aspose.Cells Cloud เป็นรูปแบบ PDF, PNG, SVG, CSV หรือรูปแบบอื่นๆ ผ่านคำขอ GET แบบเดียว พร้อมตัวอย่างโค้ดสำหรับ C#, Java, Python และอื่นๆ"
weight: 100
---

ส่งออกชีตงานสเปรดชีต/Excel แบบคลาวด์ไปยังไฟล์รูปแบบอื่นโดยใช้เว็บ API ของ Aspose.Cells Cloud

## **API ส่งออกชีตงานเป็นรูปแบบ**

### เว็บ API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}

```

### **การรักษาความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

```bash
-H "Authorization: Bearer {access_token}"
```

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์   | ประเภท   | พาธ/สตริงคิวรี/เนื้อหา HTTPBody | คำอธิบาย                                                                                                                                        |
| :----------------- | :----- | :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**           | สตริง | พาธ                       | (จำเป็น) ชื่อของไฟล์สมุดงานที่ต้องการดึงมา                                                                                                          |
| **worksheet**      | สตริง | พาธ                       | (จำเป็น) ชีตงานที่ต้องการแปลง                                                                                                      |
| **format**         | สตริง | คิวรี                      | (จำเป็น) รูปแบบเอาต์พุตที่ต้องการ (เช่น `png`, `pdf`, `svg`)                                                                                  |
| **folder**         | สตริง | คิวรี                      | (ไม่บังคับ) เส้นทางโฟลเดอร์ที่เก็บสมุดงาน ค่าเริ่มต้นคือ `null`                                                                    |
| **storageName**    | สตริง | คิวรี                      | (ไม่บังคับ) ชื่อของพื้นที่จัดเก็บคลาวด์แบบกำหนดเอง ใช้พื้นที่จัดเก็บเริ่มต้นหากไม่ระบุ                                                                   |
| **outPath**        | สตริง | คิวรี                      | (ไม่บังคับ) เส้นทางโฟลเดอร์เอาต์พุต ค่าเริ่มต้นคือ `null`                                                                                          |
| **outStorageName** | สตริง | คิวรี                      | (ไม่บังคับ) ชื่อพื้นที่จัดเก็บไฟล์เอาต์พุต                                                                                                               |
| **fontsLocation**  | สตริง | คิวรี                      | (ไม่บังคับ) ระบุฟอนต์ที่กำหนดเองหากจำเป็น                                                                                                         |
| **region**         | สตริง | คิวรี                      | (ไม่บังคับ) การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) ส่งผลต่อการจัดรูปแบบตัวเลข การแปลงวันที่ และพฤติกรรมเฉพาะพื้นที่ |
| **password**       | สตริง | คิวรี                      | (ไม่บังคับ) รหัสผ่านสำหรับการเข้าถึงไฟล์สเปรดชีต                                                                                        |

### **การตอบกลับ**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย               | คำอธิบาย                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | สำเร็จ (OK)                    | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request)           | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)      |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)          | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                                     |
| 413  | ข้อมูลส่งไปขนาดใหญ่เกินไป (Payload Too Large)     | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                 |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์                                          |

## **ควรใช้ API ส่งออกชีตงานเป็นรูปแบบอื่นในกรณีใด?**

- **การย้ายระบบเก่า** – แปลงไฟล์ XLS แบบเก่าหลายพันไฟล์เป็น XLSX เพื่อใช้กับระบบสมัยใหม่
- **การมาตรฐานการเก็บถาวร** – ทำให้รูปแบบสเปรดชีตต่างๆ (XLS, XLSM, ODS, CSV) เป็นรูปแบบเดียวสำหรับการจัดเก็บถาวร
- **ความเข้ากันได้ของชุดเครื่องมือสำนักงาน** – แปลงไฟล์ Excel ให้เป็นรูปแบบที่ใช้ได้กับ LibreOffice, Google Sheets หรือ Apple Numbers
- **การมาตรฐานแหล่งข้อมูล** – แปลงรูปแบบสเปรดชีตต่างๆ เป็น CSV หรือ JSON เพื่อใช้กับฐานข้อมูล
- **การเผยแพร่บนเว็บ** – แปลงแบบจำลองการเงินเป็น HTML เพื่อแสดงบนเว็บ

## เหตุใดจึงควรใช้ API ส่งออกชีตงานเป็นรูปแบบอื่น?

- **รองรับ SDK หลายภาษา** – มีไลบรารีไคลเอ็นต์สำหรับภาษาโปรแกรมหลายภาษา ช่วยให้นักพัฒนาสามารถเรียกใช้ API ได้โดยตรงจากสภาพแวดล้อมที่เลือก
- **การแปลงโดยตรงโดยไม่ต้องอัปโหลดขั้นกลาง** – อนุญาตให้แปลงชีตงานที่จัดเก็บไว้ในพื้นที่จัดเก็บคลาวด์เป็นรูปแบบที่ต้องการโดยไม่ต้องดาวน์โหลดและอัปโหลดไฟล์ซ้ำ
- **การดึงข้อมูลเท่านั้น** – ส่งคืนเนื้อหาของชีตงานในรูปแบบที่เลือกโดยไม่รักษาลักษณะการจัดรูปแบบ

## วิธีใช้ API ส่งออกชีตงานเป็นรูปแบบด้วย SDK?

### ข้อมูลจำเพาะของ API ส่งออกชีตงานเป็นรูปแบบ

[ข้อมูลจำเพาะของ API ส่งออกชีตงานเป็นรูปแบบ](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportWorksheetAsFormat) จัดเตรียมอินเทอร์เฟซโปรแกรมที่เข้าถึงได้สาธารณะสำหรับการโต้ตอบแบบ REST โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (เข้ารหัสแบบ Base64)",
  "contentType": "ประเภท MIME",
  "fileDownloadName": "ชื่อไฟล์ (ไม่บังคับ)"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจากซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถส่งออกชีตงานสเปรดชีตเป็นไฟล์รูปแบบได้ด้วยโค้ดสั้นๆ  
โปรดดูที่ [repository บน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportWorksheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportWorksheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportWorksheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportWorksheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportWorksheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportWorksheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportWorksheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportWorksheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}