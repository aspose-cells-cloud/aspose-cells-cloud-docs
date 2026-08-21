---
---
title: "Aspose.Cells Cloud – แทนที่ข้อความในไฟล์ Excel บนเครื่อง (API ค้นหาและแทนที่)"
second_title: "เอกสาร"
ArticleTitle: "แทนที่ข้อความแบบแบตช์ในไฟล์ Excel บนเครื่อง – API ค้นหาและแทนที่"
linktype: "แทนที่เนื้อหาในสเปรดชีต"
type: docs
url: /replace-spreadsheet-content/
keywords: "แทนที่ข้อความใน Excel, Aspose.Cells ค้นหาและแทนที่, API สเปรดชีตบนเครื่อง, แทนที่ไฟล์ Excel, API แทนที่เนื้อหา"
description: "แทนที่ข้อความในสมุดงาน Excel บนเครื่องโดยไม่ต้องอัปโหลดไปยังคลาวด์ ใช้ Aspose.Cells Cloud Find & Replace API เพื่ออัปเดตช่วงที่ระบุ ชีตงาน หรือไฟล์ทั้งหมดในคำขอเพียงครั้งเดียว"
weight: 100
---

แทนที่ข้อความที่ระบุในไฟล์สเปรดชีต Excel บนเครื่องโดยไม่ต้องอัปโหลดขึ้นคลาวด์ อัปเดตเนื้อหาในสมุดงานอย่างมีประสิทธิภาพโดยใช้ Aspose.Cells Find & Replace API สำหรับการแก้ไขแบบออฟไลน์

## **API แทนที่เนื้อหาในสเปรดชีต**

### **Web API**

