---
title: "เพิ่มวัตถุ OLE ในสมุดงาน Excel"
second_title: "เอกสาร"
linktitle: "เพิ่มวัตถุ OLE"
type: docs
url: /th/oleobjects/add/
aliases: [/add-oleobject-to-excel-worksheet/]
keywords: "เพิ่มวัตถุ OLE, Excel, Aspose.Cells Cloud, REST API, SDK"
description: "ใช้ Aspose.Cells Cloud REST API เพื่อเพิ่มวัตถุ OLE ลงในสมุดงาน Excel API สามารถเรียกใช้โดยตรงหรือผ่าน SDK สำหรับ C#, Java, PHP, Ruby, Node.js, Python, Perl และ Go"
ArticleTitle: "เพิ่มวัตถุ OLE ลงในสมุดงาน Excel ด้วย Aspose.Cells Cloud API"
weight: 20
---

Aspose.Cells Cloud API ช่วยให้คุณสามารถจัดการสมุดงาน Excel ผ่านโปรแกรม รวมถึงการฝังวัตถุ OLE (เช่น เอกสาร Word, PDF หรือไฟล์ไบนารีอื่นๆ) ลงในชีตงานโดยตรง

REST API นี้จะเพิ่ม **วัตถุ OLE** ลงในชีตงาน Excel

**ข้อกำหนดเบื้องต้น** – คุณต้องมีโทเค็น JWT สำหรับการยืนยันตัวตนที่ถูกต้อง และไฟล์ต้นทางที่อ้างอิงโดย `oleFile` หรือ `imageFile` ต้องถูกอัปโหลดไปยังตำแหน่งที่จัดเก็บที่ระบุก่อนที่จะเรียกใช้ปลายทาง (endpoint)

## API PutWorksheetOleObject

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย                                            |
| ---------------- | -------- | -------- | ----------------------------------------------------- |
| name             | string   | path     | ชื่อไฟล์สมุดงาน                                      |
| sheetName        | string   | path     | ชื่อชีตงาน                                           |
| oleObject        | object   | body     | นิยามของวัตถุ OLE                                     |
| upperLeftRow     | integer  | query    | ดัชนีแถวของมุมบนซ้าย (ค่าเริ่มต้น 0)                 |
| upperLeftColumn  | integer  | query    | ดัชนีคอลัมน์ของมุมบนซ้าย (ค่าเริ่มต้น 0)             |
| height           | integer  | query    | ความสูงของวัตถุ OLE (ค่าเริ่มต้น 0)                   |
| width            | integer  | query    | ความกว้างของวัตถุ OLE (ค่าเริ่มต้น 0)                 |
| oleFile          | string   | query    | ชื่อไฟล์ต้นทางของ OLE                                |
| imageFile        | string   | query    | ชื่อไฟล์ภาพตัวอย่าง                                  |
| folder           | string   | query    | โฟลเดอร์ที่เก็บสมุดงาน                              |
| storageName      | string   | query    | ชื่อพื้นที่จัดเก็บที่จะใช้                            |

**หมายเหตุ** – `upperLeftRow` และ `upperLeftColumn` ใช้การนับดัชนีแบบเริ่มต้นที่ 0 `oleFile` (และ `imageFile` ถ้ามี) ต้องมีอยู่แล้วในพื้นที่จัดเก็บเป้าหมาย มิฉะนั้นคำขอนี้จะส่งกลับข้อผิดพลาด

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/OleObjects/PutWorksheetOleObject) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้สาธารณะ และอนุญาตให้คุณดำเนินการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเรียกใช้บริการเว็บของ Aspose.Cells ตัวอย่างด้านล่างแสดงวิธีเพิ่มวัตถุ OLE ด้วย cURL **ต้องใช้ HTTPS สำหรับการเรียกใช้งานทุกครั้งในระบบจริง**

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/oleobjects" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"ImageSourceFullName":"aspose-logo.png", "IsAutoSize":true, "SourceFullName":"Sample_Book2.xls", "UpperLeftRow":15, "Top":10, "UpperLeftColumn":5, "Left":10, "Width":400, "Height":400}'
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

![ภาพหน้าจอแสดงวัตถุ OLE ที่ฝังอยู่ในชีตงาน Excel](/cells/images/ole-object-example.png)

**โค้ดสถานะ HTTP ที่เป็นไปได้**

| โค้ด | คำอธิบาย                                               |
|------|--------------------------------------------------------|
| 200  | เพิ่มวัตถุ OLE สำเร็จ                                  |
| 400  | คำขอไม่ถูกต้อง – ขาดหรือพารามิเตอร์ไม่ถูกต้อง         |
| 401  | ไม่ได้รับอนุญาต – โทเค็น JWT ไม่ถูกต้องหรือขาดหาย     |
| 404  | ไม่พบ – สมุดงาน ชีตงาน หรือไฟล์ต้นทางไม่มีอยู่        |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เกิดข้อผิดพลาดที่ไม่คาดคิด |

การตอบกลับที่สำเร็จโดยทั่วไปจะส่งกลับข้อมูล JSON ดังนี้:

```json
{
  "Code": 200,
  "Status": "OK",
  "Data": {
    "OleObjectId": "12345",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Width": 400,
    "Height": 400,
    "SourceFullName": "Sample_Book2.xls",
    "ImageSourceFullName": "aspose-logo.png"
  }
}
```

## ครอบครัว SDK สำหรับคลาวด์

การใช้ SDK จะช่วยเร่งการพัฒนาได้ SDK จะซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณ ดู [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}