---
title: "เพิ่มคอลัมน์ว่างลงในแผ่นงาน Excel - Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktitle: "เพิ่ม"
type: docs
url: /th/columns/add/
aliases:
  - /add-an-empty-column-in-an-excel-worksheet/
  - /add-an-empty-column-in-a-worksheet/
keywords: "เพิ่ม, คอลัมน์, Excel, API, Aspose.Cells, Cloud, REST, แทรก"
description: "เรียนรู้วิธีการแทรกคอลัมน์ใหม่ลงในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API ซึ่งประกอบด้วยไวยากรณ์คำร้องขอ ตัวอย่าง cURL และตัวอย่างโค้ด SDK"
weight: 20
ArticleTitle: "เพิ่มคอลัมน์ว่างลงในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud API"
---

REST API นี้แทรกคอลัมน์หนึ่งคอลัมน์หรือมากกว่านั้นลงในแผ่นงาน  

**ข้อกำหนดเบื้องต้น**  
ก่อนเรียกจุดปลายทางนี้ โปรดตรวจสอบว่าคุณได้ดำเนินขั้นตอนต่อไปนี้เสร็จสมบูรณ์แล้ว:

- รับโทเค็นการเข้าถึง OAuth 2.0 ที่ถูกต้อง และแนบไว้ในส่วนหัว `Authorization`  
- จัดเก็บสมุดงานเป้าหมายไว้ในพื้นที่จัดเก็บที่เลือก (ค่าเริ่มต้น = "Default") หรือระบุพารามิเตอร์ `folder` และ `storageName` ที่เหมาะสม  
- ตรวจสอบว่าชื่อแผ่นงานที่ระบุใน `sheetName` มีอยู่ในสมุดงานแล้ว

## API PutInsertWorksheetColumns

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}?totalColumns=1
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

### พารามิเตอร์คำร้องขอ

| ชื่อพารามิเตอร์    | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                         |
| ------------------- | ---------- | -------- | ---------------------------------------------------------------- |
| **name**            | string     | path     | ชื่อไฟล์สมุดงาน                                                 |
| **sheetName**       | string     | path     | ชื่อแผ่นงาน                                                     |
| **columnIndex**     | integer    | path     | ดัชนีแบบเริ่มต้นที่ 0 ของคอลัมน์ที่เริ่มการแทรก                 |
| **totalColumns**    | integer    | query    | จำนวนคอลัมน์ที่จะแทรก                                           |
| **updateReference** | boolean    | query    | เมื่อตั้งค่าเป็น **true** การอ้างอิงเซลล์จะถูกอัปเดตเพื่อสะท้อนการแทรก |
| **folder**          | string     | query    | เส้นทางไปยังโฟลเดอร์ที่มีสมุดงาน                                |
| **storageName**     | string     | query    | ชื่อของบริการพื้นที่จัดเก็บ                                     |

**หมายเหตุ**

- `columnIndex` ต้องอยู่ระหว่าง 0 ถึงจำนวนคอลัมน์ปัจจุบันในแผ่นงาน การแทรกระยะที่เกินขอบเขตที่มีอยู่จะขยายแผ่นงานโดยอัตโนมัติ  
- การแทรกหลายคอลัมน์ (`totalColumns` > 1) จะเลื่อนคอลัมน์ที่มีอยู่ไปทางขวา  
- ค่าเริ่มต้นของฟlag `updateReference` คือ `false` ตั้งค่าเป็น `true` เพื่ออัปเดตสูตรและช่วงที่ตั้งชื่อไว้

<a href="https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetColumns" target="_blank" rel="noopener noreferrer">สเปค OpenAPI</a> กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้สาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเรียกบริการเว็บของ Aspose.Cells ตัวอย่างต่อไปนี้แสดงคำร้องขอที่สมบูรณ์ รวมถึงการยืนยันตัวตนและพารามิเตอร์เส้นทางที่ถูกต้อง

{{< tabs tabTotal="2" tabID="11" tabName11="คำร้องขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?totalColumns=1&updateReference=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json"
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

**รหัสการตอบกลับ**

| รหัส | คำอธิบาย                                          |
|------|---------------------------------------------------|
| 200  | แทรกคอลัมน์เรียบร้อยแล้ว                         |
| 400  | คำร้องขอผิดรูปแบบ – พารามิเตอร์สูญหายหรือไม่ถูกต้อง |
| 401  | ไม่ได้รับอนุญาต – โทเค็นไม่ถูกต้องหรือสูญหาย       |
| 404  | ไม่พบสมุดงานหรือแผ่นงาน                          |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์                         |

**ตัวอย่างการตอบกลับข้อผิดพลาด**

```json
// 400 Bad Request – พารามิเตอร์สูญหายหรือไม่ถูกต้อง
{
  "Code": 400,
  "Message": "พารามิเตอร์ไม่ถูกต้อง: totalColumns ต้องเป็นจำนวนเต็มบวก"
}

// 401 Unauthorized – โทเค็นไม่ถูกต้องหรือสูญหาย
{
  "Code": 401,
  "Message": "การยืนยันตัวตนล้มเหลว โทเค็นการเข้าถึงสูญหายหรือไม่ถูกต้อง"
}

// 404 Not Found – ไม่มีสมุดงานหรือแผ่นงานดังกล่าว
{
  "Code": 404,
  "Message": "ไม่พบสมุดงาน 'test.xlsx'"
}

// 500 Internal Server Error
{
  "Code": 500,
  "Message": "เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์"
}
```

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นไปที่ตรรกะของโครงการของคุณ ดู <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">ที่เก็บ GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}