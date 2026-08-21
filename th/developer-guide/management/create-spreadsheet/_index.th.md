---
---
title: "สร้าง Spreadsheet API – Aspose.Cells Cloud (v5.0) | สร้างไฟล์ Excel"
second_title: "เอกสาร"
ArticleTitle: "วิธีการสร้างสมุดงาน Excel ใหม่ – สร้างไฟล์เปล่าหรือไฟล์จากแม่แบบ"
linktype: "สร้าง Spreadsheet"
type: docs
url: /create-spreadsheet/
keywords: "Aspose.Cells, API spreadsheet, สร้าง Excel, คลาวด์, XLSX, ODS, CSV, แม่แบบ, SDK, อัตโนมัติ"
description: "เรียนรู้วิธีการสร้างสมุดงาน Excel แบบเปล่าหรือจากแม่แบบโดยใช้ Aspose.Cells Cloud API (v5.0) ซึ่งประกอบด้วย endpoint, พารามิเตอร์, รหัสข้อผิดพลาด, ขั้นตอนการยืนยันตัวตน และตัวอย่าง SDK"
weight: 100
---

สร้าง spreadsheet Excel ใหม่ด้วย Aspose.Cells Cloud API แบบเขียนโปรแกรม สร้างสมุดงานเปล่าหรือสร้างไฟล์จากแม่แบบที่กำหนดเอง API แบบ RESTful นี้ช่วยให้สามารถสร้างไฟล์ Excel โดยอัตโนมัติ ซึ่งเหมาะอย่างยิ่งสำหรับการสร้างรายงาน อัตโนมัติเอกสาร และเวิร์กฟลows การประมวลผลข้อมูล

## **Spreadsheet API สำหรับการสร้าง**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/create
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องมี <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์   | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                                                                                         |
| ------------------ | -------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| **format**         | String   | Query    | **จำเป็น**. รูปแบบไฟล์ของ spreadsheet ใหม่ (เช่น `XLSX`, `XLS`, `ODS`, `CSV`)                                                                      |
| **template**       | String   | Query    | **ไม่บังคับ**. ชื่อไฟล์แม่แบบที่เก็บไว้ใน cloud storage ของคุณ (เช่น `invoice_template.xlsx`) หากไม่ระบุ สมุดงานเปล่าจะถูกสร้างขึ้น               |
| **outPath**        | String   | Query    | **ไม่บังคับ**. เส้นทางโฟลเดอร์เป้าหมายใน cloud storage สำหรับไฟล์ที่สร้างขึ้น หากเป็น `null` หรือไม่ระบุ spreadsheet จะถูกบันทึกไว้ในตำแหน่งเริ่มต้น |
| **outStorageName** | String   | Query    | **จำเป็น**. ตัวระบุ cloud storage ที่กำหนดค่าไว้ (เช่น `MyDrive`)                                                                                |
| **region**         | String   | Query    | **ไม่บังคับ**. การตั้งค่าภาษา和地区 (เช่น `fr-FR`) ซึ่งกำหนดรูปแบบวันที่ ตัวเลข และสกุลเงินเริ่มต้น                                               |
| **password**       | String   | Query    | **ไม่บังคับ**. รหัสผ่านสำหรับไฟล์แม่แบบที่เข้ารหัส ปล่อยว่างไว้หากแม่แบบไม่มีการป้องกัน                                                         |

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

| รหัส | ความหมาย               | คำอธิบาย                                                          |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | สำเร็จ (OK)           | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับประกอบด้วยรายละเอียดของปฏิบัติการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ)            |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | JWT token ไม่ถูกต้องหรือขาดหาย                                             |
| 413  | ข้อมูลส่งออกมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                          |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) | ข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด                                      |

## ควรใช้ Create Spreadsheet API ในกรณีใด?

- **เริ่มต้นระบบสร้างรายงานอัตโนมัติ** – สร้างสมุดงานเปล่าใหม่หรือสร้างไฟล์รายงานจากแม่แบบมาตรฐานในจุดเริ่มต้นของแต่ละวัฏจักรการอัตโนมัติรายวัน/รายสัปดาห์
- **พอร์ทัลบริการตนเองของผู้ใช้** – ให้ลูกค้าเลือกแม่แบบ (ใบเสนอราคา ตารางเวลาโครงการ ฯลฯ) และดาวน์โหลดไฟล์ Excel ที่ปรับแต่งตามต้องการได้ทันที
- **ส่งออกและกระจายข้อมูลแบบแบทช์** – สร้างสมุดงานแยกต่างหากในรูปแบบเดียวกันสำหรับชุดข้อมูลที่ส่งออกแต่ละชุด ทำให้ง่ายต่อการกระจายและประมวลผลขั้นตอนถัดไป

สำหรับการดำเนินการต่อไป เช่น การเพิ่มworksheet หรือการกรอกข้อมูลในเซลล์ โปรดดูที่ **Add Worksheet API**, **Update Cell API** และ **Export Workbook API**

## เหตุใดจึงควรใช้ Create Spreadsheet API?

- **เป็นมิตรกับนักพัฒนา** – มี SDK สำหรับหลายภาษาและเอกสารประกอบที่ครอบคลุม ทำให้การรวมระบบทำได้ง่ายกว่าการสร้างโซลูชันเอง
- **เพิ่มประสิทธิภาพแรงงาน** – ช่วยให้สามารถอัตโนมัติการรวมเอกสาร ลดความพยายามด้านแรงงาน
- **การคิดค่าใช้จ่ายตามการใช้งานจริง** – ค่าใช้จ่ายขึ้นอยู่กับการใช้งาน API โดยไม่มีค่าธรรมเนียมล่วงหน้าสำหรับใบอนุญาต
- **บริการที่จัดการแล้ว** – API นี้ถูกโฮสต์โดยสมบูรณ์ ไม่จำเป็นต้องดูแลเซิร์ฟเวอร์ภายในหรืออัปเดตซอฟต์แวร์

## วิธีการใช้ Create Spreadsheet API ด้วย SDK

### ข้อมูลจำเพาะ Create Spreadsheet API

[ข้อมูลจำเพาะ Create Spreadsheet API](https://reference.aspose.cloud/cells/#/ManagementController/CreateSpreadsheet) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้จากภายนอก และสามารถใช้ปฏิสัมพันธ์ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL บรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/create?format=XLSX&outStorageName=MyStorage" \
  -H "Authorization: Bearer {access_token}"
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

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจากซ่อนรายละเอียดระดับต่ำ และช่วยให้คุณสร้าง spreadsheet ด้วยโค้ดที่กระชับ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}