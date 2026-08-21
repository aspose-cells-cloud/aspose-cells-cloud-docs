---
title: "รวมไฟล์ Excel หลายไฟล์เข้าเป็นสมุดงานเดียว – Aspose.Cells Cloud API"
second_title: "เอกสาร"
ArticleTitle: "รวมไฟล์ Excel หลายไฟล์เข้าเป็นไฟล์เดียว – รวมสมุดงานเป็นกลุ่มไปยังรูปแบบมากกว่า 30 รูปแบบ"
linktype: "รวมสมุดงาน"
type: docs
url: /merge-spreadsheets/
keywords: "Aspose.Cells, รวมสมุดงาน, Excel API, สมุดงานบนคลาวด์, รวมเป็นกลุ่ม, การแปลง PDF, รวม CSV, รวม ODS, การอ้างอิง API, SDK"
description: "รวมไฟล์ Excel, CSV หรือ ODS หลายไฟล์ที่อยู่ในเครื่องเข้าเป็นสมุดงานเดียว และแปลงผลลัพธ์ไปยังรูปแบบมากกว่า 30 รูปแบบ (เช่น PDF, HTML) โดยใช้ Aspose.Cells Cloud API พร้อมข้อมูลจุดปลาย (endpoint), พารามิเตอร์, คู่มือการยืนยันตัวตน และตัวอย่าง SDK"
weight: 100
---

รวมไฟล์ Excel, CSV หรือ ODS หลายไฟล์ที่อยู่ในเครื่องเข้าเป็นสมุดงานเดียว และแปลงเป็นรูปแบบเอาต์พุตมากกว่า 30 รูปแบบโดยใช้ API ของ Aspose.Cells Cloud

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ประเภทข้อมูล | ตำแหน่ง | คำอธิบาย |
| --------------- | ------- | ---------------- | ------------------------------------------------------------------------------------------------ |
| Spreadsheet     | ไฟล์    | FormData         | ไฟล์สมุดงานในเครื่องที่จะอัปโหลด รองรับ XLSX, XLS, CSV, ODS เป็นต้น |
| outFormat       | ข้อความ | Query            | รูปแบบเอาต์พุตที่ต้องการ (เช่น `XLSX`, `PDF`, `CSV`, `HTML`) รองรับรูปแบบมากกว่า 30 รูปแบบ |
| mergeInOneSheet | ค่าบูลีน | Query            | `true` → รวมข้อมูลทั้งหมดลงในแผ่นงานเดียว; `false` → รักษาแผ่นงานเดิมไว้แต่ละแผ่น |
| outPath         | ข้อความ | Query (ไม่บังคับ) | พาธของโฟลเดอร์บนคลาวด์ที่จะบันทึกไฟล์ที่รวมแล้ว หากไม่ระบุ จะใช้ตำแหน่งเริ่มต้น |
| outStorageName  | ข้อความ | Query            | ชื่อพื้นที่จัดเก็บบนคลาวด์ที่จะใช้ (ค่าเริ่มต้นหรือแบบกำหนดเอง) |
| fontsLocation   | ข้อความ | Query (ไม่บังคับ) | โฟลเดอร์บนคลาวด์ที่มีฟอนต์แบบกำหนดเองสำหรับการเรนเดอร์ PDF/รูปภาพอย่างถูกต้อง |
| region          | ข้อความ | Query (ไม่บังคับ) | ภาษา和地区สำหรับการจัดรูปแบบตัวเลข วันที่ และสกุลเงิน (เช่น `en-US`, `zh-CN`) |
| password        | ข้อความ | Query (ไม่บังคับ) | รหัสผ่านสำหรับเปิดสมุดงานที่ได้รับการป้องกัน |

### **การตอบกลับ**

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

ไฟล์สามารถดาวน์โหลดโดยตรงหรือบันทึกไปยังตำแหน่งที่ระบุไว้ใน `outPath`

**รายละเอียดการตอบกลับเมื่อสำเร็จ**

| รหัสสถานะ | Content‑Type               | คำอธิบาย |
| ----------- | -------------------------- | ------------------------------------------ |
| 200 OK      | `application/octet-stream` | สตรีมไบนารีของไฟล์สมุดงานที่รวมแล้ว |

