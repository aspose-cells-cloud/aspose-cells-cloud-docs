---
title: "รับช่วงที่ตั้งชื่อไว้ในสมุดงาน Excel"
second_title: "เอกสาร"
linktype: "ชื่อ"
type: docs
url: /ranges/get/name/
aliases: [/get-named-ranges-inside-the-workbook/]
keywords: "ช่วงที่ตั้งชื่อไว้, Excel, Aspose.Cells, API คลาวด์, แผ่นงาน"
description: "ดึงข้อมูลช่วงที่ตั้งชื่อไว้จากสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API ซึ่งประกอบด้วยรายละเอียดคำขอ, ตัวอย่างคำสั่ง cURL และตัวอย่าง SDK สำหรับภาษาโปรแกรมต่างๆ หลายภาษา"
ArticleTitle: "รับช่วงที่ตั้งชื่อไว้ในสมุดงาน Excel – Aspose.Cells Cloud API"
weight: 10
---

API REST นี้ส่งคืนข้อมูลเกี่ยวกับช่วงที่ตั้งชื่อไว้ที่กำหนดไว้ภายในแผ่นงาน

**พื้นหลัง** – *ช่วงที่ตั้งชื่อไว้* (named range) คือตัวระบุที่ผู้ใช้กำหนดขึ้นเอง ซึ่งอ้างอิงไปยังเซลล์หรือชุดของเซลล์ที่ระบุในแผ่นงาน การตั้งชื่อช่วงช่วยให้การสร้างสูตรง่ายขึ้น ทำให้อ่านเข้าใจได้ชัดเจนขึ้น และสามารถเข้าถึงพื้นที่ที่ใช้งานบ่อยในสมุดงานผ่านการเขียนโปรแกรมได้

**ข้อกำหนดเบื้องต้น** – การเข้าถึง Aspose.Cells Cloud API จำเป็นต้องมีโทเคน JWT ที่ถูกต้อง คุณสามารถรับโทเคนดังกล่าวโดยการยืนยันตัวตนด้วย client ID และ client secret ของ Aspose Cloud ผ่านจุดสิ้นสุด OAuth 2.0 เพื่อขอโทเคน แล้วแนบโทเคนนั้นไว้ในส่วนหัวคำขอทุกคำขอภายใต้รูปแบบ `Authorization: Bearer <jwt token>`

## API GetNamedRanges

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/ranges
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยสูงและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
| -------------- | ------ | ------------ | -------------------------------------------- |
| name           | string | Path         | ชื่อของเอกสาร Excel |
| folder         | string | Query string | โฟลเดอร์ที่เก็บเอกสารไว้ |
| storageName    | string | Query string | ชื่อของพื้นที่จัดเก็บที่เอกสารนั้นอยู่ |

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | คำอธิบาย |
|------|-----------------------------|--------------------------------------------------|
| 200  | คำขอสำเร็จ (OK)             | แอ็คชันกรองดำเนินการสำเร็จ; ข้อมูลการตอบกลับประกอบด้วยรายละเอียดของคำขอ |
| 400  | คำขอผิดรูปแบบ (Bad Request) | พารามิเตอร์ไม่ครบหรือผิด (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ผิดหรือไม่มี |
| 413  | ข้อมูลส่งไปขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดภายในเซิร์ฟเวอร์ |

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetNamedRanges) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เปิดให้เข้าถึงได้จากสาธารณะ ซึ่งช่วยให้คุณสามารถโต้ตอบกับ REST API ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ซึ่งรันผ่านคำสั่งในคอมมานด์ไลน์เพื่อเรียกใช้บริการเว็บของ Aspose.Cells ตัวอย่างด้านล่างแสดงวิธีการดึงข้อมูลช่วงที่ตั้งชื่อไว้โดยใช้ cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/ranges" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Ranges": {
    "RangeList": [
      {
        "ColumnCount": 7,
        "ColumnWidth": 8.428571428571429,
        "FirstColumn": 1,
        "FirstRow": 9,
        "Name": "data",
        "RefersTo": "=Sheet1!$B$10:$H$10",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**โครงสร้างข้อมูลของการตอบกลับ**

| ฟิลด์          | ชนิดข้อมูล | คำอธิบาย |
|----------------|---------|------------------------------------------------------|
| `ColumnCount`  | integer | จำนวนคอลัมน์ในช่วงข้อมูล |
| `ColumnWidth`  | number  | ความกว้างของแต่ละคอลัมน์ (หน่วยเป็นจุด) |
| `FirstColumn`  | integer | ดัชนีของคอลัมน์แรกในช่วงข้อมูล (เริ่มนับจาก 0) |
| `FirstRow`     | integer | ดัชนีของแถวแรกในช่วงข้อมูล (เริ่มนับจาก 0) |
| `Name`         | string  | ชื่อที่ผู้ใช้กำหนดให้กับช่วงข้อมูล |
| `RefersTo`     | string  | สูตรที่กำหนดที่อยู่อ้างอิงของเซลล์ (เช่น `=Sheet1!$B$10:$H$10`) |
| `RowCount`     | integer | จำนวนแถวในช่วงข้อมูล |
| `RowHeight`    | number  | ความสูงของแต่ละแถว (หน่วยเป็นจุด) |
| `Worksheet`    | string  | ชื่อของแผ่นงานที่มีช่วงข้อมูลนี้อยู่ |

## ครอบครัว SDK สำหรับคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการผสานรวมฟังก์ชันนี้เข้ากับแอปพลิเคชันของคุณ SDK จะจัดการรายละเอียดระดับต่ำให้คุณโดยอัตโนมัติ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณเองได้ ตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ผ่าน SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetNamedRanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetNamedRanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetNamedRanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetNamedRanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetNamedRanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetNamedRanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetNamedRanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetNamedRanges.go" >}}

{{< /tab >}}

{{< /tabs >}}