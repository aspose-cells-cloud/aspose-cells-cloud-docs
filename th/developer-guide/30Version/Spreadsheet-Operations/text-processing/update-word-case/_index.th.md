---
title: "Aspose.Cells – API สำหรับอัปเดตรูปแบบตัวพิมพ์ใหญ่-เล็กของคำ"
second_title: "เอกสาร"
linktype: "เอกสาร"
type: docs
url: /post-update-word-case/
keywords: "Aspose.Cells, API สำหรับอัปเดตรูปแบบตัวพิมพ์ใหญ่-เล็กของคำ, การแปลงรูปแบบตัวพิมพ์ใหญ่-เล็กของข้อความ, Excel, CSV, Google Sheets, REST API"
description: "แปลงรูปแบบตัวพิมพ์ใหญ่-เล็กของข้อความในไฟล์ Excel, CSV หรือ Google Sheets โดยใช้ API สำหรับอัปเดตรูปแบบตัวพิมพ์ใหญ่-เล็กของคำจาก Aspose.Cells Cloud รองรับการเปลี่ยนเป็นตัวพิมพ์ใหญ่/ตัวพิมพ์เล็ก, ตัวพิมพ์ใหญ่ต้นคำ (Title Case) และการขึ้นต้นด้วยตัวพิมพ์ใหญ่สำหรับตัวอักษรตัวแรก"
weight: 100
ArticleTitle: "เอกสารประกอบ Aspose.Cells – API สำหรับอัปเดตรูปแบบตัวพิมพ์ใหญ่-เล็กของคำ"
---

**เวอร์ชัน API:** 3.0

การจัดการรูปแบบตัวพิมพ์ใหญ่-เล็กที่ไม่สอดคล้องกันในสเปรดชีต (Excel, Google Sheets, CSV) อาจทำให้หงุดหงิดได้ โดยเฉพาะเมื่อจัดการกับชุดข้อมูลขนาดใหญ่ **PostUpdateWordCase web API** ช่วยอัตโนมัติการแปลงรูปแบบตัวพิมพ์ใหญ่-เล็กของข้อความ เพื่อให้ข้อมูลของคุณสะอาด สม่ำเสมอ และพร้อมสำหรับการประมวลผลเพิ่มเติมหรือการวิเคราะห์

## **Web API สำหรับ Excel – API สำหรับอัปเดตรูปแบบตัวพิมพ์ใหญ่-เล็กของคำ**

