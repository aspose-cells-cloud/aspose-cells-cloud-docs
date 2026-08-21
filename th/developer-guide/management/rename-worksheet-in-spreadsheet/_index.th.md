---
---
title: "การเปลี่ยนชื่อแผ่นงานใน Excel – API ของ Aspose.Cells Cloud"
second_title: "เอกสาร"
ArticleTitle: "วิธีการเปลี่ยนชื่อแผ่นงานใน Excel – เปลี่ยนชื่อแท็บ"
linktype: "เปลี่ยนชื่อแผ่นงานในสเปรดชีต"
type: docs
url: /rename-worksheet-in-spreadsheet/
keywords: "เปลี่ยนชื่อแผ่นงาน, Aspose.Cells Cloud, Excel API, สเปรดชีต, SDK, REST API"
description: "เปลี่ยนชื่อแผ่นงานใน Excel ได้อย่างง่ายดายผ่าน API ของ Aspose.Cells Cloud ศึกษาพารามิเตอร์ที่จำเป็น ดูตัวอย่าง cURL และรับโค้ด SDK สำหรับ C#, Java, Python และอื่นๆ"
weight: 100
---

เปลี่ยนชื่อแผ่นงานในสมุดงาน Excel โดยใช้ API ของ Aspose.Cells Cloud แบบโปรแกรม ปรับเปลี่ยนชื่อแผ่นงาน อัปเดตป้ายกำกับแท็บแบบไดนามิก และทำให้กระบวนการจัดการสเปรดชีตเป็นอัตโนมัติผ่านการเรียก API แบบ RESTful ช่วยให้เกิดการมาตรฐานเอกสารและการทำงานอัตโนมัติของเวิร์กโฟลว์

