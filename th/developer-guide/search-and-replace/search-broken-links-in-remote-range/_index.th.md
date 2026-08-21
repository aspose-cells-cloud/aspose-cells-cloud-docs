---
title: "Aspose.Cells Cloud – ตรวจหาลิงก์ที่เสียในช่วงข้อมูลของไฟล์ Excel (API)"
second_title: "เอกสาร"
ArticleTitle: "ค้นหาและแก้ไขลิงก์ที่เสียในช่วงข้อมูลของไฟล์ Excel บนคลาวด์ – เครื่องมือตรวจสอบลิงก์สเปรดชีตบนคลาวด์"
linktitle: "ค้นหาลิงก์ที่เสียในช่วงข้อมูลระยะไกล"
type: docs
url: /search-broken-links-in-remote-range/
keywords: "Aspose, Cells, ลิงก์ที่เสีย, API, ช่วงข้อมูล Excel, การตรวจสอบ, คลาวด์, สเปรดชีต, อ้างอิงภายนอก, เครื่องมือตรวจสอบ"
description: "ใช้ Aspose.Cells Cloud API เพื่อสแกนช่วงข้อมูลของไฟล์ Excel เพื่อหาลิงก์ภายนอกที่เสีย สูตรที่ไม่ถูกต้อง หรือแหล่งข้อมูลที่หายไป ปลอดภัย รวดเร็ว และทำงานบนคลาวด์"
weight: 100
---

## **ค้นหาลิงก์ที่เสียในช่วงข้อมูลระยะไกลผ่าน API**

ตรวจจับลิงก์ที่เสียในข้อมูลช่วงของไฟล์ Excel ที่เก็บไว้ในพื้นที่จัดเก็บบนคลาวด์โดยอัตโนมัติ API ของเราสแกนช่วงข้อมูลที่ระบุเพื่อหาการอ้างอิงภายนอกที่เสีย สูตรที่ไม่ถูกต้อง หรือแหล่งข้อมูลที่หายไป รองรับการตรวจสอบสเปรดชีตระยะไกล การตรวจสอบคุณภาพอัตโนมัติ และการผนวกเข้ากับผู้ให้บริการพื้นที่จัดเก็บบนคลาวด์ API แบบ RESTful สำหรับการประมวลผลอัตโนมัติในระบบองค์กร

### **Web API**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/broken-links
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

```bash
-H "Authorization: Bearer {access_token}"
```

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย                                                                                                                                                          |
| ---------------- | ------ | -------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name             | String | Path     | **จำเป็น** ชื่อไฟล์สมุดงาน Excel (เช่น `financial_report.xlsx`) ที่เก็บไว้ในพื้นที่จัดเก็บบนคลาวด์ ซึ่งคุณต้องการสแกนหาลิงก์ที่เสีย                                        |
| worksheet        | String | Path     | **จำเป็น** ชื่อของแผ่นงานที่ระบุ (เช่น `Sheet1`, `Q4_Data`) ภายในสมุดงานที่ต้องการค้นหาลิงก์ที่เสีย                                                         |
| cellArea         | String | Path     | **จำเป็น** ที่อยู่ของช่วงเซลล์เป้าหมาย (เช่น `A1:F100`) ภายในแผ่นงานที่ระบุที่ต้องการสแกนหาการอ้างอิงภายนอกที่เสีย สูตรหรือลิงก์ที่ไม่ถูกต้อง                    |
| folder           | String | Query    | **ไม่บังคับ** เส้นทางไดเรกทอรีในพื้นที่จัดเก็บบนคลาวด์ที่สมุดงานเป้าหมายอยู่ หากไม่ระบุ จะถือว่าอยู่ในไดเรกทอรีราก                                           |
| storageName      | String | Query    | **ไม่บังคับ** ชื่อของบริการพื้นที่จัดเก็บบนคลาวด์ที่กำหนดค่าไว้ (เช่น `DropboxBusiness`, `S3Bucket`) หากไม่ระบุ API จะใช้พื้นที่จัดเก็บเริ่มต้นของบัญชี         |
| region           | String | Query    | **ไม่บังคับ** การตั้งค่าภาษา和地区 (เช่น `en-GB`, `de-DE`) ที่ใช้ในการตีความข้อมูลที่เกี่ยวข้องกับภูมิภาคระหว่างการสแกน                                         |
| password         | String | Query    | **ไม่บังคับ** รหัสผ่านสำหรับถอดรหัสที่จำเป็นเพื่อเข้าถึงสมุดงานที่ได้รับการป้องกันด้วยรหัสผ่าน ปล่อยว่างไว้หากไฟล์ไม่ได้เข้ารหัสไว้                                 |

**ตัวอย่างเนื้อหาคำขอ**

```json
{
  "name": "financial_report.xlsx",
  "worksheet": "Sheet1",
  "cellArea": "A1:F100",
  "folder": "reports/2024",
  "storageName": "MyDropbox",
  "region": "en-US",
  "password": ""
}
```

