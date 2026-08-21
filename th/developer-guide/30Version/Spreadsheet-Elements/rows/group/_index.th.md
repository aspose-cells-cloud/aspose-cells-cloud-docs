---
title: "จัดกลุ่มแถวในสมุดงาน Excel"
second_title: "เอกสาร"
linktype: "docs"
url: "/rows/group/"
aliases: [/group-rows-in-excel-worksheet/]
keywords: "จัดกลุ่มแถว, Excel, Aspose.Cells Cloud, REST API, SDK, แผ่นงาน, Excel API"
description: "จัดกลุ่มแถวในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API รองรับ SDK หลายภาษา (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) เพื่อการผสานรวมที่ง่ายดาย"
weight: 60
ArticleTitle: "จัดกลุ่มแถวในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud API"
---

REST API นี้ใช้จัดกลุ่มแถวในแผ่นงาน Excel

**ข้อกำหนดเบื้องต้น:**  
- ต้องระบุโทเคน OAuth 2.0 ที่ถูกต้อง (Bearer JWT) ในส่วนหัว `Authorization`  
- ต้องมีสมุดงานอยู่แล้วใน `folder` ที่ระบุของ `storageName` ที่เลือก (หรือในพื้นที่เก็บข้อมูลเริ่มต้น) ก่อนที่จะส่งคำขอ

## API PostGroupWorksheetRows

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/group
```

### **ความปลอดภัยและการพิสูจน์ตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การพิสูจน์ตัวตนแบบ JWT token</a>

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ประเภท    | ตำแหน่ง | คำอธิบาย                                                              |
| ---------------- | --------- | -------- | --------------------------------------------------------------------- |
| name             | string    | path     | ชื่อไฟล์สมุดงาน                                                      |
| sheetName        | string    | path     | ชื่อแผ่นงาน                                                          |
| firstIndex       | integer   | query    | ดัชนีแบบเริ่มต้นที่ 0 ของแถวแรกที่จะจัดกลุ่ม                        |
| lastIndex        | integer   | query    | ดัชนีแบบเริ่มต้นที่ 0 ของแถวสุดท้ายที่จะจัดกลุ่ม                     |
| hide             | boolean   | query    | ระบุว่าจะซ่อนแถวที่จัดกลุ่มหรือไม่ (`true` หรือ `false`)             |
| folder           | string    | query    | เส้นทางไปยังโฟลเดอร์ที่เก็บสมุดงาน                                  |
| storageName      | string    | query    | ชื่อพื้นที่เก็บข้อมูลที่สมุดงานอยู่                                 |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetRows) กำหนด API ที่สามารถเข้าถึงได้แบบสาธารณะ และให้คุณใช้ REST โต้ตอบโดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/group?firstIndex=1&lastIndex=2&hide=true" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย                                         |
|------|------------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                  | ใช้ตัวกรองสำเร็จ การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                   |
| 413  | ข้อมูลในเนื้อคำขอใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด              |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดในเซิร์ฟเวอร์         |

ตัวอย่างการตอบกลับข้อผิดพลาดทั่วไป:

- **400 Bad Request** – ตรวจสอบว่า `firstIndex` และ `lastIndex` เป็นจำนวนเต็มที่ถูกต้อง และ `firstIndex` ≤ `lastIndex`  
- **401 Unauthorized** – ตรวจสอบให้แน่ใจว่าส่วนหัว `Authorization` มีโทเคน JWT ที่ยังใช้งานได้  
- **404 Not Found** – ตรวจสอบให้แน่ใจว่าสมุดงาน (`name`) และแผ่นงาน (`sheetName`) มีอยู่ใน `folder`/`storageName` ที่ระบุ

{{< /tab >}}

{{< /tabs >}}

**ดูเพิ่มเติม:** [ยกเลิกการจัดกลุ่มแถวในแผ่นงาน Excel](../rows/ungroup/ "ยกเลิกการจัดกลุ่มแถวในแผ่นงาน Excel"), [ซ่อนแถวในแผ่นงาน Excel](../rows/hide/ "ซ่อนแถวในแผ่นงาน Excel"), [ยกเลิกการซ่อนแถวในแผ่นงาน Excel](../rows/unhide/ "ยกเลิกการซ่อนแถวในแผ่นงาน Excel").

## ครอบครัว SDK ของ Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ ให้คุณสามารถมุ่งเน้นไปที่งานโครงการของคุณได้ โปรดดูที่[ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}