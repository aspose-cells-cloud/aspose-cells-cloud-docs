---
title: "Aspose.Cells Cloud Web API – แปลงสเปรดชีตเป็น PDF"
second title: "เอกสาร"
ArticleTitle: "วิธีการแปลงสเปรดชีตในเครื่องเป็น PDF โดยใช้ Aspose.Cells Cloud API"
linktitle: "แปลงสเปรดชีตเป็น PDF"
type: docs
url: /th/convert-spreadsheet-to-pdf/
keywords: "Aspose.Cells Cloud, แปลงสเปรดชีตเป็น PDF, การแปลง Excel, cloud API, การสร้าง PDF, REST API, v4.0"
description: "คู่มือทีละขั้นตอนในการแปลงสเปรดชีตในเครื่องเป็น PDF โดยใช้ Aspose.Cells Cloud API ประกอบด้วยไวยากรณ์ของคำขอ พารามิเตอร์ รายละเอียดของคำตอบ การจัดการข้อผิดพลาด และตัวอย่างการใช้งานจริง"
weight: 100
---

ปลายทาง **ConvertSpreadsheetToPdf** รับไฟล์สเปรดชีตที่อัปโหลดจากไดรฟ์ในเครื่อง ประมวลผลไฟล์บนเซิร์ฟเวอร์ของ Aspose.Cells Cloud และส่งคืนเอกสาร PDF ที่ได้เป็นสตรีมไบนารี การแปลงแบบเน็ตเวิร์กคลาวด์นี้ช่วยลดความจำเป็นในการอัปโหลดไฟล์ต้นฉบับไปยังพื้นที่จัดเก็บ ลดการใช้ทรัพยากร และทำให้กระบวนการทำงานง่ายขึ้นโดยส่งคืน PDF ตรงไปยังไคลเอนต์ รูปแบบที่รองรับขึ้นอยู่กับไลบรารีที่ใช้เบื้องหลัง; API จะตรวจสอบความมีอยู่ของไฟล์ สิทธิ์การเข้าถึง และความสมบูรณ์ของการแปลง แล้วส่งโค้ดข้อผิดพลาด HTTP ที่เหมาะสมเมื่อพบข้อมูลนำเข้าไม่ถูกต้องหรือเกิดข้อผิดพลาดระหว่างการประมวลผล

## **Convert Spreadsheet To Pdf API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

### **พารามิเตอร์ของคำขอ:**

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | จำเป็น/ไม่จำเป็น | คำอธิบาย                                                                                                                                                                                    |
| :------------- | :----- | :------- | :---------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | ไฟล์   | FormData | จำเป็น          | ไฟล์สเปรดชีตต้นฉบับ (XLS, XLSX, CSV เป็นต้น) ที่ต้องการแปลง ต้องเป็นไฟล์ที่ถูกต้องและอ่านได้ ขนาดสูงสุดคือ 100 MB ตัวอย่าง: `myWorkbook.xlsx`                                        |
| outPath        | สตริง | Query    | ไม่จำเป็น          | เส้นทางไปยังโฟลเดอร์ปลายทางที่จะเก็บไฟล์ PDF ที่แปลงแล้วบนเซิร์ฟเวอร์ (ถ้าต้องการบันทึกไว้) หากไม่ระบุ ไฟล์จะถูกส่งคืนโดยตรงในส่วนของคำตอบ ตัวอย่าง: `/output/reports/` |
| outStorageName | สตริง | Query    | ไม่จำเป็น          | ชื่อของบริการพื้นที่จัดเก็บเป้าหมาย (เช่น `MyCloudStorage`) ใช้เมื่อระบุ `outPath` และพื้นที่จัดเก็บไม่ใช่ค่าเริ่มต้น                                                          |
| fontsLocation  | สตริง | Query    | ไม่จำเป็น          | เส้นทางไปยังโฟลเดอร์ฟอนต์แบบกำหนดเองบนเซิร์ฟเวอร์ เพื่อให้การแสดงผลข้อความใน PDF เป็นไปอย่างถูกต้อง ตัวอย่าง: `/fonts/custom/`                                                                             |
| region         | สตริง | Query    | ไม่จำเป็น          | การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) มีผลต่อการจัดรูปแบบตัวเลข การประมวลผลวันที่ และพฤติกรรมเฉพาะของท้องถิ่น                                                        |
| password       | สตริง | Query    | ไม่จำเป็น          | รหัสผ่านที่จำเป็นสำหรับการเปิดสเปรดชีตที่มีการป้องกัน ไม่ต้องระบุหากไฟล์ไม่ได้เข้ารหัส                                                                                                          |

### **คำตอบ**

คำตอบที่สำเร็จ (200 OK)  
Content-Type: application/pdf  
Content‑Disposition: attachment; filename="converted.pdf"  
Content‑Length: `<ขนาดเป็นไบต์>`

