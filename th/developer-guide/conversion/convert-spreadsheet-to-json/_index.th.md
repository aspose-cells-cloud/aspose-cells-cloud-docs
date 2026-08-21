---
title: "Aspose.Cells Cloud Web API – แปลงไฟล์สเปรดชีตเป็น JSON"
second_title: "เอกสาร"
ArticleTitle: "วิธีการแปลงไฟล์สเปรดชีตในเครื่องเป็น JSON โดยใช้ Aspose.Cells Cloud API"
linktype: "แปลงสเปรดชีตเป็น JSON"
type: docs
url: /th/convert-spreadsheet-to-json/
keywords: "Aspose Cells Cloud, แปลงสเปรดชีตเป็น JSON, Excel to JSON API, Aspose.Cells Cloud API, REST API, การแปลงสเปรดชีต"
description: "เรียนรู้วิธีการแปลงไฟล์ Excel ในเครื่องเป็น JSON โดยใช้ Aspose.Cells Cloud API รวมถึง endpoint, พารามิเตอร์, ตัวอย่างโค้ด และการจัดการข้อผิดพลาด เพื่อการบูรณาการที่ราบรื่น"
weight: 100
---

**ปลายทาง ConvertSpreadsheetToJson** ใช้แปลงไฟล์สเปรดชีตที่เก็บอยู่บนไดรฟ์ในเครื่องให้เป็นไฟล์ JSON ทั้งหมดบนเซิร์ฟเวอร์ของ Aspose.Cells Cloud โดยส่งไฟล์สเปรดชีตในรูปแบบ `multipart/form-data` บริการจะสตรีมไฟล์ JSON กลับมาให้คุณสามารถดาวน์โหลดหรือประมวลผลต่อได้ทันที การแปลงแบบคลาวด์เนทีฟนี้ช่วยลดความจำเป็นในการอัปโหลดไฟล์ไปยังพื้นที่จัดเก็บก่อน และลดค่าใช้จ่ายในการจัดเก็บข้อมูล รวมทั้งทำให้กระบวนการทำงานของแอปพลิเคชันที่ต้องการข้อมูลสเปรดชีตในรูปแบบ JSON เพื่อการวิเคราะห์ การรายงาน หรือการแลกเปลี่ยนข้อมูลมีความเรียบง่ายยิ่งขึ้น

**ข้อกำหนดเบื้องต้น**: คุณต้องมีบัญชี Aspose Cloud, โทเค็น JWT ที่ใช้งานได้ และต้องตั้งค่า SDK หรือ API key ของ Aspose.Cells Cloud แล้ว

**ข้อมูลเบื้องหลัง**: การแปลงสเปรดชีตเป็น JSON เป็นขั้นตอนที่พบบ่อยเมื่อเชื่อมต่อข้อมูล Excel กับเว็บเซอร์วิส ฐานข้อมูล NoSQL หรือแอปพลิเคชัน JavaScript ฝั่งไคลเอนต์ API สำหรับการแปลงสเปรดชีตเป็น JSON นี้ช่วยให้การแปลงเกิดขึ้นที่เซิร์ฟเวอร์อย่างรวดเร็ว โดยไม่จำเป็นต้องจัดเก็บไฟล์ต้นฉบับไว้ล่วงหน้า

## API สำหรับการแปลงสเปรดชีตเป็น JSON

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยสูงและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล                  | ตำแหน่ง | จำเป็น/ไม่จำเป็น | คำอธิบาย                                                                                                                                                                     |
| :------------- | :------------------------- | :------- | :---------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet    | ไฟล์ (multipart/form-data) | FormData | จำเป็น           | ไฟล์สเปรดชีตต้นทาง (เช่น .xls, .xlsx, .xlsm) ตัวอย่าง: `curl -F "Spreadsheet=@myfile.xlsx"`                                                                           |
| outPath        | สตริง                      | Query    | ไม่จำเป็น         | เส้นทางไปยังโฟลเดอร์เป้าหมายในพื้นที่จัดเก็บบนคลาวด์ ที่ไฟล์ JSON ที่แปลงแล้วจะถูกบันทึก หากไม่ระบุ JSON จะถูกส่งกลับโดยตรงในสตรีมของคำตอบ ตัวอย่าง: `outPath=/output/` |
| outStorageName | สตริง                      | Query    | ไม่จำเป็น         | ชื่อของพื้นที่จัดเก็บบนคลาวด์ (เช่น Amazon S3, Azure Blob) ที่ไฟล์ผลลัพธ์จะถูกบันทึก ใช้เมื่อระบุ `outPath` กับพื้นที่จัดเก็บที่ไม่ใช่ค่าเริ่มต้นเท่านั้น               |
| fontsLocation  | สตริง                      | Query    | ไม่จำเป็น         | เส้นทางไปยังโฟลเดอร์ฟอนต์ที่กำหนดเองบนเซิร์ฟเวอร์ ใช้เมื่อไฟล์สเปรดชีตอ้างอิงถึงฟอนต์ที่ไม่อยู่ในไลบรารีค่าเริ่มต้น                                        |
| region         | สตริง                      | Query    | ไม่จำเป็น         | การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) ซึ่งมีผลต่อรูปแบบตัวเลข วันที่ และสกุลเงินระหว่างการแปลง                                               |
| password       | สตริง                      | Query    | ไม่จำเป็น         | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีตที่มีการป้องกันด้วยรหัสผ่าน ไม่ต้องระบุสำหรับไฟล์ที่ไม่มีการป้องกัน                                                                                                  |

