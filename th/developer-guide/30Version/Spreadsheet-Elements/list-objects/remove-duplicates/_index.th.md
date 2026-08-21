---
title: "ลบแถวที่ซ้ำกันออกจาก ListObject – เอกสารประกอบ API ของ Aspose.Cells Cloud"
second_title: "เอกสาร"
linktype: "ลบรายการที่ซ้ำกัน"
type: docs
keywords: "ลบรายการที่ซ้ำกัน, listobject, API ของ Aspose.Cells Cloud, Excel, REST"
url: /th/list-objects/remove-duplicates/th/
description: "เรียนรู้วิธีการลบแถวที่ซ้ำกันออกจาก ListObject ในแผ่นงาน Excel โดยใช้ REST API ของ Aspose.Cells Cloud ซึ่งรวมถึง endpoint, พารามิเตอร์, การตรวจสอบสิทธิ์ และตัวอย่างคำขอและคำตอบ"
weight: 20
---

REST API นี้จะลบแถวที่ซ้ำกันออกจาก **ListObject** ในแผ่นงาน Excel

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates
```

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์     | ประเภท   | ตำแหน่ง | คำอธิบาย                                             |
| -------------------- | ------- | -------- | ----------------------------------------------------- |
| **name**             | String  | Path     | ชื่อของไฟล์ Excel                                    |
| **sheetName**        | String  | Path     | ชื่อของแผ่นงานที่มี list object                     |
| **listObjectIndex**  | Integer | Path     | ดัชนีแบบ zero-based ของ list object ที่ต้องการประมวลผล |
| **folder**           | String  | Query    | (ไม่บังคับ) เส้นทางโฟลเดอร์ที่จัดเก็บไฟล์ไว้         |
| **storageName**      | String  | Query    | (ไม่บังคับ) ชื่อของบริการจัดเก็บข้อมูล                |

### ตัวอย่างคำขอ (cURL)

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="คำตอบ" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "DuplicateRowsRemoved": 12,
  "Message": "ลบแถวที่ซ้ำกันเรียบร้อยแล้ว"
}
```

{{< /tab >}}
{{< /tabs >}}

### คำตอบ

เมื่อสำเร็จ บริการจะคืนค่า JSON object ที่คล้ายกับตัวอย่างด้านบน โดยมีฟิลด์ต่างๆ ดังนี้:

- **Code** – รหัสสถานะ HTTP (`200` สำหรับความสำเร็จ)
- **Status** – คำอธิบายข้อความของสถานะ
- **DuplicateRowsRemoved** – จำนวนแถวที่ถูกลบออก
- **Message** – ข้อมูลเพิ่มเติมเกี่ยวกับการดำเนินการ

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | คำอธิบาย                                           |
|------|-------------------------------|-----------------------------------------------------|
| 200  | สำเร็จ (OK)                   | ใช้ตัวกรองเรียบร้อยแล้ว; คำตอบประกอบด้วยรายละเอียดการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | JWT token ไม่ถูกต้องหรือขาดหาย                        |
| 413  | ข้อมูลส่งไปมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดเกินขีดจำกัดขนาด                        |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์               |

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบที่ repository บน GitHub เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectRemoveDuplicates.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectRemoveDuplicates.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectRemoveDuplicates.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectRemoveDuplicates.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectRemoveDuplicates.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectRemoveDuplicates.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectRemoveDuplicates.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectRemoveDuplicates.go" >}}

{{< /tab >}}

{{< /tabs >}}