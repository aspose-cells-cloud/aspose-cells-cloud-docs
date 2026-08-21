---
title: "Aspose.Cells Cloud – API ตรวจหาลิงก์เสียใน Excel – สแกน & ตรวจสอบความถูกต้องของลิงก์สมุดงานภายนอก"
second_title: "เอกสาร"
ArticleTitle: "ค้นหาและแก้ไขลิงก์เสียใน Excel แบบรันผ่านคลาวด์ – เครื่องมือตรวจสอบลิงก์สมุดงานบนคลาวด์"
linktitle: "ค้นหาลิงก์เสียในสมุดงานภายนอก"
type: docs
url: /th/search-broken-links-in-remote-spreadsheet/
keywords: "Excel, ลิงก์เสีย, API, คลาวด์, สเปรดชีต, การตรวจสอบ, Aspose.Cells"
description: "ใช้ Aspose.Cells Cloud API เพื่อสแกนสมุดงาน Excel ที่เก็บไว้ในพื้นที่จัดเก็บบนคลาวด์ เพื่อหาลิงก์ภายนอกที่เสีย สูตรที่ไม่ถูกต้อง และแหล่งข้อมูลที่ขาดหาย"
weight: 100
---

## **ค้นหาลิงก์เสียในสมุดงานภายนอกผ่าน API**

ตรวจจับลิงก์เสียในไฟล์ Excel ที่เก็บไว้ในพื้นที่จัดเก็บบนคลาวด์โดยอัตโนมัติ API นี้จะสแกนช่วงที่ระบุเพื่อค้นหาการอ้างอิงภายนอกที่เสีย สูตรที่ไม่ถูกต้อง และแหล่งข้อมูลที่ขาดหาย รองรับการตรวจสอบคุณภาพสมุดงานบนคลาวด์ การตรวจสอบคุณภาพอัตโนมัติ และการผนวกเข้ากับผู้ให้บริการพื้นที่จัดเก็บบนคลาวด์ ใช้ RESTful API เพื่อทำให้กระบวนการทางธุรกิจระดับองค์กรเป็นไปโดยอัตโนมัติ

### **Web API**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/broken-links
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยสูงและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

```bash
-H "Authorization: Bearer {access_token}"
```

### **พารามิเตอร์ของคำขอ:**

| ชื่อพารามิเตอร์ | ประเภท | Path/Query String/HTTPBody | คำอธิบาย                                                                                                                                               |
| :------------- | :----- | :------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String | Path                       | **จำเป็น** ชื่อไฟล์สมุดงาน Excel ที่ต้องการสแกนหาลิงก์เสีย (เช่น `Quarterly_Report.xlsx`)                                         |
| worksheet      | String | Query                      | **จำเป็น** ชื่อแผ่นงานที่จะดำเนินการค้นหา ระบุชื่อแผ่นงานให้ตรงกับชื่อที่ปรากฏในสมุดงาน |
| cellArea       | String | Query                      | **จำเป็น** ช่วงเซลล์ที่ต้องการวิเคราะห์หาลิงก์เสีย โดยใช้รูปแบบ A1 (เช่น `C5:J50`) API จะค้นหาเฉพาะภายในพื้นที่นี้เท่านั้น          |
| folder         | String | Query                      | **ไม่บังคับ** เส้นทางไปยังไดเรกทอรีที่เก็บสมุดงานไว้ในพื้นที่จัดเก็บบนคลาวด์ หากไม่ระบุ จะใช้ไดเรกทอรีรากเป็นค่าเริ่มต้น                         |
| storageName    | String | Query                      | **ไม่บังคับ** ชื่อการตั้งค่าพื้นที่จัดเก็บบนคลาวด์แบบกำหนดเอง หากไม่ระบุ จะใช้พื้นที่จัดเก็บเริ่มต้นของระบบ                                      |
| region         | String | Query                      | **ไม่บังคับ** การตั้งค่าภูมิภาคที่ใช้ระหว่างการประมวลผล (เช่น `en-US`) อาจส่งผลต่อการตีความไวยากรณ์หรือการอ้างอิงของสูตรที่ขึ้นกับภูมิภาค |
| password       | String | Query                      | **ไม่บังคับ** รหัสผ่านที่จำเป็นสำหรับการเปิดสมุดงานที่เข้ารหัส หากไฟล์ไม่ได้รับการป้องกันด้วยรหัสผ่าน ให้เว้นว่างไว้                                             |

**ตัวอย่างคำขอ cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Quarterly_Report.xlsx/search/broken-links?worksheet=Sheet1&cellArea=C5:J50" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **การตอบกลับ**

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

**ตัวอย่าง JSON ของการตอบกลับ**

