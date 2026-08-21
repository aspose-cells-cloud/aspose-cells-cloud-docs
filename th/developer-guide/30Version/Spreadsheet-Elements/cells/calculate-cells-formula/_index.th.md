---
title: "คำนวณสูตรของเซลล์ – API ของ Aspose.Cells Cloud"
type: docs
url: /th/calculate-cells-formula/
weight: 90
keywords: "Aspose.Cells Cloud, คำนวณสูตรของเซลล์, Excel API, REST API, SDK"
description: "คำนวณสูตรของเซลล์ในไฟล์ Excel ผ่าน REST API ของ Aspose.Cells Cloud (เวอร์ชัน 3.0) รวมถึง endpoint, พารามิเตอร์, ตัวอย่าง cURL และโค้ดตัวอย่าง SDK"
ArticleTitle: "คำนวณสูตรของเซลล์ – เอกสารประกอบ API ของ Aspose.Cells Cloud"
---

## REST API

REST API นี้ใช้คำนวณ **สูตรของเซลล์** ในสมุดงาน Excel

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/calculate
```

## ความปลอดภัยและการตรวจสอบสิทธิ์

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้การตรวจสอบสิทธิ์แบบใช้โทเค็น JWT [ดูรายละเอียดเพิ่มเติม](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

### พารามิเตอร์ของ Request

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่งพารามิเตอร์ (path/query/body) | คำอธิบาย |
| -------------- | ------ | ------------------------------------ | -------------------------------------------------------------------- |
| name           | string | path                                 | ชื่อไฟล์ Excel (เช่น `Book1.xlsx`) |
| sheetName      | string | path                                 | ชื่อแผ่นงานที่มีเซลล์ที่ต้องการคำนวณ |
| cellName       | string | path                                 | ที่อยู่ของเซลล์ที่ต้องการคำนวณ (เช่น `A1`) |
| options        | object | body                                 | ออบเจ็กต์ JSON ที่มีตัวเลือกการคำนวณ (ดูตาราง **Options object**) |
| folder         | string | query                                | โฟลเดอร์ในพื้นที่จัดเก็บที่ไฟล์อยู่ |
| storageName    | string | query                                | ชื่อพื้นที่จัดเก็บของ Aspose Cloud |

#### ออบเจ็กต์ Options

| ฟิลด์         | ชนิดข้อมูล | คำอธิบาย                                                                    | ค่าเริ่มต้น |
| ------------- | ------- | ------------------------------------------------------------------------------ | ------- |
| CalcStackSize | string  | ขนาดสูงสุดของสแต็กการคำนวณ                                                | `"1"`   |
| IgnoreError   | boolean | หากเป็น `true` จะละเลยข้อผิดพลาดในการคำนวณ และตั้งค่าค่าของเซลล์เป็น `#N/A` | `false` |
| Recursive     | boolean | เปิดใช้งานการคำนวณแบบเรียกซ้ำสำหรับเซลล์ที่ขึ้นต่อกัน                      | `false` |
| Precision     | string  | จำนวนตำแหน่งทศนิยมสำหรับผลลัพธ์เชิงตัวเลข                                  | `"15"`  |
| UseThreading  | boolean | เปิดใช้งานการคำนวณแบบหลายเธรด                                               | `false` |


### **Response**

```json
{
    "Status":"OK",
    "Code":200
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | คำอธิบาย                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | ใช้ตัวกรองเรียบร้อยแล้ว; response ประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | Bad Request                 | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | Unauthorized                | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | Payload Too Large           | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | Internal Server Error       | ข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด |

## วิธีใช้ API PostCellCalculate ผ่าน SDK

### ข้อมูลจำเพาะของ API PostCellCalculate

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostCellCalculate) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้โดยสาธารณะ และช่วยให้คุณสามารถโต้ตอบกับ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียก API ผ่าน cURL **ก่อนอื่นให้รับ JWT token** โดยการตรวจสอบสิทธิ์กับ endpoint `/connect/token` และแทนที่ `<jwt token>` ด้วยค่าโทเค็นที่ได้รับ

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/calculate" \
  -d '{"CalcStackSize":"1"}' \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK ซ่อนรายละเอียดระดับต่ำไว้ และช่วยให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCellCalculate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCellCalculate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCellCalculate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCellCalculate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCellCalculate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCellCalculate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCellCalculate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCellCalculate.go" >}}

{{< /tab >}}

{{< /tabs >}}
---