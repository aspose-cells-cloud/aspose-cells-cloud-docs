---
title: "ลบคอลัมน์ว่างจาก Excel ด้วย Aspose.Cells Cloud API – ตัวอย่าง REST อย่างรวดเร็ว"
second_title: "เอกสาร"
ArticleTitle: "วิธีลบคอลัมน์ว่างใน Excel – ทำให้กระบวนการล้างคอลัมน์เป็นอัตโนมัติ"
linktype: "ลบคอลัมน์ว่าง"
type: docs
url: /delete-spreadsheet-blank-columns/
keywords: "API ลบคอลัมน์ว่างใน Excel, Aspose.Cells Cloud, REST API, การล้างไฟล์ Excel, การทำให้ตารางงานเป็นอัตโนมัติ"
description: "เรียนรู้วิธีลบคอลัมน์ว่างออกจากไฟล์ Excel โดยใช้ Aspose.Cells Cloud REST API พร้อมตัวอย่าง endpoint, การยืนยันตัวตน, ตัวอย่างคำขอ/การตอบกลับ และโค้ด SDK ใน C#, Java, Python และอื่นๆ"
weight: 100
---

ใช้ Aspose.Cells Cloud API เพื่อลบคอลัมน์ว่างทั้งหมดออกจากตารางงาน Excel โดยอัตโนมัติ API ที่ชาญฉลาดนี้ตรวจจับและลบคอลัมน์ที่เซลล์ภายในไม่มีข้อมูล สูตร ความคิดเห็น แผนภูมิ หรือวัตถุใดๆ API รองรับการประมวลผลแบบแบตช์ การทำให้เป็นอัตโนมัติผ่านคลาวด์ และการผสานรวม REST แบบเนียนสำหรับกระบวนการล้างตารางงานระดับองค์กร

**พื้นหลัง:**  
คอลัมน์ว่างมักปรากฏขึ้นหลังการนำเข้าข้อมูล การสร้างเทมเพลต หรือการย้ายถ่ายไฟล์รุ่นเก่า การลบคอลัมน์ว่างเหล่านี้ช่วยปรับปรุงขนาดไฟล์ ประสิทธิภาพการเรนเดอร์ และความถูกต้องของการประมวลผลข้อมูลขั้นตอนถัดไป API สำหรับลบคอลัมน์ว่างในตารางงานจึงเป็นวิธีที่รวดเร็วและดำเนินการบนเซิร์ฟเวอร์เพื่อล้างตารางงานโดยไม่ต้องแก้ไขด้วยตนเอง

## **DeleteSpreadsheetBlankColumns API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/delete/blank-columns
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องการ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

```bash
-H "Authorization: Bearer {access_token}"
```

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์   | ประเภท   | ตำแหน่ง                     | คำอธิบาย                                                                                                                       |
| ------------------ | -------- | ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | ไฟล์     | Form‑Data (multipart)        | สมุดงาน Excel ที่ต้องประมวลผล                                                                                                  |
| **outPath**        | สตริง    | Query                        | ทางเลือก โฟลเดอร์ปลายทางในพื้นที่จัดเก็บบนคลาวด์สำหรับไฟล์ที่ล้างแล้ว หากไม่ระบุ ผลลัพธ์จะถูกส่งกลับในเนื้อหาของคำตอบ |
| **outStorageName** | สตริง    | Query                        | ทางเลือก ชื่อของพื้นที่จัดเก็บบนคลาวด์ที่จะบันทึกผลลัพธ์                                                                      |
| **region**         | สตริง    | Query                        | ทางเลือก ตัวระบุภาษา和地区 (เช่น `en-US`, `de-DE`)                                                                              |
| **password**       | สตริง    | Query                        | ทางเลือก รหัสผ่านสำหรับเปิดสมุดงานที่ได้รับการป้องกัน                                                                         |

### การตอบกลับ

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

### รหัสข้อผิดพลาด