```json
{
  "BrokenLinks": [
    {
      "Worksheet": "Sheet1",
      "CellName": "D12",
      "Link": "https://example.com/data/source.xlsx",
      "IsValid": false,
      "ErrorMessage": "ไม่พบไฟล์"
    },
    {
      "Worksheet": "Sheet1",
      "CellName": "F30",
      "Link": "C:\\LocalFolder\\data.xlsx",
      "IsValid": false,
      "ErrorMessage": "การอ้างอิงภายนอกไม่รองรับในโหมดคลาวด์"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

### รหัสข้อผิดพลาด

- **400 Bad Request** – URI ของ Aspose.Cells Cloud API ไม่ถูกต้อง  
- **401 Unauthorized** – token การเข้าถึง ไคลเอนต์ ID หรือไคลเอนต์ซีเรต ไม่ถูกต้อง  
- **404 Not Found** – ไม่สามารถเข้าถึงไฟล์สมุดงานได้  
- **500 Server Error** – เกิดข้อผิดพลาดระหว่างการดึงข้อมูลการคำนวณ  

## ควรใช้ API ค้นหาลิงก์เสียในสมุดงานในกรณีใด?

- **การตรวจสอบแบบสม่ำเสมอในแบบจำลองการเงินขนาดใหญ่** – ก่อนเผยแพร่รายงานรายเดือนหรือรายไตรมาส สแกนพื้นที่คำนวณสำคัญ (เช่น `Dashboard!B5:K50`) ที่มีการอ้างอิงข้อมูลภายนอกจำนวนมาก เพื่อยืนยันว่าลิงก์ทั้งหมดชี้ไปยังไฟล์ต้นทางที่ยังใช้งานได้  
- **การผนวกข้อมูลสำหรับการควบคุมกิจการและซื้อกิจการ** – เมื่อผนวกสมุดงานหลายใบที่แสดงถึงหน่วยธุรกิจต่างๆ หลังการผนวก สแกนแผ่นงาน “Overview” เพื่อหาลิงก์ที่อาจเสียเนื่องจากเปลี่ยนเส้นทางไฟล์หรือปัญหาสิทธิ์การเข้าถึง  
- **การเตรียมชุดข้อมูลสำหรับนักลงทุน** – ก่อนจัดทำสื่อประกอบการนำเสนอที่มีกราฟและตารางเชื่อมโยงกับฐานข้อมูลภายนอกหรือแหล่งข้อมูลตลาด ตรวจสอบความถูกต้องของลิงก์ทั้งหมด  

## ทำไมควรใช้ API ค้นหาลิงก์เสียในสมุดงาน?

- **ใช้งานง่ายสำหรับนักพัฒนา** – Aspose.Cells Cloud มี SDK ให้ใช้งานในหลายภาษา ช่วยให้พัฒนาได้อย่างรวดเร็วพร้อมเอกสารประกอบที่ครบถ้วน เมื่อเทียบกับการสร้างโซลูชันแบบปรับแต่งเอง ช่วยลดความพยายามในการพัฒนาอย่างมาก  
- **ลดต้นทุนแรงงาน** – ทำให้การตรวจสอบลิงก์เป็นไปโดยอัตโนมัติ ไม่ต้องจ้างบุคลากรเฉพาะทางมาตรวจสอบเอกสารด้วยตนเอง  
- **จ่ายตามการใช้งานจริง** – ไม่ต้องลงทุนล่วงหน้า จ่ายเฉพาะเมื่อมีการเรียกใช้ API เท่านั้น  
- **ไม่มีต้นทุนการดูแลรักษา** – ไม่ต้องดูแลเซิร์ฟเวอร์ ไม่ต้องอัปเดตซอฟต์แวร์ และไม่ต้องกังวลเรื่องความเข้ากันได้  

## วิธีใช้ API ค้นหาลิงก์เสียในสมุดงานด้วย SDK

### **สเปค OpenAPI**

[OpenAPI Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteSpreadsheet) นิยามอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ ช่วยให้คุณสามารถโต้ตอบกับ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

### **ใช้ Aspose.Cells Cloud SDK**

การใช้ SDK เป็นวิธีที่มีประสิทธิภาพที่สุดในการเร่งการพัฒนา SDK ซ่อนรายละเอียด HTTP ไว้เบื้องหลัง ทำให้คุณสามารถใช้งานการตรวจจับลิงก์เสียได้ด้วยโค้ดเพียงไม่กี่บรรทัด ดู [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีโต้ตอบกับ Aspose.Cells web services โดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteSpreadsheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteSpreadsheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteSpreadsheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteSpreadsheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteSpreadsheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteSpreadsheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}