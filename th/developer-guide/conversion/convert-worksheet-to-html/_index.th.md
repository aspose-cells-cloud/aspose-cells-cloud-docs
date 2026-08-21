---
title: "Aspose.Cells Cloud Web API – แปลงแผ่นงานเป็น HTML"
second_title: "เอกสาร"
ArticleTitle: "วิธีการแปลงแผ่นงานเป็น HTML โดยใช้ Aspose.Cells Cloud API"
linktype: "แปลงแผ่นงานเป็น HTML"
type: docs
url: /th/convert-worksheet-to-html/
description: "เรียนรู้วิธีแปลงแผ่นงาน Excel เป็น HTML โดยใช้ Aspose.Cells Cloud API – ไม่ต้องอัปโหลดล่วงหน้า รองรับฟอนต์ที่กำหนดเอง รองรับภูมิภาค และการจัดการข้อผิดพลาด"
keywords: "Aspose.Cells, Excel ไปยัง HTML, การแปลงแผ่นงาน, API บนคลาวด์"
weight: 100
---

จุดปลายทาง **ConvertWorksheetToHtml** อ่านสมุดงาน Excel จากระบบไฟล์ในเครื่อง ดึงแผ่นงานที่ระบุ และส่งคืนเนื้อหาในรูปแบบไฟล์ HTML การแปลงดำเนินการที่เซิร์ฟเวอร์คลาวด์ของ Aspose ทั้งหมด จึงไม่จำเป็นต้องอัปโหลดหรือจัดเก็บข้อมูลชั่วคราวใดๆ เหมาะสำหรับการสร้างมุมมองที่พร้อมใช้บนเว็บของข้อมูลสเปรดชีต ทั้งยังรองรับเส้นทางผลลัพธ์ที่กำหนดเอง ฟอนต์ที่กำหนดเอง การตั้งค่าภูมิภาค และสมุดงานที่ป้องด้วยรหัสผ่าน

## API สำหรับแปลงแผ่นงานเป็น HTML

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/html
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์ด้วยโทเค็น JWT</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | จำเป็น/ไม่บังคับ | คำอธิบาย                                                                                                                                                                                                |
| :------------- | :----- | :------- | :---------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | ไฟล์   | จำเป็น   | FormData          | ไฟล์ Excel แบบไบนารีที่ต้องประมวลผล ต้องเป็น .xlsx, .xls, .xlsb เป็นต้น ตัวอย่าง: `myWorkbook.xlsx` ไฟล์ Excel จะถูกอ่านโดยตรงจากเนื้อหาของคำขอ ไม่จำเป็นต้องอัปโหลดไปยังพื้นที่จัดเก็บบนคลาวด์ล่วงหน้า |
| worksheet      | สตริง | จำเป็น   | Query             | ชื่อของแผ่นงานที่ต้องการแปลง (แยกแยะตัวพิมพ์เล็ก-ใหญ่) ต้องมีอยู่ในสมุดงานที่ส่งมา ตัวอย่าง: `Sheet1`                                                                                                 |
| outPath        | สตริง | ไม่บังคับ | Query             | เส้นทางไปยังโฟลเดอร์เป้าหมาย (ในพื้นที่จัดเก็บบนคลาวด์) ที่จะบันทึกไฟล์ HTML ที่สร้างขึ้น หากไม่ระบุ ไฟล์จะส่งกลับโดยตรงในส่วนตอบกลับของคำขอ ตัวอย่าง: `/output/html/`                                    |
| outStorageName | สตริง | ไม่บังคับ | Query             | ชื่อของบริการพื้นที่จัดเก็บบนคลาวด์ที่ใช้กับ `outPath` จำเป็นเฉพาะเมื่อ `outPath` ชี้ไปยังพื้นที่จัดเก็บที่ไม่ใช่ค่าเริ่มต้น                                                                                      |
| fontsLocation  | สตริง | ไม่บังคับ | Query             | เส้นทางสัมบูรณ์ไปยังโฟลเดอร์ที่มีฟอนต์ TrueType/OpenType ที่กำหนดเองซึ่งต้องใช้ในการแปลง เพื่อให้สามารถแสดงผลอักขระที่ไม่เป็นมาตรฐานได้อย่างถูกต้อง                                           |
| region         | สตริง | ไม่บังคับ | Query             | ตัวระบุภาษาและภูมิภาค (locale) ซึ่งมีผลต่อรูปแบบตัวเลข/วันที่ (เช่น `en-US`, `fr-FR`) โดยค่าเริ่มต้นจะใช้การตั้งค่าภูมิภาคภายในของสมุดงาน                                                                      |
| password       | สตริง | ไม่บังคับ | Query             | รหัสผ่านที่จำเป็นสำหรับการเปิดสมุดงานที่ได้รับการป้องกัน ไม่ต้องระบุสำหรับไฟล์ที่ไม่ได้ป้องกัน                                                                                                                                |

