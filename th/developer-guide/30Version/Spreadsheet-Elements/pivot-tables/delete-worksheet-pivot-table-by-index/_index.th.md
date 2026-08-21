---
title: "การลบพิวต์ตารางในแผ่นงาน Excel"
second_title: "Document"
linktitle: Delete
type: docs
url: /th/pivot-tables/delete/
aliases: [/th/delete-worksheet-pivot-table-by-index/]
keywords: "Aspose.Cells, พิวต์ตาราง, ลบ, Excel, REST API"
description: "การลบพิวต์ตารางจากแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API (v3.0) รวมถึงรูปแบบคำขอตัวอย่าง cURL รหัสข้อผิดพลาด และตัวอย่าง SDK สำหรับ C#, Java, Python และ Node.js"
weight: 70
ArticleTitle: "วิธีลบพิวต์ตารางในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud"
---

REST API นี้จะลบพิวต์ตารางออกจากแผ่นงานตามดัชนีของมัน

**ข้อกำหนดเบื้องต้น** – คุณต้องมีโทเค็น JWT ที่ถูกต้องสำหรับการเข้าถึง Aspose.Cells Cloud และไฟล์ Excel เป้าหมายต้องถูกจัดเก็บไว้ในตำแหน่งที่จัดเก็บข้อมูลที่รองรับ ตรวจสอบให้แน่ใจว่าชื่อไฟล์ ชื่อแผ่นงาน และรายละเอียดการจัดเก็บข้อมูลได้รับการระบุอย่างถูกต้องก่อนที่จะเรียกใช้ API

พิวต์ตารางเป็นวิธีที่มีประสิทธิภาพในการสรุปข้อมูลใน **แผ่นงาน Excel** โดยใช้ Aspose.Cells Cloud คุณสามารถลบพิวต์ตารางที่ไม่ต้องการออกโดยใช้คำขอ HTTP DELETE เพียงคำขอเดียว ซึ่งเหมาะอย่างยิ่งเมื่อคุณต้องการทำความสะอาดแผ่นงาน ทำให้กระบวนการสร้างรายงานเป็นอัตโนมัติ หรือผสานการจัดการ Excel เข้ากับแอปพลิเคชันของคุณ

## API DeleteWorksheetPivotTable

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย                                                |
| ---------------- | -------- | -------- | --------------------------------------------------------- |
| name             | string   | path     | ชื่อของเอกสาร Excel                                       |
| sheetName        | string   | path     | ชื่อของแผ่นงานที่มีพิวต์ตาราง                            |
| pivotTableIndex  | integer  | path     | ดัชนีแบบเริ่มต้นที่ 0 ของพิวต์ตารางที่ต้องการลบ          |
| folder           | string   | query    | ตำแหน่งของโฟลเดอร์ที่เก็บเอกสารไว้                      |
| storageName      | string   | query    | ชื่อของบริการจัดเก็บข้อมูล                               |

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTable) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบเปิดเผย และช่วยให้คุณสามารถดำเนินการโต้ตอบ REST ผ่านเว็บเบราว์เซอร์ได้โดยตรง

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API ผ่าน cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**ตัวอย่างการตอบกลับ**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

การตอบกลับมีโครงสร้าง JSON ง่ายๆ ดังนี้:

```json
{
  "Code": integer,   // รหัสสถานะแบบ HTTP ของ operation
  "Status": string   // คำอธิบายแบบข้อความ เช่น "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### การจัดการข้อผิดพลาด

รหัสสถานะการตอบกลับที่พบบ่อยมีดังนี้:

| สถานะ HTTP | คำอธิบาย                                                           |
| ----------- | ------------------------------------------------------------------- |
| 400         | คำขอไม่ถูกต้อง – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง                 |
| 401         | ไม่ได้รับอนุญาต – โทเค็น JWT ไม่ถูกต้องหรือไม่มีอยู่               |
| 404         | ไม่พบ – ไฟล์ แผ่นงาน หรือพิวต์ตารางไม่มีอยู่                      |
| 500         | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เกิดสถานการณ์ที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

## ครอบครัว SDK สำหรับ Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งกระบวนการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ และช่วยให้คุณสามารถมุ่งเน้นไปที่งานของโครงการของคุณ โปรดดูที่ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-DeleteWorksheetPivotTableIndex-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-DeleteWorksheetPivotTableIndex-delete-worksheet-pivot-table-index.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteWorksheetPivotTablesByIndex.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-DeleteWorksheetPivotTableIndex-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-DeleteWorksheetPivotTableIndex-delete-worksheet-pivot-table-index.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-DeleteWorksheetPivotTableIndex-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "8798eca5f30bf41a4675b83583a72ec3" >}}

{{< /tab >}}

{{< /tabs >}}