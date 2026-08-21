---
title: "เพิ่มหลายแถวลงในเวิร์กชีต Excel"
ArticleTitle: "เพิ่มหลายแถวลงในเวิร์กชีต Excel โดยใช้ Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktype: "Rows"
type: docs
url: /th/rows/add/rows/
keywords: "Aspose.Cells Cloud, แทรกแถว, เวิร์กชีต Excel, REST API, SDK, เพิ่มหลายแถว"
description: "เรียนรู้วิธีใช้ Aspose.Cells Cloud REST API ในการแทรกหลายแถวลงในเวิร์กชีต Excel คู่มือนี้ครอบคลุม endpoint, พารามิเตอร์คำขอ, ตัวอย่างคำสั่ง cURL และตัวอย่างการใช้งาน SDK"
weight: 20
---

REST API นี้จะเพิ่มหลายแถวใหม่ลงในเวิร์กชีต Excel

## API PutInsertWorksheetRows

```http
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย                                                                 |
|------------------|----------|----------|--------------------------------------------------------------------------|
| name             | string   | path     | ชื่อสมุดงาน                                                            |
| sheetName        | string   | path     | ชื่อเวิร์กชีต                                                           |
| startrow         | integer  | query    | ดัชนีของแถวแรกที่จะแทรก (**เริ่มนับจาก 0**)                            |
| totalRows        | integer  | query    | จำนวนแถวที่จะแทรก                                                      |
| updateReference  | boolean  | query    | กำหนดว่าจะอัปเดตการอ้างอิงเซลล์หลังการแทรกหรือไม่ (`true` หรือ `false`) |
| folder           | string   | query    | โฟลเดอร์ที่เก็บเอกสาร                                                   |
| storageName      | string   | query    | ชื่อพื้นที่จัดเก็บ                                                     |

**ข้อกำหนดเบื้องต้น**  
สมุดงานต้องมีอยู่แล้วในพื้นที่จัดเก็บ (หรือโฟลเดอร์) ที่ระบุก่อนเรียกใช้การทำงานนี้

**การยืนยันตัวตน**  
API นี้ต้องมีโทเค็น JWT ที่ถูกต้อง โดยต้องระบุไว้ในหัวข้อ `Authorization` ดังที่แสดงในตัวอย่าง cURL ด้านล่าง

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetRows) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และอนุญาตให้คุณใช้งาน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=11&updateReference=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **หมายเหตุ:** การดำเนินการ `PUT` นี้ไม่ต้องการเนื้อหาคำขอ; คุณสามารถส่งวัตถุ JSON ว่าง (`{}`) ได้หากไลบรารีไคลเอนต์บังคับให้ส่งข้อมูล

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*รหัสการตอบกลับที่เป็นไปได้*  

- **200 OK** – แทรกแถวเรียบร้อยแล้ว  
- **400 Bad Request** – พารามิเตอร์ไม่ถูกต้อง (เช่น ดัชนีแถวติดลบ)  
- **401 Unauthorized** – โทเค็น JWT ขาดหายหรือไม่ถูกต้อง  
- **404 Not Found** – สมุดงานหรือเวิร์กชีตที่ระบุไม่มีอยู่  
- **500 Internal Server Error** – เกิดข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด

{{< /tab >}}

{{< /tabs >}}

สำหรับการทำงานเพิ่มเติมเกี่ยวกับแถว โปรดดูที่หน้าที่เกี่ยวข้อง: **ลบแถว**, **ดึงข้อมูลแถว**, และ **คัดลอกแถว**

## Cloud SDK Family

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นไปที่โครงการของคุณได้ โปรดตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}