```http
PUT https://api.aspose.cloud/v4.0/cells/replace/content
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์ด้วย JWT token</a>

```bash
-H "Authorization: Bearer {access_token}"
```

### **พารามิเตอร์คำขอ:**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | Path/Query String/HTTPBody | คำอธิบาย                                                                                                                                                                                           |
| :------------- | :----- | :------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | ไฟล์   | FormData                   | ไฟล์สเปรดชีตบนเครื่องที่จะดำเนินการ รูปแบบที่รองรับ ได้แก่ XLSX, XLS, ODS, CSV เป็นต้น                                                                                                       |
| searchText     | สตริง | Query                      | สตริงข้อความที่จะค้นหาภายในชีตงานและพื้นที่เซลล์ที่ระบุ                                                                                                                           |
| replaceText    | สตริง | Query                      | สตริงข้อความที่จะแทนที่ทุกครั้งที่พบ `searchText` ภายในช่วงที่ระบุ                                                                                                         |
| worksheet      | สตริง | Query                      | _(ไม่บังคับ)_ ชื่อชีตงานที่จะดำเนินการค้นหาและแทนที่ หากไม่ระบุ การดำเนินการจะใช้กับชีตงานแรก                                                                                                              |
| cellArea       | สตริง | Query                      | _(ไม่บังคับ)_ ช่วงเซลล์เฉพาะ (เช่น `"A1:D20"`, `"B5:F15"`) ที่จะค้นหาและแทนที่ข้อความ หากไม่ระบุ การดำเนินการจะใช้กับเซลล์ที่ใช้งานทั้งหมดในชีตงานที่ระบุ |
| region         | สตริง | Query                      | _(ไม่บังคับ)_ ตั้งค่าภูมิภาคสำหรับการจัดการข้อความ ซึ่งอาจส่งผลต่อกรณีของตัวอักษรและการเข้ารหัสอักขระในการค้นหา (เช่น `"en-US"`, `"fr-FR"`)                                           |
| password       | สตริง | Query                      | _(ไม่บังคับ)_ หากไฟล์สเปรดชีตที่อัปโหลดมีการป้องกันด้วยรหัสผ่าน ให้ระบุรหัสผ่านเพื่อเปิดและดำเนินการกับไฟล์                                                                                    |

### **การตอบกลับ**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

การตอบกลับคือสตรีมไบนารีที่ประกอบด้วยสมุดงานที่อัปเดตแล้ว บันทึกไฟล์ด้วยส่วนขยายที่เหมาะสม (เช่น `.xlsx`)

### **รหัสข้อผิดพลาด**

- **400 Bad Request** – URI ของ Aspose.Cells Cloud API ไม่ถูกต้องหรือพารามิเตอร์ผิดรูปแบบ
- **401 Unauthorized** – โทเคนการเข้าถึงไม่ถูกต้องหรือขาดหาย ขอโทเคนใหม่
- **404 Not Found** – ไม่สามารถเข้าถึงไฟล์สเปรดชีตหรือชีตงานที่ระบุไม่มีอยู่
- **500 Server Error** – สมุดงานเกิดข้อผิดพลาดภายในระหว่างประมวลผล ติดต่อฝ่ายสนับสนุนหากปัญหายังคงอยู่

## ควรใช้ API แทนที่เนื้อหาในสเปรดชีตในกรณีใด?

- **ประมวลผลแบบแบตช์ของไฟล์ Excel บนเครื่อง** – สร้างระบบอัตโนมัติสำหรับการค้นหาและแทนที่ในหลายสมุดงานที่เก็บไว้บนเครื่อง
- **สายการผลิตข้อมูลแบบภายในองค์กร** – ผสาน API เข้ากับงานตามกำหนดเวลาเพื่อดัดแปลงรายงานก่อนที่จะเก็บถาวรหรือจัดส่ง
- **การสร้างรายงานบนเครื่อง** – แทรกค่าลงในเทมเพลตสมุดงานแบบไดนามิกโดยไม่ต้องอัปโหลดไปยังคลาวด์

## ทำไมจึงควรใช้ API แทนที่เนื้อหาในสเปรดชีต?

- **เป็นมิตรกับนักพัฒนา** – Aspose.Cells Cloud มีไลบรารี SDK รองรับหลายภาษา ช่วยให้พัฒนาได้อย่างรวดเร็วและมีเอกสารครบถ้วน เมื่อเทียบกับการสร้างโซลูชันแบบปรับแต่งเอง ช่วยลดความพยายามในการพัฒนาอย่างมาก
- **ลดค่าใช้จ่ายแรงงาน** – ลดความจำเป็นในการจ้างบุคลากรเฉพาะด้านเพื่อดำเนินการรวมเอกสารด้วยตนเอง
- **จ่ายตามการใช้งานจริง** – ไม่ต้องลงทุนล่วงหน้า จ่ายเฉพาะเมื่อเรียกใช้ API จริง
- **ไม่มีค่าใช้จ่ายในการดูแลรักษา** – ไม่มีเซิร์ฟเวอร์ต้องดูแล ไม่มีการอัปเดตซอฟต์แวร์ และไม่ต้องกังวลเรื่องความเข้ากันได้
- **คงรักษารูปแบบ Excel ที่ซับซ้อนไว้** – รูปแบบ สูตร และกราฟิกของสมุดงานต้นฉบับยังคงสมบูรณ์หลังการแทนที่

## วิธีใช้ API แทนที่เนื้อหาในสเปรดชีตพร้อม SDK

### **สเปค OpenAPI**

[OpenAPI Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceSpreadsheetContent) นิยามอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ ช่วยให้คุณสามารถโต้ตอบกับ REST API ได้โดยตรงจากเว็บเบราว์เซอร์

### **ใช้ Aspose.Cells Cloud SDK**

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK จัดการรายละเอียดเบื้องต้น ช่วยให้คุณดำเนินการแทนที่เนื้อหาด้วยโค้ดน้อยที่สุด ดู repository **Aspose.Cells Cloud SDK GitHub** ทางการเพื่อดูรายชื่อภาษาที่รองรับทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีโต้ตอบกับ Aspose.Cells web services ด้วย SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ReplaceTextInLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ReplaceTextInLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ReplaceTextInLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ReplaceTextInLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ReplaceTextInLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ReplaceTextInLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ReplaceTextInLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ReplaceTextInLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}