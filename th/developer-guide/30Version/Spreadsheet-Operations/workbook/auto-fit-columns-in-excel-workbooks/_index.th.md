---
title: "ปรับขนาดคอลัมน์ให้พอดีในไฟล์ Excel"
second_title: "เอกสาร"
linktype: "คอลัมน์"
type: docs
url: /autofit-columns-on-an-excel-file/
aliases:
  [
    "/auto-fit-columns-in-excel-workbooks",
    "/autofit-columns-in-excel-workbooks/",
    "/columns/autofit/",
    "/workbook/autofit/columns/",
  ]
keywords: "ปรับขนาดคอลัมน์ให้พอดี, Excel, Aspose.Cells Cloud, REST API, SDK, cURL, API"
description: "เรียนรู้วิธีใช้ Aspose.Cells Cloud REST API เพื่อปรับขนาดคอลัมน์ให้พอดีในสมุดงาน Excel รวมถึงรายละเอียดคำขอ ตัวอย่าง cURL และตัวอย่างโค้ด SDK สำหรับภาษาต่างๆ"
weight: 90
---

REST API นี้รองรับการปรับขนาดคอลัมน์ให้พอดีในสมุดงาน Excel

## API PostAutofitWorkbookColumns

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitcolumns
```

พารามิเตอร์คำขอมีดังนี้:

| ชื่อพารามิเตอร์      | ประเภท   | ตำแหน่ง | คำอธิบาย                                         |
| --------------------- | ------- | -------- | ------------------------------------------------- |
| **name**              | สตริง   | path     | ชื่อไฟล์สมุดงาน                                 |
| **autoFitterOptions** | ออบเจกต์ | body     | ตัวเลือกที่ควบคุมพฤติกรรมการปรับขนาดให้พอดี   |
| **startColumn**       | จำนวนเต็ม | query    | ดัชนีแบบเริ่มต้นที่ 0 ของคอลัมน์แรกที่จะปรับขนาดให้พอดี |
| **endColumn**         | จำนวนเต็ม | query    | ดัชนีแบบเริ่มต้นที่ 0 ของคอลัมน์สุดท้ายที่จะปรับขนาดให้พอดี |
| **folder**            | สตริง   | query    | โฟลเดอร์ที่เก็บสมุดงาน                         |
| **storageName**       | สตริง   | query    | ชื่อของบริการจัดเก็บข้อมูล                      |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookColumns){:rel="noopener noreferrer"} นิยามอินเทอร์เฟซโปรแกรมที่เข้าถึงได้สาธารณะ และช่วยให้คุณดำเนินการโต้ตอบแบบ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง cURL เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitcolumns" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

> **หมายเหตุ:** ให้ใช้ปลายทาง HTTPS เสมอในระบบจริง และรักษาความลับของโทเค็น JWT ของคุณ

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### ข้อกำหนดเบื้องต้น
ก่อนเรียกใช้งานโอเปอเรชันนี้ ให้ตรวจสอบว่าคุณมีคีย์ API ของ Aspose Cloud ที่ถูกต้อง โทเค็น JWT ที่สร้างขึ้น และสมุดงานเป้าหมายมีอยู่แล้วในตำแหน่งที่จัดเก็บที่ระบุ

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                   | คำอธิบาย                                       |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                | ใช้ตัวกรองเรียบร้อยแล้ว การตอบกลับมีรายละเอียดโอเปอเรชัน |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                 |
| 413  | ข้อมูลร้องขอใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด               |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์        |

API สามารถส่งรหัสสถานะ HTTP ต่อไปนี้กลับมา:

| รหัส | คำอธิบาย                                     |
|------|---------------------------------------------|
| 200  | สำเร็จ – คอลัมน์ถูกปรับขนาดให้พอดีแล้ว     |
| 400  | คำขอไม่ถูกต้อง – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง |
| 401  | ไม่ได้รับอนุญาต – โทเค็น JWT ไม่ถูกต้องหรือหมดอายุ |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ – การประมวลผลภายในล้มเหลว |

## ครอบครัว SDK สำหรับคลาวด์

การใช้ SDK เป็นวิธีที่มีประสิทธิภาพที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะของโครงการของคุณ โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}