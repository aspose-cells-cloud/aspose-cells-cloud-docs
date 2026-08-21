---
title: "Aspose.Cells Cloud Web API - การส่งออกแผ่นงาน Excel ระยะไกลไปยังรูปแบบอื่นๆ - เครื่องมือออนไลน์ฟรี"
second_title: "เอกสาร"
ArticleTitle: "วิธีส่งออกแผ่นงานสเปรดชีตระยะไกลไปยังรูปแบบอื่นๆ: คู่มือแบบทีละขั้นตอน"
linktitle: "ส่งออกสเปรดชีตเป็นรูปแบบ"
type: docs
url: /export-spreadsheet-as-format/
keywords: "Aspose.Cells, การแปลงสเปรดชีต, API, ส่งออก, PDF, CSV, JSON, XLSX"
description: "แปลงสมุดงาน Excel ที่จัดเก็บไว้ใน Aspose Cloud เป็นรูปแบบ PDF, XLSX, CSV, JSON หรือ HTML ผ่านจุดปลายทาง REST เดียว เรียนรู้ไวยากรณ์คำขอ พารามิเตอร์ และตัวอย่าง SDK ใน C#, Java, Python และอื่นๆ"
weight: 100
---

ส่งออกสเปรดชีต (Excel) บนคลาวด์ไปยังรูปแบบไฟล์อื่น