### การตอบกลับ

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer"
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String"
      }
    }
  ]
}
```

คอลเลกชัน `BrokenLinks` จะมีวัตถุประเภท **BrokenLink** ซึ่งแต่ละวัตถุมีคุณสมบัติดังนี้:

- **CellName** – ที่อยู่ของเซลล์ที่มีการอ้างอิงที่เสีย (เช่น `B12`)
- **LinkType** – ประเภทของลิงก์ที่เสีย (เช่น `ExternalReference`, `Formula`)
- **ErrorMessage** – คำอธิบายว่าทำไมลิงก์นี้จึงถือว่าเสีย

**หมายเหตุ**: API นี้มีข้อจำกัดเรื่องอัตราการเรียกใช้งาน (rate limits) กรุณาดูรายละเอียดได้ที่หน้า [ราคาและข้อจำกัดอัตรา](https://www.aspose.cloud/pricing)

### รหัสข้อผิดพลาด

- **400 Bad Request** – URI ของ Aspose.Cells Cloud API ไม่ถูกต้อง
- **401 Unauthorized** – โทเคนการเข้าถึง (access token) หรือ Client ID/Client Secret ไม่ถูกต้อง
- **404 Not Found** – ไม่สามารถเข้าถึงไฟล์สเปรดชีตได้
- **500 Server Error** – สเปรดชีตเกิดข้อผิดพลาดขณะดึงข้อมูลการคำนวณ

## ควรใช้ Search for broken links within the range of the Spreadsheet API ในกรณีใดบ้าง?

- **การตรวจสอบแบบสม่ำเสมอสำหรับโมเดลการเงินขนาดใหญ่** – ก่อนเผยแพร่รายงานรายเดือนหรือรายไตรมาส สแกนพื้นที่คำนวณหลัก (เช่น `Dashboard!B5:K50`) ที่มีการอ้างอิงข้อมูลภายนอกจำนวนมาก เพื่อให้มั่นใจว่าลิงก์ทั้งหมดชี้ไปยังไฟล์ต้นทางที่ถูกต้อง
- **การบูรณาการข้อมูลสำหรับการควบคุมกิจการและเข้าซื้อกิจการ (M&A)** – เมื่อรวมไฟล์สเปรดชีตหลายไฟล์ที่แทนหน่วยธุรกิจต่างๆ สแกนแผ่นงาน “Overview” หลังการรวมเพื่อระบุลิงก์ที่อาจเสียเนื่องจากเปลี่ยนเส้นทางไฟล์หรือปัญหาสิทธิ์การเข้าถึง
- **การเตรียมชุดข้อมูลสำหรับนักลงทุน** – ก่อนส่งมอบวัสดุนำเสนอที่มีกราฟและตารางเชื่อมโยงกับฐานข้อมูลภายนอกหรือแหล่งข้อมูลตลาด สแกนตรวจสอบความถูกต้องของลิงก์ทั้งหมด

## เหตุใดจึงควรใช้ Search for broken links within the range of the Spreadsheet API?

- **เป็นมิตรกับนักพัฒนา** – Aspose.Cells Cloud มี SDK สำหรับหลายภาษา ช่วยให้พัฒนาได้อย่างรวดเร็วพร้อมเอกสารประกอบที่ครบถ้วน เมื่อเทียบกับการสร้างโซลูชันแบบปรับแต่ง ช่วยลดภาระงานพัฒนาอย่างมาก
- **ลดต้นทุนแรงงาน** – ไม่จำเป็นต้องมีบุคลากรเฉพาะเพื่อจัดทำเอกสารด้วยตนเอง
- **จ่ายตามการใช้งานจริง (Pay-per-use)** – ไม่ต้องลงทุนล่วงหน้า จ่ายเฉพาะเมื่อเรียกใช้งาน API จริงเท่านั้น
- **ไม่มีต้นทุนการบำรุงรักษา** – ไม่มีเซิร์ฟเวอร์ต้องดูแล ไม่ต้องอัปเดตซอฟต์แวร์ และไม่มีปัญหาความเข้ากันได้
- **คงรูปแบบ Excel ที่ซับซ้อนไว้** – ผลลัพธ์สามารถส่งออกเป็นรูปแบบ PDF ซึ่งเข้าถึงได้ทั่วไป โดยไม่สูญเสียรูปแบบ

## วิธีใช้ Search for broken links within the range of the Spreadsheet API ด้วย SDK

### ข้อกำหนด OpenAPI

[ข้อกำหนด OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteRange) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณโต้ตอบกับ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

### ใช้ Aspose.Cells Cloud SDK

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดเบื้องต้นทั้งหมด ช่วยให้คุณใช้ฟังก์ชัน "ค้นหาลิงก์ที่เสียในช่วง" ด้วยโค้ดเพียงเล็กน้อย กรุณาดู [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บ Aspose.Cells ผ่าน SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}