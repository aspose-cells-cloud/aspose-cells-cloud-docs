---
title: "รวมสเปรดชีตที่ตรงกันในโฟลเดอร์ระยะไกล"
description: "รวมไฟล์สเปรดชีตที่จัดเก็บไว้ในพื้นที่จัดเก็บบนคลาวด์ของ Aspose Cloud ให้เป็นไฟล์เดียว รองรับรูปแบบเอาต์พุตมากกว่า 30 รูปแบบ เช่น PDF, CSV, JSON, XLSX, ODS, XPS และอื่นๆ"
keywords: "Aspose.Cells, รวมสเปรดชีต, โฟลเดอร์ระยะไกล, API, PDF, CSV, JSON, XLSX, ODS, XPS"
weight: 100
type: docs
url: /merge-spreadsheets-in-remote-folder/
---

รวมไฟล์สเปรดชีตหลายไฟล์ที่อยู่ในโฟลเดอร์พื้นที่จัดเก็บระยะไกลของ Aspose Cloud ให้กลายเป็นไฟล์เอาต์พุตเดียว การดำเนินการนี้ทำงานทั้งหมดบนคลาวด์ จึงไม่จำเป็นต้องดาวน์โหลดไฟล์ต้นฉบับมายังเครื่องของคุณ รองรับรูปแบบเอาต์พุตมากกว่า 30 รูปแบบ (PDF, CSV, JSON, XLSX, ODS, XPS, …)

## API MergeSpreadsheetsInRemoteFolder

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### **ความปลอดภัยและการยืนยันตัวตน**

APIs ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### พารามิเตอร์คำขอ <a id="request-parameters"></a>

| ชื่อ                    | ชนิดข้อมูล | ตำแหน่ง | จำเป็น | คำอธิบาย                                                                                          |
| ----------------------- | ---------- | -------- | ------ | -------------------------------------------------------------------------------------------------- |
| **folder**              | สายอักขระ   | query    | **ใช่** | โฟลเดอร์ในพื้นที่จัดเก็บบนคลาวด์ที่มีสเปรดชีตต้นฉบับ                                             |
| **fileMatchExpression** | สายอักขระ   | query    | **ใช่** | รูปแบบสำหรับเลือกไฟล์ (เช่น `*report*.xlsx`) รองรับเครื่องหมายจัตุรัส `*` และเครื่องหมายคำถาม `?` |
| **outFormat**           | สายอักขระ   | query    | **ใช่** | รูปแบบเอาต์พุตที่ต้องการ (`PDF`, `CSV`, `JSON`, `XLSX`, `ODS`, `XPS`, …)                            |
| **mergeInOneSheet**     | ค่าบูลีน    | query    | **ใช่** | `true` – รวมข้อมูลทั้งหมดลงในวORKชีตเดียว `false` – ไฟล์ต้นฉบับแต่ละไฟล์จะอยู่ในวORKชิตของตัวเอง |
| **storageName**         | สายอักขระ   | query    | ไม่จำเป็น | ชื่อพื้นที่จัดเก็บแบบกำหนดเอง หากไม่ระบุ จะใช้พื้นที่จัดเก็บหลักเป็นค่าเริ่มต้น                      |
| **outPath**             | สายอักขระ   | query    | ไม่จำเป็น | โฟลเดอร์ปลายทางสำหรับไฟล์ที่ถูกรวม หากไม่ระบุ ไฟล์จะถูกบันทึกไว้ในโฟลเดอร์ต้นฉบับ                 |
| **outStorageName**      | สายอักขระ   | query    | ไม่จำเป็น | ชื่อพื้นที่จัดเก็บที่จะบันทึกไฟล์ที่ถูกรวม                                                         |
| **fontsLocation**       | สายอักขระ   | query    | ไม่จำเป็น | เส้นทางไปยังโฟลเดอร์ที่มีฟอนต์ที่กำหนดเอง (จำเป็นสำหรับการส่งออกเป็น PDF/รูปภาพ)                  |
| **region**              | สายอักขระ   | query    | ไม่จำเป็น | ภูมิภาคสำหรับการจัดรูปแบบตัวเลข วันที่ และเงินตร (เช่น `en-US`, `de-DE`)                            |
| **password**            | สายอักขระ   | query    | ไม่จำเป็น | รหัสผ่านสำหรับเปิดสเปรดชีตต้นฉบับที่ได้รับการป้องกัน                                               |

## ตัวอย่างคำขอ (cURL) <a id="request-example"></a>

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

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

คุณสามารถดาวน์โหลดไฟล์โดยตรงจาก `FileUrl` หรือบันทึกไว้ในตำแหน่งที่ระบุโดย `outPath`

**รายละเอียดการตอบกลับที่สำเร็จ**

| โค้ดสถานะ | Content‑Type               | คำอธิบาย                                     |
| --------- | -------------------------- | -------------------------------------------- |
| 200 OK    | `application/octet-stream` | สตรีมไบนารีของไฟล์สมุดงานที่ถูกรวบรวม        |
| 202 Accepted | `application/json`         | JSON ที่มี `FileUrl`, `FileName`, เป็นต้น |

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย               | คำอธิบาย                                                        |
| ---- | ---------------------- | --------------------------------------------------------------- |
| 200  | OK                    | ใช้ตัวกรองสำเร็จ; การตอบกลับมีรายละเอียดของการดำเนินการ       |
| 400  | Bad Request           | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | Unauthorized          | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                                |
| 413  | Payload Too Large     | ไฟล์ที่อัปโหลดเกินขีดจำกัดขนาด                                  |
| 500  | Internal Server Error | เกิดข้อผิดพลาดภายในเซิร์ฟเวอร์ที่ไม่คาดคิด                      |

## วิธีใช้ API รวมสเปรดชีตด้วย SDK

### ข้อกำหนด OpenAPI

<a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder" rel="noopener noreferrer">ข้อกำหนด OpenAPI</a> ให้คำอธิบาย API ในรูปแบบที่เครื่องอ่านได้ ทำให้สามารถโต้ตอบกับ REST API โดยตรงได้

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง cURL เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/Book1.xlsx" \
  -F "Spreadsheet=@/path/to/Book2.xlsx"
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

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจาก SDK ซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถนำข้อมูลเข้าไปยังวORKชีตของสเปรดชีตได้ด้วยโค้ดเพียงไม่กี่บรรทัด โปรดดู <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บบน GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

---