---
---
title: "Aspose.Cells Cloud Excel Password Protection Web API – สร้างระบบอัตโนมัติในการเข้ารหัสลับด้วยรหัสผ่านการเปิดและแก้ไข"
second_title: "คู่มือนักพัฒนาสำหรับการป้องกัน Excel"
ArticleTitle: "เครื่องมือป้องกันรหัสผ่าน Excel – ตั้งค่ารหัสผ่านการเปิดและแก้ไข – รักษาความปลอดภัยสมุดงานของคุณ"
linktype: "ป้องกันสมุดงาน"
type: docs
url: /protect-spreadsheet/
keywords: "Aspose.Cells, การป้องกันรหัสผ่าน Excel, API, รหัสผ่านการเปิด, รหัสผ่านการแก้ไข, ที่จัดเก็บบนคลาวด์, ความปลอดภัยของสมุดงาน"
description: "รักษาความปลอดภัยไฟล์ Excel ด้วยระบบโปรแกรมด้วย Aspose.Cells Cloud ตั้งค่ารหัสผ่านการเปิดและแก้ไขผ่านคำขอ API เพียงครั้งเดียว รองรับ .xlsx, .xls และที่จัดเก็บบนคลาวด์ ลองใช้งานฟรีได้เลย"
weight: 100
---

สร้างระบบป้องกันรหัสผ่าน Excel แบบอัตโนมัติในระดับองค์กรด้วย API สำหรับนักพัฒนาของเรา—ใช้รหัสผ่านการเปิดและแก้ไขโดยผ่านการเขียนโค้ด ใช้งานได้ดีในกระบวนการขององค์กรและรองรับทั้งรูปแบบ .xlsx และรูปแบบเก่า รับเอกสารประกอบและเริ่มต้นใช้งานแบบฟรีได้เลยวันนี้

## **API ป้องกันสมุดงาน**

### **Web API**

