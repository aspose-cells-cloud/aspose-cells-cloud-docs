---
title: "ยกเลิกการซ่อนแถวในแผ่นงาน Excel"
second_title: "เอกสาร"
linktitle: "ยกเลิกการซ่อน"
type: docs
url: /th/rows/unhide/
aliases: [  /th/unhide-rows-in-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, ยกเลิกการซ่อนแถว, REST API, สเปรดชีต, .NET, Java, Python, Node.js, Ruby, Go, PHP, Perl, Swift, Aspose.Cells Cloud REST API"
description: "ใช้ Aspose.Cells Cloud REST API เพื่อยกเลิกการซ่อนแถวในแผ่นงาน Excel API นี้มีให้ผ่าน SDK ต่างๆ เช่น .NET, Java, Python, Node.js, Ruby, Go, PHP, Perl และ Swift"
weight: 50
ArticleTitle: "ยกเลิกการซ่อนแถวในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud API"
---

REST API นี้ใช้ยกเลิกการซ่อนแถวในแผ่นงาน Excel

**ข้อกำหนดเบื้องต้น:** รับโทเค็น JWT ที่ถูกต้องจากบริการยืนยันตัวตนของ Aspose Cloud และอัปโหลดสมุดงานเป้าหมายไปยังพื้นที่จัดเก็บที่รองรับก่อนเรียกใช้ปลายทางนี้

## PostUnhideWorksheetRows API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/unhide
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ประเภท    | ตำแหน่ง | คำอธิบาย                                     |
| ---------------- | ------- | -------- | -------------------------------------------- |
| name             | string  | path     | ชื่อสมุดงาน                                 |
| sheetName        | string  | path     | ชื่อแผ่นงาน                                  |
| startrow         | integer | query    | ดัชนีแบบเริ่มต้นที่ 0 ของแถวแรกที่จะยกเลิกการซ่อน |
| totalRows        | integer | query    | จำนวนแถวที่จะยกเลิกการซ่อน                    |
| height           | number  | query    | ความสูงของแถว (ค่าเริ่มต้นคือ 15.0)            |
| folder           | string  | query    | โฟลเดอร์ของเอกสาร                             |
| storageName      | string  | query    | ชื่อของพื้นที่จัดเก็บ                         |

<a href="https://apireference.aspose.cloud/cells/#/Cells/PostUnhideWorksheetRows" rel="noopener noreferrer">สเปซิฟิเคชัน OpenAPI</a> กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้สาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

**การยืนยันตัวตน**  
คำขอทั้งหมดต้องได้รับการยืนยันตัวตนโดยใช้โทเค็น JWT ที่ได้รับจากบริการยืนยันตัวตนของ Aspose Cloud ใส่โทเค็นนี้ในส่วนหัว `Authorization: Bearer <jwt token>`

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/unhide?startrow=1&totalRows=1&height=15" \
 -X POST \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt token>"
# หมายเหตุ: เนื้อหา POST ว่างเปล่าสำหรับปลายทางนี้
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย                                               |
|-----|-----------------------------|--------------------------------------------------------|
| 200 | OK                          | ใช้ตัวกรองสำเร็จ; การตอบกลับประกอบด้วยรายละเอียดของ operation |
| 400 | Bad Request                 | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401 | Unauthorized                | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                          |
| 413 | Payload Too Large           | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                          |
| 500 | Internal Server Error       | เกิดข้อผิดพลาดภายในเซิร์ฟเวอร์อย่างไม่คาดคิด                 |

สำหรับการแก้ไขปัญหาแบบละเอียด โปรดดูที่[คู่มือการจัดการข้อผิดพลาด](/error-handling/)

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งกระบวนการพัฒนา SDK จัดการรายละเอียดระดับต่ำเพื่อให้คุณสามารถมุ่งเน้นไปที่งานในโปรเจกต์ของคุณ โปรดดูที่[ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}