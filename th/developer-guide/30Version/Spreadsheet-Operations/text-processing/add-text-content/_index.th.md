---
title: "เพิ่มข้อความลงใน Excel: แทรกข้อมูลอย่างมีประสิทธิภาพด้วย Spreadsheet Web API"
second_title: "เอกสาร"
linktype: "เพิ่มข้อความ"
type: docs
url: /th/excel-add-text/
keywords: "Excel, Aspose.Cells, เพิ่มข้อความ, Spreadsheet API, REST API, Office Cloud, การแทรกข้อความ, Excel API"
description: "เพิ่มข้อความลงในตำแหน่งที่ระบุในสมุดงาน Excel ผ่าน Aspose.Cells Cloud API"
weight: 100
---

เพิ่มเนื้อหาข้อความลงในตำแหน่งที่ระบุภายในสมุดงาน ซึ่งต้องการออบเจกต์ที่กำหนดข้อความที่จะเพิ่มและตำแหน่งที่จะแทรก

## **Excel API: PostAddTextContent**

```
POST http://api.aspose.cloud/v3.0/cells/addtext
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### **คำอธิบายฟังก์ชัน**

เมธอดนี้เพิ่มข้อความใหม่ลงในเซลล์ที่ระบุอย่างปลอดภัย โดยรองรับโหมดการแทรกหลายแบบและการจัดการรูปแบบ

- **เพิ่มข้อความลงต้นเซลล์ที่เลือก**  
  แทรกข้อความไว้หน้าเซลล์ที่เลือกทั้งหมด ช่วยให้ข้อมูลที่ป้อนมีความสอดคล้องกัน เหมาะสำหรับการเพิ่มตัวระบุหรือป้ายกำกับทั่วไป เช่น รหัสสินค้า หมวดหมู่ หรือคำนำหน้า

- **แทรกอักขระก่อนหรือหลังข้อความที่ระบุ**  
  วางอักขระก่อนหรือหลังข้อความเป้าหมายในเซลล์ที่เลือก ช่วยให้คุณสร้างเนื้อหาที่มีโครงสร้างและจัดระเบียบได้ง่าย

- **เพิ่มข้อความเดียวกันลงท้ายเซลล์ที่เลือกทั้งหมด**  
  เพิ่มข้อความเดียวกันลงท้ายเซลล์หลายเซลล์ในหนึ่งการดำเนินการ ช่วยให้การป้อนข้อมูลง่ายขึ้นและรับประกันลักษณะที่สม่ำเสมอ

- **แทรกข้อความก่อนหรือหลังจำนวนอักขระที่กำหนด**  
  แทรกข้อความหลังจำนวนอักขระที่กำหนดจากจุดเริ่มต้นหรือจุดสิ้นสุดของแต่ละเซลล์ในช่วงที่ระบุ ใช้ทั่วไปในการจัดรูปแบบรหัส วันที่เวลา หรือตัวคั่นแบบกำหนดเอง

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
|----------------|---------|----------|-----------|
| addTextOptions | Class   | Body     | ระบุเนื้อหาข้อความและตำแหน่งที่จะเพิ่มข้อความ |

### **การตอบกลับ**

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย |
|------|------------------------------|-----------|
| 200  | สำเร็จ (OK)                 | กรองข้อมูลเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400  | คำขอผิด (Bad Request)       | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | JWT token ไม่ถูกต้องหรือขาดหาย |
| 413  | ข้อมูลในคำขอใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

## วิธีใช้ PostAddTextContent API ร่วมกับ SDK

### ข้อมูลเฉพาะของ PostAddTextContent API

[OpenAPI Specification](https://reference.aspose.cloud/cells/#/TextProcessingController/PostAddTextContent) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้สาธารณะ และช่วยให้คุณดำเนินการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่มีประสิทธิภาพที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานโครงการของคุณ โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostAddTextContent.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostAddTextContent.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostAddTextContent.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostAddTextContent.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostAddTextContent.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostAddTextContent.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostAddTextContent.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostAddTextContent.go" >}}
{{</ tab>}}
{{< /tabs >}}