- **400 Bad Request** – พารามิเตอร์คำขอไม่ถูกต้องหรือ URI มีรูปแบบผิด
- **401 Unauthorized** – โทเคนการเข้าถึงขาดหายหรือไม่ถูกต้อง
- **404 Not Found** – ไม่พบไฟล์ Excel ที่ระบุ
- **500 Server Error** – เงื่อนไขที่ไม่คาดคิดทำให้ API ไม่สามารถประมวลผลไฟล์ได้

## เมื่อใดควรใช้ API สำหรับลบคอลัมน์ว่างในตารางงาน

- **กระบวนการนำเข้าข้อมูลและการล้างข้อมูล** – ลบคอลัมน์ว่างท้ายหรือคอลัมน์โครงสร้างทันทีหลังจากโหลดข้อมูลจาก CSV ฐานข้อมูล หรือ API บนเว็บ
- **การสร้างรายงานและแดชบอร์ด** – รับประกันว่ารายงานสุดท้ายมีเค้าโครงที่สะอาดโดยไม่มีคอลัมน์ว่างที่ไม่จำเป็น
- **พายพล ETL** – ประมวลผลล่วงหน้าไฟล์ Excel ก่อนโหลดลงในคลังข้อมูล เช่น Snowflake หรือ BigQuery
- **การผสานรวมระบบ** – ทำให้ไฟล์ Excel ที่ผู้ให้บริการภายนอกส่งมามาตรฐานก่อนประมวลผลเพิ่มเติม
- **การทำให้เอกสารเป็นอัตโนมัติแบบแบตช์** – ลบคอลัมน์ตัวอย่างออกจากเทมเพลตที่สร้างขึ้นเป็นจำนวนมาก
- **เนื้อหาที่ผู้ใช้สร้าง** – ล้างไฟล์ Excel ที่อัปโหลดจากพอร์ทัลเว็บก่อนจัดเก็บหรือวิเคราะห์
- **การย้ายข้อมูลเก่า** – ทำให้คลังข้อมูลตารางงานเก่าเรียบร้อยโดยลบคอลัมน์ที่ว่างมาแต่เดิม

## เหตุใดจึงควรใช้ API นี้

- **เป็นมิตรกับนักพัฒนา** – มี SDK ให้ใช้งานใน C#, Java, Python, PHP, Ruby, Node.js, Go และอื่นๆ ช่วยลดความพยายามในการพัฒนา
- **คุ้มค่า** – รูปแบบการชำระเงินตามการใช้งานช่วยลดต้นทุนโครงสร้างพื้นฐานล่วงหน้า
- **ไม่ต้องดูแลรักษา** – ไม่ต้องจัดการเซิร์ฟเวอร์ บริการได้รับการอัปเดตอย่างต่อเนื่องโดย Aspose

## วิธีใช้ API สำหรับลบคอลัมน์ว่างในตารางงานด้วย SDK

### ข้อมูลจำเพาะ API

[ข้อมูลจำเพาะ API สำหรับลบคอลัมน์ว่างในตารางงาน](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/RemoveSpreadsheetBlankColumns) ให้คำจำกัดความ OpenAPI แบบเต็มและตัวอย่าง

### การใช้งาน Aspose.Cells Cloud SDKs

SDK ทำหน้าที่ซ่อนรายละเอียด HTTP ระดับต่ำ ช่วยให้คุณลบคอลัมน์ว่างได้ด้วยโค้ดเพียงไม่กี่บรรทัด ดูที่ repository อย่างเป็นทางการบน GitHub เพื่อดูรายชื่อภาษาที่รองรับทั้งหมด: <https://github.com/aspose-cells-cloud>

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียก API ด้วย SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteSpreadsheetBlankColumns.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteSpreadsheetBlankColumns.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteSpreadsheetBlankColumns.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteSpreadsheetBlankColumns.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteSpreadsheetBlankColumns.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteSpreadsheetBlankColumns.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteSpreadsheetBlankColumns.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteSpreadsheetBlankColumns.go" >}}
{{</tab>}}
{{< /tabs >}}
---