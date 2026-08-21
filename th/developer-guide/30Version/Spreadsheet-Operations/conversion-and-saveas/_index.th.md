---
title: "แปลงไฟล์ Excel เป็นรูปแบบอื่นหรือบันทึกในรูปแบบที่ต่างกัน"
second_title: "เอกสาร"
linktitle: "การแปลงและการบันทึกเป็น"
type: docs
url: /conversion-and-save-as/
aliases: [/convert-excel/, /convert/]
keywords: "Aspose.Cells, API สำหรับการแปลง Excel, แปลง Excel เป็น PDF, Excel เป็น CSV, Excel เป็น JSON, การแปลงสเปรดชีตบนคลาวด์"
description: "เรียนรู้วิธีการแปลงสมุดงาน Excel เป็น PDF, CSV, JSON, HTML และรูปแบบอื่นๆ อีกมากกว่า 15 รูปแบบ โดยใช้ Aspose.Cells Cloud REST API พร้อมรายละเอียดของ endpoint ตัวอย่างคำสั่ง cURL และโค้ดตัวอย่าง SDK สำหรับ Java, .NET, Python และอื่นๆ"
weight: 30
ArticleTitle: "แปลงไฟล์ Excel เป็น PDF, CSV, JSON และอื่นๆ ด้วย Aspose.Cells Cloud"
---

หากคุณสร้างไฟล์ Excel ขึ้นมาในรูปแบบหนึ่งๆ ตั้งแต่ต้น—เช่น [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), หรือ [CSV](https://docs.fileformat.com/spreadsheet/csv/)—คุณอาจพบว่าการแปลงไฟล์ Excel ดังกล่าวเป็นรูปแบบอื่นมีประโยชน์ เพื่อใช้ประโยชน์จากคุณสมบัติพิเศษต่างๆ ตัวอย่างเช่น การแปลงไฟล์ Excel เป็น [PDF](https://docs.fileformat.com/pdf/) จะช่วยป้องกันเนื้อหาจากการถูกแก้ไขโดยบุคคลที่ไม่ได้รับอนุญาต และทำให้ง่ายต่อการอ่านและการแบ่งปัน

**ข้อกำหนดเบื้องต้น**  
ก่อนเรียกใช้ API สำหรับการแปลง คุณต้องขอโทเค็นการเข้าถึง OAuth 2.0 จาก Aspose Cloud และตรวจสอบให้แน่ใจว่าสมุดงานถูกจัดเก็บไว้ในพื้นที่จัดเก็บบนคลาวด์ของคุณ (หรือแนบมาในเนื้อหาคำขอสำหรับ endpoint การแปลงแบบ PUT)

การแปลงเอกสารเป็นกระบวนการที่ซับซ้อน มีหลายปัจจัยที่ส่งผลต่อความซับซ้อนของกระบวนการแปลง และควรพิจารณาอย่างรอบคอบระหว่างการแปลง การให้บริการแปลงระหว่างรูปแบบ Excel อย่างแม่นยำและมีคุณภาพระดับมืออาชีพนั้นถือเป็นคุณสมบัติสำคัญของ Aspose.Cells Cloud

บริการนี้สามารถทำงานได้อย่างลื่นไหลสำหรับการแปลงเอกสารทุกรูปแบบ คุณสามารถนำเข้าและส่งออกเอกสารในรูปแบบต่างๆ ดังนี้:

**รูปแบบที่รองรับ**  
- นำเข้า/ส่งออก: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/)
- ส่งออกเท่านั้น: [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/)

### API สำหรับการแปลง

| API                         | คำอธิบาย                                                                 |
| :-------------------------- | :---------------------------------------------------------------------- |
| `GET /cells/{name}`         | ดึงสมุดงาน Excel จากพื้นที่จัดเก็บบนคลาวด์และแปลงเป็นรูปแบบที่ร้องขอ     |
| `PUT /cells/convert`        | แปลงสมุดงาน Excel ที่ส่งมาในเนื้อหาคำขอให้อยู่ในรูปแบบเอาต์พุตที่กำหนด |
| `POST /cells/{name}/saveAs` | บันทึกสมุดงาน Excel ที่มีอยู่แล้วเป็นรูปแบบอื่นโดยตรงลงในพื้นที่จัดเก็บบนคลาวด์ |

**รายละเอียด API**

- **GET /cells/{name}**  
  - **พารามิเตอร์เส้นทาง (Path parameters):** `name` – ชื่อไฟล์สมุดงาน (จำเป็นต้องระบุ)  
  - **พารามิเตอร์คิวรี (Query parameters):** `format` – รูปแบบเป้าหมาย (เช่น pdf, csv, json); `storage` – ชื่อพื้นที่จัดเก็บบนคลาวด์ (ไม่บังคับ); `folder` – เส้นทางโฟลเดอร์ภายในพื้นที่จัดเก็บ (ไม่บังคับ)  
  - **คำตอบ (Response):** สตรีมไฟล์ของสมุดงานที่แปลงแล้ว; `Content‑Type` จะสอดคล้องกับรูปแบบเป้าหมาย  
  - **รหัสสถานะ (Status codes):** 200 OK, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error  

