---
---
title: "Aspose.Cells Cloud Web API - แปลงข้อมูลตารางในไฟล์ Excel ที่มีอยู่ในเครื่องเป็นไฟล์ภาพ - เครื่องมือออนไลน์ฟรี"
secondtitle: "เอกสาร"
articletitle: "วิธีการแปลงข้อมูลตารางในไฟล์สเปรดชีตในเครื่องเป็นไฟล์ภาพ: คู่มือแบบทีละขั้นตอน"
linktitle: "แปลงตารางเป็นภาพ"
type: docs
url: /convert-table-to-image/
keywords: "Aspose.Cells, Cloud API, แปลงตารางเป็นภาพ, Excel, PNG, JPEG, TIFF, BMP, SVG"
description: "แปลงตารางในไฟล์สเปรดชีต Excel ที่มีอยู่ในเครื่องเป็นไฟล์ภาพได้อย่างรวดเร็วด้วย Aspose.Cells Cloud API รองรับรูปแบบ PNG, JPEG, TIFF, BMP, SVG และอื่นๆ อีกหลายรูปแบบ"
weight: 100
---

ส่งออกข้อมูลตารางจากไฟล์ Excel ที่มีอยู่ในเครื่องเป็นไฟล์ [Image](https://docs.fileformat.com/image/) ผ่าน Cloud API

**รูปแบบภาพที่รองรับ:**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **API สำหรับแปลงตารางเป็นภาพ**

ก่อนใช้งานจุดสิ้นสุด (endpoint) นี้ โปรดตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังนี้:

- โทเคน JWT ที่ถูกต้องซึ่งได้มาจากการยืนยันตัวตนกับ Aspose.Cells Cloud
- บัญชีพื้นที่จัดเก็บข้อมูลที่เข้าถึงได้ หากคุณต้องการใช้พารามิเตอร์ `outPath` หรือ `outStorageName`
- สมุดงานต้นฉบับ (ไฟล์ Excel ที่มีอยู่ในเครื่อง) ต้องสามารถอ่านได้ และหากมีการป้องกันไว้ ต้องระบุรหัสผ่านที่ถูกต้อง

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/image
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยสูงและต้องใช้การยืนยันตัวตนแบบ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">โทเคน JWT</a>

### **พารามิเตอร์คำขอ:**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | Path/Query String/HTTP Body | คำอธิบาย                                                                                                                                              |
| :--------------- | :----- | :-------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | ไฟล์   | FormData                    | อัปโหลดไฟล์สเปรดชีต                                                                                                                                   |
| worksheet        | สตริง  | Query                       | ชื่อแผ่นงานของสเปรดชีต/Excel                                                                                                                         |
| tableName        | สตริง  | Query                       | ชื่อตารางที่ต้องการแปลง                                                                                                                              |
| format           | สตริง  | Query                       | รูปแบบไฟล์ภาพที่ต้องการ (เช่น png, svg)                                                                                                               |
| outPath          | สตริง  | Query                       | (ไม่บังคับ) พาธของโฟลเดอร์ที่จะบันทึกไฟล์ภาพที่แปลงแล้ว ค่าเริ่มต้นคือ null                                                                          |
| outStorageName   | สตริง  | Query                       | ระบุชื่อพื้นที่จัดเก็บสำหรับไฟล์ผลลัพธ์                                                                                                               |
| fontsLocation    | สตริง  | Query                       | ใช้ฟอนต์ที่กำหนดเองหากจำเป็น                                                                                                                         |
| region           | สตริง  | Query                       | การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) มีผลต่อการจัดรูปแบบตัวเลข การแปลงวันที่ และพฤติกรรมที่เกี่ยวข้องกับภูมิภาค               |
| password         | สตริง  | Query                       | รหัสผ่านที่จำเป็นสำหรับการเข้าถึงไฟล์สเปรดชีต                                                                                                        |

### **การตอบกลับ**

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