```http
PUT https://api.aspose.cloud/v4.0/cells/protection/spreadsheet
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

```bash
-H "Authorization: Bearer {access_token}"
```

### **พารามิเตอร์คำขอ:**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | Path/Query String/HTTPBody | คำอธิบาย                                                                                                                                    |
| :------------- | :----- | :------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | ไฟล์   | FormData                   | ไฟล์สมุดงาน Excel ที่จะอัปโหลดและป้องกันด้วยการเข้ารหัสด้วยรหัสผ่าน                                                                  |
| openPassword   | ข้อความ | Query                      | รหัสผ่านที่จำเป็นในการเปิด (ถอดรหัส) สมุดงานที่ได้รับการป้องกัน                                                                          |
| modifyPassword | ข้อความ | Query                      | รหัสผ่านที่จำเป็นในการเปิดใช้งานการแก้ไขหรือการแก้ไขเนื้อหาของสมุดงาน                                                                  |
| outPath        | ข้อความ | Query                      | (ไม่บังคับ) ระบุเส้นทางโฟลเดอร์ผลลัพธ์ที่จะบันทึกสมุดงานที่ได้รับการป้องกัน หากไม่ระบุ ไฟล์จะส่งกลับในส่วนของคำขอตอบกลับ                   |
| outStorageName | ข้อความ | Query                      | ชื่อของที่จัดเก็บบนคลาวด์ที่ใช้สำหรับจัดเก็บไฟล์ที่ได้รับการป้องกันผลลัพธ์                                                                  |
| region         | ข้อความ | Query                      | ระบุการตั้งค่าภูมิภาค/วัฒนธรรม (เช่น รูปแบบวันที่ การจัดรูปแบบตัวเลข) ที่จะใช้กับสมุดงานระหว่างการประมวลผล                                          |

**การยืนยันตัวตน**  
คำขอทั้งหมดไปยัง Protect Spreadsheet API จำเป็นต้องมี OAuth 2.0 access token ที่ถูกต้อง ใส่ token ลงใน header `Authorization`:

```http
Authorization: Bearer {access_token}
```

Token ต้องได้รับจากจุดจบการยืนยันตัวตนของ Aspose Cloud และต้องมี scope **Cells** รวมอยู่ด้วย

## **ผลลัพธ์การตอบกลับ**

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
| 200  | OK                    | กรองถูกใช้งานสำเร็จ; ผลตอบกลับมีรายละเอียดของการดำเนินการ |
| 400  | Bad Request           | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)      |
| 401  | Unauthorized          | JWT token ไม่ถูกต้องหรือขาดหาย                                     |
| 413  | Payload Too Large     | ไฟล์ที่อัปโหลดเกินขีดจำกัดขนาด                                     |
| 500  | Internal Server Error | เกิดข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด                                          |

## ควรใช้ Protect Spreadsheet API ที่ไหน?

- **รักษาความปลอดภัยข้อมูลทางการเงินที่ละเอียดอ่อน** – ป้องกันไฟล์ Excel ที่มีข้อมูลงบประมาณ ใบแจ้งหนี้ หรือเงินเดือนด้วยรหัสผ่านการเปิดและแก้ไข เพื่อป้องกันการเข้าถึงหรือแก้ไขโดยไม่ได้รับอนุญาต
- **แบ่งปันรายงานที่เป็นความลับอย่างปลอดภัย** – รับประกันว่าผู้รับที่ได้รับอนุญาตเท่านั้นที่สามารถดูหรือแก้ไขรายงานธุรกิจ การตรวจสอบ หรือรายงานการปฏิบัติตามข้อบังคับเมื่อส่งภายในหรือภายนอกองค์กร
- **ทำให้ความปลอดภัยของเอกสารเป็นระบบอัตโนมัติในกระบวนการ** – ผนวก API เข้ากับระบบองค์กร (เช่น ERP, CRM) เพื่อป้องกันรหัสผ่านสมุดงานที่สร้างขึ้นโดยอัตโนมัติก่อนการจัดเก็บหรือการส่งทางอีเมล
- **บังคับใช้การเข้าถึงแบบอ่านเท่านั้น** – อนุญาตให้ผู้ใช้เปิดรายงานเพื่อดูเท่านั้น โดยจำกัดการแก้ไขด้วยรหัสผ่านการแก้ไขแยกต่างหาก—เหมาะสำหรับแม่แบบหรือชุดข้อมูลที่เสร็จสมบูรณ์แล้ว
- **ปฏิบัติตามข้อกำหนดด้านการกำกับดูแล** – ช่วยให้สอดคล้องกับข้อกำหนด GDPR, HIPAA หรือ SOX โดยการเข้ารหัสข้อมูลสมุดงานที่ละเอียดอ่อนทั้งเมื่อจัดเก็บและขณะส่งผ่านระบบเครือข่ายผ่านการป้องกันอัตโนมัติ

## ทำไมจึงควรใช้ Protect Spreadsheet API?

- **เป็นมิตรกับนักพัฒนา** – Aspose.Cells Cloud มี SDK รองรับหลายภาษา ช่วยให้พัฒนาได้อย่างรวดเร็ว และมาพร้อมเอกสารประกอบที่ครบถ้วน เมื่อเทียบกับการสร้างโซลูชันแบบปรับแต่งเอง ช่วยลดภาระงานพัฒนาได้อย่างมาก
- **ลดความจำเป็นในการจ้างงาน** – ทำให้การรวบรวมและรักษาความปลอดภัยของเอกสารเป็นระบบอัตโนมัติ ลดความจำเป็นในการจ้างบุคลากรเฉพาะด้าน
- **จ่ายตามการใช้งานจริง** – ไม่ต้องลงทุนล่วงหน้า จ่ายเฉพาะค่า API call ที่ใช้งานจริงเท่านั้น
- **ไม่มีค่าใช้จ่ายในการดูแลรักษา** – ไม่มีเซิร์ฟเวอร์ให้ดูแล ไม่มีอัปเดตซอฟต์แวร์ และไม่มีปัญหาเรื่องความเข้ากันได้
- **คงรูปแบบ Excel ต้นฉบับทั้งหมดไว้** ขณะใช้การป้องกันรหัสผ่าน ทำให้สมุดงานที่ได้รับการป้องกันมีหน้าตาเหมือนกับไฟล์ต้นฉบับเป๊ะ

## วิธีใช้ Protect Spreadsheet API ด้วย SDKs

### **ข้อกำหนด OpenAPI**

[Protect Spreadsheet API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet) ให้ programming interface ที่เข้าถึงได้จากสาธารณะ เพื่อสนับสนุนการใช้งาน REST โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL บรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="ผลลัพธ์ตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/protection/spreadsheet?openPassword=MyOpenPwd&modifyPassword=MyModifyPwd" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/workbook.xlsx"
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

### **ใช้งาน Aspose.Cells Cloud SDKs**

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จัดการรายละเอียดเบื้องต้นทั้งหมด ทำให้คุณสามารถใช้ฟังก์ชันการป้องกันสมุดงานได้ด้วยโค้ดน้อยที่สุด โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการโต้ตอบกับบริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ProtectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ProtectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ProtectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ProtectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ProtectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ProtectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ProtectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ProtectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}