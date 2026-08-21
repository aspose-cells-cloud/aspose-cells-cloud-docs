---
title: "Aspose.Cells Cloud Web API - แปลงกราฟใน Excel เป็นรูปภาพ - เครื่องมือฟรีออนไลน์"
second_title: "เอกสาร"
ArticleTitle: "วิธีการแปลงกราฟในสเปรดชีตเป็นรูปภาพ: คู่มือแบบทีละขั้นตอน"
linktitle: "แปลงกราฟเป็นรูปภาพ"
type: docs
url: /th/convert-chart-to-image/
keywords: "แปลงกราฟเป็นรูปภาพ, Aspose.Cells, การส่งออกกราฟ Excel, PNG, SVG, JPEG, BMP, TIFF"
description: "ใช้ Aspose.Cells Cloud Web API ในการแปลงกราฟใน Excel เป็นรูปภาพ PNG, SVG, TIFF, JPEG หรือ BMP โดยตรงจากไฟล์สเปรดชีต"
weight: 100
---

กราฟใน Excel เป็นภาพแทนข้อมูลที่สามารถฝังไว้ในแผ่นงานได้ การแปลงกราฟเหล่านี้เป็นรูปแบบไฟล์รูปภาพช่วยให้สามารถนำกลับมาใช้ใหม่ได้ง่ายในเอกสาร, เว็บเพจ และรายงานต่างๆ โดยไม่จำเป็นต้องเปิด Excel

แปลงกราฟจากสเปรดชีตในเครื่องหรือไฟล์ Excel เป็นไฟล์รูปภาพ รองรับ **รูปแบบรูปภาพ:** <a href="https://docs.fileformat.com/image/png/" rel="noopener noreferrer">PNG</a>, <a href="https://docs.fileformat.com/page-description-language/svg/" rel="noopener noreferrer">SVG</a>, <a href="https://docs.fileformat.com/image/tiff/" rel="noopener noreferrer">TIFF</a>, <a href="https://docs.fileformat.com/image/jpeg/" rel="noopener noreferrer">JPEG</a>, <a href="https://docs.fileformat.com/image/bmp/" rel="noopener noreferrer">BMP</a>

## **แปลงกราฟเป็นรูปภาพผ่าน API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/image
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/chart/image?format=png&chartIndex=0" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@MyWorkbook.xlsx" \
     -o chart.png
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### **พารามิเตอร์คำขอ:**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | Path/Query String/HTTPBody | คำอธิบาย                                                                                     | จำเป็น |
| :------------- | :------ | :------------------------- | :------------------------------------------------------------------------------------------- | :------- |
| Spreadsheet    | ไฟล์    | FormData                   | อัปโหลดไฟล์สเปรดชีตที่มีกราฟที่ต้องการแปลง                                                  | ใช่      |
| worksheet      | สตริง  | Query                      | ระบุชื่อแผ่นงานหากจำเป็น                                                                     | ไม่ใช่   |
| chartIndex     | จำนวนเต็ม | Query                      | ดัชนีของกราฟที่ต้องการแปลง                                                                   | ใช่      |
| format         | สตริง  | Query                      | (จำเป็น) รูปแบบรูปภาพที่ต้องการ (เช่น svg, png, jpg)                                         | ใช่      |
| outPath        | สตริง  | Query                      | (ไม่บังคับ) พาธของโฟลเดอร์ที่จะเก็บไฟล์ผลลัพธ์; ค่าเริ่มต้นเป็น null                           | ไม่ใช่   |
| outStorageName | สตริง  | Query                      | ชื่อของพื้นที่จัดเก็บสำหรับไฟล์ผลลัพธ์                                                        | ไม่ใช่   |
| fontsLocation  | สตริง  | Query                      | ระบุฟอนต์ที่กำหนดเองหากจำเป็น                                                                 | ไม่ใช่   |
| region         | สตริง  | Query                      | ตั้งค่าภูมิภาคของสเปรดชีต                                                                     | ไม่ใช่   |
| password       | สตริง  | Query                      | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต                                                                | ไม่ใช่   |

## **การตอบกลับ**

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
| 200  | สำเร็จ (OK)                    | กรองข้อมูลสำเร็จ; ข้อมูลการตอบกลับประกอบด้วยรายละเอียดการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request)           | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ)      |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)          | JWT token ไม่ถูกต้องหรือขาดหาย                                     |
| 413  | ข้อมูลในคำขอใหญ่เกินไป (Payload Too Large)     | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                 |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดในเซิร์ฟเวอร์                                          |

## คุณควรใช้ Convert Chart to Image API ในกรณีใด?