## **API ส่งออกสเปรดชีตเป็นรูปแบบ**

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}?format={format}&folder={folder}&storageName={storageName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}
```

### **ความปลอดภัยและการรับรองความถูกต้อง**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การรับรองความถูกต้องแบบ JWT token</a>

### **พารามิเตอร์คำขอ:**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | Path/Query String/HTTP Body | คำอธิบาย                                                                                                                                        |
| :------------- | :----- | :-------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String | Path                        | (จำเป็น) ชื่อไฟล์สมุดงานที่ต้องการเรียกคืน                                                                                          |
| format         | String | Query                       | (จำเป็น) รูปแบบผลลัพธ์ที่ต้องการ (เช่น “Xlsx”, “PDF”, “CSV”)                                                                                 |
| folder         | String | Query                       | (ไม่บังคับ) เส้นทางโฟลเดอร์ที่จัดเก็บสมุดงาน ค่าเริ่มต้นคือ null                                                                      |
| storageName    | String | Query                       | (ไม่บังคับ) ชื่อพื้นที่จัดเก็บเมื่อใช้คลาวด์สตอเรจแบบกำหนดเอง ใช้พื้นที่จัดเก็บเริ่มต้นหากไม่ระบุ                                                  |
| outPath        | String | Query                       | (ไม่บังคับ) เส้นทางโฟลเดอร์ที่จะจัดเก็บสมุดงาน ค่าเริ่มต้นคือ null                                                                 |
| outStorageName | String | Query                       | (ไม่บังคับ) ชื่อพื้นที่จัดเก็บไฟล์ผลลัพธ์                                                                                                               |
| fontsLocation  | String | Query                       | (ไม่บังคับ) ตำแหน่งฟอนต์แบบกำหนดเอง                                                                                                                  |
| region         | String | Query                       | (ไม่บังคับ) การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) มีผลต่อการจัดรูปแบบตัวเลข การแยกวิเคราะห์วันที่ และพฤติกรรมเฉพาะของภูมิภาค |
| password       | String | Query                       | (ไม่บังคับ) รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต                                                                                          |

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

การตอบกลับจะมีวัตถุเดียวซึ่งแสดงสตรีมไฟล์ที่แปลงแล้ว

**รหัสสถานะ HTTP**

| รหัส | ความหมาย               | คำอธิบาย                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดการดำเนินการ |
| 400  | Bad Request           | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)      |
| 401  | Unauthorized          | JWT token ไม่ถูกต้องหรือขาดหาย                                     |
| 413  | Payload Too Large     | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                 |
| 500  | Internal Server Error | เกิดข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด                                          |

## คุณควรใช้ API ส่งออกสเปรดชีตเป็นรูปแบบอื่นในกรณีใด?

- **การย้ายระบบเดิม**: แปลงไฟล์ XLS เดิมหลายพันไฟล์เป็น XLSX สำหรับระบบสมัยใหม่
- **การมาตรฐานการจัดเก็บข้อมูล**: ปรับรูปแบบสเปรดชีตต่างๆ (XLS, XLSM, ODS, CSV) ให้เป็นรูปแบบเดียวสำหรับการจัดเก็บถาวร
- **การรองรับระบบสูตรการใช้งานสำนักงาน**: แปลงไฟล์ Excel เป็นรูปแบบที่ใช้ได้กับ LibreOffice, Google Sheets หรือ Apple Numbers
- **การมาตรฐานแหล่งข้อมูล**: แปลงสเปรดชีตรูปแบบต่างๆ เป็น CSV หรือ JSON เพื่อนำเข้าสู่ฐานข้อมูล
- **การเผยแพร่บนเว็บ**: แปลงแบบจำลองทางการเงินเป็น HTML เพื่อแสดงผลบนเว็บ

## คุณควรใช้ API ส่งออกสเปรดชีตเป็นรูปแบบอื่นเพราะเหตุใด?

- **เป็นมิตรกับนักพัฒนา**: Aspose.Cells Cloud มี SDK สำหรับภาษาต่างๆ หลายภาษา ช่วยให้การพัฒนาทำได้อย่างรวดเร็ว และมีเอกสารประกอบอย่างครบถ้วน เมื่อเทียบกับการสร้างโซลูชันการเรนเดอร์กราฟิกแบบกำหนดเอง วิธีนี้ช่วยลดภาระงานพัฒนาอย่างมาก
- **ลดต้นทุนแรงงาน**: ลดความจำเป็นในการจัดตำแหน่งงานเฉพาะสำหรับการรวมเอกสาร
- **จ่ายตามการใช้งาน**: ไม่ต้องลงทุนล่วงหน้า; คุณจ่ายเฉพาะสำหรับคำขอ API ที่ใช้งานจริงเท่านั้น
- **ไม่ต้องดูแลรักษาเซิร์ฟเวอร์ฝั่งผู้ให้บริการ**: ไม่จำเป็นต้องดูแลเซิร์ฟเวอร์ อัปเดตซอฟต์แวร์ หรือจัดการปัญหาความเข้ากันได้
- **รองรับรูปแบบอย่างครบถ้วน**: แปลงระหว่างสเปรดชีตรูปแบบต่างๆ มากกว่า 20 รูปแบบ
- **คงความถูกต้องของข้อมูลและการจัดรูปแบบเดิม**: รักษาโครงสร้าง ฟอร์มูล่า และสไตล์ดั้งเดิมไว้ระหว่างการแปลง

## วิธีใช้ API ส่งออกสเปรดชีตเป็นรูปแบบด้วย SDK?

### ข้อมูลจำเพาะ API ส่งออกสเปรดชีตเป็นรูปแบบ

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportSpreadsheetAsFormat" rel="noopener noreferrer">ข้อมูลจำเพาะ API ส่งออกสเปรดชีตเป็นรูปแบบ</a> มีอินเทอร์เฟซโปรแกรมที่เข้าถึงได้สาธารณะ เพื่อปฏิบัติการ REST อย่างราบรื่น

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง cURL เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (เข้ารหัส Base64)",
  "contentType": "MIME type",
  "fileDownloadName": "ชื่อไฟล์ (ไม่บังคับ)"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจาก SDK ซ่อนรายละเอียดระดับต่ำไว้ ช่วยให้คุณส่งออกสเปรดชีตเป็นไฟล์รูปแบบด้วยโค้ดที่สั้นกระชับ  
ก่อนเรียกใช้ API ให้รับ OAuth 2.0 access token และใส่ไว้ในส่วนหัว `Authorization: Bearer <token>`

โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีโต้ตอบกับบริการเว็บของ Aspose.Cells ผ่าน SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportSpreadsheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportSpreadsheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportSpreadsheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportSpreadsheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportSpreadsheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportSpreadsheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportSpreadsheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportSpreadsheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}