### การตอบกลับ

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

| รหัส | ความหมาย                | คำอธิบาย                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | สำเร็จ (OK)                    | ใช้ตัวกรองสำเร็จ; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request)           | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ)      |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)          | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                                     |
| 413  | ข้อมูลในคำขอใหญ่เกินไป (Payload Too Large)     | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                 |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | ข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์                                          |

## ควรใช้ API สำหรับแปลงแผ่นงานเป็น HTML ในกรณีใดบ้าง?

- ฝังข้อมูลสเปรดชีตแบบเรียลไทม์ลงในพอร์ทัลเว็บ – แปลงแผ่นงานรายงานทางการเงินเป็น HTML เพื่อดูโดยตรงในเบราว์เซอร์โดยไม่จำเป็นต้องใช้ปลั๊กอิน Excel
- สร้างหน้าอินเวอร์ส HTML ที่พร้อมพิมพ์จากเทมเพลต Excel – อัตโนมัติการสร้างหน้าอินเวอร์สที่พร้อมใช้บนเว็บจากแผ่นงานที่กำหนดไว้ล่วงหน้า
- สร้าง snippets สำหรับเอกสาร – แปลงแผ่นงานสเปคดีไซน์เป็น HTML fragments ที่สามารถแทรกลงในคู่มือทางเทคนิคหรือวิกิได้
- พัฒนาแดชบอร์ด BI แบบ low-code – ดึงข้อมูลจากแผ่นงาน แปลงเป็น HTML และแสดงผลภายในวิดเจ็ตแดชบอร์ดที่กำหนดเอง

## เหตุใดจึงควรใช้ API สำหรับแปลงแผ่นงานเป็น HTML?

- **กระบวนการทำงานแบบไม่ต้องอัปโหลดล่วงหน้า** – แปลงไฟล์ในเครื่องโดยตรงบนคลาวด์ ไม่จำเป็นต้องส่งโอนสมุดงานขนาดใหญ่ไปยังพื้นที่จัดเก็บก่อน
- **การเรนเดอร์ที่มีประสิทธิภาพสูง** – การแปลงฝั่งเซิร์ฟเวอร์ใช้เอนจิ้นที่ปรับแต่งแล้วของ Aspose ให้ผลลัพธ์ HTML ที่รวดเร็วและแม่นยำ
- **การควบคุมผลลัพธ์แบบเต็มรูปแบบ** – พารามิเตอร์เสริม (ฟอนต์ที่กำหนดเอง, ภูมิภาค, รหัสผ่าน) ช่วยปรับแต่ง HTML ให้สอดคล้องกับความต้องการด้านภาษาและแบรนด์
- **การผสานรวมอย่างราบรื่น** – คำขอ PUT แบบง่ายพร้อม multipart/form‑data ผสานเข้ากับท่อ CI/CD,ไมโครเซอร์วิส หรือฟังก์ชันแบบเซิร์ฟเวอร์เลสได้อย่างเป็นธรรมชาติ

## วิธีใช้ API สำหรับแปลงแผ่นงานเป็น HTML ด้วย SDK

### 仕様 API สำหรับแปลงแผ่นงานเป็น HTML

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToHtml" target="_blank" rel="noopener noreferrer">仕akah API สำหรับแปลงแผ่นงานเป็น HTML</a> ให้อินเทอร์เฟซโปรแกรมที่เข้าถึงได้สาธารณะสำหรับดำเนินการปฏิสัมพันธ์ REST โดยตรงจากเบราว์เซอร์เว็บ

คุณสามารถใช้เครื่องมือ cURL บนคอมมานด์ไลน์เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/html?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.html
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

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจากซ่อนรายละเอียดระดับต่ำไว้ ช่วยให้คุณผสานรวมแผ่นงานด้วยโค้ดที่กระชับ  
โปรดดูที่ <a href="https://github.com/aspose-cells-cloud/aspnet-sdk" target="_blank" rel="noopener noreferrer">ที่เก็บ GitHub ของ Aspose.Cells Cloud SDK</a> สำหรับรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด  
ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการโต้ตอบกับบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}