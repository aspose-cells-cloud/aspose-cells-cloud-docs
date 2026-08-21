---
title: "อัปเดตวัตถุรายการในสมุดงาน Excel"
ArticleTitle: "อัปเดตวัตถุรายการในสมุดงาน Excel – เอกสารประกอบ API ของ Aspose.Cells Cloud"
second_title: "เอกสาร"
linktype: "อัปเดต"
type: docs
url: /th/list-objects/update/
aliases:
  - /update-a-list-object-or-table-inside-the-worksheet/
  - /tables/update/
keywords: "Aspose.Cells, ListObject, อัปเดตตาราง, Excel API, REST, SDK บนคลาวด์, การอัปเดตวัตถุรายการ, สมุดงาน Excel, ตาราง"
description: "เรียนรู้วิธีอัปเดตตารางใน Excel โดยใช้ Aspose.Cells Cloud API (เวอร์ชัน 3.0) ซึ่งประกอบด้วย endpoint, พารามิเตอร์, ตัวอย่าง cURL, รหัสข้อผิดพลาด และตัวอย่าง SDK"
weight: 20
---

REST API นี้ใช้อัปเดตคุณสมบัติของ **วัตถุรายการ** (ตาราง) ในสมุดงาน Excel

## ความปลอดภัยและการยืนยันตัวตน

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ [การยืนยันตัวตนแบบ JWT token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## โครงสร้าง Request Body

DTO `listObject` มีฟิลด์ต่อไปนี้ คุณจำเป็นต้องส่งเฉพาะฟิลด์ที่ต้องการเปลี่ยนแปลงใน request body เท่านั้น

| ฟิลด์                                           | ชนิดข้อมูล        | จำเป็น | คำอธิบาย                                                                  |
| ----------------------------------------------- | ----------------- | ------ | -------------------------------------------------------------------------- |
| **DisplayName**                                 | string            | ไม่จำเป็น | ชื่อที่แสดงสำหรับตาราง                                                     |
| **StartRow** / **StartColumn**                  | integer           | ไม่จำเป็น | ดัชนีเริ่มต้น (เริ่มจาก 0) ของแถว/คอลัมน์แรกของตาราง                            |
| **EndRow** / **EndColumn**                      | integer           | ไม่จำเป็น | ดัชนีสิ้นสุด (เริ่มจาก 0) ของแถว/คอลัมน์สุดท้ายของตาราง                          |
| **Range**                                       | string            | ไม่จำเป็น | ที่อยู่รูปแบบ A1 ที่ระบุช่วงของตาราง (เช่น `A1:D10`)                           |
| **ShowHeaderRow**                               | boolean           | ไม่จำเป็น | ตั้งค่า `true` เพื่อแสดงแถวส่วนหัว                                               |
| **ShowTotals**                                  | boolean           | ไม่จำเป็น | ตั้งค่า `true` เพื่อแสดงแถวผลรวม                                               |
| **TableStyleName**                              | string            | ไม่จำเป็น | ชื่อของรูปแบบตารางในตัวที่ต้องการใช้                                           |
| **TableStyleType**                              | string            | ไม่จำเป็น | ประเภทของรูปแบบ (`TableStyleLight`, `TableStyleMedium` เป็นต้น)                 |
| **ListColumns**                                 | array of objects  | ไม่จำเป็น | คอลเลกชันนิยามคอลัมน์ (`Name`, `TotalsCalculation`)                           |
| **Sorter**, **AutoFilter**, **ShowTableStyle…** | object            | ไม่จำเป็น | ตัวเลือกขั้นสูงสำหรับการจัดรูปแบบและการกรอง (ดู DTO ฉบับเต็มได้จาก OpenAPI spec) |

### ตัวอย่าง Payload แบบเรียบง่าย

```json
{
  "DisplayName": "SalesData",
  "Range": "A1:E20",
  "ShowHeaderRow": true,
  "ShowTotals": false
}
```

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}
```

### **พารามิเตอร์ของ Request**

| ชื่อพารามิเตอร์    | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                            |
| ------------------- | ---------- | -------- | ----------------------------------- |
| **name**            | string     | path     | ชื่อเอกสาร                           |
| **sheetName**       | string     | path     | ชื่อของworksheet                    |
| **listObjectIndex** | integer    | path     | ดัชนีของวัตถุรายการที่ต้องการอัปเดต       |
| **listObject**      | object     | body     | DTO `ListObject` ใน request body     |
| **folder**          | string     | query    | โฟลเดอร์ที่เก็บเอกสารไว้              |
| **storageName**     | string     | query    | ชื่อของ storage                      |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObject) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

### Request

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet7/listobjects/0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
    "DisplayName": "SalesData",
    "Range": "A1:E20",
    "ShowHeaderRow": true,
    "ShowTotals": false,
    "ListColumns": [
      { "Name": "Product", "TotalsCalculation": "None" },
      { "Name": "Quantity", "TotalsCalculation": "Sum" },
      { "Name": "Price", "TotalsCalculation": "Average" }
    ]
  }'
```

