---
---
title: "บันทึกสเปรดชีตเป็นรูปแบบอื่น – API ของ Aspose.Cells Cloud (v4.0)"
second_title: "เอกสาร"
ArticleTitle: "วิธีบันทึกสเปรดชีตเป็นไฟล์ในรูปแบบอื่นบนที่จัดเก็บข้อมูลบนคลาวด์: คู่มือแบบทีละขั้นตอน"
linktype: "บันทึกสเปรดชีตเป็น"
type: docs
url: /save-spreadsheet-as/
keywords: "Aspose Cells การแปลงสเปรดชีต บันทึกเป็น API XLSX เป็น PDF ที่จัดเก็บข้อมูลบนคลาวด์ Excel เป็น PDF การส่งออก CSV การแปลงบนคลาวด์"
description: "เรียนรู้วิธีบันทึกสเปรดชีตที่จัดเก็บไว้ใน Aspose Cloud ให้อยู่ในรูปแบบอื่น (เช่น XLSX, PDF, CSV เป็นต้น) โดยใช้ API ของ Aspose.Cells Cloud สำหรับการบันทึกสเปรดชีต คู่มือนี้ประกอบด้วยไวยากรณ์คำขอ พารามิเตอร์ ตัวอย่าง curl และโค้ด SDK"
weight: 100
---

บันทึกสเปรดชีตหรือไฟล์ Excel บนคลาวด์ให้อยู่ในรูปแบบอื่นบนที่จัดเก็บข้อมูลบนคลาวด์

## **API สำหรับการบันทึกสเปรดชีตเป็น**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/saveas
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

### **พารามิเตอร์ของคำขอ**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                                   |
| :-------------- | :----- | :------- | :---------------------------------------------------------------------------------------- |
| name            | String | Path     | **จำเป็น** ชื่อของไฟล์สมุดบันทึกที่ต้องการแปลง                                               |
| format          | String | Query    | **จำเป็น** รูปแบบผลลัพธ์ที่ต้องการ (เช่น `Xlsx`, `PDF`, `CSV`)                                |
| saveOptionsData | Class  | Body     | ข้อมูลตัวเลือกการบันทึกแบบไม่บังคับ หากไม่ระบุจะมีค่าเริ่มต้นเป็น `null`                        |
| folder          | String | Query    | เส้นทางโฟลเดอร์ที่จัดเก็บสมุดบันทึกต้นทางแบบไม่บังคับ หากไม่ระบุจะมีค่าเริ่มต้นเป็น `null`          |
| storageName     | String | Query    | ชื่อที่จัดเก็บข้อมูลแบบกำหนดเองแบบไม่บังคับ หากไม่ระบุจะใช้ที่จัดเก็บข้อมูลเริ่มต้น                 |
| outPath         | String | Query    | เส้นทางผลลัพธ์สำหรับไฟล์ที่แปลงแล้วแบบไม่บังคับ หากไม่ระบุจะมีค่าเริ่มต้นเป็น `null`               |
| outStorageName  | String | Query    | ชื่อที่จัดเก็บข้อมูลสำหรับไฟล์ผลลัพธ์แบบไม่บังคับ                                               |
| fontsLocation   | String | Query    | ตำแหน่งของฟอนต์แบบกำหนดเองแบบไม่บังคับ                                                       |
| region          | String | Query    | การตั้งค่าภูมิภาคของสเปรดชีตแบบไม่บังคับ                                                      |
| password        | String | Query    | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีตแบบไม่บังคับ                                                    |

**รูปแบบผลลัพธ์ที่รองรับ**

| รูปแบบ   | ส่วนขยาย                                          |
| :------- | :----------------------------------------------- |
| Xlsx     | .xlsx                                            |
| Pdf      | .pdf                                             |
| Csv      | .csv                                             |
| Html     | .html                                            |
| Ods      | .ods                                             |
| Xls      | .xls                                             |
| Txt      | .txt                                             |
| Mhtml    | .mhtml                                           |
| Tiff     | .tiff                                            |
| Pptx     | .pptx                                            |
| … (เพิ่มเติม) | ดูข้อมูลจำเพาะของ API เพื่อดูรายการแบบเต็ม (มากกว่า 20 รูปแบบ) |

### **การตอบกลับ**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**ตัวอย่างการตอบกลับข้อผิดพลาด (400 Bad Request)**

