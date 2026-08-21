---
---
title: "Aspose.Cells Cloud Web API – แปลงแผ่นงานเป็น JSON"
second_title: "เอกสาร"
ArticleTitle: "วิธีการแปลงแผ่นงานในสมุดงานเป็น JSON โดยใช้ Aspose.Cells Cloud API"
linktype: "แปลงแผ่นงานเป็น JSON"
type: docs
url: /convert-worksheet-to-json/
keywords: "Aspose.Cells, แผ่นงานเป็น JSON, การแปลง Excel, API บนคลาวด์, API v4, การส่งออกข้อมูล"
description: "คู่มือแบบทีละขั้นตอนเกี่ยวกับการแปลงแผ่นงาน Excel เป็น JSON โดยใช้ Aspose.Cells Cloud API รวมถึงพารามิเตอร์คำขอ การจัดการกับการตอบกลับ รหัสข้อผิดพลาด และตัวอย่าง SDK"
weight: 100
---

endpoint **ConvertWorksheetToJson** อ่านไฟล์สมุดงานจากไฟล์ในระบบ本地 แยกแผ่นงานที่ระบุไว้ และส่งคืนเนื้อหาในรูปแบบไฟล์ JSON การแปลงนี้ดำเนินการบนเซิร์ฟเวอร์ของ Aspose.Cells Cloud ทั้งหมด จึงไม่จำเป็นต้องอัปโหลดหรือจัดเก็บข้อมูลชั่วคราวก่อนหน้านี้ API นี้รองรับสมุดงานที่มีรหัสผ่าน ตำแหน่งแบบอักษรที่กำหนดเอง และการตั้งค่าภูมิภาค ทำให้ได้โซลูชันบนคลาวด์ที่รวดเร็วสำหรับการส่งออกข้อมูลแผ่นงานเป็น JSON เพื่อนำไปประมวลผลขั้นตอนถัดไป

## **API แปลงแผ่นงานเป็น JSON**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/json
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### **พารามิเตอร์คำขอ:**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | จำเป็น/ไม่จำเป็น | คำอธิบาย                                                                                                                                                                                            |
| :------------- | :----- | :------- | :---------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | ไฟล์   | FormData | จำเป็น          | สมุดงาน Excel ที่ต้องประมวลผล ต้องอยู่ในรูปแบบที่รองรับ (xls, xlsx, csv เป็นต้น) ส่งผ่าน multipart/form-data ตัวอย่าง: `Spreadsheet=@C:\Docs\Sample.xlsx`                                       |
| worksheet      | สตริง | Query    | จำเป็น          | ชื่อที่แท้จริงของแผ่นงานที่ต้องการแปลง (แยกแยะตัวพิมพ์เล็ก/ใหญ่) หากไม่ระบุหรือไม่พบ จะคืนค่าข้อผิดพลาดจาก API ตัวอย่าง: `worksheet=Sheet1`.                                                               |
| outPath        | สตริง | Query    | ไม่จำเป็น          | โฟลเดอร์ปลายทางบนพื้นที่จัดเก็บบนคลาวด์ที่กำหนดไว้ ซึ่งไฟล์ JSON ที่สร้างขึ้นจะถูกบันทึกไว้ หากไม่ระบุ JSON จะถูกส่งกลับโดยตรงในสตรีมการตอบกลับ ตัวอย่าง: `outPath=/converted/`. |
| outStorageName | สตริง | Query    | ไม่จำเป็น          | ชื่อของพื้นที่จัดเก็บเป้าหมาย (เช่น "MyStorage") ที่มี `outPath` จะใช้พื้นที่จัดเก็บเริ่มต้นเมื่อลบพารามิเตอร์นี้ออก                                                                                     |
| fontsLocation  | สตริง | Query    | ไม่จำเป็น          | โฟลเดอร์ฝั่งเซิร์ฟเวอร์ที่เก็บแบบอักษรที่กำหนดเองซึ่งจำเป็นสำหรับการแสดงผลข้อความในแผ่นงานอย่างถูกต้อง ตัวอย่าง: `fontsLocation=/fonts/custom/`.                                                          |
| region         | สตริง | Query    | ไม่จำเป็น          | ตัวระบุวัฒนธรรม/ภูมิภาคที่มีผลต่อรูปแบบตัวเลข วันที่ และสกุลเงินใน JSON ที่สร้างขึ้น (เช่น `en-US`, `fr-FR`).                                                                        |
| password       | สตริง | Query    | ไม่จำเป็น          | รหัสผ่านสำหรับเปิดสมุดงานที่เข้ารหัส หากสมุดงานไม่ได้ป้องกันด้วยรหัสผ่าน ให้ละเว้นพารามิเตอร์นี้                                                                                                |

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

