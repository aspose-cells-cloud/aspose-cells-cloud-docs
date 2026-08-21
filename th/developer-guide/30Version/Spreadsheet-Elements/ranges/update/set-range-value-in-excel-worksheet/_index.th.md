---
title: "การตั้งค่าค่าในช่วงของแผ่นงาน Excel"
second_title: "เอกสาร"
linktitle: "ตั้งค่าค่า"
type: docs
url: /ranges/update/values/
aliases: [/set-range-value-in-excel-worksheet/]
keywords: "Aspose.Cells, API สำหรับ Excel, ตั้งค่าค่าในช่วง, REST API, SDK บนคลาวด์, การอัปเดตแผ่นงาน"
description: "เรียนรู้วิธีการตั้งค่าค่าในเซลล์หรือช่วงของสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API (v3.0) ซึ่งรวมถึง endpoint, พารามิเตอร์, ตัวอย่าง cURL, ตัวอย่างโค้ด SDK และการจัดการข้อผิดพลาด"
weight: 72
ArticleTitle: "การตั้งค่าค่าในช่วงของแผ่นงาน Excel – API ของ Aspose.Cells Cloud"
---

ใช้ REST API นี้เพื่อตั้งค่าค่าในช่วงที่ระบุ เมื่อเหมาะสม ค่าที่ป้อนจะถูกแปลงเป็นชนิดข้อมูลอื่น และรูปแบบตัวเลขของเซลล์จะถูกรีเซ็ต

**ข้อกำหนดเบื้องต้น**
- บัญชี Aspose Cloud ที่ถูกต้อง
- โทเค็น JWT ที่มีขอบเขต `Cells.ReadWrite`
- สมุดงานต้องถูกอัปโหลดไว้ยังตำแหน่งที่จัดเก็บเป้าหมายเรียบร้อยแล้ว

## API PostWorksheetCellsRangeValue

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

พารามิเตอร์ของคำขอมีดังนี้:

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
|----------------|----------|---------|------------------------------------------------------------|
| name           | string   | path    | ชื่อสมุดงาน                                              |
| sheetName      | string   | path    | ชื่อแผ่นงาน                                             |
| value          | string   | query   | ค่าที่ป้อนเข้ามา                                          |
| range          | object   | body    | วัตถุช่วง (Range object) ในแผ่นงาน                        |
| isConverted    | boolean  | query   | ระบุว่าควรแปลงค่าที่ป้อนเข้ามาหรือไม่                    |
| setStyle       | boolean  | query   | ระบุว่าควรใช้รูปแบบกับเซลล์เป้าหมายหรือไม่              |
| folder         | string   | query   | โฟลเดอร์ของสมุดงาน                                       |
| storageName    | string   | query   | ชื่อพื้นที่จัดเก็บ                                      |

**ตัวอย่างของวัตถุ `range`** ที่สามารถส่งในเนื้อหาคำขอ:

```json
{
  "range": {
    "FirstRow": 0,
    "FirstColumn": 0,
    "RowCount": 1,
    "ColumnCount": 1
  }
}
```

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeValue) นิยามอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ผ่าน cURL **ต้องแนบโทเค็น JWT ที่ถูกต้องในส่วนหัว `Authorization`**

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?value=25&isConverted=false&setStyle=false" \
  -X POST \
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

**โครงสร้างการตอบกลับ**

| ฟิลด์   | ชนิดข้อมูล | คำอธิบาย |
|---------|-----------|----------------------------------------------------------|
| Code    | integer   | รหัสสถานะ HTTP ของการดำเนินการ                           |
| Status  | string    | คำอธิบายสั้นของผลลัพธ์ (เช่น "OK")                      |
| Message | string    | ข้อความแสดงข้อผิดพลาดโดยละเอียดเมื่อคำขอล้มเหลว (ไม่บังคับ) |
| Result  | object    | ข้อมูลเพิ่มเติมที่ส่งคืนสำหรับการเรียกที่สำเร็จ (ไม่บังคับ) |

**รหัสสถานะ HTTP ที่เป็นไปได้**

- **200 OK** – ตั้งค่าค่าในช่วงสำเร็จแล้ว  
- **400 Bad Request** – พารามิเตอร์ไม่ถูกต้องหรือเนื้อหาคำขอผิดรูปแบบ  
- **401 Unauthorized** – โทเค็น JWT ขาดหายหรือไม่ถูกต้อง  
- **403 Forbidden** – ไม่มีสิทธิ์เพียงพอสำหรับการดำเนินการที่ร้องขอ  
- **404 Not Found** – สมุดงาน แผ่นงาน หรือช่วงที่ระบุไม่มีอยู่  
- **500 Internal Server Error** – ข้อผิดพลาดที่ไม่คาดคิดจากเซิร์ฟเวอร์

*ตัวอย่างการตอบกลับข้อผิดพลาดเมื่อเกิดข้อผิดพลาด 400 Bad Request:*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "วัตถุ 'range' ขาดฟิลด์ที่จำเป็น"
}
```

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานของโครงการได้ โปรดดูที่ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}
{{< /tab >}}

{{< /tabs >}}