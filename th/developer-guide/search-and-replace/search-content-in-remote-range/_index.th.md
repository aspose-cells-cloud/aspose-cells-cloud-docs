---
title: "API ค้นหาข้อความใน Excel ของ Aspose.Cells Cloud – ค้นหาข้อความในช่วงของสมุดงานระยะไกล"
second_title: "เอกสาร"
ArticleTitle: "ค้นหาข้อความในสมุดงาน Excel ระยะไกล – ค้นหาข้อมูลในช่วงที่กำหนด"
linktype: "ค้นหาเนื้อหาในช่วงระยะไกล"
type: docs
url: /search-content-in-remote-range/
keywords: "Aspose.Cells, API Excel, ค้นหาข้อความ, ช่วงระยะไกล, สมุดงานบนคลาวด์, REST API, การค้นพบข้อมูล"
description: "ค้นหาข้อความ ตัวเลข หรือสูตรในช่วงที่กำหนดของสมุดงาน Excel ที่จัดเก็บไว้ใน Aspose Cloud"
weight: 100
---

## **ค้นหาเนื้อหาในช่วงระยะไกล**

ค้นหาข้อความที่ระบุภายในช่วงใดๆ ของไฟล์ Excel โดยใช้ Aspose.Cells Cloud API ค้นหาข้อความ ตัวเลข หรือสูตรในไฟล์ที่จัดเก็บในพื้นที่จัดเก็บบนคลาวด์ API แบบ RESTful สำหรับการค้นพบข้อมูลอัตโนมัติ การวิเคราะห์เนื้อหา และกระบวนการทำงานตรวจสอบสมุดงาน

### **เว็บ API**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/content
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

```bash
-H "Authorization: Bearer {access_token}"
```


