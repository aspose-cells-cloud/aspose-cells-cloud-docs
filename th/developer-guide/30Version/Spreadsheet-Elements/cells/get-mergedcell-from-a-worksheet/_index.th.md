---
title: "รับช่วงเซลล์ที่ถูกผสานจากสมุดงาน Excel – Aspose.Cells Cloud API"
type: docs
url: /get-mergedcell-from-a-worksheet/
weight: 60
keywords: "Aspose.Cells Cloud, เซลล์ที่ผสาน, สมุดงาน Excel, REST API, Aspose.Cells SDK, เซลล์ที่ผสานใน Excel"
description: "เรียนรู้วิธีดึงข้อมูลช่วงเซลล์ที่ผสานจากสมุดงาน Excel โดยใช้ Aspose.Cells Cloud API (เวอร์ชัน 3.0) ซึ่งรวมถึงขั้นตอนการตรวจสอบสิทธิ์ คำสั่ง cURL แบบเต็ม โครงสร้างการตอบกลับ การจัดการข้อผิดพลาด และตัวอย่าง SDK ในภาษา C#, Java, Python และอื่นๆ"
---

REST API นี้คืนข้อมูลเกี่ยวกับ **เซลล์ที่ผสาน** ในสมุดงาน Excel

> **หมายเหตุ** – วัตถุ API มีชื่อว่า **MergedCell** (รูปเดียว) ในเนื้อหาที่เป็นข้อความเราจะกล่าวถึง *แนวคิด* ของเซลล์ที่ผสาน (รูปหลายจำนวน)

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/mergedCells
```

## ความปลอดภัยและการตรวจสอบสิทธิ์

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ [การตรวจสอบสิทธิ์ด้วยโทเคน JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                              |
|------------------|------------|----------|---------------------------------------|
| **name**         | string     | path     | ชื่อไฟล์ Excel                        |
| **sheetName**    | string     | path     | ชื่อworksheet                        |
| **folder**       | string     | query    | โฟลเดอร์ที่เก็บเอกสารไว้             |
| **storageName**  | string     | query    | ชื่อที่จัดเก็บที่ต้องการใช้งาน        |

## **การตอบกลับ**

ส่งคืน MergedCellsResponse

```json
{
  "Status":"OK",
  "Code":200,
  "MergedCells":{
    "Count": 0,
    "MergedCellList":[
      {
        "Link":{
          "Href":"",
          "Rel":"",
          "Type":"",
          "Title":""
        }
      }
    ]
  }
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                    | คำอธิบาย                                         |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                 | กรองข้อมูลเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหายไป                   |
| 413  | ข้อมูลในคำขอมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด         |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดภายในเซิร์ฟเวอร์         |

## วิธีการใช้งาน API GetWorksheetMergedCells ร่วมกับ SDK

### ข้อมูลเฉพาะของ API GetWorksheetMergedCells

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetMergedCells) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้จากภายนอก และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ผ่าน cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/mergedCells" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MergedCells": {
    "Count": 1,
    "MergedCells": [
      {
      "link": {
            "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/cells/mergedcells/0",
            "Rel": "self"
          }
      }
    ]    
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### ใช้งาน SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนาโปรแกรมที่เชื่อมต่อกับ API SDK จะจัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณเอง ดู [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้เว็บเซอร์วิสของ Aspose.Cells ผ่าน SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetMergedCells.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetMergedCells.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetMergedCells.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetMergedCells.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetMergedCells.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetMergedCells.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetMergedCells.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetMergedCells.go" >}}

{{< /tab >}}

{{< /tabs >}}