---
title: "รับจำนวนหน้าสำหรับแผ่นงาน Excel"
second_title: "เอกสาร"
linktitle: "PageCount"
type: docs
url: /th/worksheets/page-count/
keywords: "Aspose.Cells, API สำหรับ Excel, จำนวนหน้าของแผ่นงาน, REST, SDK บนคลาวด์, การแบ่งหน้าใน Excel"
description: "ดึงจำนวนหน้าที่สามารถพิมพ์ได้ในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API (เวอร์ชัน 3.0) รวมถึงรูปแบบคำขอ HTTPS, ขั้นตอนการตรวจสอบสิทธิ์, ตัวอย่าง cURL, การตอบกลับ JSON แบบเต็ม, รหัสสถานะ และตัวอย่างโค้ด SDK"
weight: 10
ArticleTitle: "รับจำนวนหน้าสำหรับแผ่นงาน Excel – Aspose.Cells Cloud API"
---

REST API นี้จะส่งคืน **จำนวนหน้า** ของแผ่นงาน

**การตรวจสอบสิทธิ์:** ปลายทางทั้งหมดของ Aspose.Cells Cloud ต้องใช้โทเค็น Bearer ที่ได้มาผ่านขั้นตอน OAuth2 โดยใส่โทเค็นในส่วนหัว `Authorization` ดังที่แสดงในตัวอย่าง cURL ด้านล่าง

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagecount
```

### พารามิเตอร์คำขอ

| พารามิเตอร์     | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                   |
| --------------- | ---------- | -------- | ------------------------------------------ |
| name            | string     | path     | ชื่อเอกสาร                                 |
| sheetName       | string     | path     | ชื่อแผ่นงาน                                |
| folder          | string     | query    | โฟลเดอร์ที่เก็บเอกสารไว้                   |
| storageName     | string     | query    | ชื่อของพื้นที่จัดเก็บ (storage)            |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/GetPageCount) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการโต้ตอบ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างด้านล่างแสดงวิธีเรียกใช้ API ผ่าน cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/worksheets/Sheet1/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "PageCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

### รายละเอียดการตอบกลับ

| รหัสสถานะ HTTP | ความหมาย                                              |
| -------------- | ----------------------------------------------------- |
| **200**        | สำเร็จ – ส่งคืน payload JSON ดังที่แสดงไว้ด้านบน    |
| **401**        | ไม่ได้รับอนุญาต – ขาดโทเค็นหรือโทเค็นไม่ถูกต้อง     |
| **404**        | ไม่พบ – ไฟล์หรือแผ่นงานไม่มีอยู่                    |
| **500**        | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน – เงื่อนไขเซิร์ฟเวอร์ผิดปกติ |

### ประวัติเวอร์ชัน

_API เวอร์ชัน **v3.0** (เผยแพร่เมื่อปี 2025) หากคุณกำลังใช้เวอร์ชันใหม่กว่า โปรดอ้างอิงเอกสารปลายทางที่อัปเดต_

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK ช่วยซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณ ดู [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

### หมายเหตุ

- จำนวนหน้าสะท้อนการจัดรูปแบบที่สามารถพิมพ์ได้ โดยพิจารณาการแบ่งหน้า ขอบกระดาษ และการปรับขนาดแล้ว แถวหรือคอลัมน์ที่ซ่อนไว้อาจส่งผลต่อผลลัพธ์
- ตรวจสอบให้แน่ใจว่าแผ่นงานเป้าหมายมีอยู่และไฟล์ถูกจัดเก็บไว้ใน `folder` และ `storageName` ที่ระบุก่อนที่จะส่งคำขอ