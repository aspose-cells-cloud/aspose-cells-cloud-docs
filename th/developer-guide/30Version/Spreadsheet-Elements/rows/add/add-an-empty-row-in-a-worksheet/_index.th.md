---
title: "เพิ่มแถวว่างในแผ่นงาน Excel"
ArticleTitle: "เพิ่มแถวว่างลงในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktitle: "แถว"
type: docs
url: /rows/add/row/
aliases: [/add-an-empty-row-in-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, เพิ่มแถวว่าง, แผ่นงาน, REST API, แทรกแถว, สเปรดชีตบนคลาวด์"
description: "ใช้ Aspose.Cells Cloud REST API เพื่อแทรกแถวว่างลงในแผ่นงาน Excel รองรับ SDK หลายภาษา (C#, Java, Python, Go, PHP, Ruby, Node.js, Perl, Android, Swift) สำหรับการพัฒนาอย่างรวดเร็ว"
weight: 20
---

API นี้ของ REST จะเพิ่มแถวใหม่ลงในแผ่นงาน Excel โดยจะแทรกแถวว่างที่ตำแหน่งดัชนีแบบศูนย์ (zero-based index) ที่กำหนดไว้

**ข้อกำหนดเบื้องต้น:**  
- ต้องมีโทเคนการเข้าถึง Aspose Cloud ที่ถูกต้อง (Bearer JWT) ซึ่งต้องระบุไว้ในหัวข้อ `Authorization`  
- ไฟล์สมุดงานเป้าหมายต้องถูกอัปโหลดไว้ในพื้นที่จัดเก็บของ Aspose Cloud แล้ว และพารามิเตอร์ `folder` และ `storageName` ควรชี้ไปยังตำแหน่งของไฟล์ดังกล่าว

**หมายเหตุ:**  
- `rowIndex` เป็นดัชนีแบบศูนย์ (zero-based); การแทรกที่ดัชนี 0 จะเพิ่มแถวเข้าไปที่ด้านบนสุดของแผ่นงาน  
- แผ่นงาน Excel มีจำนวนแถวสูงสุดอยู่ที่ 1,048,576 แถว; หากพยายามแทรกเกินขีดจำกัดนี้จะส่งผลให้เกิดข้อผิดพลาด

## API PutInsertWorksheetRow

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### **พารามิเตอร์ของคำขอ**

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย                                               |
| ---------------- | -------- | -------- | ------------------------------------------------------ |
| name             | string   | path     | ชื่อไฟล์สมุดงาน                                      |
| sheetName        | string   | path     | ชื่อแผ่นงาน                                          |
| rowIndex         | integer  | path     | ดัชนีแบบศูนย์ที่จะแทรกแถวใหม่เข้าไป                 |
| folder           | string   | query    | ตำแหน่งโฟลเดอร์ในพื้นที่จัดเก็บที่มีสมุดงานอยู่      |
| storageName      | string   | query    | ชื่อของพื้นที่จัดเก็บ Aspose Cloud ที่ต้องการใช้งาน  |

<a href="https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetRow" rel="noopener noreferrer">สเปค OpenAPI</a> กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถโต้ตอบกับ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/10" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **หมายเหตุ:** ปลายทาง (endpoint) ทั้งหมดของ Aspose.Cells Cloud ต้องใช้ HTTPS เท่านั้น ใช้รูปแบบที่ปลอดภัย `https://` สำหรับการเรียกใช้งานในระบบจริง

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

| โค้ด | ความหมาย                   | คำอธิบาย                                             |
|-----|----------------------------|------------------------------------------------------|
| 200 | สำเร็จ (OK)                | ใช้ตัวกรองเรียบร้อยแล้ว การตอบกลับจะมีรายละเอียดของการดำเนินการ |
| 400 | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401 | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                        |
| 413 | ข้อมูลส่งไปมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด           |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์             |

*ตัวอย่างการตอบกลับข้อผิดพลาด (เช่น เมื่อดัชนีแถวเกินขีดจำกัดของแผ่นงาน):*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "ดัชนีแถวอยู่นอกช่วงที่อนุญาต จำนวนแถวสูงสุดที่อนุญาตคือ 1048576"
}
```

## ชุดเครื่องมือพัฒนาบนคลาวด์ (Cloud SDK Family)

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะช่วยซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานหลักของโครงการได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บ GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}