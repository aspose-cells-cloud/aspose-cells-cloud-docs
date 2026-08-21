---
title: "วิธีการรวมเซลล์ในสมุดงาน Excel – Aspose.Cells Cloud API (v3.0)"
type: docs
url: /th/merge-cells-in-excel-worksheet/
weight: 110
keywords: "รวมเซลล์, Aspose.Cells, Cloud API, Excel"
description: "คู่มือการรวมเซลล์ในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API พร้อมตัวอย่าง cURL และ SDK"
ArticleTitle: "วิธีการรวมเซลล์ในสมุดงาน Excel – Aspose.Cells Cloud API (v3.0)"
---

Aspose.Cells Cloud REST API ช่วยรวมกลุ่มเซลล์รูปสี่เหลี่ยมผืนผ้าให้เป็นเซลล์เดียวที่ครอบคลุมแถวและคอลัมน์ที่ระบุ

**ข้อกำหนดเบื้องต้น**  
- โทเค็น JWT ที่ถูกต้องสำหรับการยืนยันตัวตน  
- สมุดงานต้องมีอยู่แล้วในโฟลเดอร์ที่ระบุของพื้นที่เก็บข้อมูล  
- ต้องกำหนดค่าพื้นที่เก็บข้อมูล (ชื่อโฟลเดอร์และชื่อพื้นที่เก็บข้อมูล) ในบัญชี Aspose.Cloud ของคุณแล้ว

## API PostWorksheetMerge

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/merge
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบใช้โทเค็น JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย |
|------------------|--------|----------|-----------|
| name             | string | path     | ชื่อสมุดงาน |
| sheetName        | string | path     | ชื่อworksheet |
| startRow         | integer | query   | ดัชนีของแถวแรก (เริ่มต้นที่ 0 = แถวแรก) |
| startColumn      | integer | query   | ดัชนีของคอลัมน์แรก (เริ่มต้นที่ 0 = คอลัมน์แรก) |
| totalRows        | integer | query   | จำนวนแถวที่ต้องการรวม |
| totalColumns     | integer | query   | จำนวนคอลัมน์ที่ต้องการรวม |
| folder           | string | query    | โฟลเดอร์ที่เก็บสมุดงาน |
| storageName      | string | query    | ชื่อพื้นที่เก็บข้อมูล |

*ไม่จำเป็นต้องส่งเนื้อหาคำขอ (request body) สำหรับการดำเนินการนี้*

## **การตอบกลับ**

ส่งกลับ CellsCloudResponse

```json
{
  "Status":"OK",
  "Code":200
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | คำอธิบาย |
|------|-------------------------------|-----------|
| 200  | สำเร็จ (OK)                  | กรองถูกใช้งานเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | ข้อมูลโหลดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

## วิธีใช้ API PostWorksheetMerge ร่วมกับ SDK

### ข้อมูลกำกับ API PostWorksheetMerge

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetMerge) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้สาธารณะ และช่วยให้คุณสามารถดำเนินการโต้ตอบ REST ผ่านเว็บเบราว์เซอร์ได้โดยตรง

คุณสามารถใช้เครื่องมือ **cURL command line** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ผ่าน cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/merge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
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

### ใช้ Aspose.Cells Cloud SDK

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ผ่าน SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}