ส่วนเนื้อหา: สตรีมไบนารีของไฟล์ PDF ที่สร้างขึ้น

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย               | คำอธิบาย                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | ใช้ตัวกรองสำเร็จ; คำตอบประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | Bad Request           | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น รูปแบบไฟล์ที่ไม่รองรับ)      |
| 401  | Unauthorized          | JWT token ไม่ถูกต้องหรือขาดหาย                                     |
| 413  | Payload Too Large     | ไฟล์ที่อัปโหลดเกินขีดจำกัดขนาด                                     |
| 500  | Internal Server Error | เกิดข้อผิดพลาดของเซิร์ฟเวอร์โดยไม่คาดคิด                                          |

## ควรใช้ Convert Spreadsheet To Pdf API ในกรณีใดบ้าง?

- **ระบบการสร้างรายงานอัตโนมัติ** – แปลงรายงาน Excel ที่สร้างทุกวันเป็น PDF เพื่อเก็บถาวรหรือส่งทางอีเมล โดยไม่ต้องทำด้วยมือ
- **ระบบจัดการเอกสาร** – จัดเก็บไฟล์ PDF โดยตรงในระบบจัดการเอกสาร (DMS) หลังการแปลง โดยเก็บสเปรดชีตต้นฉบับไว้เฉพาะที่ฝั่งไคลเอนต์
- **แอปพลิเคชันเว็บที่ส่งออกแบบเรียลไทม์** – อนุญาตให้ผู้ใช้สุดปลายดาวน์โหลดไฟล์ PDF ของสเปรดชีตที่แก้ไขในเบราว์เซอร์ โดยใช้การแปลงบนคลาวด์เพื่อรักษาเค้าโครงให้สมบูรณ์
- **การปฏิบัติตามข้อบังคับ** – สร้างภาพถ่าย PDF แบบคงที่ของสเปรดชีตทางการเงินเพื่อใช้เป็นหลักฐานการตรวจสอบ โดยรับประกันว่าไฟล์ต้นฉบับไม่เคยออกจากสภาพแวดล้อมของไคลเอนต์
- **กระบวนการทำงานแปลงข้ามรูปแบบ** – ผนวกเข้ากับปลายทางการแปลงอื่นๆ เช่น [Convert Spreadsheet to CSV](/convert-spreadsheet-to-csv/) API เพื่อสร้างการเก็บถาวรหลายรูปแบบ

## เหตุใดจึงควรใช้ Convert Spreadsheet To Pdf API?

- **กระบวนการทำงานแบบไม่ต้องอัปโหลด** – ไม่จำเป็นต้องอัปโหลดไฟล์ต้นฉบับไปยังพื้นที่จัดเก็บบนคลาวด์ การแปลงเกิดขึ้นโดยตรงจากสตรีมที่อัปโหลด ช่วยประหยัดแบนด์วิดท์และค่าใช้จ่ายในการจัดเก็บ
- **การแสดงผลที่แม่นยำ** – Aspose.Cells รักษาสูตร แผนภูมิ และรูปแบบที่ซับซ้อนไว้เมื่อแปลงเป็น PDF ให้เทียบเท่ากับผลลัพธ์จาก Excel บนเดสก์ท็อป
- **การประมวลผลบนคลาวด์ที่ปรับขนาดได้** – ใช้โครงสร้างพื้นฐานบนคลาวด์ของ Aspose สำหรับการแปลงที่รวดเร็วและเชื่อถือได้ ไม่ว่าฮาร์ดแวร์ของไคลเอนต์จะเป็นอย่างไร
- **อินเทอร์เฟซ REST ที่เรียบง่าย** – มีคำสั่ง `PUT` คำเดียวพร้อมพารามิเตอร์ query ที่เลือกได้; ส่งคืนสตรีม PDF ที่พร้อมดาวน์โหลด ทำให้การบูรณาการเป็นเรื่องง่ายในทุกภาษา

## วิธีการใช้ Convert Spreadsheet To Pdf API ร่วมกับ SDKs

### ข้อมูลจำเพาะของ Convert Spreadsheet To Pdf API

[ข้อมูลจำเพาะของ Convert Spreadsheet To Pdf API](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/ConversionController/ConvertSpreadsheetToPdf) ให้อินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้สาธารณะสำหรับดำเนินการ REST interactions โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL บรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="คำตอบ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.pdf
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "MIME type",
  "fileDownloadName": "optional file name"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจากซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถผสานสเปรดชีตเข้าด้วยกันได้ด้วยโค้ดเพียงไม่กี่บรรทัด โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการโต้ตอบกับบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToPdf.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToPdf.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToPdf.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToPdf.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToPdf.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToPdf.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToPdf.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToPdf.go" >}}
{{</tab>}}
{{< /tabs >}}