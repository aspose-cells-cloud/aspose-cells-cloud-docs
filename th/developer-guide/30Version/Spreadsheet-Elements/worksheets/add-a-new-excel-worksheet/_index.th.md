---
title: "เพิ่มแผ่นงาน Excel"
ArticleTitle: "เพิ่มแผ่นงาน Excel - คู่มือ API ของ Aspose.Cells Cloud"
second_title: "เอกสาร"
linktype: "เพิ่ม"
type: docs
url: /worksheets/add/
aliases: [/add-a-new-excel-worksheet/]
keywords: "เพิ่มแผ่นงาน Excel, Aspose.Cells Cloud, REST API, PUT worksheet, สมุดงาน Excel, API request"
description: "คู่มือแบบทีละขั้นตอนในการเพิ่มแผ่นงานใหม่ลงในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API ซึ่งประกอบด้วยรายละเอียดคำขอตัวอย่าง cURL และโค้ดตัวอย่าง SDK สำหรับหลายภาษา"
weight: 20
---

REST API นี้เพิ่มแผ่นงานใหม่ลงในสมุดงานที่มีอยู่

**ข้อกำหนดเบื้องต้น**: เพื่อเรียกใช้จุดปลายทางนี้ คุณต้องมีโทเคนยืนยันตัวตนที่ถูกต้องของ Aspose Cloud, สมุดงานเป้าหมายต้องถูกอัปโหลดลงในพื้นที่จัดเก็บของ Aspose Cloud และคุณควรทราบชื่อพื้นที่จัดเก็บ (หากใช้พื้นที่จัดเก็บแบบกำหนดเอง)

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                               |
|------------------|-----------|----------|--------------------------------------------------------|
| name             | string    | path     | ชื่อไฟล์สมุดงาน                                        |
| sheetName        | string    | path     | ชื่อของแผ่นงานใหม่ที่จะสร้าง                           |
| position         | integer   | query    | ตำแหน่งแบบ zero-based ที่จะแทรกแผ่นงาน               |
| sheettype        | string    | query    | ประเภทของแผ่นงานใหม่ (เช่น **Chart**, **Dialog**)     |
| folder           | string    | query    | โฟลเดอร์ที่มีสมุดงานอยู่                              |
| storageName      | string    | query    | ชื่อของพื้นที่จัดเก็บ Aspose Cloud                     |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PutAddNewWorksheet) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ที่รันผ่านบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Tasks" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

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

**สถานะโค้ดการตอบกลับที่เป็นไปได้**

| สถานะโค้ด | คำอธิบาย                                             |
|-----------|------------------------------------------------------|
| 200       | เพิ่มแผ่นงานเรียบร้อยแล้ว                           |
| 400       | คำขอไม่ถูกต้อง – พารามิเตอร์ไม่ถูกต้อง               |
| 401       | ไม่ได้รับอนุญาต – โทเคนยืนยันตัวตนหายไปหรือไม่ถูกต้อง |
| 404       | ไม่พบ – สมุดงานหรือโฟลเดอร์ไม่มีอยู่จริง            |
| 500       | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เงื่อนไขที่ไม่คาดคิด      |

## ครอบครัว SDK สำหรับคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK ช่วยซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่โปรเจกต์ของคุณได้ กรุณาตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostPutAddNewWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPutAddNewWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPutAddNewWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPutAddNewWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPutAddNewWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPutAddNewWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPutAddNewWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPutAddNewWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}