**ตัวอย่าง cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Orders_2024/ranges/B2:H100/search/content?searchText=Report&ignoreCase=true" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json"
```

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท | Path/Query/String/HTTPBody | คำอธิบาย                                                                                                                                              |
| :------------- | :------ | :------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String  | Path                       | **จำเป็น**. ชื่อไฟล์ (รวมนามสกุล) ของสมุดงาน Excel ที่ต้องการค้นหา เช่น `customer_data.xlsx`                                                      |
| worksheet      | String  | Path                       | **จำเป็น**. ชื่อของเวิร์กชีตที่อยู่ภายในสมุดงานที่ต้องการค้นหา เช่น `Orders_2024`                                                                |
| cellArea       | String  | Path                       | **จำเป็น**. ช่วงของเซลล์เป้าหมายสำหรับการค้นหา โดยระบุในรูปแบบ A1 notation (เช่น `B2:H100`) การค้นหาจะจำกัดอยู่ในพื้นที่นี้เท่านั้น             |
| searchText     | String  | Query                      | **จำเป็น**. ข้อความ ตัวเลข หรือเนื้อหาบางส่วนที่ต้องการค้นหาภายในช่วงเซลล์ที่กำหนด                                                               |
| ignoreCase     | Boolean | Query                      | **ไม่บังคับ**. เมื่อตั้งค่าเป็น `true` การค้นหาจะไม่คำนึงถึงตัวพิมพ์เล็ก-ใหญ่ (เช่น “Report” จะตรงกับ “report”) ค่าเริ่มต้นคือ `false` (แยกแยะตัวพิมพ์เล็ก-ใหญ่) |
| folder         | String  | Query                      | **ไม่บังคับ**. เส้นทางไดเรกทอรีในพื้นที่จัดเก็บบนคลาวด์ที่สมุดงานอยู่ หากไม่ระบุ จะใช้ไดเรกทอรีราก                                               |
| storageName    | String  | Query                      | **ไม่บังคับ**. ตัวระบุสำหรับการตั้งค่าพื้นที่จัดเก็บบนคลาวด์แบบกำหนดเอง หากไม่ระบุ จะใช้พื้นที่จัดเก็บเริ่มต้นของบัญชี                               |
| region         | String  | Query                      | **ไม่บังคับ**. การตั้งค่าวัฒนธรรม/ภูมิภาค (เช่น `en‑AU`) ซึ่งอาจส่งผลต่อการตีความอักขระหรือรูปแบบที่เฉพาะเจาะจงของภูมิภาคระหว่างการค้นหา        |
| password       | String  | Query                      | **ไม่บังคับ**. รหัสผ่านสำหรับถอดรหัสและเข้าถึงไฟล์สมุดงานที่มีการป้องกันด้วยรหัสผ่าน ไม่ต้องระบุหากไฟล์ไม่ได้ถูกเข้ารหัส                             |

### การตอบกลับ

```json
{
  "Code": 200,
  "Status": "OK",
  "TextItems": [
    {
      "Filename": "string",
      "Worksheet": "string",
      "Position": "string",
      "Content": "string"
    }
  ]
}
```

### รหัสข้อผิดพลาด

- **400 Bad Request** – URI ของ Aspose.Cells Cloud API ไม่ถูกต้อง  
- **401 Unauthorized** – token การเข้าถึง รหัสไคลเอนต์ หรือความลับของไคลเอนต์ไม่ถูกต้อง  
- **404 Not Found** – ไม่สามารถเข้าถึงไฟล์สมุดงานได้  
- **500 Server Error** – เงื่อนไขที่ไม่คาดคิดทำให้เซิร์ฟเวอร์ไม่สามารถประมวลผลคำขอได้  

## ควรใช้ API ค้นหาเนื้อหาในช่วงของสมุดงานในกรณีใดบ้าง?

- **การตรวจสอบคุณภาพข้อมูลระดับใหญ่** – ในขั้นตอนการยอมรับของกระบวนการ ETL ในคลังข้อมูล ค้นหาคำอธิบายฟิลด์ที่ขาดหาย ตัวย่อที่ไม่ได้กำหนด หรือข้อความแทน (เช่น `"TBD"` หรือ `"NULL"`) ในตารางแมปข้อมูล (`DataDictionary!B2:F1000`) เพื่อระบุคำจำกัดความข้อมูลที่ไม่สมบูรณ์  
- **การสร้างรายงานแบบไดนามิกและการสกัดเนื้อหา** – ในระบบสร้างรายงานอัตโนมัติ ค้นหาและสกัดบล็อกข้อมูลของช่วงเวลาปัจจุบันที่ทำเครื่องหมายด้วยตัวระบุเฉพาะ (เช่น `"[KPI]"`) จากเวิร์กชีตเทมเพลตที่มีข้อมูลผสมกัน (`Monthly_Metrics!C10:G50`) เพื่อประกอบรายงานสุดท้าย  
- **การวิเคราะห์สัญญาและเอกสารทางกฎหมาย** – เมื่อทบทวนส่วนแนบสมุดงานที่มีข้อความจำนวนมาก ค้นหาคำศัพท์ทางกฎหมายเฉพาะ (เช่น `"liability limit"`), ชื่อบุคคล/องค์กร หรือวันที่ภายในช่วงที่กำหนด (`Contract_Terms!A:A`) เพื่อเร่งกระบวนการทบทวน  

## ทำไมควรใช้ API ค้นหาเนื้อหาในช่วงของสมุดงาน?

- **เป็นมิตรกับนักพัฒนา** – Aspose.Cells Cloud มี SDK รองรับหลายภาษา ช่วยให้พัฒนาได้อย่างรวดเร็วและมีเอกสารประกอบครบถ้วน ซึ่งลดภาระงานพัฒนาเมื่อเทียบกับการสร้างโซลูชันแบบกึ่งเอง  
- **ลดค่าใช้จ่ายด้านแรงงาน** – ไม่จำเป็นต้องมีตำแหน่งเฉพาะสำหรับการจัดการรวมเอกสาร  
- **จ่ายตามการใช้งานจริง** – ไม่ต้องลงทุนล่วงหน้า จ่ายเฉพาะเมื่อเรียกใช้ API เท่านั้น  
- **ไม่มีค่าใช้จ่ายในการดูแลรักษา** – ไม่ต้องดูแลเซิร์ฟเวอร์ ไม่ต้องอัปเดตซอฟต์แวร์ และไม่ต้องกังวลเรื่องความเข้ากันได้  

## วิธีใช้ API ค้นหาเนื้อหาในช่วงของสมุดงานด้วย SDK

### ข้อมูลจำเพาะ OpenAPI

[ข้อมูลจำเพาะ OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchContentInRemoteRange) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และอนุญาตให้คุณดำเนินการโต้ตอบ REST โดยตรงจากเว็บเบราว์เซอร์

### ใช้ Aspose.Cells Cloud SDK

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดเบื้องต้น ทำให้คุณสามารถใช้งานค้นหาเนื้อหาในช่วงของสมุดงานได้โดยใช้โค้ดน้อยที่สุด โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}
---