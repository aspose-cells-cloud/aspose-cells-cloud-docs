---
title: "ซ่อมแซมไฟล์ Excel"
second_title: "เอกสาร"
type: docs
linktitle: "ซ่อมแซมไฟล์ Excel"
url: /repair-excel-files/
keywords: "Aspose Cells, API ซ่อมแซม Excel, XLSX ที่เสียหาย, การกู้คืนสเปรดชีต, API บนคลาวด์"
description: "ใช้ Aspose.Cells Cloud REST API เพื่อซ่อมแซมไฟล์ Excel ที่เสียหาย (XLS, XLSX, XLSM, XLSB, ODS) อัปโหลดไฟล์หนึ่งไฟล์หรือหลายไฟล์ เลือกรูปแบบไฟล์ผลลัพธ์ และรับไฟล์ที่ซ่อมแซมแล้วในรูปแบบ Base64 ไม่จำเป็นต้องติดตั้งโปรแกรมใดๆ"
weight: 39
---

REST API นี้ช่วยให้คุณสามารถ **ซ่อมแซม** ไฟล์ Excel ได้

- ซ่อมแซมไฟล์สเปรดชีตรูปแบบต่างๆ เช่น XLS, XLSX, XLSM, XLSB, ODS และอื่นๆ  
- รองรับการอัปโหลดไฟล์หลายไฟล์ในคำขอเดียว

Aspose.Cells Cloud Excel Repair ช่วยกู้คืนข้อมูลจากไฟล์ Excel ที่เสียหายผ่านออนไลน์โดยไม่ต้องติดตั้งโปรแกรมใดๆ ไฟล์ Excel ที่เสียหายมักเป็นปัญหาเนื่องจากไม่สามารถเปิดใช้งานได้ คุณสามารถใช้แอป Aspose.Cells Cloud Excel Repair เพื่อกู้คืนข้อมูลจากไฟล์ดังกล่าว

## REST API

ปลายทาง (endpoint) **ซ่อมแซมไฟล์ Excel** ใช้ซ่อมแซมไฟล์สเปรดชีตที่เสียหาย และส่งเนื้อหาที่ซ่อมแซมแล้วกลับมา

```bash
POST https://api.aspose.cloud/v3.0/cells/repair
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยสูงและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ประเภทข้อมูล | ตำแหน่ง                     | คำอธิบาย |
|----------------|--------|------------------------------|-------------|
| file           | ไฟล์   | formData (multipart)         | ไฟล์ที่จะอัปโหลด |
| format         | สายอักขระ | query                        | รูปแบบไฟล์ผลลัพธ์ที่ต้องการ หากไม่ระบุ (null) รูปแบบไฟล์ผลลัพธ์จะเท่ากับรูปแบบไฟล์ต้นฉบับ |

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

| รหัส | ความหมาย                     | คำอธิบาย                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                          | ประมวลผลสำเร็จ; การตอบกลับประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request)                 | พารามิเตอร์สูญหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)                | JWT token ไม่ถูกต้องหรือสูญหาย |
| 413  | ข้อมูลในคำขอใหญ่เกินไป (Payload Too Large)           | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error)       | เกิดข้อผิดพลาดที่ไม่คาดคิดภายในเซิร์ฟเวอร์ |
## วิธีใช้ PostRepair API ด้วย SDK

### ข้อมูลจำเพาะของ PostRepair API

[ข้อมูลจำเพาะ OpenAPI](https://reference.aspose.cloud/cells/#/LightCells/PostRepair) นิยามอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถใช้งาน REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/repair" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@file1.xlsx' \
  -F 'file2=@file2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "file2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

เมื่อสำเร็จ บริการจะส่งกลับ HTTP 200 พร้อมข้อมูล JSON ที่มีอาร์เรย์ `Files` สำหรับสถานการณ์ที่เกิดข้อผิดพลาด API จะใช้รหัสสถานะ HTTP มาตรฐานต่อไปนี้:

- **400 Bad Request** – พารามิเตอร์ไม่ถูกต้องหรือไฟล์ที่ไม่สามารถกู้คืนได้  
- **401 Unauthorized** – JWT token สูญหายหรือไม่ถูกต้อง  
- **413 Payload Too Large** – ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด  
- **500 Internal Server Error** – เกิดข้อขัดข้องที่ไม่คาดคิดภายในเซิร์ฟเวอร์

## ครอบครัว Cloud SDK

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ และช่วยให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostRepair.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostRepair.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostRepair.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostRepair.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostRepair.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostRepair.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostRepair.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostRepair.go" >}}

{{< /tab >}}

{{< /tabs >}}