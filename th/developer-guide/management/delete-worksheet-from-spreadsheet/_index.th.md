---
---
title: "API สำหรับการลบแผ่นงาน Excel บนคลาวด์จาก Aspose.Cells - ลบแผ่นงานออกจากสมุดงานอย่างเป็นโปรแกรม"
second_title: "เอกสาร"
ArticleTitle: "วิธีลบแผ่นงานออกจาก Excel - ลบแผ่นงานออกจากสมุดงาน"
linktype: "ลบแผ่นงานออกจากสเปรดชีต"
type: docs
url: /delete-worksheet-from-spreadsheet/
keywords: "Aspose Cells, API ลบแผ่นงาน, การลบแผ่นงาน Excel, สเปรดชีตบนคลาวด์, REST API"
description: "เรียนรู้วิธีลบแผ่นงานออกจากไฟล์ Excel โดยใช้ Aspose.Cells Cloud API รวมถึง endpoint, พารามิเตอร์, ตัวอย่าง cURL และตัวอย่าง SDK"
weight: 100
---

ลบแผ่นงานออกจากสมุดงาน Excel อย่างเป็นโปรแกรมโดยใช้ Aspose.Cells Cloud API ลบแผ่นงานเดียวหรือหลายแผ่นอย่างปลอดภัย ปรับโครงสร้างสมุดงานให้เรียบร้อย และทำให้การปรับแต่งสเปรดชีตเป็นไปโดยอัตโนมัติ API แบบ RESTful สำหรับการจัดการ Excel ระดับองค์กรและเวิร์กโฟลว์การประมวลผลเอกสาร

## API สำหรับการลบแผ่นงานออกจากสเปรดชีต

### Web API

```http
PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet?sheetName={sheetName}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}"
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### พารามิเตอร์ของคำขอ:

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย                                                                                                                                                                                             |
| :------------- | :----- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet    | ไฟล์   | FormData | **จำเป็น** ไฟล์สมุดงาน Excel ต้นทาง (.xlsx, .xls เป็นต้น) ที่จะลบแผ่นงานออกจาก                                                                                                                                                                |
| sheetName      | สตริง | Query    | **จำเป็น** ชื่อที่แน่นอนของแผ่นงานที่ต้องการลบ (เช่น `Sheet1`, `TemporaryData`)                                                                                                          |
| outPath        | สตริง | Query    | **ไม่บังคับ** เส้นทางโฟลเดอร์เป้าหมายในพื้นที่จัดเก็บบนคลาวด์ที่จะบันทึกสมุดงานที่แก้ไขแล้ว หากไม่ระบุหรือเป็น `null` สมุดงานจะถูกบันทึกไว้ที่ตำแหน่งเดียวกับไฟล์ต้นทางหรือเส้นทางเริ่มต้น                                                                 |
| outStorageName | สตริง | Query    | **ไม่บังคับ** ตัวระบุของบริการพื้นที่จัดเก็บบนคลาวด์ (เช่น `ProjectStorage`) ที่จะบันทึกไฟล์ผลลัพธ์ หากไม่ระบุจะใช้พื้นที่จัดเก็บเริ่มต้น                                 |
| region         | สตริง | Query    | **ไม่บังคับ** การตั้งค่าภาษา和地区 (เช่น `it-IT`) ซึ่งอาจมีผลต่อสูตรหรือข้อมูลที่เฉพาะเจาะจงตามภูมิภาคในระหว่างการบันทึก                                                                                                                                            |
| password       | สตริง | Query    | **ไม่บังคับ** รหัสผ่านที่จำเป็นในการเปิดและแก้ไขสเปรดชีตที่ป้องกันด้วยรหัสผ่าน ไม่ต้องระบุหากไฟล์ไม่ได้เข้ารหัส                                                                             |

### คำตอบ

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

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย               | คำอธิบาย                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | สำเร็จ (OK)                    | กรองถูกใช้งานเรียบร้อยแล้ว; คำตอบประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request)           | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ)      |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)          | JWT token ไม่ถูกต้องหรือขาดหาย                                     |
| 413  | ข้อมูลส่งไปมีขนาดใหญ่เกินไป (Payload Too Large)     | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                 |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | ข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์                                          |

## ควรใช้ API สำหรับการลบแผ่นงานออกจากสเปรดชีตในกรณีใด?

- **การประมวลผลหลังการสร้างรายงานอัตโนมัติ** – หลังจากสร้างรายงานการเงินขั้นสุดท้าย ให้ลบแผ่นงานแบบกลางที่ใช้ในการคำนวณชั่วคราวออกโดยอัตโนมัติ เพื่อรักษาไฟล์สุดท้ายให้สะอาดและมืออาชีพ
- **การปรับปรุงเทมเพลตไฟล์แบบไดนามิก** – เมื่อผู้ใช้สร้างเอกสารที่ปรับแต่งเอง (เช่น ใบเสนอราคา) จากเทมเพลต ให้ลบหน้าทางเลือกที่ไม่ได้เลือกออก
- **การปรับปรุงการเก็บถาวรเวิร์กโฟลว์** – หลังจากเสร็จสิ้นโครงการหรือการตรวจสอบ ให้ลบแผ่นงานแบบร่างหรือที่ใช้ร่วมกันออก เหลือเฉพาะเวอร์ชันสุดท้ายไว้สำหรับการเก็บถาวรและการปฏิบัติตามข้อกำหนด

## เหตุใดจึงควรใช้ API สำหรับการลบแผ่นงานออกจากสเปรดชีต?

- **เป็นมิตรกับนักพัฒนา** – Aspose.Cells Cloud มี SDK ให้ใช้งานในหลายภาษา ช่วยให้พัฒนาได้อย่างรวดเร็วและมีเอกสารประกอบที่ครอบคลุม
- **ลดต้นทุนแรงงาน** – ไม่จำเป็นต้องมีบุคลากรเฉพาะเพื่อรวมเอกสารด้วยตนเอง
- **จ่ายตามการใช้งาน (Pay-per-Use)** – ไม่ต้องลงทุนล่วงหน้า จ่ายเฉพาะค่า API ที่คุณใช้งานจริงเท่านั้น
- **ไม่มีต้นทุนการดูแลรักษา** – ไม่ต้องดูแลเซิร์ฟเวอร์ ไม่ต้องอัปเดตซอฟต์แวร์ และไม่มีปัญหาด้านความเข้ากันได้

## วิธีใช้ API สำหรับการลบแผ่นงานออกจากสเปรดชีตด้วย SDK

### ข้อมูลจำเพาะ API สำหรับการลบแผ่นงานออกจากสเปรดชีต

<a href="https://reference.aspose.cloud/cells/#/ManagementController/DeleteWorksheetFromSpreadsheet" rel="noopener noreferrer">ข้อมูลจำเพาะ API สำหรับการลบแผ่นงานออกจากสเปรดชีต</a> กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้จากภายนอก ช่วยให้คุณสามารถเรียกใช้การโต้ตอบ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API โดยใช้ cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="คำตอบ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet?sheetName=Sheet1" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/path/to/input.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (เข้ารหัสแบบ Base64)",
  "contentType": "ประเภท MIME",
  "fileDownloadName": "ชื่อไฟล์ (ไม่บังคับ)"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจาก SDK ซ่อนรายละเอียดระดับต่ำไว้และช่วยให้คุณลบแผ่นงานได้ด้วยโค้ดเพียงเล็กน้อย โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer"> kho ข้อมูล GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}

---