---
title: "ปรับขนาดแถวให้พอดีในสมุดงาน Excel"
second_title: "เอกสาร"
linktype: "แถว"
type: docs
url: /autofit-rows-on-an-excel-file/
aliases: [/auto-fit-rows-in-excel-workbooks/, /workbook/autofit/rows/]
keywords: "ปรับขนาดแถวให้พอดี, สมุดงาน Excel, Aspose.Cells Cloud, REST API, ตัวเลือกการปรับขนาดอัตโนมัติ"
description: "เรียนรู้วิธีการปรับความสูงของแถวให้อัตโนมัติในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API ซึ่งประกอบด้วย endpoint, พารามิเตอร์, ตัวอย่าง cURL และโค้ดตัวอย่าง SDK สำหรับ C#, Java, Python และอื่นๆ อีกมากมาย"
weight: 90
ArticleTitle: "ปรับขนาดแถวให้พอดีในสมุดงาน Excel – Aspose.Cells Cloud API"
---

**ข้อกำหนดเบื้องต้น**  
ก่อนเรียก API คุณต้องรับโทเค็น Bearer JWT ที่ถูกต้องจากบริการยืนยันตัวตนของ Aspose และตรวจสอบให้แน่ใจว่าสมุดงานเป้าหมายถูกจัดเก็บไว้ในตำแหน่งที่เก็บข้อมูลที่รองรับ (ค่าเริ่มต้นคือการจัดเก็บเริ่มต้น หรือคุณสามารถกำหนดเองได้)

REST API นี้ช่วยให้คุณสามารถ **ปรับขนาดแถวให้พอดี** ในสมุดงาน Excel โดยจะปรับความสูงของแถวอัตโนมัติเมื่อมีการแทรกหรือแก้ไขข้อมูล

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitrows
```

พารามิเตอร์ของคำขอประกอบด้วย:

| ชื่อพารามิเตอร์   | ชนิดข้อมูล        | ตำแหน่ง | คำอธิบาย                                                                 |
| ----------------- | ----------------- | -------- | ------------------------------------------------------------------------ |
| name              | string            | path     | ชื่อของไฟล์สมุดงาน                                                      |
| autoFitterOptions | AutoFitterOptions | body     | ตัวเลือกที่ควบคุมพฤติกรรมการปรับขนาดอัตโนมัติ                          |
| startRow          | integer           | query    | ดัชนีของแถวแรกที่จะปรับขนาดให้พอดี                                     |
| endRow            | integer           | query    | ดัชนีของแถวสุดท้ายที่จะปรับขนาดให้พอดี                                 |
| firstColumn       | integer           | query    | ดัชนีของคอลัมน์แรกที่ใช้พิจารณาในการปรับขนาดให้พอดี                   |
| lastColumn        | integer           | query    | ดัชนีของคอลัมน์สุดท้ายที่ใช้พิจารณาในการปรับขนาดให้พอดี               |
| onlyAuto          | boolean           | query    | หากตั้งค่าเป็น **true** จะประมวลผลเฉพาะแถวที่มีแฟลก AutoFit เท่านั้น (ค่าเริ่มต้นคือ **false**) |
| folder            | string            | query    | เส้นทางโฟลเดอร์ที่จัดเก็บสมุดงาน                                        |
| storageName       | string            | query    | ชื่อของบริการที่เก็บข้อมูล                                               |

**AutoFitterOptions** เป็นวัตถุที่ระบุวิธีการดำเนินการปรับขนาดให้พอดี (เช่น `AutoFitMergedCells`, `IgnoreHidden`)

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                 | คำอธิบาย                                                                 |
|------|---------------------------|--------------------------------------------------------------------------|
| 200  | สำเร็จ (OK)              | ใช้ตัวกรองสำเร็จ; การตอบกลับจะมีรายละเอียดของการดำเนินการ             |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ)           |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                                          |
| 413  | ข้อมูลส่งออกมากเกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด                               |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                               |

[สเปค OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookRows) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการโต้ตอบ REST ผ่านเบราว์เซอร์เว็บได้โดยตรง

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่ง command-line เพื่อเรียกใช้บริการเว็บของ Aspose.Cells โดยแทนที่ `<jwt token>` ด้วยโทเค็น Bearer JWT ที่ถูกต้องที่ได้รับจากบริการยืนยันตัวตนของ Aspose

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitrows" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*ตัวอย่างการตอบกลับข้อผิดพลาด (เช่น สมุดงานไม่พบ):*

```json
{
  "Code": 404,
  "Status": "Not Found",
  "Message": "ไม่พบสมุดงานที่ระบุ 'myWorkbook.xlsx'"
}
```

{{< /tab >}}

{{< /tabs >}}

**หมายเหตุ**  
- เมื่อตั้งค่า `AutoFitMergedCells` เป็น **true** เซลล์ที่ถูกรวมจะถูกพิจารณาเป็นหน่วยเดียวกันระหว่างการดำเนินการปรับขนาดให้พอดี  
- การตั้งค่า `IgnoreHidden` เป็น **true** จะข้ามแถวและคอลัมน์ที่ซ่อนอยู่ และรักษาความสูง/ความกว้างปัจจุบันไว้

## ชุด SDK สำหรับคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา โดย SDK จะซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่โปรเจกต์ของคุณได้ ดู [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookRows.go" >}}

{{< /tab >}}

{{< /tabs >}}