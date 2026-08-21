---
title: "Aspose.Cells Cloud Split Excel Web API – แยกไฟล์ Excel แบบโลคัลเป็นหลายไฟล์ และส่งออกเป็นรูปแบบกว่า 30 รูปแบบ"
second title: "เอกสาร"
ArticleTitle: "เครื่องมือแยกไฟล์ Excel – แบ่งสเปรดชีตโลคัลเป็นไฟล์หลายไฟล์ในรูปแบบกว่า 30 รูปแบบ"
linktitle: "แยกสเปรดชีต"
type: docs
url: /th/split-spreadsheet/
keywords: "แยก, excel, aspose cells, spreadsheet API, ส่งออก pdf, csv, json"
description: "แยกสมุดงาน Excel แบบโลคัลเป็นไฟล์แยกต่างหากโดยใช้ Aspose.Cells Cloud API สามารถส่งออกเป็นรูปแบบกว่า 30 รูปแบบ (PDF, CSV, JSON, XLSX, HTML) โดยไม่ต้องอัปโหลดไปยังคลาวด์"
weight: 100
---

แบ่งสมุดงาน Excel แบบโลคัลเป็นไฟล์แยกต่างหากโดยสมบูรณ์ — ไม่จำเป็นต้องใช้พื้นที่จัดเก็บบนคลาวด์ รองรับผลลัพธ์ในรูปแบบไฟล์กว่า 30 รูปแบบ เช่น PDF, CSV, JSON, ODS และ XPS

## **Split Spreadsheet API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/split/spreadsheet
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

```bash
-H "Authorization: Bearer {access_token}"
```

### **พารามิเตอร์คำขอ:**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | Path/Query String/HTTPBody | คำอธิบาย                                                                                                                                                               |
| :------------- | :------ | :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet    | ไฟล์    | FormData                   | ไฟล์สเปรดชีตโลคัลที่จะถูกแบ่ง รองรับรูปแบบไฟล์ เช่น XLSX, XLS, ODS, CSV เป็นต้น ไฟล์จะถูกประมวลผลทั้งหมดบนเซิร์ฟเวอร์โดยไม่ต้องใช้พื้นที่จัดเก็บบนคลาวด์ |
| from           | จำนวนเต็ม | Query                      | ดัชนีเริ่มต้นของช่วงชีต (เริ่มจาก 0) ที่จะแบ่ง (เช่น `0` คือชีตแรก)                                                                        |
| to             | จำนวนเต็ม | Query                      | ดัชนีสิ้นสุดของช่วงชีต (เริ่มจาก 0) ที่จะแบ่ง (เช่น `2` จะแบ่งชีตที่ 0, 1 และ 2)                                                                |
| outFormat      | สตริง  | Query                      | รูปแบบไฟล์ผลลัพธ์ที่ได้จากการแบ่ง รองรับกว่า 30 รูปแบบ เช่น `PDF`, `CSV`, `JSON`, `XLSX`, `HTML`                                                                 |
| outPath        | สตริง  | Query                      | _(ไม่บังคับ)_ ที่อยู่โฟลเดอร์โลคัลที่จะบันทึกไฟล์ผลลัพธ์ที่แบ่งแล้ว หากไม่ระบุ ไฟล์จะถูกบันทึกไว้ในตำแหน่งชั่วคราวเริ่มต้น                               |
| outStorageName | สตริง  | Query                      | ตัวระบุพื้นที่จัดเก็บสำหรับจัดระเบียบไฟล์ผลลัพธ์ ในโหมดการประมวลผลแบบโลคัล มักหมายถึงป้ายกำกับพื้นที่จัดเก็บแบบเซสชันหรือผู้ใช้กำหนดเอง                     |
| fontsLocation  | สตริง  | Query                      | _(ไม่บังคับ)_ ระบุไดเรกทอรีฟอนต์โลคัลหรือแบบกำหนดเอง เพื่อให้การแสดงผลข้อความแม่นยำเมื่อส่งออกเป็นรูปแบบ PDF หรือรูปภาพ                                         |
| region         | สตริง  | Query                      | _(ไม่บังคับ)_ ตั้งค่าการตั้งค่าภูมิภาคสำหรับรูปแบบตัวเลข วันที่ และสกุลเงินในไฟล์ผลลัพธ์ (เช่น `"en-US"`, `"de-DE"`)                                                  |
| password       | สตริง  | Query                      | _(ไม่บังคับ)_ หากสเปรดชีตที่อัปโหลดมีการป้องกันด้วยรหัสผ่าน ให้ระบุรหัสผ่านเพื่อเปิดและประมวลผลไฟล์                                                        |

## **การตอบกลับ**

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

ไฟล์สามารถดาวน์โหลดโดยตรงหรือบันทึกไปยังตำแหน่งที่ระบุไว้ใน `outPath`

