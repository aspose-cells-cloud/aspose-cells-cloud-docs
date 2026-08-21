---
title: "แทรกตัวกรองแบบสไลเซอร์ลงใน ListObject ของ Excel – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktitle: "แทรกสไลเซอร์"
type: docs
keywords: "Aspose.Cells, สไลเซอร์ Excel, ListObject, REST API, SDK บนคลาวด์"
description: "เรียนรู้วิธีการเพิ่มสไลเซอร์ลงใน ListObject ของ Excel โดยใช้ Aspose.Cells Cloud REST API (เวอร์ชัน 3.0) ซึ่งประกอบด้วย endpoint, พารามิเตอร์, การตรวจสอบสิทธิ์, ตัวอย่างคำสั่ง cURL และ JSON ของคำตอบ"
weight: 20
ArticleTitle: "แทรกตัวกรองแบบสไลเซอร์ลงใน ListObject ของ Excel – Aspose.Cells Cloud API"
---

REST API นี้แทรกสไลเซอร์ให้กับ list object บนแผ่นงาน Excel

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer
```

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
|------------------|-----------|---------|----------|
| name | String | Path | ชื่อไฟล์ Excel |
| sheetName | String | Path | ชื่อของแผ่นงานที่มี list object |
| listObjectIndex | Integer | Path | ดัชนีแบบ zero-based ของ list object ที่จะเพิ่มสไลเซอร์ |
| columnIndex | Integer | Query | ดัชนีแบบ zero-based ของคอลัมน์ที่สไลเซอร์อ้างอิง |
| destCellName | String | Query | ที่อยู่อ้างอิงของเซลล์ (เช่น **A1**) ที่จะวางสไลเซอร์ |
| folder | String | Query | โฟลเดอร์ในพื้นที่จัดเก็บที่มีไฟล์ Excel |
| storageName | String | Query | ชื่อบริการพื้นที่จัดเก็บของ Aspose Cloud |

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเรียกใช้ API ได้:

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="คำตอบ" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **หมายเหตุ:** คำขอนี้ต้องใช้ JWT bearer token ที่ถูกต้องซึ่งได้รับจากบริการตรวจสอบสิทธิ์ของ Aspose Cloud API จุดปลายทางนี้ไม่ต้องการเนื้อหาในคำขอ; ส่ง object JSON ว่าง `{}` หากไลบรารีไคลเอนต์ของคุณบังคับให้มี payload

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Slicer": {
    "Name": "Slicer1",
    "ColumnIndex": 2,
    "Position": "A1"
  }
}
```

> **หัวเรื่องคำตอบ:** `Content-Type: application/json`

{{< /tab >}}
{{< /tabs >}}

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย | คำอธิบาย |
|------|----------|----------|
| 200 | สำเร็จ (OK) | แอ็พพลายตัวกรองเรียบร้อยแล้ว; คำตอบมีรายละเอียดของคำสั่ง |
| 400 | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401 | ไม่ได้รับอนุญาต (Unauthorized) | JWT token ไม่ถูกต้องหรือขาดหาย |
| 413 | Payload ใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดเกินขีดจำกัดขนาด |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์ |

### การจัดการข้อผิดพลาด

เมื่อเกิดข้อผิดพลาด API จะส่งกลับ JSON object ที่มีฟิลด์ `ErrorMessage` ซึ่งอธิบายปัญหาไว้ ตรวจสอบ HTTP status code และ `ErrorMessage` เพื่อกำหนดแนวทางการแก้ไข

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ และช่วยให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบที่ repository บน GitHub เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectInsertSlicer.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectInsertSlicer.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectInsertSlicer.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectInsertSlicer.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectInsertSlicer.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectInsertSlicer.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectInsertSlicer.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectInsertSlicer.go" >}}
{{< /tab >}}

{{< /tabs >}}