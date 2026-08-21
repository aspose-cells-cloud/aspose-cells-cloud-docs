---
title: "แปลงเวิร์กชีตเป็น CSV – เอกสารประกอบ API ของ Aspose.Cells Cloud"
second_title: "เอกสาร"
ArticleTitle: "วิธีการแปลงเวิร์กชีตในไฟล์สเปรดชีตเป็น CSV โดยใช้ Aspose.Cells Cloud API"
linktype: "แปลงเวิร์กชีตเป็น CSV"
type: docs
url: /convert-worksheet-to-csv/
keywords: "Aspose.Cells, การแปลง CSV, การแปลงเวิร์กชีตเป็น CSV, REST API, สเปรดชีตบนคลาวด์, Excel เป็น CSV"
description: "เรียนรู้วิธีการแปลงเวิร์กชีตที่ระบุจากไฟล์ Excel เป็น CSV โดยใช้ Aspose.Cells Cloud API (v4.0) ได้แก่ endpoint, พารามิเตอร์, ตัวอย่าง cURL, โค้ด SDK และการจัดการข้อผิดพลาด"
weight: 100
---

**ConvertWorksheetToCsv** endpoint แปลงเวิร์กชีตเดียวจากไฟล์สเปรดชีตในเครื่องให้เป็นเอกสาร CSV ทั้งหมดบนเซิร์ฟเวอร์ของ Aspose.Cells Cloud โดยผู้ใช้เพียงอัปโหลดไฟล์ต้นฉบับและระบุชื่อเวิร์กชีตที่ต้องการแปลง เท่านั้นจึงจะได้รับสตรีมไบนารีของ CSV โดยไม่จำเป็นต้องจัดเก็บไฟล์ไว้ในพื้นที่จัดเก็บบนคลาวด์ ซึ่ง API นี้เหมาะสำหรับการใช้ในการดึงข้อมูลอัตโนมัติ ผสานข้อมูลจากสเปรดชีตเข้ากับระบบย่อย และลดภาระการจัดเก็บข้อมูล

## API สำหรับการแปลงเวิร์กชีตเป็น CSV

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/csv
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

```bash
-H "Authorization: Bearer {access_token}"
```

### พารามิเตอร์ของ Request

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | จำเป็น/ไม่จำเป็น | คำอธิบาย |
| :------------- | :----- | :------- | :---------------- | :------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet    | ไฟล์   | FormData | **จำเป็น**      | ไฟล์ไบนารีของสเปรดชีตต้นฉบับ (เช่น `.xlsx`, `.xls`) ตัวอย่าง: `myWorkbook.xlsx` |
| worksheet      | สตริง | Query    | **จำเป็น**      | ชื่อเวิร์กชีตที่ต้องการแปลง (แยกแยะตัวพิมพ์เล็ก-ใหญ่) หากไม่ระบุ จะใช้เวิร์กชีตแรก |
| outPath        | สตริง | Query    | ไม่จำเป็น          | เส้นทางโฟลเดอร์เป้าหมายในพื้นที่จัดเก็บบนคลาวด์ที่จะบันทึกไฟล์ CSV ที่สร้างขึ้น หากไม่ระบุ CSV จะถูกส่งกลับในสตรีมของ response |
| outStorageName | สตริง | Query    | ไม่จำเป็น          | ชื่อของบริการจัดเก็บข้อมูล (เช่น Azure, AWS S3) ที่จะใช้บันทึกไฟล์ผลลัพธ์ ต้องระบุเมื่อใช้ `outPath` เท่านั้น |
| fontsLocation  | สตริง | Query    | ไม่จำเป็น          | เส้นทางไปยังโฟลเดอร์ฟอนต์ที่กำหนดเองบนเซิร์ฟเวอร์ ซึ่งช่วยให้เครื่องมือแปลงสามารถใช้ฟอนต์ที่ไม่เป็นมาตรฐานได้ |
| region         | สตริง | Query    | ไม่จำเป็น          | ตัวระบุภาษาและภูมิภาคที่ส่งผลต่อรูปแบบตัวเลข/วันที่ใน CSV (เช่น `en-US`, `fr-FR`) |
| password       | สตริง | Query    | ไม่จำเป็น          | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีตที่มีการป้องกัน โดยต้องตรงกับรหัสผ่านที่ใช้ในการเข้ารหัสไฟล์ต้นฉบับ |