### คำตอบ

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

| รหัส | ความหมาย              | คำอธิบาย                                                         |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | สำเร็จ (OK)           | ใช้ตัวกรองเรียบร้อยแล้ว; คำตอบประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)      |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | JWT token ไม่ถูกต้องหรือขาดหาย                                  |
| 413  | ข้อมูลส่งมาขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด                    |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                       |

## ควรใช้ API สำหรับการแปลงสเปรดชีตเป็น JSON ในกรณีใด?

- **เส้นทางการย้ายข้อมูล (Data migration pipelines)** – แปลงรายงาน Excel รุ่นเก่าให้เป็น JSON เพื่อนำเข้าสู่ฐานข้อมูล NoSQL หรือ data lakes สมัยใหม่
- **แอปพลิเคชันบนมือถือหรือเว็บ** – แปลงสเปรดชีตที่ผู้ใช้อัปโหลดให้เป็น JSON อย่างรวดเร็วสำหรับการแสดงผลฝั่งไคลเอนต์ โดยไม่ต้องจัดเก็บไฟล์ต้นฉบับไว้บนคลาวด์
- **การรายงานอัตโนมัติ (Automated reporting)** – สร้าง JSON payload สำหรับบริการวิเคราะห์ขั้นตอนหลัง (เช่น Power BI, Tableau) โดยตรงจากข้อมูลสเปรดชีต
- **ฟังก์ชันแบบ Serverless** – ใช้ API ภายใน AWS Lambda หรือ Azure Functions เพื่อแปลงไฟล์แบบทันทีโดยไม่ต้องจัดการพื้นที่จัดเก็บชั่วคราว

## เหตุใดจึงควรใช้ API สำหรับการแปลงสเปรดชีตเป็น JSON?

- การแปลงแบบคลาวด์เนทีฟช่วยลดความจำเป็นในการอัปโหลดไฟล์ขนาดใหญ่ไปยังพื้นที่จัดเก็บก่อนประมวลผล ลดความล่าช้าและค่าใช้จ่ายในการจัดเก็บ
- กระบวนการทำงานด้วยคำขอเพียงครั้งเดียว: อัปโหลดสเปรดชีตแล้วรับ JSON ผ่าน HTTP call เดียวกัน ทำให้ตรรกะการบูรณาการเรียบง่าย
- รองรับสเปรดชีตที่มีการป้องกันด้วยรหัสผ่านและสเปรดชีตที่ตั้งค่าภูมิภาคเฉพาะ รับประกันการแสดงข้อมูลอย่างถูกต้องตามภูมิภาคต่างๆ
- ปรับขนาดได้บนโครงสร้างพื้นฐานของ Aspose – จัดการสมุดงานขนาดใหญ่และสูตรที่ซับซ้อนโดยไม่กระทบทรัพยากรเซิร์ฟเวอร์ของคุณ

## วิธีใช้ API สำหรับการแปลงสเปรดชีตเป็น JSON ด้วย SDK

### ข้อมูลจำเพาะ API สำหรับการแปลงสเปรดชีตเป็น JSON

[ข้อมูลจำเพาะ API สำหรับการแปลงสเปรดชีตเป็น JSON](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheetToJson) ให้อินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะสำหรับดำเนินการปฏิสัมพันธ์ REST โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="คำตอบ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json?outPath=/output/result.json" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myWorkbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เพราะซ่อนรายละเอียดระดับต่ำไว้เบื้องหลัง และช่วยให้คุณแปลงสเปรดชีตเป็น JSON ด้วยเพียงไม่กี่บรรทัดของโค้ด  
โปรดดูที่ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด  
ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการโต้ตอบกับเว็บเซอร์วิสของ Aspose.Cells ด้วย SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToJson.go" >}}
{{</tab>}}
{{< /tabs >}}