- **การสร้างรายงานและแดชบอร์ด**: แปลงกราฟจากข้อมูล Excel เป็นรูปภาพ (PNG, JPEG เป็นต้น) แบบอัตโนมัติเพื่อฝังไว้ในรายงาน PDF, แดชบอร์ดเว็บ หรือการนำเสนอ PowerPoint
- **แอปพลิเคชันเว็บ/อีเมล**: แสดงรูปภาพกราฟโดยตรงในเว็บเพจหรืออีเมล โดยไม่ต้องให้ผู้ใช้ดาวน์โหลดหรือเปิดไฟล์ Excel นี้เหมาะสำหรับเครื่องมือรายงานแบบไดนามิก, จดหมายข่าว หรือการแจ้งเตือนอัตโนมัติ
- **กระบวนการทำงานด้านการประมวลผลเอกสาร**: ผสานรวมเข้ากับระบบอัตโนมัติ (เช่น การทำบิล, การวิเคราะห์ข้อมูล) ที่ต้องแทรกกราฟจาก Excel ลงในรูปแบบอื่นๆ (Word, PDF, HTML)
- **แอปพลิเคชันมือถือและเดสก์ท็อป**: แสดงกราฟในแอปพลิเคชันที่ไม่จำเป็นต้องเรนเดอร์สเปรดชีตทั้งหมดหรือไม่สามารถทำได้
- **การจัดเก็บและแสดงผลข้อมูล**: บันทึกกราฟเป็นรูปภาพเดี่ยวเพื่อเก็บรักษาไว้นานๆ, ใช้เป็นรูปภาพตัวอย่าง หรือดูภาพรวมโดยไม่ต้องพึ่งพา Excel

## คุณควรใช้ Convert Chart to Image API เหตุผลใด?

- **คงความถูกต้องของภาพ**: รักษาการจัดรูปแบบกราฟให้เหมือนทุกประการ (สี, ป้ายกำกับ, การปรับขนาด) เหมือนใน Excel เพื่อให้ได้ผลลัพธ์ที่มีคุณภาพระดับมืออาชีพ
- **ไม่ขึ้นกับแพลตฟอร์ม**: ไม่จำเป็นต้องติดตั้ง Excel ใช้งานข้ามแพลตฟอร์ม (Windows, Linux, macOS) ผ่าน REST API เหมาะสำหรับแอปพลิเคชันที่ทำงานบนคลาวด์หรือฝั่งเซิร์ฟเวอร์
- **การประมวลผลอัตโนมัติและปรับขนาดได้**: แปลงกราฟหรือไฟล์หลายไฟล์พร้อมกันผ่านการเขียนโปรแกรม ประหยัดเวลาเมื่อเทียบกับการส่งออกด้วยตนเอง และจัดการปริมาณข้อมูลขนาดใหญ่ได้อย่างมีประสิทธิภาพในคลาวด์
- **รูปแบบผลลัพธ์ที่ยืดหยุ่น**: รองรับรูปแบบรูปภาพยอดนิยม (PNG, JPG, BMP, SVG เป็นต้น) ทำให้สามารถผสานรวมกับระบบที่หลากหลายและสื่อต่างๆ ได้
- **ปลอดภัยและเชื่อถือได้**: ประมวลผลไฟล์ในสภาพแวดล้อมคลาวด์ของ Aspose โดยไม่ต้องเปิดเผยข้อมูลที่ละเอียดอ่อนให้กับเครื่องมือฝั่งไคลเอนต์ มีความพร้อมใช้งานสูงและประสิทธิภาพคงที่
- **เป็นมิตรกับนักพัฒนา**: Aspose.Cells Cloud มี SDK ให้ใช้งานในหลายภาษา ช่วยให้พัฒนาแอปพลิเคชันได้อย่างรวดเร็ว และมาพร้อมเอกสารประกอบที่ครบถ้วน เมื่อเทียบกับการสร้างโซลูชันการเรนเดอร์กราฟแบบกันเอง สิ่งนี้ช่วยลดภาระงานพัฒนาได้อย่างมาก
- **คุ้มค่า**: คุณสามารถแปลงกราฟได้โดยไม่จำเป็นต้องอัปโหลดสมุดงานก่อน ซึ่งช่วยประหยัดพื้นที่จัดเก็บและลดต้นทุน

## วิธีใช้ Convert Chart to Image API ร่วมกับ SDKs?

### ข้อมูลจำเพาะ Convert Chart to Image API

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToImage" rel="noopener noreferrer">ข้อมูลจำเพาะ Convert Chart to Image API</a> กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้สาธารณะ และช่วยให้คุณดำเนินการ REST interaction โดยตรงจากเว็บเบราว์เซอร์

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจากซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถแปลงกราฟเป็นรูปภาพได้ด้วยโค้ดสั้นๆ  
โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้ Aspose.Cells web services โดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToImage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToImage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToImage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToImage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToImage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToImage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToImage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToImage.go" >}}
{{</tab>}}
{{< /tabs >}}

---