```http
POST https://api.aspose.cloud/v3.0/cells/updatewordcase
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องการ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### **คำอธิบายฟังก์ชัน**

API สำหรับ PostUpdateWordCase ช่วยแก้ปัญหาทั่วไปเกี่ยวกับการใช้รูปแบบตัวพิมพ์ใหญ่-เล็กของข้อความที่ไม่สอดคล้องกันในสเปรดชีต ซึ่งอาจส่งผลกระทบอย่างมากต่อการวิเคราะห์และการประมวลผลข้อมูล API นี้ช่วยอัตโนมัติการแปลงรูปแบบตัวพิมพ์ใหญ่-เล็ก เพื่อให้ข้อมูลของคุณสะอาด สม่ำเสมอ และพร้อมสำหรับการประมวลผลหรือการวิเคราะห์เพิ่มเติม

- **การแปลงรูปแบบตัวพิมพ์ใหญ่-เล็กของข้อความโดยอัตโนมัติ**
  - **ตัวพิมพ์ใหญ่เป็นตัวพิมพ์เล็ก** – แปลงตัวอักษรพิมพ์ใหญ่ทั้งหมดให้เป็นตัวพิมพ์เล็ก
  - **ตัวพิมพ์เล็กเป็นตัวพิมพ์ใหญ่** – แปลงตัวอักษรพิมพ์เล็กทั้งหมดให้เป็นตัวพิมพ์ใหญ่
  - **ขึ้นต้นด้วยตัวพิมพ์ใหญ่** – ขึ้นต้นด้วยตัวพิมพ์ใหญ่สำหรับตัวอักษรตัวแรกของแต่ละคำ
  - **ตัวพิมพ์ใหญ่ต้นคำ (Title Case)** – แปลงข้อความให้อยู่ในรูปแบบตัวพิมพ์ใหญ่ต้นคำ โดยตัวอักษรตัวแรกของคำหลักแต่ละคำจะถูกขึ้นต้นด้วยตัวพิมพ์ใหญ่

- **รองรับหลายรูปแบบไฟล์** – API นี้ทำงานกับรูปแบบสเปรดชีตที่หลากหลาย รวมถึง Excel, OpenOffice, JSON, CSV และอื่นๆ อีกมากมาย ทำให้เหมาะสำหรับความต้องการในการประมวลผลข้อมูลที่หลากหลาย

### **พารามิเตอร์สำหรับคำขอ (Request Parameters)**

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย |
|------------------|--------|----------|-----------|
| `wordCaseOptions` | object | Request body | ตัวเลือกที่กำหนดการเปลี่ยนแปลงรูปแบบตัวพิมพ์ใหญ่-เล็กที่ต้องการ เช่น ช่วงแหล่งข้อมูล ประเภทรูปแบบตัวพิมพ์ใหญ่-เล็กเป้าหมาย และการตั้งค่าเพิ่มเติมอื่นๆ |

**โครงสร้าง `wordCaseOptions`**

```json
{
  "Range": "A1:B10", // ช่วงข้อมูลในรูปแบบ Excel ที่ต้องการประมวลผล (จำเป็นต้องระบุ)
  "CaseType": "Upper", // Enum: Upper, Lower, Capitalize, Title (จำเป็นต้องระบุ)
  "IgnoreBlank": true // ค่าบูลีน, ไม่บังคับ – เมื่อตั้งค่าเป็น true เซลล์ว่างจะไม่ถูกเปลี่ยนแปลง
}
```

**ตัวอย่างเนื้อหาคำขอ (Request Body)**

```json
{
  "Range": "A1:B10",
  "CaseType": "Upper",
  "IgnoreBlank": true
}
```

- **Range** – ช่วงของเซลล์ที่จะใช้การแปลงรูปแบบตัวพิมพ์ใหญ่-เล็ก (เช่น `A1:C5`)
- **CaseType** – ประเภทของการแปลงรูปแบบตัวพิมพ์ใหญ่-เล็ก ค่าที่อนุญาตคือ `Upper`, `Lower`, `Capitalize` และ `Title`
- **IgnoreBlank** – หากตั้งค่าเป็น `true` เซลล์ว่างจะถูกละเลย ค่าเริ่มต้นคือ `false`

### **การตอบกลับ (Response)**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[ชื่อไฟล์ที่รวมแล้ว]",
    "Filesize" : [ขนาดไฟล์],
    "FileContent" : "[Base64String]"
}
```

- **Filename** – ชื่อของไฟล์ที่ผ่านการประมวลผลแล้ว
- **FileSize** – ขนาดของไฟล์เป็นหน่วยไบต์
- **FileContent** – เนื้อหาของไฟล์ที่ผ่านการแปลงแล้วในรูปแบบ Base64

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย | คำอธิบาย |
|------|-----------|-----------|
| 200 | OK | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับประกอบด้วยรายละเอียดของคำสั่งที่ดำเนินการ |
| 400 | Bad Request | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401 | Unauthorized | JWT token ไม่ถูกต้องหรือขาดหาย |
| 413 | Payload Too Large | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด |
| 500 | Internal Server Error | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์ |

## วิธีใช้ PostUpdateWordCase API ด้วย SDKs

### ข้อมูลจำเพาะ PostUpdateWordCase API

<a href="https://reference.aspose.cloud/cells/#/TextProcessingController/PostUpdateWordCase" target="_blank" rel="noopener noreferrer">ข้อมูลจำเพาะ OpenAPI</a> กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้โดยสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำและช่วยให้คุณมุ่งเน้นไปที่งานโครงการของคุณ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้ Aspose.Cells web services โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostUpdateWordCase.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostUpdateWordCase.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostUpdateWordCase.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostUpdateWordCase.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostUpdateWordCase.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostUpdateWordCase.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostUpdateWordCase.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostUpdateWordCase.go" >}}
{{</ tab>}}
{{</ tabs >}}