### Response

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

**รหัสสถานะ HTTP**

| รหัส | ความหมาย               | คำอธิบาย |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | ดำเนินการกรองสำเร็จ; response ประกอบด้วยรายละเอียดของกระบวนการ |
| 400  | Bad Request           | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401  | Unauthorized          | JWT token ไม่ถูกต้องหรือขาดหาย |
| 413  | Payload Too Large     | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | Internal Server Error | เกิดข้อผิดพลาดภายในเซิร์ฟเวอร์ที่ไม่คาดคิด |

## ควรใช้ API แปลงเวิร์กชีตเป็น CSV เมื่อใด?

- **การดึงข้อมูลเพื่อใช้ใน pipeline ของ BI** – ดึงเวิร์กชีตที่ระบุจากรายงาน Excel และส่ง CSV ที่ได้ไปยัง Power BI หรือ Tableau โดยไม่ต้องจัดการไฟล์ขั้นกลาง
- **การประมวลผลใบแจ้งหนี้อัตโนมัติ** – แปลงเวิร์กชีตที่มีแถวข้อมูลของใบแจ้งหนี้เป็น CSV เพื่อนำเข้าสู่ระบบบัญชีอย่างรวดเร็ว
- **การผสานกับระบบเดิม** – ส่งออกข้อมูลเวิร์กชีตเป็น CSV เพื่อให้แอปพลิเคชันเก่าที่รับเฉพาะไฟล์ข้อความแบบมี delimiter สามารถใช้งานได้
- **การสร้างรายงานแบบเรียลไทม์** – สร้างภาพ CSV ของข้อมูลสเปรดชีตแบบสดในเว็บเซอร์วิส และส่งกลับไฟล์ให้เบราว์เซอร์ของผู้ใช้ทันที

## เหตุใดจึงควรใช้ API แปลงเวิร์กชีตเป็น CSV?

- **ไม่จำเป็นต้องมีพื้นที่จัดเก็บบนคลาวด์ถาวร** – ไฟล์จะถูกส่งผ่านไปยังเครื่องมือแปลงโดยตรงและถูกลบหลังการแปลง ช่วยประหยัดแบนด์วิดท์และค่าใช้จ่ายในการจัดเก็บ
- **ประมวลผลบนคลาวด์ด้วยประสิทธิภาพสูง** – การแปลงดำเนินการบนเซิร์ฟเวอร์ที่ได้รับการปรับแต่งของ Aspose โดยปกติแล้วจะเสร็จภายใน 2 วินาทีสำหรับไฟล์ขนาดไม่เกิน 100 MB
- **ควบคุมได้อย่างละเอียด** – เลือกเวิร์กชีตเดียว ใช้ฟอนต์ที่กำหนดเอง ตั้งค่ารูปแบบตามภูมิภาค และการป้องกันด้วยรหัสผ่านในคำขอเดียว
- **ผลลัพธ์ CSV ที่สม่ำเสมอข้านแพลตฟอร์ม** – รับประกันว่าไฟล์ CSV ที่ได้มีเนื้อหาเท่ากันทุกครั้งไม่ว่าจะใช้ SDK บน .NET, Java, Python หรืออื่นๆ ที่เรียกผ่าน endpoint เดียวกัน

## วิธีการใช้ API แปลงเวิร์กชีตเป็น CSV ร่วมกับ SDKs

### ข้อกำหนด API สำหรับการแปลงเวิร์กชีตเป็น CSV

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToCsv" target="_blank" rel="noopener noreferrer">ข้อกำหนด API สำหรับการแปลงเวิร์กชีตเป็น CSV</a> จัดเตรียมอินเทอร์เฟซโปรแกรมที่เปิดให้เข้าถึงได้ เพื่อให้สามารถเรียกใช้งาน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/image?format=png&worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.png
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

การใช้ SDK จะช่วยลดความซับซ้อนในการพัฒนาด้วยการซ่อนรายละเอียดระดับต่ำ ช่วยให้คุณผสานสเปรดชีตเข้ากับอีกไฟล์หนึ่งได้ด้วยโค้ดที่กระชับ โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToCsv.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToCsv.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToCsv.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToCsv.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToCsv.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToCsv.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToCsv.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToCsv.go" >}}  
{{</tab>}}  
{{< /tabs >}}