**รหัสสถานะ HTTP**

| รหัส | ความหมาย               | คำอธิบาย                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | สำเร็จ (OK)                    | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request)           | พารามิเตอร์หายไปหรือไม่ถูกต้อง (เช่น ไฟล์ไม่อยู่ในรูปแบบที่รองรับ)      |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)          | JWT token ไม่ถูกต้องหรือไม่มีการระบุไว้                                     |
| 413  | ข้อมูลในคำขอมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด                                 |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | ข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์                                          |

## ควรใช้ API แปลงแผ่นงานเป็น JSON ที่ไหน?

- **แดชบอร์ดบนเว็บ** – ส่งออกข้อมูลแผ่นงานเป็น JSON เพื่อใช้กับไลบรารีการสร้างกราฟฝั่งไคลเอนต์ (เช่น Chart.js, D3.js)
- **การย้ายข้อมูล** – ย้ายข้อมูล Excel รุ่นเก่าไปยังฐานข้อมูล NoSQL หรือบริการ REST ที่รับข้อมูล JSON
- **แอปมือถือหรือแบบออฟไลน์** – แปลงเนื้อหาแผ่นงานเป็น JSON บนเซิร์ฟเวอร์ จากนั้นซิงค์ข้อมูลขนาดเบาไปยังอุปกรณ์มือถือ
- **สายงานรายงานข้อมูล** – ส่งข้อมูลแผ่นงานโดยตรงไปยังเครื่องมือวิเคราะห์ข้อมูลที่รับข้อมูล JSON โดยไม่ต้องผ่านขั้นตอน CSV ก่อนหน้า

## ทำไมควรใช้ API แปลงแผ่นงานเป็น JSON?

- **เวิร์กโฟลว์แบบไม่ต้องอัปโหลด** – ประมวลผลไฟล์ในเครื่องบนคลาวด์โดยไม่ต้องอัปโหลดไฟล์ไปยังพื้นที่จัดเก็บก่อน ช่วยประหยัดแบนด์วิดท์และค่าใช้จ่ายในการจัดเก็บ
- **การแปลงที่ครบถ้วน** – รองรับสมุดงานที่มีรหัสผ่าน แบบอักษรที่กำหนดเอง และการจัดรูปแบบตามภูมิภาค เพื่อแสดงข้อมูลอย่างถูกต้องแม่นยำ
- **การทำงานที่รวดเร็วและขยายขนาดได้** – ใช้เอนจิ้น Aspose.Cells ที่มีประสิทธิภาพสูงบนโครงสร้างพื้นฐานคลาวด์ จัดการแผ่นงานขนาดใหญ่ได้อย่างมีประสิทธิภาพ
- **การผสานรวมที่เรียบง่าย** – คำสั่ง PUT ครั้งเดียวให้ผลลัพธ์ไฟล์ JSON ที่พร้อมใช้งานหรือจัดเก็บไว้โดยตรง ลดความซับซ้อนของโค้ดในแอปพลิเคชันฝั่งไคลเอนต์

## วิธีใช้ API แปลงแผ่นงานเป็น JSON ด้วย SDK

### ข้อมูลจำเพาะ API แปลงแผ่นงานเป็น JSON

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToJson" rel="noopener noreferrer">ข้อมูลจำเพาะ API แปลงแผ่นงานเป็น JSON</a> ให้ programming interface ที่เข้าถึงได้สาธารณะสำหรับการดำเนินการ REST ผ่านเว็บเบราว์เซอร์โดยตรง

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง cURL เพื่อเข้าถึงบริการเว็บ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/json?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
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

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจากซ่อนรายละเอียดระดับต่ำไว้และให้คุณทำงานกับสมุดงานผ่านโค้ดที่กระชับ โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด  
ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการโต้ตอบกับบริการเว็บ Aspose.Cells ผ่าน SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToJson.go" >}}
{{</tab>}}
{{< /tabs >}}