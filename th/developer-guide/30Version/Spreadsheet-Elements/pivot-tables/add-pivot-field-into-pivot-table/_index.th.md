---
title: "เพิ่มฟิลด์พิวต์ลงในตารางพิวต์"
second_title: "เอกสาร"
linktitle: "เพิ่มฟิลด์พิวต์"
type: docs
url: /th/pivot-tables/add-pivot-field/
aliases: [  /th/add-a-pivot-table-in-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, pivot table, add pivot field, REST API, SDK"
description: "เพิ่มฟิลด์พิวต์ลงในตารางพิวต์ที่มีอยู่โดยใช้ Aspose.Cells Cloud REST API ประกอบด้วยรายละเอียดคำขอ ตัวอย่าง cURL และโค้ดตัวอย่าง SDK"
weight: 40
ArticleTitle: "เพิ่มฟิลด์พิวต์ลงในตารางพิวต์ – เอกสารประกอบ Aspose.Cells Cloud"
---

REST API นี้ **เพิ่ม** ฟิลด์พิวต์ลงในตารางพิวต์ที่มีอยู่

> **ข้อกำหนดเบื้องต้น:** ก่อนเรียกใช้จุด endpoints นี้ คุณต้องระบุโทเค็น JWT สำหรับการรับรองความถูกต้องที่ถูกต้องใน header `Authorization` และตรวจสอบให้แน่ใจว่าสมุดงานถูกจัดเก็บไว้ในโฟลเดอร์ที่ระบุหรือในพื้นที่จัดเก็บเริ่มต้น

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField
```

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                 |
| ---------------- | --------- | -------- | ------------------------------------------------------------------------ |
| name             | string    | path     | ชื่อเอกสาร                                                               |
| sheetName        | string    | path     | ชื่อแผ่นงาน                                                             |
| pivotTableIndex  | integer   | path     | ดัชนีของตารางพิวต์                                                      |
| pivotFieldType   | string    | query    | ประเภทของพื้นที่ฟิลด์ (เช่น Row, Column)                                |
| request          | object    | body     | DTO ที่มีดัชนีฟิลด์ที่ต้องการเพิ่ม                                      |
| needReCalculate  | boolean   | query    | ตั้งค่าเป็น **true** เพื่อคำนวณตารางพิวต์ใหม่หลังจากดำเนินการเสร็จสิ้น   |
| folder           | string    | query    | โฟลเดอร์ที่เอกสารถูกจัดเก็บ                                             |
| storageName      | string    | query    | ชื่อของพื้นที่จัดเก็บ                                                   |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PivotTables/PutPivotTableField) นิยามอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้แบบเปิดเผย และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเรียกใช้บริการเว็บของ Aspose.Cells ตัวอย่างต่อไปนี้แสดงวิธีการเพิ่มฟิลด์พิวต์โดยใช้ cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/PivotField?pivotFieldType=Row" \
  -X PUT \
  -d '{"Data":[1,2]}' \
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

เมื่อการดำเนินการสำเร็จ การตอบกลับจะส่งคืนออบเจกต์ JSON ที่มีฟิลด์ `Code` และ `Status` โครงสร้างตัวอย่างมีดังนี้:

```json
{
  "Code": 0,        // จำนวนเต็มที่ระบุรหัสสถานะ HTTP
  "Status": "OK"    // ข้อความแบบสตริง
}
```

การตอบกลับข้อผิดพลาดที่เป็นไปได้ ได้แก่ **400 Bad Request** (คำขอล้มเหลวเนื่องจากพารามิเตอร์ไม่ครบถ้วน), **401 Unauthorized** (โทเค็นไม่ถูกต้อง) และ **500 Internal Server Error** (ข้อผิดพลาดที่เกิดขึ้นภายในเซิร์ฟเวอร์)

## Cloud SDK Family

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการผสานรวมฟังก์ชันนี้ SDK จะจัดการรายละเอียดระดับต่ำ ช่วยให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณ ดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมดได้ที่ [GitHub repository](https://github.com/aspose-cells-cloud)

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="Ruby" tabName4="Python" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivotFieldInPivottable-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotFieldInPivotTable.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivotFieldInPivottable-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivotFieldInPivottable-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "8f9b66d50f7cfa2b14c24fa7ddb396e7" >}}

{{< /tab >}}

{{< /tabs >}}

**ดูเพิ่มเติม:**  
- [เพิ่มตารางพิวต์](https://docs.aspose.cloud/cells/pivot-tables/add-pivot-table/)  
- [ลบฟิลด์พิวต์](https://docs.aspose.cloud/cells/pivot-tables/delete-pivot-field/)