- **PUT /cells/convert**  
  - **เนื้อหาคำขอ (Request body):** multipart/form‑data ที่ประกอบด้วยไฟล์สมุดงานต้นทาง (`file`) และฟิลด์ที่จำเป็น `format` ซึ่งระบุรูปแบบเอาต์พุตที่ต้องการ  
  - **คำตอบ (Response):** สตรีมไบนารีของไฟล์ที่แปลงแล้ว  
  - **รหัสสถานะ (Status codes):** 200 OK, 400 Bad Request, 401 Unauthorized, 500 Internal Server Error  

- **POST /cells/{name}/saveAs**  
  - **พารามิเตอร์เส้นทาง (Path parameters):** `name` – ชื่อสมุดงานที่มีอยู่  
  - **พารามิเตอร์คิวรี (Query parameters):** `format` – รูปแบบเป้าหมาย; `outPath` – เส้นทางปลายทางในพื้นที่จัดเก็บบนคลาวด์ (ไม่บังคับ); `storage` – ชื่อพื้นที่จัดเก็บ (ไม่บังคับ)  
  - **คำตอบ (Response):** ออบเจกต์ JSON ที่ระบุผลลัพธ์ของการดำเนินการและเส้นทางของไฟล์ที่บันทึกไว้ ตัวอย่างคำตอบ:  

    ```json
    {
      "status": "OK",
      "code": 200,
      "message": "บันทึกไฟล์เรียบร้อยแล้ว",
      "path": "Converted/MyWorkbook.pdf"
    }
    ```  

  - **รหัสสถานะ (Status codes):** 200 OK, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error  

**ตัวอย่าง cURL สำหรับการแปลงเป็น PDF**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx?format=pdf" \
  -H "Authorization: Bearer {access_token}" \
  -o MyWorkbook.pdf
```

**โค้ดตัวอย่าง SDK ภาษา Java (GET /cells/{name})**

```java
CellsApi apiInstance = new CellsApi();
String name = "MyWorkbook.xlsx";
String format = "pdf";
File result = apiInstance.cellsGetWorkbook(name, format, null, null);
result.renameTo(new File("MyWorkbook.pdf"));
```

**โค้ดตัวอย่าง SDK ภาษา .NET (PUT /cells/convert)**

```csharp
var api = new CellsApi();
var file = File.ReadAllBytes("MyWorkbook.xlsx");
var format = "pdf";
var result = api.ConvertWorkbook(new MemoryStream(file), format);
File.WriteAllBytes("MyWorkbook.pdf", result);
```

**โค้ดตัวอย่าง SDK ภาษา Python (POST /cells/{name}/saveAs)**

```python
import asposecellscloud
api = asposecellscloud.CellsApi()
api.post_save_as(name="MyWorkbook.xlsx", format="pdf", out_path="Converted/MyWorkbook.pdf")
```

บทความต่อไปนี้อธิบายแต่ละ API อย่างละเอียด และรวมตัวอย่าง cURL และ SDK เพิ่มเติม:

- [แปลงไฟล์ Excel เป็นรูปแบบอื่น](/cells/convert-an-excel-file-to-different-formats)
- [บันทึกไฟล์ Excel เป็นรูปแบบอื่น](/cells/save-an-excel-file-as-other-formats-files)
- [แปลงไฟล์ Excel เป็นไฟล์ CSV](/cells/convert-excel-file-to-csv-file)
- [แปลงไฟล์ Excel เป็นไฟล์ DOCX](/cells/convert-excel-file-to-docx-file)
- [แปลงไฟล์ Excel เป็นไฟล์ HTML](/cells/convert-excel-file-to-html-file)
- [แปลงไฟล์ Excel เป็นไฟล์ JSON](/cells/convert-excel-file-to-json-file)
- [แปลงไฟล์ Excel เป็นไฟล์ Markdown](/cells/convert-excel-file-to-markdown-file)
- [แปลงไฟล์ Excel เป็นไฟล์ PDF](/cells/convert-excel-file-to-pdf-file)
- [แปลงไฟล์ Excel เป็นไฟล์ PNG](/cells/convert-excel-file-to-png-file)
- [แปลงไฟล์ Excel เป็นไฟล์ PPTX](/cells/convert-excel-file-to-pptx-file)
- [แปลงไฟล์ Excel เป็นไฟล์ SQL](/cells/convert-excel-file-to-sql-file)
- [แปลงไฟล์ Excel เป็นไฟล์ TIFF](/cells/convert-excel-file-to-tiff-file)
---