## การเปลี่ยนชื่อแผ่นงานใน Spreadsheet API

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sourceName={sourceName}&targetName={targetName}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}
```

**ตัวอย่าง cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sourceName=Sheet1&targetName=Report_Q1" \
     -H "Authorization: Bearer {access_token}" \
     -F "spreadsheet=@myWorkbook.xlsx"
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์     | ประเภท   | ตำแหน่ง | คำอธิบาย                                                                                                                                                                                                     |
| ------------------ | ------ | -------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | ไฟล์   | FormData | **จำเป็น**. ไฟล์สมุดงาน Excel (.xlsx, .xls ฯลฯ) ที่มีแผ่นงานที่ต้องการเปลี่ยนชื่อ                                                                                                               |
| **sourceName**     | สตริง | Query    | **จำเป็น**. ชื่อปัจจุบันของแผ่นงานที่คุณต้องการเปลี่ยนชื่อ                                                                                                                                             |
| **targetName**     | สตริง | Query    | **จำเป็น**. ชื่อใหม่ที่จะกำหนดให้กับแผ่นงาน ต้องปฏิบัติตามกฎการตั้งชื่อของ Excel (ห้ามใช้ `:`, `\`, `?`, `*`, `[`, `]`) และต้องไม่ซ้ำกันภายในสมุดงาน                                                                      |
| **outPath**        | สตริง | Query    | **ไม่บังคับ**. เส้นทางโฟลเดอร์เป้าหมายในที่เก็บข้อมูลคลาวด์ที่จะบันทึกสมุดงานที่เปลี่ยนชื่อแล้ว หากเป็น `null` หรือเว้นว่างไว้ บริการจะบันทึกไฟล์ไว้ในโฟลเดอร์เดียวกับสมุดงานต้นทาง (หรือเส้นทางค่าเริ่มต้น) |
| **outStorageName** | สตริง | Query    | **ไม่บังคับ**. ชื่อระบุตัวของบริการที่เก็บข้อมูลคลาวด์ที่กำหนดค่าไว้ (เช่น `ArchiveStorage`) หากเว้นว่างไว้ จะใช้ที่เก็บข้อมูลเริ่มต้น                                                                   |
| **region**         | สตริง | Query    | **ไม่บังคับ**. การตั้งค่าการLocale (เช่น `ko-KR`) ซึ่งอาจส่งผลต่อการเข้ารหัสอักขระหรือข้อกำหนดการตั้งชื่อตามภูมิภาค                                                                          |
| **password**       | สตริง | Query    | **ไม่บังคับ**. รหัสผ่านสำหรับถอดรหัสที่จำเป็นในการเปิดและแก้ไขสมุดงานที่ป้องกันด้วยรหัสผ่าน เว้นว่างไว้หากไฟล์ไม่ได้ถูกเข้ารหัส                                                                             |

**หมายเหตุ**: ชื่อแผ่นงานจำกัดอยู่ที่ 31 อักขระ และห้ามมีอักขระ `:`, `\`, `?`, `*`, `[`, หรือ `]`

### การตอบกลับ

คำขอที่สำเร็จจะส่งคืนวัตถุ JSON ที่มีข้อมูลสถานะและลิงก์ไปยังไฟล์ที่เปลี่ยนชื่อแล้ว

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
| 200  | สำเร็จ (OK)                    | กรองข้อมูลสำเร็จ; การตอบกลับมีรายละเอียดของ оперATION |
| 400  | คำขอไม่ถูกต้อง (Bad Request)           | พารามิเตอร์ไม่ครบหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ)      |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)          | JWT token ไม่ถูกต้องหรือขาดหาย                                     |
| 413  | ข้อมูลในคำขอมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                 |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) | ข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด                                          |

## ควรใช้ API การเปลี่ยนชื่อแผ่นงานในสเปรดชีตเมื่อใด?

- **การสร้างรายงานและการทำให้สอดคล้องกับมาตรฐานแบรนด์** – เมื่อสร้างรายงานลูกค้าโดยอัตโนมัติ ชื่อแผ่นงานทั่วไป (เช่น `Sheet1`) จะถูกเปลี่ยนเป็นชื่อเฉพาะของลูกค้า (เช่น `AcmeCorp_Q1_Summary`) เพื่อให้แน่ใจว่าการส่งมอบมีความเป็นมืออาชีพ
- **มาตรฐานขั้นตอนการประมวลผลข้อมูล** – ในเวิร์กโฟลว์ ETL แผ่นงานที่ส่งออกด้วยชื่อที่ไม่สม่ำเสมอจะถูกเปลี่ยนชื่อให้เป็นชื่อมาตรฐาน เช่น `Raw_Data` หรือ `Cleaned_Data` เพื่อให้ตรงกับข้อกำหนดในการวิเคราะห์ขั้นตอนถัดไป
- **การจัดส่งเนื้อหาแบบพหุภาษา** – ตามความชอบภาษาของผู้ใช้ ชื่อแผ่นงานจะถูกแปลให้เป็นภาษาท้องถิ่น (เช่น `数据` หรือ `Data`) ก่อนส่งไฟล์ เพื่อให้ผู้ใช้ได้รับประสบการณ์ที่ปรับแต่งเฉพาะบุคคล

## ทำไมจึงควรใช้ API การเปลี่ยนชื่อแผ่นงานในสเปรดชีต?

- **เป็นมิตรกับนักพัฒนา** – มี SDK สำหรับหลายภาษาพร้อมเอกสารประกอบอย่างครบถ้วน ทำให้การผสานรวมง่ายกว่าการสร้างโซลูชันแบบกำหนดเอง
- **ลดภาระงาน** – ทำให้การเปลี่ยนชื่อแผ่นงานเป็นอัตโนมัติ ลดความพยายามในการทำงานด้วยตนเอง
- **โมเดลการชำระเงินตามการใช้งาน** – เรียกเก็บค่าบริการเฉพาะเมื่อมีการเรียกใช้ API เท่านั้น ไม่ต้องจ่ายค่าใบอนุญาตล่วงหน้า
- **ไม่ต้องดูแลเซิร์ฟเวอร์** – เป็นบริการคลาวด์ จึงไม่จำเป็นต้องจัดการเซิร์ฟเวอร์หรือติดตั้งการอัปเดตซอฟต์แวร์เอง
- **รองรับการอัตโนมัติ** – สนับสนุนการทำให้เอกสารเป็นมาตรฐานอัตโนมัติในเวิร์กโฟลว์ต่างๆ

## วิธีใช้ API การเปลี่ยนชื่อแผ่นงานในสเปรดชีตพร้อม SDK

### ข้อมูลจำเพาะ OpenAPI

<a href="https://reference.aspose.cloud/cells/#/ManagementController/RenameWorksheetInSpreadsheet" target="_blank" rel="noopener noreferrer">ข้อมูลจำเพาะ OpenAPI</a> ระบุอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ ช่วยให้สามารถโต้ตอบ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sheetName=Sheet1&destName=NewSheetName" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/path/to/input.xlsx"
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

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK ซ่อนรายละเอียด HTTP ที่อยู่เบื้องหลัง ทำให้คุณสามารถเปลี่ยนชื่อแผ่นงานด้วยโค้ดน้อยที่สุด ดู repository บน GitHub เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RenameWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RenameWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RenameWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RenameWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RenameWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RenameWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RenameWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RenameWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}