**รายละเอียดการตอบกลับเมื่อสำเร็จ**

| สถานะโค้ด (Status Code) | Content-Type               | คำอธิบาย                                |
| ---------------------- | -------------------------- | ---------------------------------------- |
| 200 OK                 | `application/octet-stream` | สตรีมไบนารีของไฟล์สมุดงานที่รวมแล้ว       |

**สถานะโค้ด HTTP**

| โค้ด | ความหมาย             | คำอธิบาย                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับประกอบด้วยรายละเอียดการทำงาน |
| 400  | Bad Request           | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น รูปแบบไฟล์ที่ไม่รองรับ)      |
| 401  | Unauthorized          | JWT token ไม่ถูกต้องหรือขาดหาย                                     |
| 413  | Payload Too Large     | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                  |
| 500  | Internal Server Error | เกิดข้อผิดพลาดภายในเซิร์ฟเวอร์อย่างไม่คาดคิด                         |

## ควรใช้ Split Spreadsheet API ในกรณีใดบ้าง?

- **การแจกจ่ายข้อมูลตามแผนก**: แยกสมุดงานรวมที่มีข้อมูลจากหลายแผนกเป็นไฟล์แยกตามแผนก
- **การแจกจ่ายรายงานตามภูมิภาค**: แยกรายงานการขายระดับประเทศเป็นไฟล์รายงานรายภูมิภาค
- **การแจกจ่ายข้อมูลลูกค้าแบบซ่อนข้อมูลที่สำคัญ**: แยกสมุดงานที่มีข้อมูลละเอียดอ่อนเป็นไฟล์สำหรับลูกค้าที่ผ่านการปรับแต่งแล้ว
- **การแบ่งรายงานตามช่วงเวลา**: แบ่งรายงานสรุปเป็นรายงานรายสัปดาห์หรือรายวันโดยอัตโนมัติทุกเดือน
- **การแจกจ่ายหลายรูปแบบ**: แยกไฟล์ Excel เดียวเป็นหลายเวอร์ชันในรูปแบบต่างๆ เช่น PDF, CSV, JSON ฯลฯ พร้อมกัน
- **การแบ่งตามเทมเพลต**: แบ่งไฟล์ข้อมูลเป็นไฟล์ผลลัพธ์มาตรฐานตามเทมเพลตที่กำหนดไว้ล่วงหน้า
- **การประมวลผลข้อมูลก่อนโหลด**: แยกไฟล์ Excel เป็นไฟล์ CSV มาตรฐานก่อนโหลดข้อมูลลงฐานข้อมูล
- **การเตรียมข้อมูลสำหรับ API**: แบ่งชุดข้อมูลขนาดใหญ่เป็นชิ้นส่วนที่เล็กลง เพื่อให้เหมาะสมกับการส่งผ่าน API

## เหตุใดจึงควรใช้ Split Spreadsheet API?

- **เป็นมิตรกับนักพัฒนา**: Aspose.Cells Cloud มี SDK ให้ใช้งานในหลายภาษา ช่วยให้การพัฒนาทำได้อย่างรวดเร็ว และมีเอกสารประกอบที่ครบถ้วน เมื่อเทียบกับการสร้างโซลูชันสำหรับการเรนเดอร์กราฟิกแบบกึ่งอัตโนมัติ จะช่วยลดภาระงานพัฒนาอย่างมาก
- **ลดค่าใช้จ่ายด้านแรงงาน**: ลดความจำเป็นในการจ้างบุคลากรเฉพาะด้านสำหรับการรวมเอกสาร
- **จ่ายตามการใช้งานจริง**: ไม่ต้องลงทุนล่วงหน้า; จ่ายเฉพาะเมื่อใช้งาน API จริง
- **ไม่มีค่าใช้จ่ายในการดูแลรักษา**: ไม่จำเป็นต้องดูแลเซิร์ฟเวอร์ อัปเดตซอฟต์แวร์ หรือจัดการปัญหาความเข้ากันได้
- **คงรักษาการจัดรูปแบบ Excel ที่ซับซ้อนไว้ในรูปแบบ PDF ที่เข้าถึงได้ทั่วไป**

## วิธีการใช้ Split Spreadsheet API ร่วมกับ SDK

### ข้อมูลอ้างอิง Split Spreadsheet API

[Split Spreadsheet API Specification](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitSpreadsheet) ให้ API ที่เปิดเผยสำหรับการเข้าถึงผ่านเว็บเบราว์เซอร์โดยตรง
คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่ง command-line เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/split/spreadsheet?outFormat=PDF" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o split-spreadsheet.zip
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

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจากซ่อนรายละเอียดระดับต่ำไว้เบื้องหลัง ช่วยให้คุณแบ่งสเปรดชีตเป็นไฟล์แยกต่างหากได้ด้วยโค้ดเพียงไม่กี่บรรทัด  
โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}