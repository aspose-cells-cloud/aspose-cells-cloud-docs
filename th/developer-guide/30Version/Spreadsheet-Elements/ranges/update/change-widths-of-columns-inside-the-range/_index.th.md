---
title: "เปลี่ยนความกว้างคอลัมน์ภายในช่วงข้อมูล"
ArticleTitle: "เปลี่ยนความกว้างคอลัมน์ภายในช่วงข้อมูล – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktitle: "ความกว้างคอลัมน์"
type: docs
url: /th/ranges/update/column-width/
aliases: [  /th/change-widths-of-columns-inside-the-range/ ]
keywords: "Aspose.Cells, ความกว้างคอลัมน์, REST API, Excel, SDK, ช่วงข้อมูล, คลาวด์"
description: "เรียนรู้วิธีการเปลี่ยนความกว้างคอลัมน์ภายในช่วงข้อมูลโดยใช้ Aspose.Cells Cloud REST API หรือ SDK (C#, Java, Python เป็นต้น) รวมถึงรายละเอียด cURL, โครงสร้างคำขอ/การตอบกลับ และขั้นตอนการตรวจสอบสิทธิ์"
weight: 74
---

REST API นี้ตั้งค่าความกว้างคอลัมน์ของช่วงข้อมูล

## ความปลอดภัยและการตรวจสอบสิทธิ์
API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้การตรวจสอบสิทธิ์แบบ JWT token ([รายละเอียดเพิ่มเติม](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/))

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth
```

**ข้อกำหนดเบื้องต้น** – ก่อนเรียกใช้ endpoint คุณต้อง:

1. สร้างบัญชี Aspose Cloud และรับ *client ID* และ *client secret*  
2. ขอ JWT token โดยเรียกใช้ OAuth endpoint (`/connect/token`) ซึ่ง token จะถูกส่งกลับมาในฟิลด์ `access_token`  
3. อัปโหลดไฟล์สมุดค่าที่ต้องการใช้งานไปยังพื้นที่จัดเก็บของ Aspose Cloud (หรือตรวจสอบว่าไฟล์นั้นมีอยู่แล้วในโฟลเดอร์ที่ระบุ)  

พารามิเตอร์ของคำขอ มีดังนี้:

| พารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
|-------------|-----------|----------|----------|
| name        | string    | path     | ชื่อไฟล์สมุดค่า |
| sheetName   | string    | path     | ชื่อแผ่นงาน |
| value       | number    | query    | ค่าความกว้างคอลัมน์ที่ต้องการ |
| range       | object    | body     | อ็อบเจกต์ช่วงข้อมูลที่ระบุเซลล์เป้าหมาย |
| folder      | string    | query    | พาธโฟลเดอร์ที่เก็บสมุดค่าไว้ |
| storageName | string    | query    | ชื่อบริการพื้นที่จัดเก็บข้อมูล |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeColumnWidth) นิยามอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถโต้ตอบกับ REST API ผ่านเว็บเบราว์เซอร์ได้โดยตรง

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

<h3 id="request">คำขอ</h3>

```bash
# เรียกใช้ endpoint สำหรับตั้งค่าความกว้างคอลัมน์ของสมุดค่า *test.xlsx*,
# แผ่นงาน *Sheet1*, โดยตั้งค่าความกว้างคอลัมน์ที่เลือกไว้ที่ 20 จุด
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/columnWidth?value=20" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "ColumnCount": 7,
        "ColumnWidth": 19,
        "FirstColumn": 0,
        "FirstRow": 9,
        "Name": "string",
        "RefersTo": "string",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

<h3 id="response">การตอบกลับ</h3>

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*การตอบกลับข้อผิดพลาดที่เป็นไปได้*

| HTTP Code | คำอธิบาย |
|-----------|----------|
| 400       | Bad Request – JSON หรือพารามิเตอร์ไม่ถูกต้อง |
| 401       | Unauthorized – ไม่มี token หรือ token ไม่ถูกต้อง |
| 404       | Not Found – ไม่พบสมุดค่าหรือแผ่นงาน |

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว Cloud SDK

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งกระบวนการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeColumnWidth.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeColumnWidth.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeColumnWidth.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeColumnWidth.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeColumnWidth.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeColumnWidth.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeColumnWidth.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeColumnWidth.go" >}}

{{< /tab >}}

{{< /tabs >}}

## FAQ

**Q:** *ฉันควรเรียก endpoint ใดเพื่อตั้งค่าความกว้างคอลัมน์ของช่วงข้อมูลในไฟล์สมุดค่า Excel?*  
**A:** `POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth` โดยที่ `{name}` คือชื่อไฟล์สมุดค่า และ `{sheetName}` คือแผ่นงานเป้าหมาย

**Q:** *ฉันจะตรวจสอบสิทธิ์คำขอเมื่อใช้ API ตั้งค่าความกว้างคอลัมน์ได้อย่างไร?*  
**A:** ใส่ header `Authorization: Bearer <jwt token>` โดยรับ JWT token ผ่านกระบวนการ OAuth ของ Aspose Cloud (`/connect/token`) โดยใช้ client ID และ client secret ของคุณ

**Q:** *ฉันควรส่ง JSON body ใดเพื่อเปลี่ยนความกว้างคอลัมน์ A–C ให้เป็น 25 จุด?*  
**A:**  

```json
{
  "FirstColumn": 0,
  "ColumnCount": 3,
  "FirstRow": 0,
  "RowCount": 1
}
```

เพิ่มพารามิเตอร์ query `value=25` ลงใน URL ของคำขอ