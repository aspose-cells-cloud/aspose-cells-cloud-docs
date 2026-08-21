---
title: "Aspose.Cells Cloud – แปลงช่วงของไฟล์ Excel เป็น HTML"
description: "แปลงช่วงที่ระบุของไฟล์ Excel (เช่น A1:C10) เป็นไฟล์ HTML โดยใช้ Aspose.Cells Cloud REST API ครอบคลุมการยืนยันตัวตน ตัวอย่างคำขอ การจัดการคำตอบ ตัวอย่างโค้ด SDK และรหัสข้อผิดพลาด"
keywords: "Aspose.Cells, Excel เป็น HTML, การแปลงช่วง, API บนคลาวด์, สเปรดชีต"
slug: convert-range-to-html
date: 2026-07-30
type: docs
weight: 100
---

แปลงช่วงที่เลือกของสมุดงาน Excel ที่อยู่บนเครื่องของคุณเป็นไฟล์ HTML โดยตรงผ่าน Aspose.Cells Cloud การแปลงเกิดขึ้นบนเซิร์ฟเวอร์คลาวด์ทั้งหมด ดังนั้นคุณไม่จำเป็นต้องอัปโหลดสมุดงานทั้งหมดหรือติดตั้ง Excel บนเครื่องของคุณ

## API สำหรับการแปลงช่วงเป็น HTML

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/html
```

เนื้อหาคำขอเป็น `multipart/form-data` ซึ่งมีไฟล์สเปรดชีต ส่วนตัวเลือกอื่นๆ จะถูกส่งผ่านพารามิเตอร์แบบ query

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์   | ชนิดข้อมูล | ตำแหน่ง | จำเป็น | คำอธิบาย                                                                 |
| ------------------ | --------- | -------- | ------ | -------------------------------------------------------------------------- |
| **Spreadsheet**    | ไฟล์     | FormData | ใช่    | สมุดงาน Excel ที่ต้องการแปลง                                              |
| **worksheet**      | สตริง     | Query    | ใช่    | ชื่อแผ่นงานที่มีช่วงที่ต้องการแปลง                                        |
| **range**          | สตริง     | Query    | ใช่    | พื้นที่เซลล์ที่ต้องการแปลง เช่น `A1:C10`                                 |
| **outPath**        | สตริง     | Query    | ไม่จำเป็น | เส้นทางไปยังโฟลเดอร์ที่จะบันทึกไฟล์ HTML ผลลัพธ์ (ค่าเริ่มต้น `null`)      |
| **outStorageName** | สตริง     | Query    | ไม่จำเป็น | ชื่อบริการจัดเก็บข้อมูลสำหรับไฟล์ผลลัพธ์                                  |
| **fontsLocation**  | สตริง     | Query    | ไม่จำเป็น | เส้นทางไปยังโฟลเดอร์ฟอนต์ที่กำหนดเอง                                      |
| **AutoRowsFit**    | ค่าบูลีน  | Query    | ไม่จำเป็น | ปรับความสูงของแถวทั้งหมดในแผ่นงานให้พอดีโดยอัตโนมัติ                      |
| **AutoColumnsFit** | ค่าบูลีน  | Query    | ไม่จำเป็น | ปรับความกว้างของคอลัมน์ทั้งหมดในแผ่นงานให้พอดีโดยอัตโนมัติ                |
| **region**         | สตริง     | Query    | ไม่จำเป็น | ตัวระบุภาษา和地区 (เช่น `en-US`, `fr-FR`) ซึ่งส่งผลต่อรูปแบบตัวเลข/วันที่ |
| **password**       | สตริง     | Query    | ไม่จำเป็น | รหัสผ่านสำหรับเปิดสมุดงานที่ได้รับการป้องกัน                               |
| **fontsLocation**  | สตริง     | Query    | ไม่จำเป็น | ตำแหน่งฟอนต์ที่กำหนดเอง                                                   |
| **region**         | สตริง     | Query    | ไม่จำเป็น | การตั้งค่าภาษา/ภูมิภาคของสเปรดชีต                                         |
| **password**       | สตริง     | Query    | ไม่จำเป็น | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต                                            |

## คำตอบ

API จะส่งคืนไฟล์ HTML ที่แปลงแล้วเป็น **สตรีมไบนารี** (`application/octet-stream`)

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### ตัวอย่างคำตอบที่สำเร็จ (HTTP)

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.html"
Content-Length: 8423

<table>
  <tr><th>Product</th><th>Price</th></tr>
  <tr><td>Widget A</td><td>$10</td></tr>
  <tr><td>Widget B</td><td>$15</td></tr>
</table>
```

บันทึกเนื้อหาของคำตอบลงในไฟล์ (เช่น `report.html`) เพื่อดูตารางที่แสดงผลในเว็บเบราว์เซอร์

---

**รหัสสถานะ HTTP**

| รหัส | ความหมาย               | คำอธิบาย                                                        |
| ---- | ---------------------- | ---------------------------------------------------------------- |
| 200  | สำเร็จ (OK)            | ใช้ตัวกรองสำเร็จ; คำตอบประกอบด้วยรายละเอียดของปฏิบัติการ       |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)          |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | JWT token ไม่ถูกต้องหรือขาดหาย                                  |
| 413  | ข้อมูลในคำขอใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                               |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                        |

## วิธีใช้ API แปลงช่วงเป็น HTML ด้วย SDK

### ข้อกำหนด OpenAPI

[ข้อกำหนด OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToHTML) กำหนด API ที่เข้าถึงได้จากสาธารณะ ซึ่งช่วยให้คุณสามารถโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่าน command-line เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="คำตอบ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/html?worksheet=Sheet1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.html"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.html"
Content-Length: 8423

<table>
  <tr><th>Product</th><th>Price</th></tr>
  <tr><td>Widget A</td><td>$10</td></tr>
  <tr><td>Widget B</td><td>$15</td></tr>
</table>
```

{{< /tab >}}

{{< /tabs >}}

## ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจาก SDK ซ่อนรายละเอียดระดับต่ำไว้ให้คุณสามารถแปลงช่วงข้อมูลเป็นไฟล์ HTML ด้วยโค้ดเพียงเล็กน้อย  
ดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมดได้ที่ [GitHub repository](https://github.com/aspose-cells-cloud)

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ หากการโหลดจาก Gist ถูกบล็อก คุณสามารถดาวน์โหลดตัวอย่างโดยตรงจาก repository

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}