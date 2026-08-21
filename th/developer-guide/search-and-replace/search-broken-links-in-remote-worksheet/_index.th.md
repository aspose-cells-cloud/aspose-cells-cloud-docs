---
title: "Aspose.Cells Cloud – API ตรวจจับลิงก์เสียใน Excel – สแกนและตรวจสอบลิงก์สเปรดชีตในแผ่นงานระยะไกล"
second title: "เอกสาร"
ArticleTitle: "ค้นหาและแก้ไขลิงก์เสียในแผ่นงาน Excel ระยะไกล – เครื่องมือตรวจสอบลิงก์สเปรดชีตแบบคลาวด์"
linktype: "ค้นหาลิงก์เสียในแผ่นงานระยะไกล"
type: docs
url: /search-broken-links-in-remote-worksheet/
keywords: "Aspose Cells, ลิงก์เสีย, API Excel, สเปรดชีตแบบคลาวด์, การตรวจสอบลิงก์"
description: "ตรวจจับและแก้ไขลิงก์ภายนอกที่เสียในแผ่นงาน Excel ที่จัดเก็บในพื้นที่เก็บข้อมูลคลาวด์ ใช้ Aspose.Cells Cloud API เพื่อสแกนช่วงข้อมูล คืนค่ารายละเอียดลิงก์ และดำเนินการตรวจสอบคุณภาพอัตโนมัติ"
weight: 100
---

## **ค้นหาลิงก์เสียในแผ่นงานระยะไกลผ่าน API**

ตรวจจับลิงก์เสียอัตโนมัติในแผ่นงาน Excel ที่จัดเก็บในพื้นที่เก็บข้อมูลคลาวด์ API นี้จะสแกนช่วงที่ระบุเพื่อค้นหาการอ้างอิงภายนอกที่เสีย สูตรที่ไม่ถูกต้อง และแหล่งข้อมูลที่ขาดหาย รองรับการตรวจสอบสเปรดชีตแบบระยะไกล การตรวจสอบคุณภาพอัตโนมัติ และการผสานรวมกับผู้ให้บริการพื้นที่เก็บข้อมูลคลาวด์ API แบบ RESTful สำหรับการดำเนินการอัตโนมัติในกระบวนการทำงานขององค์กร

### **Web API**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

```bash
-H "Authorization: Bearer {access_token}"
```

### **พารามิเตอร์คำขอ:**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | Path/Query String/HTTP Body | คำอธิบาย                                                                                                                                                                                                                                |
| :------------- | :----- | :-------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String | Path                        | **จำเป็น** ชื่อไฟล์ (พร้อมนามสกุล) ของสมุดงาน Excel ที่ต้องการค้นหาลิงก์เสีย (เช่น `Annual_Report.xlsx`)                                                                                                                 |
| worksheet      | String | Path                        | **จำเป็น** ชื่อแผ่นงานที่จะดำเนินการสแกนลิงก์โดยตรง (เช่น `DataSheet1`)                                                                                                                              |
| folder         | String | Query                       | **ไม่บังคับ** เส้นทางไดเรกทอรีภายในพื้นที่เก็บข้อมูลคลาวด์ของคุณที่สมุดงานเป้าหมายอยู่ หากไม่ระบุ ระบบจะใช้โฟลเดอร์ราก                                                                                                      |
| storageName    | String | Query                       | **ไม่บังคับ** ตัวระบุของพื้นที่เก็บข้อมูลคลาวด์ที่กำหนดค่าเอง หากไม่ระบุ API จะใช้พื้นที่เก็บข้อมูลเริ่มต้นของบัญชี                                                                                                         |
| region         | String | Query                       | **ไม่บังคับ** การตั้งค่าภาษาท้องถิ่นที่ใช้ในการค้นหา (เช่น `fr-FR`) ค่านี้อาจส่งผลต่อการตีความสูตรบางประเภทหรือรูปแบบข้อมูลตามภูมิภาค _รหัสภาษาที่รองรับได้แก่ `en-US`, `fr-FR`, `de-DE`, `es-ES` เป็นต้น_ |
| password       | String | Query                       | **ไม่บังคับ** รหัสผ่านสำหรับถอดรหัสสเปรดชีตที่ป้องกันด้วยรหัสผ่าน ข้ามขั้นตอนนี้หากไฟล์ไม่ได้เข้ารหัส                                                                                                                             |

**ตัวอย่างคำขอ cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Annual_Report.xlsx/worksheets/DataSheet1/search/broken-links?folder=Reports&storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **การตอบกลับ**

```json
{
  "Code": 200,
  "Status": "OK",
  "BrokenLinks": [
    {
      "Address": "='C:\\Data\\Source.xlsx'!A1",
      "ErrorCode": "404",
      "ErrorMessage": "ไม่พบไฟล์ต้นฉบับ"
    }
  ]
}
```

วัตถุการตอบกลับมีชนิดเป็น **BrokenLinksResponse** และประกอบด้วย:

- **BrokenLinks** – คอลเลกชันของรายการ `BrokenLink` แต่ละรายการระบุการอ้างอิงที่มีปัญหา (ที่อยู่ รหัสข้อผิดพลาด และข้อความ)
- **Code** – รหัสสถานะเชิงตัวเลขที่บริการส่งกลับมา
- **Status** – คำอธิบายเชิงข้อความของผลลัพธ์

**หมายเหตุ**: API นี้ไม่แบ่งหน้าผลลัพธ์ สามารถส่งกลับลิงก์เสียได้สูงสุด 10,000 รายการต่อคำขอ ขีดจำกัดอัตราคือ 100 คำขอต่อนาทีต่อบัญชี

### รหัสข้อผิดพลาด

- **400 Bad Request** – URI ของ Aspose.Cells Cloud API ไม่ถูกต้อง
- **401 Unauthorized** – โทเค็นการเข้าถึงไม่ถูกต้องหรือไม่ได้ระบุมา
- **404 Not Found** – ไม่สามารถเข้าถึงไฟล์สเปรดชีตได้
- **500 Server Error** – เกิดข้อผิดพลาดระหว่างการรับข้อมูลการคำนวณ

## ควรใช้ API ค้นหาลิงก์เสียในแผ่นงานสเปรดชีตในกรณีใด?

- **การตรวจสอบอย่างสม่ำเสมอในแบบจำลองการเงินขนาดใหญ่**: ก่อนเผยแพร่รายงานรายเดือนหรือรายไตรมาส สแกนพื้นที่คำนวณสำคัญ (เช่น `Dashboard!B5:K50`) ที่มีการอ้างอิงข้อมูลภายนอกจำนวนมาก เพื่อให้แน่ใจว่าลิงก์ทั้งหมดชี้ไปยังไฟล์ต้นฉบับที่ถูกต้อง
- **การผสานรวมข้อมูลสำหรับการควบคุมกิจการและบริษัท**: เมื่อรวมไฟล์สเปรดชีตหลายไฟล์ที่แทนหน่วยธุรกิจต่างๆ สแกนแผ่นงาน "Overview" หลังกระบวนการผสานรวมเพื่อระบุลิงก์ที่เสียเนื่องจากการเปลี่ยนแปลงเส้นทางไฟล์ต้นฉบับหรือปัญหาสิทธิ์การเข้าถึง
- **การเตรียมชุดข้อมูลสำหรับนักลงทุน**: ก่อนส่งมอบวัสดุการนำเสนอที่มีแผนภูมิและตารางที่เชื่อมโยงกับฐานข้อมูลภายนอกหรือแหล่งข้อมูลตลาด ตรวจสอบความถูกต้องของลิงก์ทั้งหมด

## ทำไมจึงควรใช้ API ค้นหาลิงก์เสียในแผ่นงานสเปรดชีต?

- **เป็นมิตรกับนักพัฒนา**: Aspose.Cells Cloud มี SDK รองรับหลายภาษา ช่วยให้พัฒนาได้อย่างรวดเร็ว และมาพร้อมเอกสารประกอบที่ครบถ้วน เมื่อเทียบกับการสร้างโซลูชันการเรนเดอร์กราฟแบบกำหนดเอง สิ่งนี้ช่วยลดภาระงานพัฒนาอย่างมาก
- **ลดต้นทุนแรงงาน**: ลดความจำเป็นในการจ้างบุคลากรเฉพาะเพื่อจัดการเอกสารและตรวจสอบลิงก์ด้วยตนเอง
- **จ่ายตามการใช้งาน**: ไม่ต้องลงทุนล่วงหน้า จ่ายเฉพาะค่าใช้จ่าย API ที่ใช้งานจริงเท่านั้น
- **ไม่มีต้นทุนการดูแลรักษา**: ไม่มีเซิร์ฟเวอร์ให้ดูแล ไม่มีการอัปเดตซอฟต์แวร์ และไม่มีปัญหาความเข้ากันได้ที่ต้องจัดการ
- **รักษารูปแบบ Excel ที่ซับซ้อน** ในรูปแบบ PDF ที่เข้าถึงได้ทั่วโลก

## วิธีใช้ API ค้นหาลิงก์เสียในแผ่นงานสเปรดชีตผ่าน SDK

### ข้อมูลจำเพาะ OpenAPI

[ข้อมูลจำเพาะ OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteWorksheet) นิยามอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้สาธารณะ และช่วยให้คุณดำเนินการโต้ตอบ REST โดยตรงจากเว็บเบราว์เซอร์

### ใช้ Aspose.Cells Cloud SDK

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดเบื้องต้นให้คุณ ทำให้คุณสามารถใช้งานการค้นหาลิงก์เสียในแผ่นงานสเปรดชีตด้วยโค้ดเพียงเล็กน้อย โปรดดูที่ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}
---