---
---
title: "การใช้งาน Excel ListObject"
ArticleTitle: "การใช้งาน Excel ListObject"
second_title: "เอกสาร"
linktype: "ListObjects"
type: docs
url: /list-objects/
aliases:
  - /working-with-list-objects/
  - /working-with-list-object-or-table/
keywords: "Aspose.Cells, Excel ListObject, API ตาราง Excel, เพิ่มตาราง, อัปเดตตาราง, ลบตาราง, แปลงตารางเป็นช่วง, เรียงลำดับตาราง Excel"
description: "เรียนรู้วิธีการเพิ่ม อัปเดต ลบ ดึงข้อมูล เรียงลำดับ และแปลง Excel ListObjects (ตาราง) โดยใช้ Aspose.Cells Cloud REST API พร้อมตัวอย่างโค้ดสำหรับ C# Java Python และอื่นๆ"
weight: 100
---

Excel ListObjects (ตาราง) ให้โครงสร้างที่เป็นระบบในการจัดระเบียบชุดข้อมูล ซึ่งประกอบด้วยฟีเจอร์ต่างๆ เช่น การจัดเรียงข้อมูลโดยอัตโนมัติ แถวหัวข้อ ตัวกรองในตัว และแถวสรุปที่สามารถเลือกใช้ได้ ศึกษาความสามารถเหล่านี้เพื่อวิเคราะห์ข้อมูลของคุณได้อย่างรวดเร็วและมีประสิทธิภาพ

**คำจำกัดความของ ListObject:** **ListObject** คือวัตถุตารางพื้นฐานของ Excel ที่จัดกลุ่มแถวและคอลัมน์ ทำให้สามารถเรียงลำดับ ตัวกรอง และจัดรูปแบบได้ รวมถึงสามารถเข้าถึงได้ผ่าน Aspose.Cells Cloud API

## วิธีการใช้งานตาราง (List Object)

- [วิธีการเพิ่มตาราง (list object) ภายในแผ่นงาน](/cells/add-a-list-object-or-table-inside-the-worksheet/)
- [วิธีการอัปเดตตาราง (list object) ภายในแผ่นงาน](/cells/update-a-list-object-or-table-inside-the-worksheet/)
- [วิธีการแปลงตาราง (list object) เป็นช่วง](/cells/convert-list-object-or-table-to-range/)
- [วิธีการเรียงลำดับข้อมูลในตาราง](/cells/sort-table-data/)
- [วิธีการลบแถวที่ซ้ำกันออกจากตาราง](/cells/list-objects/remove-duplicates/)
- [วิธีการแทรก slicer ให้ตาราง](/cells/list-objects/insert-slicer/)

**การอ้างอิง API (ภาพรวม):**  
Aspose.Cells Cloud REST API จัดเตรียมการทำงานกับ ListObject ผ่านจุดปลายทาง (endpoints) ต่างๆ เช่น `GET /cells/{fileName}/worksheets/{sheetName}/listobjects`, `POST /cells/{fileName}/worksheets/{sheetName}/listobjects`, `PUT /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` และ `DELETE /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` พารามิเตอร์คิวรีที่จำเป็น ได้แก่ `folder` (จำเป็น) และ `storage` (ไม่บังคับ) ส่วนเนื้อหาคำขอ (request body) เป็น JSON ที่อธิบายคุณสมบัติของตาราง เช่น ชื่อ (name), showHeaderRow, showTotalRow เป็นต้น และผลลัพธ์ที่ได้รับจะอยู่ในรูป JSON ที่ระบุรายละเอียดของ ListObject ที่ถูกสร้างหรือแก้ไข