{{< /tab >}}

### Response

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Response ที่สำเร็จจะประกอบด้วยฟิลด์ต่อไปนี้:

| ฟิลด์   | ชนิดข้อมูล | คำอธิบาย                               |
| ------- | ---------- | ---------------------------------------- |
| Code    | integer    | รหัสสถานะ HTTP (200 หมายถึงความสำเร็จ)    |
| Status  | string     | คำอธิบายสถานะในรูปแบบข้อความ               |
| UpdatedObject *(ไม่บังคับ)* | object | การแสดงผล `ListObject` ที่อัปเดตแล้ว ซึ่งประกอบด้วยคุณสมบัติที่ถูกแก้ไข |

{{< /tab >}}

{{< /tabs >}}

## Response ข้อผิดพลาด

| รหัส HTTP | คำอธิบาย                                                                      | ตัวอย่าง Payload                                         |
| --------- | ------------------------------------------------------------------------------ | ------------------------------------------------------ |
| **400**   | Request ผิดรูปแบบ – ขาดฟิลด์ที่จำเป็นหรือ JSON มีรูปแบบไม่ถูกต้อง               | `{ "Code": 400, "Message": "Invalid request body." }`  |
| **401**   | ไม่ได้รับอนุญาต – JWT token ขาดหายไปหรือไม่ถูกต้อง                             | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**   | ไม่พบ – สมุดงาน worksheet หรือวัตถุรายการที่ระบุไม่มีอยู่จริง                    | `{ "Code": 404, "Message": "Resource not found." }`    |
| **500**   | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เกิดสถานะผิดปกติภายในเซิร์ฟเวอร์                 | `{ "Code": 500, "Message": "Server error." }`          |

## คำถามที่พบบ่อย (FAQ)

<details>  
<summary>ฉันจะอัปเดตวัตถุรายการโดยใช้ Aspose.Cells Cloud API ได้อย่างไร?</summary>

ใช้ endpoint `POST /cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}` โดยใส่ JSON body ที่ประกอบด้วยคุณสมบัติที่คุณต้องการเปลี่ยนแปลง (เช่น `DisplayName`, `ShowHeaderRow`) และยืนยันตัวตนด้วย JWT token ใน header `Authorization`

</details>

<details>  
<summary>หลังจากอัปเดตสำเร็จ ฉันจะได้รับ Response แบบไหน?</summary>

จะได้รับ JSON object ที่มี `Code: 200` และ `Status: "OK"` หากเกิดข้อผิดพลาด Response จะประกอบด้วยรหัสสถานะ HTTP ที่เหมาะสมและ object `Error` ที่อธิบายปัญหา

</details>

<details>  
<summary>ฉันสามารถอัปเดตเฉพาะคุณสมบัติบางส่วนของวัตถุรายการได้หรือไม่?</summary>

ได้ค่ะ คุณสามารถส่งเฉพาะฟิลด์ที่ต้องการแก้ไขใน request body ฟิลด์อื่นๆ ที่ไม่ได้ระบุจะไม่มีการเปลี่ยนแปลง

</details>

## เอกสารที่เกี่ยวข้อง

- [เพิ่มวัตถุรายการ](https://docs.aspose.cloud/cells/list-objects/add/)
- [รับข้อมูลวัตถุรายการ](https://docs.aspose.cloud/cells/list-objects/get/)
- [ลบวัตถุรายการ](https://docs.aspose.cloud/cells/list-objects/delete/)

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งกระบวนการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณ โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}