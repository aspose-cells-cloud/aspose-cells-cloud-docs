---
title: "ส่งออกวัตถุ OLE – API คลาวด์ของ Aspose.Cells"
second_title: "เอกสาร"
linktitle: "วัตถุ OLE"
type: docs
url: /th/export-excel-ole-object/
aliases: [  /th/export/excel-ole-object/ ]
keywords: "Aspose.Cells, วัตถุ OLE, การส่งออก, Excel, API คลาวด์, PDF, PNG, DOCX, PPTX"
description: "ส่งออกวัตถุ OLE จากสมุดงาน Excel โดยใช้ API คลาวด์ของ Aspose.Cells ศึกษารูปแบบคำขอ พารามิเตอร์ ตัวอย่าง cURL และการจัดการข้อผิดพลาด"
weight: 20
ArticleTitle: "ส่งออกวัตถุ OLE – API คลาวด์ของ Aspose.Cells"
---

## **API REST**

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **การรักษาความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>


### พารามิเตอร์คำขอ

| พารามิเตอร์     | ตำแหน่ง   | ประเภท | จำเป็น | คำอธิบาย                                                                 |
| --------------- | --------- | ------ | ------ | -------------------------------------------------------------------------- |
| `file`          | Form‑data | ไฟล์   | ใช่    | สมุดงาน Excel (`.xlsx`, `.xls` เป็นต้น) ที่มีวัตถุ OLE                    |
| `outputFormat`  | Query     | สตริง | ใช่    | รูปแบบเป้าหมายสำหรับวัตถุที่ส่งออก (`pdf`, `png`, `jpeg`, `docx`, `pptx`) |
| `objectType`    | Query     | สตริง | ใช่    | ค่าคงที่ `oleobject`                                                      |


### การตอบกลับ

คำขอที่ประสบความสำเร็จจะส่งคืนวัตถุ JSON ซึ่งแสดงรายการไฟล์ที่ส่งออก:

```json
{
  "Files": [
    {
      "Filename": "OLESlide.ppt",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "OLEDoc.docx",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                   | คำอธิบาย                                               |
|------|-----------------------------|--------------------------------------------------------|
| 200  | สำเร็จ (OK)                | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของปฏิบัติการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)     |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                          |
| 413  | ข้อมูลส่งออกมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดเกินขีดจำกัดขนาด                         |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | ข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์                      |
## วิธีใช้ PostExport API ด้วย SDK

### ข้อกำหนด PostExport API


[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้สาธารณะ และช่วยให้คุณดำเนินการโต้ตอบ REST โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API คลาวด์ด้วย cURL


```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format=pdf" \
  -H "Authorization: Bearer $ACCESS_TOKEN" \
  -F "file=@MyWorkbook.xlsx" \
  -F "outputFormat=pdf"
```

### OLE object คืออะไร?

**วัตถุ OLE (Object Linking and Embedding)** คือการฝังเนื้อหาภายนอก—เช่น เอกสาร Word สไลด์ PowerPoint รูปภาพ หรือไฟล์อื่นๆ—ไว้ภายในสมุดงาน Excel เมื่อส่งออก เนื้อหาที่ฝังไว้จะถูกแยกออกมาและบันทึกในรูปแบบที่ต้องการ

### ภาพรวมจุดปลาย (Endpoint)

`POST https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format={outputFormat}`

- `objectType` – ต้องตั้งค่าเป็น `oleobject`
- `format` – รูปแบบผลลัพธ์ที่ต้องการ (เช่น `pdf`, `png`, `jpeg`, `docx`, `pptx`)

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่ภารกิจในโครงการของคุณ โปรดตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
---