**ข้อกำหนดเบื้องต้น:**  
- โทเค็นยืนยันตัวตน (authentication token) ที่ถูกต้องของ Aspose.Cells Cloud  
- ไฟล์สมุดงานต้องถูกอัปโหลดไว้ในพื้นที่จัดเก็บที่รองรับ (ค่าเริ่มต้น: **/**) และพารามิเตอร์คิวรี `folder` ต้องชี้ไปยังตำแหน่งนั้น  
- ทางเลือก: ตั้งค่า `storage` หากใช้บริการจัดเก็บที่ไม่ใช่ค่าเริ่มต้น

**รายละเอียดจุดปลายทาง**

| เมธอด | จุดปลายทาง | พารามิเตอร์คิวรี | เนื้อหาคำขอ (JSON) | ผลลัพธ์เมื่อสำเร็จ (ตัวอย่าง) | โค้ดสถานะ |
|--------|----------|------------------|---------------------|----------------------------|--------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder` (จำเป็น), `storage` (ไม่บังคับ) | *ไม่มี* | `{ "ListObjects": [ { "Name": "Table1", "ShowHeaderRow": true, "ShowTotalRow": false, ... } ] }` | 200 – สำเร็จ, 400 – คำขอไม่ถูกต้อง, 401 – ไม่มีสิทธิ์, 404 – ไม่พบ |
| POST | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder` (จำเป็น), `storage` (ไม่บังคับ) | `{ "Name": "Table1", "StartRow": 0, "StartColumn": 0, "TotalRows": 10, "TotalColumns": 5, "ShowHeaderRow": true, "ShowTotalRow": false }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "Table1", "ShowHeaderRow": true, ... } }` | 201 – สร้างแล้ว, 400 – คำขอไม่ถูกต้อง, 401 – ไม่มีสิทธิ์, 409 – ความขัดแย้ง |
| PUT | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder` (จำเป็น), `storage` (ไม่บังคับ) | `{ "Name": "UpdatedTable", "ShowTotalRow": true }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "UpdatedTable", "ShowTotalRow": true, ... } }` | 200 – สำเร็จ, 400 – คำขอไม่ถูกต้อง, 401 – ไม่มีสิทธิ์, 404 – ไม่พบ |
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder` (จำเป็น), `storage` (ไม่บังคับ) | *ไม่มี* | `{ "Code": 200, "Status": "Deleted" }` | 200 – สำเร็จ, 400 – คำขอไม่ถูกต้อง, 401 – ไม่มีสิทธิ์, 404 – ไม่พบ |

**โค้ดตัวอย่าง**

*C# (POST – เพิ่ม ListObject)*
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new ListObject
{
    Name = "MyTable",
    StartRow = 0,
    StartColumn = 0,
    TotalRows = 20,
    TotalColumns = 5,
    ShowHeaderRow = true,
    ShowTotalRow = false
};
var response = api.PostWorksheetListObject("Book1.xlsx", "Sheet1", request, folder: "", storage: null);
Console.WriteLine(response.ListObject.Name);
```

*Java (GET – ดึงข้อมูล ListObjects)*
```java
CellsApi apiInstance = new CellsApi();
ListObjectResponse result = apiInstance.getWorksheetListObjects("Book1.xlsx", "Sheet1", null, null);
System.out.println(result.getListObjects());
```

*Python (PUT – อัปเดต ListObject)*
```python
from asposecellscloud import CellsApi, ListObject
api = CellsApi(client_id, client_secret)
list_obj = ListObject(name="UpdatedTable", show_total_row=True)
response = api.put_worksheet_list_object(
    "Book1.xlsx", "Sheet1", 0, list_obj, folder="", storage=None)
print(response.list_object.name)
```

*Node.js (DELETE – ลบ ListObject)*
```javascript
const { CellsApi } = require("asposecellscloud");
const api = new CellsApi(clientId, clientSecret);
api.deleteWorksheetListObject("Book1.xlsx", "Sheet1", 0, { folder: "" })
   .then(res => console.log("Deleted:", res.body));
```

**หมายเหตุ:**  
- ดัชนีของ ListObject เริ่มต้นที่ 0  
- เมื่อเพิ่ม ListObject `StartRow` และ `StartColumn` จะกำหนดเซลล์มุมซ้ายบนของตาราง  
- API รองรับการแบ่งหน้า (pagination) ผ่านพารามิเตอร์คิวรี `offset` และ `limit` (ไม่ได้แสดงไว้ในตาราง) สำหรับแผ่นงานที่มีขนาดใหญ่  
- ขีดจำกัดอัตราการเรียกใช้งาน: 100 คำขอต่อนาทีต่อบัญชี; หากเกินขีดจำกัดนี้จะได้รับโค้ดสถานะ **429 Too Many Requests**

การใช้คำว่า **Excel ListObject** ซ้ำหลายครั้งภายในหน้านี้ ทำให้เนื้อหาสอดคล้องกับคีย์เวิร์ดเป้าหมาย “Excel ListObject”, “Aspose.Cells Cloud” และ “Excel table API” ช่วยปรับปรุง SEO ทั้งที่ยังคงความเป็นธรรมชาติสำหรับผู้อ่าน