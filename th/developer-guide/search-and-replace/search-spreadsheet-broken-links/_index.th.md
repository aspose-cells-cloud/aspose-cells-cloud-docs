---
title: "ค้นหาลิงก์ที่เสียในสเปรดชีต – API ของ Aspose.Cells Cloud"
second_title: "เอกสาร"
ArticleTitle: "ค้นหาและแก้ไขลิงก์ที่เสียใน Excel – เครื่องมือตรวจสอบลิงก์สเปรดชีตบนคลาวด์"
linktype: "ค้นหาลิงก์ที่เสียในสเปรดชีต"
type: docs
url: /th/search-spreadsheet-broken-links/
keywords: "Aspose Cells, ลิงก์ที่เสีย, การตรวจสอบสเปรดชีต, Excel API, สเปรดชีตบนคลาวด์, เครื่องมือตรวจสอบลิงก์"
description: "ตรวจจับและแก้ไขลิงก์ที่เสียในสมุดงาน Excel ผ่าน API ของ Aspose.Cells Cloud ค้นหาช่วงข้อมูล รับผลลัพธ์ในรูปแบบ JSON อย่างละเอียด และผสานรวมกับ SDK ของภาษาใดก็ได้"
weight: 100
---

## **API สำหรับค้นหาลิงก์ที่เสียในสเปรดชีต**

ตรวจจับลิงก์ที่เสียในไฟล์ Excel อัตโนมัติ API นี้สแกนช่วงที่ระบุเพื่อค้นหาการอ้างอิงภายนอกที่เสีย ฟังก์ชันที่ไม่ถูกต้อง และแหล่งข้อมูลที่หายไป รองรับการตรวจสอบสเปรดชีตทางไกล การตรวจสอบคุณภาพอัตโนมัติ และการผสานรวมกับผู้ให้บริการพื้นที่จัดเก็บบนคลาวด์ API แบบ RESTful สำหรับการดำเนินการอัตโนมัติในเวิร์กโฟลว์องค์กร

**สรุป:** ใช้ปลายทางนี้เพื่อระบุและแก้ไขลิงก์ที่ไม่ถูกต้องในสมุดงานได้อย่างรวดเร็ว ช่วยรักษาความสมบูรณ์ของข้อมูลในโมเดลทางการเงิน ชุดข้อมูลสำหรับการควบรวมกันและ#acute;กิจการ และแพ็กเกจข้อมูลสำหรับนักลงทุน

### **Web API**

