---
---
title: "Aspose.Cells Cloud Web API – แปลงข้อมูลตาราง Excel ที่อยู่ในเครื่องให้เป็นไฟล์ JSON"
second title: "เอกสาร"
ArticleTitle: "วิธีแปลงข้อมูลตารางในสเปรดชีตในเครื่องให้เป็นไฟล์ JSON: คู่มือแบบทีละขั้นตอน"
linktype: "แปลงตารางเป็น JSON"
type: docs
url: /convert-table-to-json/
keywords: "Excel, API, JSON, การแปลง, คลาวด์, ไฟล์, สเปรดชีต"
description: "ใช้ Aspose.Cells Cloud API เพื่อแปลงตาราง Excel ที่อยู่ในเครื่องให้เป็นไฟล์ JSON ด้วยคำขอ PUT แบบเดียว ประกอบด้วยตัวอย่าง cURL พารามิเตอร์ และโค้ดตัวอย่าง SDK สำหรับ C#, Java, Python และอื่นๆ"
weight: 100
---

แปลงตารางสเปรดชีต/Excel ที่อยู่ในเครื่องให้เป็นไฟล์ **JSON** ด้วย Aspose.Cells Cloud Web API

## **API สำหรับการแปลงตารางเป็น JSON**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/json
```

### **การรักษาความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์   | ประเภท   | ตำแหน่ง | คำอธิบาย                                                                                       |
| ------------------ | ------ | -------- | ---------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | ไฟล์   | FormData | ไฟล์ Excel ที่จะอัปโหลด                                                                       |
| **worksheet**      | สตริง | Query    | ชื่อของworksheet ที่มีตาราง                                                                     |
| **tableName**      | สตริง | Query    | ชื่อของตารางที่จะแปลง                                                                          |
| **outPath**        | สตริง | Query    | (ไม่บังคับ) เส้นทางโฟลเดอร์ที่จะบันทึกไฟล์ JSON ที่ได้; ค่าเริ่มต้นคือ **null**                 |
| **outStorageName** | สตริง | Query    | (ไม่บังคับ) ชื่อของพื้นที่จัดเก็บที่จะบันทึกไฟล์ผลลัพธ์                                         |
| **fontsLocation**  | สตริง | Query    | (ไม่บังคับ) เส้นทางไปยังฟอนต์ที่กำหนดเองที่ใช้ในการแปลง                                        |
| **region**         | สตริง | Query    | (ไม่บังคับ) การตั้งค่าภูมิภาคสำหรับสมุดงาน                                                     |
| **password**       | สตริง | Query    | (ไม่บังคับ) รหัสผ่านสำหรับเปิดสมุดงานที่ได้รับการป้องกัน                                         |

### คำตอบ (Response)

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

| รหัส | ความหมาย               | คำอธิบาย                                                           |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | สำเร็จ (OK)            | ใช้ตัวกรองสำเร็จ; คำตอบประกอบด้วยรายละเอียดของ операция           |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ประเภทที่ไม่รองรับ)      |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                                   |
| 413  | ข้อมูลในคำขอใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                               |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์                        |

## **คุณควรใช้ API สำหรับการแปลงตารางเป็น JSON ในกรณีใด?**

- **แดชบอร์ดแบบเรียลไทม์** – แปลงข้อมูล Excel แบบสดให้เป็น JSON เพื่อใช้กับไลบรารีกราฟเช่น Chart.js หรือ D3.js  
- **บริการสเปรดชีต (Spreadsheet-as-a-Service)** – เผยแพร่ตาราง Excel ผ่าน JSON endpoints ให้ไมโครเซอร์วิสอื่นๆ  
- **ข้อมูลสำหรับ webhook** – แปลงข้อมูลสเปรดชีตให้เป็น JSON เพื่อใช้ใน webhook notifications  
- **การพัฒนาโปรโตไทป์ข้อมูลอย่างรวดเร็ว** – แปลงข้อมูล Excel ที่ผ่านการ清洗ให้เป็น JSON อย่างรวดเร็วสำหรับการวิเคราะห์ด้วย Python หรือ R  
- **หลักการประมวลผลข้อมูลสำหรับการเรียนรู้ของเครื่อง (Machine-Learning Pipelines)** – ประมวลผลข้อมูลฝึกอบรมที่เก็บไว้ในสเปรดชีตทางธุรกิจ  
- **การดำเนินงานอีคอมเมิร์ซ** – ซิงค์แคตตาล็อกสินค้าหรือตารางราคาเว็บไซต์ผ่าน JSON  
- **การสร้างรายงานอัตโนมัติ** – สร้าง JSON feeds จากแบบจำลองการเงินสำหรับรายงานอัตโนมัติ  
- **การตั้งค่าแอปพลิเคชัน** – จัดการ feature flags, การตั้งค่า หรือพารามิเตอร์ A/B-test ใน Excel → JSON  
- **การรองรับหลายภาษา** – แปลงสเปรดชีตสำหรับการแปลภาษาให้เป็น JSON สำหรับใช้กับ i18n libraries  
- **เมนู/การนำทางแบบไดนามิก** – เก็บโครงสร้างการนำทางเว็บไซต์ใน Excel และปรับใช้เป็น JSON  

## **เหตุใดคุณควรใช้ API สำหรับการแปลงตารางเป็น JSON?**

- **เป็นมิตรกับนักพัฒนา** – Aspose.Cells Cloud มี SDK สำหรับภาษาต่างๆ มากมาย ช่วยลดความพยายามในการพัฒนาและมีเอกสารที่ครบถ้วน  
- **ประหยัดต้นทุน** – แปลงข้อมูลตารางโดยไม่ต้องอัปโหลดสมุดงานก่อน ช่วยประหยัดพื้นที่จัดเก็บและลดต้นทุน  
- **เข้ากับเว็บและมือถือสมัยใหม่** – JSON เป็นภาษาข้อมูลหลักของเว็บ; API นี้ช่วยให้คุณสามารถส่งข้อมูลสเปรดชีตแบบสดเข้าสู่ React, Vue, Angular, แอปมือถือ หรือแอปพลิเคชันแบบหน้าเดียว (SPA) โดยไม่ต้องใช้การประมวลผลที่ซับซ้อน  
- **รองรับภาษาได้กว้างขวาง** – JSON ใช้งานได้เกือบทุกภาษาโปรแกรม ฐานข้อมูล และบริการเว็บ  
- **คงโครงสร้างข้อมูลไว้**
  - **การตรวจจับโครงสร้างอัจฉริยะ** – แปลงข้อมูลตารางให้เป็น array/object JSON ที่ถูกต้องโดยอัตโนมัติ  
  - **การแมป header** – ใช้แถวแรกเป็นคีย์ JSON เพื่อสร้างโครงสร้าง object ที่เรียบร้อย  
  - **การรักษารูปแบบข้อมูล** – คงข้อมูลตัวเลข วันที่ และค่าบูลีนไว้ (ไม่ใช่แค่ข้อความ)

_ประวัติเวอร์ชัน:_ API endpoint สำหรับการแปลงตารางเป็น JSON ถูกแนะนำในเวอร์ชัน API **v4.0** (2024) และยังคงเป็นเวอร์ชันที่เสถียรในปัจจุบัน API เวอร์ชัน v3.x ที่เก่ากว่าได้เลิกใช้งานแล้ว

## วิธีใช้ API สำหรับการแปลงตารางเป็น JSON ด้วย SDKs?

### ข้อมูลจำเพาะ API สำหรับการแปลงตารางเป็น JSON

[ข้อมูลจำเพาะ API สำหรับการแปลงตารางเป็น JSON](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToJson){:target="\_blank" rel="noopener noreferrer"} จัดเตรียมอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ ช่วยให้คุณสามารถเรียกใช้ REST API ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="คำตอบ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=MyTable" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/your/file.xlsx" \
     -F "outPath=output/folder" \
     -F "outStorageName=MyStorage"
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

```
{
 "Code": 200,
 "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK จะช่วยซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถแปลงตารางสเปรดชีตเป็นไฟล์ JSON ได้ด้วยโค้ดน้อยที่สุด ดู repository GitHub ทางการสำหรับรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการโต้ตอบกับบริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToJson.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToJson.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToJson.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToJson.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToJson.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToJson.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToJson.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToJson.go" >}}  
{{</tab>}}  
{{< /tabs >}}