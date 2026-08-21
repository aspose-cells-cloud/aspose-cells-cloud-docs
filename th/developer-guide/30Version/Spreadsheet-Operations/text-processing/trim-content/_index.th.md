---
title: "Aspose.Cells Trim Content API – ลบช่องว่างและตัวขึ้นบรรทัดใหม่จาก Excel"
second_title: "เอกสาร"
linktype: "Trim Content"
type: docs
url: /th/spreadsheet-trim-content/
keywords: "Aspose.Cells, Trim Content API, ทำความสะอาดข้อมูล Excel, ลบช่องว่างใน Excel, การลบตัวขึ้นบรรทัดใหม่, การทำความสะอาดข้อมูลสเปรดชีต"
description: "ใช้ API PostTrimContent ของ Aspose.Cells Cloud เพื่อลบช่องว่างส่วนเกิน ตัวขึ้นบรรทัดใหม่ และอักขระที่ไม่จำเป็นออกจากเซลล์ Excel อ่านข้อมูลเกี่ยวกับ endpoint รูปแบบคำขอ ตัวอย่างโค้ด และการจัดการข้อผิดพลาด"
weight: 100
---

## **Excel Web API: PostTrimContent**

**PostTrimContent** API ใช้ประมวลผลและตัดเนื้อหาในช่วงที่ระบุภายในสเปรดชีต โดยจะลบช่องว่างส่วนเกิน ตัวขึ้นบรรทัดใหม่ และอักขระที่ไม่จำเป็นอื่นๆ ออกจากเนื้อหาของเซลล์ที่เลือก ทำให้เหมาะสำหรับการทำความสะอาดข้อมูลที่ป้อนเข้า และรักษาการจัดรูปแบบสเปรดชีตอย่างสม่ำเสมอ

```http
POST https://api.aspose.cloud/v3.0/cells/trimcontent
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### **คำอธิบายฟังก์ชัน**

- **ประสิทธิภาพ** – ตัดเนื้อหาเฉพาะในช่วงที่กำหนดเท่านั้น ช่วยประหยัดเวลาและทรัพยากรโดยไม่ต้องดำเนินการกับทั้งแผ่นงาน
- **ความยืดหยุ่น** – อนุญาตให้ผู้ใช้กำหนดช่วงเซลล์ที่ต้องการประมวลผลอย่างแม่นยำ รองรับชุดข้อมูลและความต้องการที่หลากหลาย
- **ความสมบูรณ์ของข้อมูล** – ลบช่องว่างส่วนเกินและตัวขึ้นบรรทัดใหม่ ช่วยรักษาข้อมูลที่สอดคล้องและน่าเชื่อถือสำหรับการวิเคราะห์และการรายงาน
- **ความง่ายในการใช้งาน** – การผสานรวมที่เรียบง่ายด้วยการตั้งค่าขั้นต่ำ เหมาะสำหรับทั้งนักพัฒนาและผู้ใช้ทั่วไป

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์   | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                                   |
| ------------------ | --------- | -------- | ------------------------------------------------------------------------------------------ |
| trimContentOptions | คลาส      | Body     | ตัวเลือกที่ระบุวิธีการตัดเนื้อหา (เช่น ช่วงเป้าหมาย โหมดการตัด)                           |

### **การตอบกลับ**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[ชื่อไฟล์ที่รวมแล้ว]",
    "Filesize" : [ขนาดไฟล์],
    "FileContent" : "[Base64String]"
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | คำอธิบาย                                                                 |
|------|------------------------------|--------------------------------------------------------------------------|
| 200  | OK                           | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับประกอบด้วยรายละเอียดของกระบวนการ |
| 400  | Bad Request                  | พารามิเตอร์สูญหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ)         |
| 401  | Unauthorized                 | JWT token ไม่ถูกต้องหรือขาดหาย                                           |
| 413  | Payload Too Large            | ไฟล์ที่อัปโหลดเกินขีดจำกัดขนาด                                          |
| 500  | Internal Server Error        | ข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด                                     |

## วิธีใช้ PostRemoveCharacters API ด้วย SDK

### ข้อกำหนด PostRemoveCharacters API

[OpenAPI Specification](https://reference.aspose.cloud/cells/#/TextProcessingController/PostTrimContent) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้สาธารณะ และช่วยให้คุณดำเนินการโต้ตอบ REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานโครงการของคุณ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) สำหรับรายการ SDK ของ Aspose.Cells Cloud อย่างสมบูรณ์

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostTrimContent.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostTrimContent.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostTrimContent.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostTrimContent.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostTrimContent.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostTrimContent.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostTrimContent.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostTrimContent.go" >}}
{{</ tab>}}
{{< /tabs >}}

_อัปเดตล่าสุด: 2026-03-30_