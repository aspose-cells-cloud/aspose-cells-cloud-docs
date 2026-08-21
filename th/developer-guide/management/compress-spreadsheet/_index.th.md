---
---
title: "API คลาวด์ Aspose.Cells สำหรับการบีบอัดไฟล์ Excel – ลดขนาดไฟล์สเปรดชีตอย่างเป็นโปรแกรม"
second_title: "เอกสาร"
ArticleTitle: "วิธีการบีบอัดไฟล์ Excel – ลดขนาดสเปรดชีตและเพิ่มประสิทธิภาพการทำงาน"
linktype: "บีบอัดสเปรดชีต"
type: docs
url: /compress-spreadsheet/
keywords: "การบีบอัด Excel, Aspose.Cells Cloud, การลดขนาดไฟล์สเปรดชีต, API, การปรับแต่งเวิร์กบุ๊ก"
description: "เรียนรู้วิธีการบีบอัดเวิร์กบุ๊ก Excel ด้วย API ของ Aspose.Cells Cloud พร้อมตัวอย่างแบบทีละขั้นตอน พารามิเตอร์ การรับรองความถูกต้อง และแนวทางปฏิบัติที่ดีที่สุด"
weight: 100
---

บีบอัดสเปรดชีต Excel อย่างเป็นโปรแกรมและลดขนาดไฟล์ด้วย API ของ Aspose.Cells Cloud ปรับปรุงประสิทธิภาพการทำงานของเวิร์กบุ๊กโดยการลบข้อมูลที่ไม่ได้ใช้งาน บีบอัดวัตถุที่ฝังอยู่ และล้างรูปแบบต่างๆ API แบบ RESTful นี้ช่วยให้สามารถสร้างกระบวนการอัตโนมัติสำหรับการบีบอัดและปรับแต่งไฟล์ Excel ได้

## **API สำหรับบีบอัดสเปรดชีต**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

### **ความปลอดภัยและการรับรองความถูกต้อง**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การรับรองความถูกต้องด้วยโทเคน JWT</a>

```bash
-H "Authorization: Bearer {access_token}"
```

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | Path/Query/String/HTTP Body | คำอธิบาย                                                                                                                           |
| ---------------- | --------- | --------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | ไฟล์     | FormData                    | **จำเป็น** ไฟล์เวิร์กบุ๊ก Excel ต้นฉบับ (`.xlsx`, `.xls` เป็นต้น) ที่ต้องการบีบอัด                                                 |
| level            | จำนวนเต็ม | Query                       | **ไม่บังคับ** ระดับความเข้มของการบีบอัด (0 = เร็วที่สุด/ต่ำสุด, 9 = ช้าที่สุด/สูงสุด) หากไม่ระบุจะใช้ค่าเริ่มต้นที่สมดุล (5) โดยอัตโนมัติ |
| outPath          | สายอักขระ | Query                       | **ไม่บังคับ** เส้นทางโฟลเดอร์ปลายทางในพื้นที่จัดเก็บบนคลาวด์ หากไม่ระบุ ไฟล์จะถูกบันทึกไว้ในโฟลเดอร์เดียวกับเวิร์กบุ๊กต้นฉบับ     |
| outStorageName   | สายอักขระ | Query                       | **จำเป็น** ตัวระบุของบริการพื้นที่จัดเก็บบนคลาวด์ที่กำหนดค่าไว้ (เช่น `CorporateDrive`)                                          |
| region           | สายอักขระ | Query                       | **ไม่บังคับ** การตั้งค่าภาษา和地区 (เช่น `de-DE`) ซึ่งอาจมีผลต่อการจัดการข้อมูลตามภูมิภาค                                        |
| password         | สายอักขระ | Query                       | **ไม่บังคับ** รหัสผ่านสำหรับถอดรหัสสเปรดชีตที่ได้รับการป้องกันไว้ ปล่อยว่างไว้หากไฟล์ไม่ได้เข้ารหัสไว้                              |

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

| รหัส | ความหมาย               | คำอธิบาย                                                         |
| ---- | ---------------------- | ---------------------------------------------------------------- |
| 200  | สำเร็จ (OK)            | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของคำสั่งปฏิบัติการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ)     |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                                   |
| 413  | ข้อมูลในคำขอใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                         |

## ควรใช้ API สำหรับบีบอัดสเปรดชีตในกรณีใด?

- **การจัดส่งรายงานอัตโนมัติ** – บีบอัดงบการเงินรายเดือนก่อนส่งผ่านอีเมล เพื่อให้แน่ใจว่าการส่งสำเร็จและเพิ่มประสบการณ์ผู้รับ
- **การปรับปรุงไฟล์ที่ผู้ใช้อัปโหลด** – บีบอัดไฟล์ Excel ที่ผู้ใช้อัปโหลดในเบื้องหลัง เพื่อประหยัดพื้นที่จัดเก็บบนคลาวด์และลดต้นทุนการจัดเก็บ
- **การประมวลผลและย้ายข้อมูลผ่านกระบวนการ** – บีบอัดไฟล์ Excel ชั่วคราวที่สร้างขึ้นระหว่างกระบวนการ ETL เพื่อเร่งความเร็วการถ่ายโอนผ่านเครือข่ายและลดภาระการจัดเก็บชั่วคราว

## เหตุใดจึงควรใช้ API สำหรับบีบอัดสเปรดชีต?

- **เป็นมิตรกับนักพัฒนา** – Aspose.Cells Cloud มีไลบรารี SDK รองรับหลายภาษา ช่วยให้พัฒนาได้อย่างรวดเร็ว พร้อมเอกสารที่ครบถ้วน
- **ลดต้นทุนแรงงาน** – ไม่จำเป็นต้องมีบุคลากรเฉพาะเพื่อรวมเอกสารด้วยตนเอง
- **โครงสร้างราคาแบบจ่ายตามการใช้งาน** – ไม่ต้องลงทุนล่วงหน้า จ่ายเฉพาะค่า API ที่ใช้จริงเท่านั้น
- **ไม่ต้องดูแลเซิร์ฟเวอร์** – ไม่มีเซิร์ฟเวอร์ให้ดูแล ไม่มีโปรแกรมอัปเดต และไม่มีปัญหาเรื่องความเข้ากันได้

## วิธีใช้ API สำหรับบีบอัดสเปรดชีตด้วย SDK

### ข้อมูลจำเพาะ API สำหรับบีบอัดสเปรดชีต

[ข้อมูลจำเพาะ API สำหรับบีบอัดสเปรดชีต](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet) มีอินเทอร์เฟซที่เข้าถึงได้สาธารณะสำหรับการโต้ตอบแบบ REST ซึ่งช่วยให้สามารถเรียก API โดยตรงจากเว็บเบราว์เซอร์ได้

คุณสามารถใช้เครื่องมือ cURL บนบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ API บนคลาวด์ผ่าน cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/compress?level=5&outStorageName=MyStorage" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/input.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (เข้ารหัส Base64)",
  "contentType": "ประเภท MIME",
  "fileDownloadName": "ชื่อไฟล์ (ไม่บังคับ)"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เพราะซ่อนรายละเอียดระดับต่ำไว้และช่วยให้คุณบีบอัดสเปรดชีตได้ด้วยเพียงไม่กี่บรรทัดของโค้ด โปรดดูที่ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการโต้ตอบกับบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CompressSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CompressSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CompressSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CompressSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CompressSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CompressSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CompressSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CompressSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}