---
title: "แสดงคอลัมน์ที่ถูกซ่อนอยู่ในสมุดงาน Excel"
ArticleTitle: "แสดงคอลัมน์ที่ถูกซ่อนอยู่ในสมุดงาน Excel - Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktitle: "แสดงคอลัมน์"
type: docs
url: /th/columns/unhide/
aliases:
  [/unhide-columns-in-an-excel-worksheet/, /unhide-columns-in-excel-worksheet/]
keywords: "Aspose.Cells, Cloud API, แสดงคอลัมน์, Excel, REST, SDK"
description: "เรียนรู้วิธีใช้ Aspose.Cells Cloud REST API เพื่อแสดงคอลัมน์ที่ถูกซ่อนอยู่ในสมุดงาน Excel รวมถึงรายละเอียดคำขอตัวอย่างคำสั่ง cURL และโค้ดตัวอย่าง SDK สำหรับภาษาการเขียนโปรแกรมหลายภาษา"
weight: 50
---

REST API นี้ใช้ในการแสดงคอลัมน์ของชีตงาน (worksheet) ที่ถูกซ่อนอยู่

**ข้อกำหนดเบื้องต้น** – ปลายทาง (endpoints) ทั้งหมดของ Aspose.Cells Cloud จำเป็นต้องใช้ HTTPS และโทเคนการเข้าถึง OAuth 2.0 ที่ถูกต้อง โปรดตรวจสอบให้แน่ใจว่าคุณได้รับโทเคนการเข้าถึงแล้ว และแนบโทเคนดังกล่าวลงในส่วนหัว `Authorization` ของคำขอของคุณ

## API PostUnhideWorksheetColumns

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/unhide
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและบังคับใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท    | ตำแหน่ง | คำอธิบาย                                      |
| ---------------- | -------- | -------- | --------------------------------------------- |
| name             | string   | path     | ชื่อของสมุดงาน                               |
| sheetName        | string   | path     | ชื่อของชีตงาน                                |
| startColumn      | integer  | query    | ดัชนีของคอลัมน์แรกที่ต้องการประมวลผล       |
| totalColumns     | integer  | query    | จำนวนคอลัมน์ที่ต้องการประมวลผล              |
| width            | number   | query    | ความกว้างที่ต้องการของคอลัมน์ (ค่าเริ่มต้น = 50.0) |
| folder           | string   | query    | โฟลเดอร์ที่เก็บเอกสารไว้                     |
| storageName      | string   | query    | ชื่อของบริการจัดเก็บข้อมูล (storage service)  |

<a href="https://apireference.aspose.cloud/cells/#/Cells/PostUnhideWorksheetColumns" target="_blank" rel="noopener noreferrer">สเปค OpenAPI</a> กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ **cURL** ผ่านคำสั่งในบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/unhide?startColumn=1&totalColumns=1&width=15" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**รหัสสถานะ HTTP ที่พบได้ทั่วไป**

| รหัส | คำอธิบาย                                           |
|------|---------------------------------------------------|
| 200  | สำเร็จ (OK) – คอลัมน์ถูกแสดงผลเรียบร้อยแล้ว      |
| 400  | คำขอไม่ถูกต้อง (Bad Request) – พารามิเตอร์ไม่ถูกต้อง |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) – ขาดหายหรือโทเคนไม่ถูกต้อง |
| 404  | ไม่พบ (Not Found) – ไม่พบสมุดงานหรือชีตงาน       |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) – เกิดความล้มเหลวที่ไม่คาดคิด |

## ครอบครัว SDK สำหรับคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ จึงช่วยให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">ที่เก็บ GitHub</a> เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}