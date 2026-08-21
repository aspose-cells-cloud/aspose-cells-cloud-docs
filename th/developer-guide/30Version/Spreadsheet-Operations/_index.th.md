---
title: "การดำเนินการกับสเปรดชีต"
second title: "เอกสาร"
type: docs
url: /th/spreadsheet-operations/
keywords: "Aspose Cells Cloud, Excel API, การดำเนินการกับสเปรดชีต, การปรับขนาดอัตโนมัติ, การประมวลผลแบบแบตช์, การป้องกันไฟล์, การแปลงรูปแบบ, การนำเข้า/ส่งออก, การประมวลผลข้อความ"
description: "เรียนรู้วิธีการดำเนินการกับสเปรดชีต เช่น การปรับขนาดอัตโนมัติ การแปลงไฟล์แบบแบตช์ การป้องกัน การรวม และการค้นหา-แทนที่ โดยใช้ REST API ของ Aspose.Cells Cloud รวมคำอธิบายการใช้งานแบบสั้นและคำแนะนำสำหรับตัวอย่างโค้ด"
weight: 100
ArticleTitle: "การดำเนินการกับสเปรดชีต – คู่มือ API ของ Aspose.Cells Cloud"
---

การดำเนินการกับสเปรดชีตมีคำแนะนำแบบกระชับเกี่ยวกับการทำงานทั่วไปที่คุณสามารถทำได้กับสมุดงาน Excel โดยใช้ **Aspose.Cells Cloud** (เวอร์ชัน 3.0) ไม่ว่าคุณจะต้องการปรับความกว้างคอลัมน์อัตโนมัติ ประมวลผลไฟล์จำนวนมากในครั้งเดียว ป้องกันเวิร์กชีต หรือจัดการข้อความ REST API มีเอนด์พอยต์เฉพาะสำหรับแต่ละการทำงานที่รองรับภาษาต่างๆ เช่น Python, C# และ Java รายชื่อด้านล่างนี้เชื่อมโยงไปยังเอกสารประกอบโดยละเอียดของแต่ละการทำงาน พร้อมคำอธิบายการใช้งานสั้นๆ เพื่อช่วยให้คุณเริ่มต้นได้อย่างรวดเร็ว

**ข้อกำหนดเบื้องต้น**: เพื่อเรียกใช้เอนด์พอยต์เหล่านี้ คุณต้องมีคีย์ API ของ Aspose.Cells Cloud ที่ใช้งานได้ และต้องใส่เฮดเดอร์ `Authorization` (รูปแบบ `Bearer <access-token>`) ตัวอย่างที่ให้มาอ้างอิงกับเวอร์ชัน API v3.0

- **[ตัวเลือกการปรับขนาดอัตโนมัติ](/cells/auto-fitter-options/)** – ปรับความกว้างคอลัมน์และส่วนสูงของแถวโดยอัตโนมัติ `POST /cells/{file}/worksheets/{sheet}/autoFitColumns`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/autoFitColumns
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "autoFitOptions": {
      "autoFitType": "All",
      "autoFitMergedCells": true
    }
  }
  ```
- **[การประมวลผลแบบแบตช์ของไฟล์ Excel: การแปลงรูปแบบ การล็อก การป้องกัน การแยก และการปลดล็อก](/cells/batch/)** – ดำเนินการแบบหลายไฟล์ (แปลงรูปแบบ ล็อก ป้องกัน แยก และปลดล็อก) ได้สูงสุด 100 ไฟล์ต่อคำขอ `POST /cells/batch`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/batch
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "tasks": [
      { "file": "Book1.xlsx", "action": "convert", "format": "pdf" },
      { "file": "Book2.xlsx", "action": "protect", "password": "Secret123" }
    ]
  }
  ```
- **[บีบอัดและซ่อมแซมไฟล์ Excel](/cells/compress-and-repair-excel-files/)** – ลดขนาดไฟล์และแก้ไขปัญหาด้านโครงสร้าง `POST /cells/{file}/compressAndRepair`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Report.xlsx/compressAndRepair
  Authorization: Bearer {access-token}
  ```
- **[แปลงไฟล์ Excel เป็นรูปแบบอื่น หรือบันทึกในรูปแบบต่างๆ](/cells/conversion-and-save-as/)** – แปลง Excel เป็น PDF, CSV, HTML เป็นต้น หรือเปลี่ยนรูปแบบผลลัพธ์ `GET /cells/{file}/saveAs`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Financials.xlsx/saveAs?format=pdf
  Authorization: Bearer {access-token}
  ```