```json
{
  "Code": 400,
  "Message": "พารามิเตอร์คำขอไม่ถูกต้อง"
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย              | คำอธิบาย                                                          |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | กรองข้อมูลเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของ operation |
| 400  | Bad Request           | พารามิเตอร์ไม่ครบหรือไม่ถูกต้อง (เช่น ไฟล์ไม่รองรับ)                |
| 401  | Unauthorized          | JWT token ไม่ถูกต้องหรือไม่ระบุ                                   |
| 413  | Payload Too Large     | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                  |
| 500  | Internal Server Error | ข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด                              |

## ควรใช้ API สำหรับการบันทึกสเปรดชีตเป็นในกรณีใด?

### ระบบจัดการเอกสารองค์กร

- บันทึกรายงานทางการเงินเป็นไฟล์ PDF อัตโนมัติ
- สำรองข้อมูลการขายเป็นรูปแบบ CSV เป็นประจำ
- บันทึกแผนโครงการเป็นไฟล์แบบอ่านอย่างเดียวเพื่อป้องกันการเปลี่ยนแปลงโดยไม่ตั้งใจ

### กระบวนการรวมข้อมูลและการทำ ETL

- ส่งออกข้อมูลจากระบบ CRM และบันทึกเป็นเทมเพลต Excel มาตรฐาน
- แปลงข้อมูล ERP เป็น CSV เพื่อนำเข้าสู่ระบบอื่น
- บันทึกข้อมูลดิบเป็น JSON เพื่อส่งผ่าน API

### สถานการณ์การพัฒนาและการทำอัตโนมัติ

- การประมวลผลแบ็กเอนด์สำหรับแอปพลิเคชันเว็บ
- ระบบสร้างรายงานอัตโนมัติ
- แพลตฟอร์มการทำงานร่วมกันบนคลาวด์
- การผสานรวมกระบวนการอนุมัติ
- การสำรองและย้ายข้อมูล

## เหตุใดจึงควรใช้ API สำหรับการบันทึกสเปรดชีตเป็น?

- **เป็นมิตรกับนักพัฒนา** – มี SDK สำหรับภาษาต่างๆ พร้อมเอกสารประกอบที่ละเอียด ช่วยให้การผสานรวมง่ายขึ้น
- **ประหยัดแรงงาน** – จัดการการแปลงบนเซิร์ฟเวอร์ ลดความจำเป็นในการเขียนโค้ดการแปลงด้วยตนเอง
- **มีค่าใช้จ่ายตามการใช้งาน** – เรียกเก็บค่าใช้จ่ายเฉพาะ API call ที่ดำเนินการจริง ไม่มีค่าลิขสิทธิ์ล่วงหน้า
- **ไม่ต้องดูแลเซิร์ฟเวอร์** – บริการทำงานบนคลาวด์ ไม่ต้องจัดการโครงสร้างพื้นฐานการแปลง
- **รองรับรูปแบบหลากหลาย** – รองรับการแปลงระหว่างรูปแบบสเปรดชีตมากกว่า 20 รูปแบบ
- **คงความถูกต้องของข้อมูล** – รักษาเลย์เอาต์ สูตร และรูปแบบการจัดรูปแบบไว้ระหว่างการแปลง

## วิธีใช้ API สำหรับการบันทึกสเปรดชีตเป็นด้วย SDK?

### ข้อมูลจำเพาะของ API สำหรับการบันทึกสเปรดชีตเป็น

[ข้อมูลจำเพาะของ API สำหรับการบันทึกสเปรดชีตเป็น](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/SaveSpreadsheetAs) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ ช่วยให้คุณสามารถโต้ตอบกับ REST ได้โดยตรงจากเว็บเบราว์เซอร์

**ตัวอย่างพร้อมเนื้อหาคำขอและ curl**

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง cURL เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/saveas?format=pdf&outPath=output.pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{"SaveOptions":{"SaveFormat":"pdf"}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจากซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถบันทึกสเปรดชีตเป็นรูปแบบอื่นได้ด้วยโค้ดน้อยที่สุด โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_WorkbookSaveAs.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_WorkbookSaveAs.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_WorkbookSaveAs.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_WorkbookSaveAs.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_WorkbookSaveAs.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_WorkbookSaveAs.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_WorkbookSaveAs.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_WorkbookSaveAs.go" >}}
{{</tab>}}
{{< /tabs >}}