| รหัส | ความหมาย                 | คำอธิบาย                                                                 |
| ---- | ------------------------- | ------------------------------------------------------------------------ |
| 200  | สำเร็จ (OK)              | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)                 |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                                          |
| 413  | ข้อมูลโหลดมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                       |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                               |

## **คุณควรใช้ API แปลงตารางเป็นภาพในกรณีใด?**

- **ภาพนิ่งของรายงานแบบคงที่**: แปลงตารางทางการเงิน ผลลัพธ์การคำนวณ หรือข้อมูลที่จัดรูปแบบอื่นๆ เป็นภาพเพื่อใช้ในรายงาน PDF สไลด์ PowerPoint หรือเอกสารสิ่งพิมพ์ที่ไม่ต้องการการแก้ไขต่อ
- **การนำเสนอข้อมูลในรูปภาพสำหรับการนำเสนอ**: แปลงตารางสเปรดชีตที่ซับซ้อน—รวมถึงการจัดรูปแบบตามเงื่อนไขหรือการนำเสนอภาพแบบง่าย—เป็นภาพที่สามารถฝังในงานนำเสนอ (PPTX, Google Slides)
- **เอกสารคู่มือและสื่อการฝึกอบรม**: จับภาพตัวอย่างสเปรดชีต แม่แบบ หรือแบบฟอร์มป้อนข้อมูลเป็นภาพสำหรับคู่มือผู้ใช้ คู่มือการใช้งาน หรือบทความฐานความรู้
- **ภาพตัวอย่างขนาดย่อ**: สร้างภาพขนาดย่อของส่วนสำคัญของสเปรดชีตสำหรับใช้ในเบราว์เซอร์ไฟล์ คลังเอกสาร หรือผลลัพธ์การค้นหา

## เหตุใดคุณจึงควรใช้ API แปลงตารางเป็นภาพ?

- **เป็นมิตรกับนักพัฒนา**: Aspose.Cells Cloud มี SDK สำหรับภาษาโปรแกรมต่างๆ หลายภาษา ช่วยให้การพัฒนาทำได้อย่างรวดเร็ว และมีเอกสารประกอบที่ครอบคลุม เมื่อเทียบกับการสร้างโซลูชันการเรนเดอร์แบบกำหนดเอง การใช้บริการนี้ช่วยลดภาระงานพัฒนาได้อย่างมาก
- **ประหยัดต้นทุน**: คุณสามารถแปลงข้อมูลตารางได้โดยไม่จำเป็นต้องอัปโหลดสมุดงานทั้งหมดก่อน ช่วยประหยัดพื้นที่จัดเก็บและลดค่าใช้จ่าย
- **รักษาความแม่นยำของพิกเซล**: สร้างภาพผลลัพธ์ที่แสดงภาพของ Excel ได้อย่างถูกต้องตามต้นฉบับ—รวมถึงการจัดรูปแบบเซลล์ ค่าที่แสดงจากสูตร ขอบ สี และการจัดรูปแบบตามเงื่อนไข
- **เข้ากันได้ทั่วทั้งแพลตฟอร์ม**: รูปแบบภาพ (PNG, JPEG, TIFF, BMP, SVG เป็นต้น) สามารถดูได้บนอุปกรณ์หรือแพลตฟอร์มใดก็ตามโดยไม่ต้องใช้ซอฟต์แวร์เฉพาะ ช่วยให้ผู้ใช้เข้าถึงได้สูงสุด

## วิธีการใช้ API แปลงตารางเป็นภาพด้วย SDK?

### ข้อมูลจำเพาะ API แปลงตารางเป็นภาพ

[ข้อมูลจำเพาะ API แปลงตารางเป็นภาพ](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToImage) ให้อินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้สาธารณะสำหรับการโต้ตอบ REST โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL บรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/image?format=png&worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.png
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

### ใช้งาน Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจากซ่อนรายละเอียดระดับต่ำไว้ ช่วยให้คุณสามารถแปลงข้อมูลตารางในสเปรดชีตเป็นภาพได้ด้วยโค้ดเพียงไม่กี่บรรทัด โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}