- **[ตัวเลือกการแปลงสมุดงาน](/cells/convert-workbook-options/)** – ปรับแต่งการตั้งค่าการแปลง เช่น ขนาดหน้า ตัวเลือกการเรนเดอร์ และการป้องกันด้วยรหัสผ่าน `POST /cells/{file}/convert`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/convert
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "format": "pdf",
    "options": {
      "pageSetup": { "orientation": "landscape" },
      "pdfSaveOptions": { "compressImages": true }
    }
  }
  ```
- **[สร้างไฟล์ Excel หรือสร้างรายงาน Excel](/cells/creating-files-and-reports/)** – สร้างสมุดงานใหม่ตั้งแต่เริ่มต้น หรือจากเทมเพลต `PUT /cells/{newFile}`  
  ```http
  PUT https://api.aspose.cloud/v3.0/cells/NewReport.xlsx
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "templateFile": "Template.xlsx",
    "dataSource": { "name": "Q1 Sales", "value": 12345 }
  }
  ```
- **[นำเข้าข้อมูลสู่ไฟล์ Excel และส่งออกข้อมูลจากไฟล์ Excel](/cells/data-import-and-export/)** – โหลดข้อมูลจาก CSV, JSON หรือฐานข้อมูล และส่งออกข้อมูลจากเวิร์กชีต `POST /cells/{file}/importData`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Orders.xlsx/importData
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "importOptions": {
      "source": "json",
      "jsonData": [{ "OrderId": 1, "Amount": 250.0 }]
    }
  }
  ```
- **[เข้ารหัส ถอดรหัส และลงลายมือชื่อดิจิทัลไฟล์ Excel](/cells/protect/)** – ใช้การป้องกันด้วยรหัสผ่าน การเข้ารหัส หรือลายมือชื่อดิจิทัล `POST /cells/{file}/encrypt`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Sensitive.xlsx/encrypt
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "password": "StrongPass!23",
    "encryptionType": "Standard"
  }
  ```
- **[ข้อมูลไฟล์](/cells/file-info/)** – รับข้อมูลเมตา เช่น ขนาด รูปแบบ และวันที่สร้าง `GET /cells/{file}/info`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Archive.xlsx/info
  Authorization: Bearer {access-token}
  ```
- **[รวมและแยกไฟล์ Excel](/cells/merge-and-split/)** – รวมสมุดงานหลายไฟล์เป็นไฟล์เดียว หรือแยกสมุดงานเป็นไฟล์ย่อยๆ `POST /cells/merge` / `POST /cells/split`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/merge
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "files": ["Q1.xlsx", "Q2.xlsx"],
    "outputFile": "FullYear.xlsx"
  }
  ```
- **[ค้นหาและแทนที่เนื้อหาข้อความในไฟล์ Excel](/cells/search-and-replace/)** – ค้นหาและแทนที่สตริงในเวิร์กชีตต่างๆ `POST /cells/{file}/searchReplace`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Report.xlsx/searchReplace
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "text": "Draft",
    "newText": "Final",
    "options": { "matchCase": false }
  }
  ```
- **[การประมวลผลข้อความใน Excel: เพิ่มข้อความ ลบอักขระ ตัดช่องว่าง แก้ไขรูปแบบตัวพิมพ์ใหญ่-เล็ก และอื่นๆ](/cells/text-processing/)** – ดำเนินการจัดการข้อความขั้นสูงกับค่าของเซลล์ `POST /cells/{file}/textProcessing`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Notes.xlsx/textProcessing
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "operations": [
      { "type": "trim", "range": "A1:A10" },
      { "type": "toUpper", "range": "B1:B5" }
    ]
  }
  ```
- **[ใส่ลายน้ำหรือตั้งค่าพื้นหลังในไฟล์ Excel](/cells/watermark-and-background/)** – เพิ่มลายน้ำแบบรูปภาพหรือข้อความ และตั้งค่าพื้นหลังของเวิร์กชีต `POST /cells/{file}/watermark`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/watermark
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "type": "text",
    "text": "Confidential",
    "fontSize": 36,
    "color": "FF0000"
  }
  ```
- **[การทำงานกับไฟล์ Excel: การคำนวณสูตร การปรับขนาดอัตโนมัติ การล้างวัตถุ เป็นต้น](/cells/workbook/)** – ดำเนินงานสมุดงานทั่วไป เช่น การคำนวณสูตร การล้างวัตถุ และการปรับขนาดอัตโนมัติ `POST /cells/{file}/workbookOperations`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Analytics.xlsx/workbookOperations
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "operations": [
      { "type": "calculateFormula" },
      { "type": "clearObjects", "objectType": "charts" }
    ]
  }
  ```