```bash
PUT https://api.aspose.cloud/v4.0/cells/search/broken-links
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/broken-links?worksheet=Sheet1" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@sample.xlsx"
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

```bash
-H "Authorization: Bearer {access_token}"
```

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย |
|------------------|--------|----------|-----------------------------------------------------|
| Spreadsheet | ไฟล์ | FormData (multipart) | **จำเป็น** ไฟล์สมุดงาน Excel (`.xlsx`, `.xls` เป็นต้น) ที่ต้องการวิเคราะห์ |
| worksheet | สตริง | Query | **ไม่บังคับ** ชื่อของแผ่นงานที่ต้องการวิเคราะห์ หากไม่ระบุ จะใช้แผ่นงานแรก |
| cellArea | สตริง | Query | **ไม่บังคับ** ช่วงเซลล์เป้าหมายในรูปแบบ A1 (เช่น `B2:D10`) หากไม่ระบุ จะวิเคราะห์ทั้งช่วงที่ใช้งานอยู่ |
| region | สตริง | Query | **ไม่บังคับ** การตั้งค่าภาษาท้องถิ่น (เช่น `en‑GB`) ซึ่งอาจมีผลต่อการตีความวันที่ ตัวเลข หรือสกุลเงิน |
| password | สตริง | Query | **ไม่บังคับ** รหัสผ่านสำหรับสมุดงานที่เข้ารหัส เว้นว่างไว้หากไฟล์ไม่ได้รับการป้องกัน |

### คำตอบ

```json
{
  "BrokenLinks": [
    {
      "CellName": "B5",
      "Link": "C:\\Data\\source.xlsx",
      "ErrorMessage": "ไม่พบไฟล์",
      "Status": "เสีย"
    },
    {
      "CellName": "C12",
      "Link": "http://example.com/data.csv",
      "ErrorMessage": "404 ไม่พบ",
      "Status": "เสีย"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

### รหัสข้อผิดพลาด

| รหัส | คำอธิบาย |
|------|----------|
| **400 Bad Request** | URI ของ Aspose.Cells Cloud API ไม่ถูกต้อง |
| **401 Unauthorized** | โทเคนการเข้าถึง รหัสไคลเอนต์ หรือ bí mậtไคลเอนต์ไม่ถูกต้อง |
| **404 Not Found** | ไม่สามารถเข้าถึงไฟล์สเปรดชีตได้ |
| **429 Too Many Requests** | เกินขีดจำกัดอัตราการเรียกใช้ (60 ครั้ง/นาที) |
| **500 Server Error** | สมุดงานเกิดข้อผิดพลาดขณะดึงข้อมูลการคำนวณ |

## ควรใช้ API ค้นหาลิงก์ที่เสียในสเปรดชีตในกรณีใด?

- **การตรวจสอบเป็นประจำของโมเดลทางการเงินขนาดใหญ่**: ก่อนเผยแพร่รายงานรายเดือนหรือรายไตรมาส สแกนพื้นที่การคำนวณสำคัญ (เช่น `Dashboard!B5:K50`) ที่มีการอ้างอิงข้อมูลภายนอกจำนวนมาก เพื่อให้แน่ใจว่าลิงก์ทั้งหมดชี้ไปยังไฟล์ต้นฉบับที่ถูกต้อง
- **การผสานรวมข้อมูลสำหรับการควบรวมกันและ/acute;กิจการ**: เมื่อรวมไฟล์สเปรดชีตหลายไฟล์ที่แสดงหน่วยธุรกิจต่างๆ หลังการผสานรวม ให้สแกนแผ่นงาน "ภาพรวม" เพื่อระบุลิงก์ที่อาจเสียเนื่องจากเปลี่ยนเส้นทางไฟล์หรือปัญหาสิทธิ์การเข้าถึง
- **การเตรียมแพ็กเกจข้อมูลสำหรับนักลงทุน**: ก่อนจัดทำวัสดุนำเสนอที่มีกราฟและตารางเชื่อมโยงกับฐานข้อมูลภายนอกหรือแหล่งข้อมูลตลาด ให้ตรวจสอบความถูกต้องของลิงก์ทั้งหมด

## ทำไมควรใช้ API ค้นหาลิงก์ที่เสียในสเปรดชีต?

- **เป็นมิตรกับนักพัฒนา** – Aspose.Cells Cloud มีไลบรารี SDK รองรับหลายภาษา ช่วยให้การพัฒนาเป็นไปอย่างรวดเร็วและมีเอกสารประกอบที่ครบถ้วน เมื่อเทียบกับการสร้างโซลูชันแบบกำหนดเอง วิธีนี้ช่วยลดภาระงานพัฒนาอย่างมาก
- **ลดต้นทุนแรงงาน** – ไม่จำเป็นต้องมีบุคลากรเฉพาะเพื่อตรวจสอบลิงก์ในเอกสารด้วยตนเอง
- **จ่ายตามการใช้งานจริง** – ไม่ต้องลงทุนล่วงหน้า จ่ายเฉพาะค่า API ที่ใช้จริงเท่านั้น
- **ไม่มีค่าใช้จ่ายในการดูแลรักษา** – ไม่ต้องดูแลเซิร์ฟเวอร์ ไม่ต้องอัปเดตซอฟต์แวร์ และไม่มีปัญหาความเข้ากันได้
- **รักษาการจัดรูปแบบ Excel ที่ซับซ้อน** – ผลลัพธ์จะคืนในรูปแบบ JSON ที่เข้าถึงได้ทั่วไป พร้อมคงโครงสร้างของสมุดงานต้นฉบับไว้

## วิธีใช้ API ค้นหาลิงก์ที่เสียในสเปรดชีต ด้วย SDK

### ข้อมูลจำเพาะ OpenAPI

[ข้อมูลจำเพาะ OpenAPI](https://reference.aspose.cloud/cells/#/SearchController/SearchSpreadsheetBrokenLinks){:target="_blank" rel="noopener noreferrer"} นิยามอินเทอร์เฟซโปรแกรมที่เข้าถึงได้จากสาธารณะ ช่วยให้คุณสามารถดำเนินการโต้ตอบ REST โดยตรงจากเว็บเบราว์เซอร์

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดเบื้องหลัง ช่วยให้คุณสามารถใช้งานฟังก์ชันค้นหาลิงก์ที่เสียได้ด้วยโค้ดเพียงเล็กน้อย โปรดตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"} เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchSpreadsheetBrokenLinks.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchSpreadsheetBrokenLinks.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchSpreadsheetBrokenLinks.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchSpreadsheetBrokenLinks.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchSpreadsheetBrokenLinks.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchSpreadsheetBrokenLinks.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchSpreadsheetBrokenLinks.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchSpreadsheetBrokenLinks.go" >}}
{{</tab>}}
{{< /tabs >}}