**รหัสสถานะ HTTP**

| รหัส | ความหมาย               | คำอธิบาย |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | กรองข้อมูลสำเร็จ; การตอบกลับมีรายละเอียดของปฏิบัติการ |
| 400  | Bad Request           | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | Unauthorized          | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | Payload Too Large     | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | Internal Server Error | เกิดข้อผิดพลาดภายในเซิร์ฟเวอร์ที่ไม่คาดคิด |

## ควรใช้ API รวมสมุดงานในกรณีใด?

### **การศึกษาและแอปพลิเคชันทางวิชาการ**

- **การตรวจการบ้านของนักเรียน** – รวมไฟล์การบ้านของนักเรียนหลายไฟล์เพื่อให้หมายเหตุและตรวจคะแนนอย่างเป็นเอกภาพ
- **การรวบรวมข้อมูลการวิจัย** – รวมสมุดงานข้อมูลจากกลุ่มการทดลองต่างๆ
- **การสร้างสื่อการสอน** – รวมแบบฝึกหัดจากหลายบทเรียนเข้าเป็นสมุดงานข้อสอบเดียว

### **การประมวลผลและวิเคราะห์ข้อมูล**

- **การรวมชุดข้อมูลขนาดเล็ก** – รวมไฟล์ CSV หรือ Excel ที่ส่งออกจากแหล่งต่างๆ
- **การเตรียมข้อมูลก่อนการวิเคราะห์** – รวมไฟล์ข้อมูลที่เกี่ยวข้องก่อนดำเนินการวิเคราะห์
- **การกรอกข้อมูลแม่แบบรายงาน** – เติมข้อมูลลงในแม่แบบรายงานที่ตั้งไว้ล่วงหน้าด้วยข้อมูลที่รวมแล้ว

### **การพัฒนาและสนับสนุนด้านเทคนิค**

- **การเตรียมข้อมูลทดสอบ** – รวมไฟล์เคสทดสอบหลายไฟล์สำหรับการทดสอบอัตโนมัติ
- **การวิเคราะห์ไฟล์บันทึก** – รวมสมุดงานรายงานบันทึกของระบบจากช่วงเวลาต่างๆ
- **การจัดการการกำหนดค่า** – รวมสมุดงานการกำหนดค่าหลายไฟล์เป็นไฟล์การกำหนดค่าเดียว

## เหตุใดจึงควรใช้ API รวมสมุดงาน?

- **เป็นมิตรกับนักพัฒนา** – มี SDK สำหรับหลายภาษา ลดความพยายามในการพัฒนาเมื่อเทียบกับการสร้างโซลูชันแบบกําหนดเอง
- **ลดค่าใช้จ่ายแรงงาน** – ไม่จำเป็นต้องมีเจ้าหน้าที่เฉพาะด้านเพื่อทำงานรวมเอกสารด้วยตนเอง
- **จ่ายตามการใช้งานจริง** – จ่ายเฉพาะสำหรับการเรียกใช้งาน API ที่ใช้จริง ไม่ต้องลงทุนล่วงหน้า
- **ไม่มีค่าใช้จ่ายในการดูแลรักษา** – ไม่ต้องดูแลเซิร์ฟเวอร์ ไม่ต้องอัปเดตซอฟต์แวร์ และไม่ต้องกังวลเรื่องความเข้ากันได้

## วิธีใช้ API รวมสมุดงานด้วย SDK

### ข้อกำหนด OpenAPI

<a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets" rel="noopener noreferrer">ข้อกำหนด OpenAPI</a> ให้คำอธิบาย API ในรูปแบบที่เครื่องอ่านได้ ช่วยให้สามารถโต้ตอบกับ REST โดยตรง

คุณสามารถใช้เครื่องมือ cURL ที่อยู่ในบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/spreadsheet?outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/Book1.xlsx" \
  -F "Spreadsheet=@/path/to/Book2.xlsx"
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

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจากซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถนำข้อมูลเข้าสู่แผ่นงานสมุดงานได้ด้วยโค้ดสั้นๆ โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">คลังข้อมูล GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheets.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheets.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheets.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheets.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheets.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheets.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheets.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheets.go" >}}
{{</tab>}}
{{< /tabs >}}