---
title: "แสดงซ่อนแผ่นงาน Excel"
second_title: "เอกสาร"
linktype: "แสดงซ่อน"
type: docs
url: /th/worksheets/unhide/
aliases: [  /th/unhide-excel-worksheets/ ]
keywords: "Aspose.Cells, แสดงซ่อนแผ่นงาน, Excel API, สเปรดชีตบนคลาวด์, REST, ความมองเห็นของแผ่นงาน, สมุดงาน Excel"
description: "เรียนรู้วิธีใช้ Aspose.Cells Cloud REST API เพื่อแสดงซ่อนแผ่นงานในสมุดงาน Excel รวมถึงรายละเอียดคำขอตัวอย่าง cURL และโค้ดตัวอย่าง SDK สำหรับภาษาการเขียนโปรแกรมหลายภาษา"
weight: 60
---

API REST นี้จัดเตรียมจุดปลายทาง (endpoint) เพื่อ **แสดงซ่อนแผ่นงาน** ในสมุดงาน Excel

**ข้อกำหนดเบื้องต้น**  
ก่อนที่จะเรียกใช้การดำเนินการนี้ คุณต้องมี:

* โทเคนการเข้าถึง Aspose Cloud (JWT) ที่ถูกต้อง ซึ่งใส่ไว้ในส่วนหัว `Authorization`  
* สมุดงานที่จัดเก็บไว้ในตำแหน่งที่จัดเก็บข้อมูลที่รองรับ ซึ่งคุณระบุด้วยพารามิเตอร์คิวรี `folder` และ `storageName`  
* สมุดงานต้องอยู่ในรูปแบบที่ Aspose.Cells รองรับ (เช่น `.xls`, `.xlsx`, `.xlsm`)  

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/visible
```

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                   |
| ---------------- | --------- | -------- | ------------------------------------------ |
| name             | string    | path     | ชื่อเอกสาร                                 |
| sheetName        | string    | path     | ชื่อแผ่นงาน                                |
| isVisible        | boolean   | query    | ค่าความมองเห็นใหม่ของแผ่นงาน (`true`)      |
| folder           | string    | query    | โฟลเดอร์ของเอกสาร                          |
| storageName      | string    | query    | ชื่อที่จัดเก็บข้อมูล (storage)             |

[สเปค OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PutChangeVisibilityWorksheet) นิยามอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้จากสาธารณะ ซึ่งช่วยให้คุณสามารถโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเรียกใช้บริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการส่งคำขอโดยใช้ cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/visible?isVisible=true" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"   # แทนที่ <jwt token> ด้วยโทเคนการเข้าถึงของคุณ
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**รหัสการตอบกลับที่เป็นไปได้**

| โค้ด HTTP | ความหมาย                                     | ร่างการตอบกลับ (กรณีมี)                                   |
|-----------|----------------------------------------------|-----------------------------------------------------------|
| 200       | อัปเดตความมองเห็นของแผ่นงานเสร็จสมบูรณ์    | `{ "Code": 200, "Status": "OK" }`                         |
| 400       | คำขอไม่ถูกต้อง — พารามิเตอร์ขาดหายหรือไม่ถูกต้อง | `{ "Code": 400, "Message": "Invalid request parameters." }` |
| 401       | ไม่ได้รับอนุญาต — โทเคน JWT ขาดหายหรือไม่ถูกต้อง | `{ "Code": 401, "Message": "Authentication failed." }`     |
| 404       | ไม่พบ — สมุดงานหรือแผ่นงานไม่มีอยู่จริง     | `{ "Code": 404, "Message": "File or worksheet not found." }` |
| 500       | ข้อผิดพลาดภายในเซิร์ฟเวอร์                   | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา โดย SDK จะจัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นไปที่โครงการของคุณได้ ดู [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Perl" tabName8="Android" tabName9="Objective C" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Worksheet-UnhideWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutChangeVisibilityWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-change_worksheet_visibility-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UnhideExcelWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UnhideWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UnhideWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e30ac521e9cdb174baa702a743be16ae" >}}

{{< /tab >}}

{{< /tabs >}}