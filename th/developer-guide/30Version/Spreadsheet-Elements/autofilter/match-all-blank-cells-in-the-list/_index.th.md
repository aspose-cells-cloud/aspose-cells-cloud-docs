---
title: "จับคู่เซลล์ว่างทั้งหมดในแผ่นงาน Excel"
ArticleTitle: "จับคู่เซลล์ว่างทั้งหมดในแผ่นงาน Excel – คู่มือ API Aspose.Cells Cloud"
second_title: "เอกสาร"
linktype: "docs"
url: /th/autofilter/match-all-blank/
aliases: [  /th/match-all-blank-cells-in-the-list/ ]
keywords: "Aspose.Cells, เซลล์ว่าง, AutoFilter, REST API, Excel"
description: "เรียนรู้วิธีใช้ Aspose.Cells Cloud REST API เพื่อกรองและจับคู่เซลล์ว่างทั้งหมดในแผ่นงาน Excel รวมถึง endpoint, พารามิเตอร์, ขั้นตอนการยืนยันตัวตน, ตัวอย่าง cURL และตัวอย่าง SDK สำหรับ C#, Java, Python และอื่นๆ"
weight: 100
---

API นี้จับคู่ **เซลล์ว่าง** ทั้งหมดในรายการตัวกรองของแผ่นงาน Excel

**ข้อกำหนดเบื้องต้น:** ก่อนเรียก endpoint นี้ คุณต้องมีโทเค็น JWT ที่ถูกต้อง อัปโหลดสมุดงานลงในที่จัดเก็บของ Aspose Cloud และทราบเส้นทางโฟลเดอร์ในที่จัดเก็บ (หากมี) ระบุพารามิเตอร์ `folder` และ `storageName` เมื่อไฟล์ไม่อยู่ในรูทเริ่มต้น

## API PostWorksheetMatchBlanks

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchBlanks
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
|----------------|---------|----------|------------------------------------------------------------------------|
| name           | string  | path     | ชื่อไฟล์สมุดงาน |
| sheetName      | string  | path     | ชื่อแผ่นงานที่มีตัวกรอง |
| fieldIndex     | integer | query    | ดัชนี (เริ่มต้นที่ 0) ของคอลัมน์ที่นำไปใช้ตัวกรอง |
| folder         | string  | query    | เส้นทางโฟลเดอร์ในที่จัดเก็บที่อยู่ของสมุดงาน |
| storageName    | string  | query    | ชื่อของที่จัดเก็บ Aspose Cloud |

### **การตอบกลับ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                      | คำอธิบาย |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                          | ใช้ตัวกรองสำเร็จ; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request)                 | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)                | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | ข้อมูลในคำขอใหญ่เกินไป (Payload Too Large)           | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error)       | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์ |

## วิธีใช้ API PostWorksheetMatchBlanks ร่วมกับ SDK

### ข้อกำหนด API PostWorksheetMatchBlanks

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchBlanks) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้สาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}
```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchBlanks?fieldIndex=0" \
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

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งกระบวนการพัฒนา SDK จะช่วยซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโปรเจกต์ของคุณ ตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้เว็บเซอร์วิสของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchBlanks.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchBlanks.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchBlanks.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchBlanks.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchBlanks.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchBlanks.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchBlanks.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchBlanks.go" >}}
{{< /tab >}}

{{< /tabs >}}
---