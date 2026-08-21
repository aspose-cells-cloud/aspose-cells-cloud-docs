---
title: "เพิ่มตัวกรอง Top 10 ลงในแผ่นงาน Excel (Aspose.Cells Cloud)"
ArticleTitle: "เพิ่มตัวกรอง Top 10 ลงในแผ่นงาน Excel – Aspose.Cells Cloud"
second_title: "เอกสาร"
linktype: "เพิ่มตัวกรอง top 10"
type: docs
url: /th/autofilter/add-top-10-filter/
aliases:
  [/th/filter-the-top-10-items-in-the-list/, /th/autofilter/add-a-top-10-filter/]
keywords: "Aspose.Cells, AutoFilter, ตัวกรอง Top 10, Excel API"
description: "เรียนรู้วิธีใช้ตัวกรอง Top 10 กับแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API ซึ่งรวมถึง endpoint, พารามิเตอร์, ตัวอย่าง HTTPS cURL, รายละเอียดการยืนยันตัวตน, การจัดการข้อผิดพลาด และตัวอย่าง SDK สำหรับ C#, Java, Python และอื่นๆ"
weight: 65
---

REST API นี้จะกรองรายการ **Top 10** ที่อยู่ในรายการ

> **ข้อกำหนดเบื้องต้น**  
> • รับโทเค็น JWT ที่ถูกต้องโดยใช้การยืนยันตัวตนของ Aspose.Cells Cloud  
> • อัปโหลดสมุดงาน Excel ไปยังพื้นที่จัดเก็บบน Aspose Cloud ของคุณ (หรือระบุพื้นที่จัดเก็บ/โฟลเดอร์ที่อยู่)  
> • ทราบชื่อแผ่นงานและช่วงเซลล์ที่ต้องการกรอง

## PutWorksheetFilterTop10 API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filterTop10
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | จำเป็น | ค่าเริ่มต้น | คำอธิบาย |
| --------------- | ------- | -------- | -------- | ------- | --------------------------------------------------------------------------- |
| **name** | string | path | จำเป็น | — | ชื่อไฟล์ Excel |
| **sheetName** | string | path | จำเป็น | — | ชื่อแผ่นงานที่มีข้อมูล |
| **range** | string | query | จำเป็น | — | ช่วงเซลล์ที่จะใช้ตัวกรอง (เช่น `A1:B10`) |
| **fieldIndex** | integer | query | จำเป็น | — | ดัชนีของคอลัมน์ที่จะใช้ตัวกรอง (เริ่มต้นที่ 0) |
| **isTop** | boolean | query | จำเป็น | `true` | `true` เพื่อกรองรายการที่อยู่อันดับต้นๆ; `false` สำหรับรายการที่อยู่อันดับท้ายๆ |
| **isPercent** | boolean | query | ไม่จำเป็น | `false` | `true` ให้ถือว่า `itemCount` เป็นเปอร์เซ็นต์; `false` สำหรับจำนวนที่แน่นอน |
| **itemCount** | integer | query | ไม่จำเป็น | `10` | จำนวนรายการที่จะรวมไว้ในตัวกรอง |
| **matchBlanks** | boolean | query | ไม่จำเป็น | `false` | `true` เพื่อรวมเซลล์ว่างในผลลัพธ์ของตัวกรอง |
| **refresh** | boolean | query | ไม่จำเป็น | `false` | `true` เพื่ออัปเดตตัวกรองหลังจากใช้งานแล้ว |
| **folder** | string | query | ไม่จำเป็น | — | โฟลเดอร์ในพื้นที่จัดเก็บที่ไฟล์ Excel อยู่ |
| **storageName** | string | query | ไม่จำเป็น | — | ชื่อของพื้นที่จัดเก็บบน Aspose Cloud |

### **การตอบกลับ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**การตอบกลับข้อผิดพลาดทั่วไป**

```json
{
    "Code":400,
    "Message":"คำขอไม่ถูกต้อง – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง"
}
```

```json
{
    "Code":401,
    "Message":"ไม่ได้รับอนุญาต – โทเค็น JWT ไม่ถูกต้องหรือขาดหาย"
}
```

```json
{
    "Code":413,
    "Message":"ข้อมูลส่งออกมีขนาดใหญ่เกินไป – ไฟล์ที่อัปโหลดเกินขนาดที่อนุญาต"
}
```

```json
{
    "Code":500,
    "Message":"ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน – เงื่อนไขที่ไม่คาดคิดของเซิร์ฟเวอร์"
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย | คำอธิบาย |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK) | ใช้งานตัวกรองสำเร็จ; การตอบกลับมีรายละเอียดของคำสั่งดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | ข้อมูลส่งออกมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดเกินขีดจำกัดขนาด |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์ |

## วิธีใช้ PutWorksheetFilterTop10 API ด้วย SDK

### ข้อมูลจำเพาะ PutWorksheetFilterTop10 API

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilterTop10) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณโต้ตอบกับ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียก API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filterTop10?range=A1:B10&fieldIndex=0&isTop=true&itemCount=10" \
  -X PUT \
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

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นไปที่โปรเจกต์ของคุณได้ โปรดตรวจสอบที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilterTop10.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilterTop10.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilterTop10.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilterTop10.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilterTop10.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilterTop10.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilterTop10.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilterTop10.go" >}}

{{< /tab >}}

{{< /tabs >}}