---
title: "เพิ่มตัวแบ่งหน้าแนวนอน"
second_title: "เอกสาร"
linktype: "เพิ่มตัวแบ่งหน้าแนวนอน"
type: docs
url: /page-breaks/add-horizontal-page-break/
aliases: [/insert-horizontal-page-break-inside-worksheet/]
keywords: "ตัวแบ่งหน้าแนวนอน, Aspose.Cells Cloud, Excel API, REST, SDK, แผ่นงาน, cURL"
description: "เรียนรู้วิธีเพิ่มตัวแบ่งหน้าแนวนอนลงในแผ่นงาน Excel โดยใช้ REST API ของ Aspose.Cells Cloud รวมถึงรายละเอียดคำขอ ตัวอย่าง cURL และโค้ดตัวอย่าง SDK สำหรับภาษาการเขียนโปรแกรมหลายภาษา"
weight: 30
ArticleTitle: "เพิ่มตัวแบ่งหน้าแนวนอน – Aspose.Cells Cloud API"
---

API **เพิ่มตัวแบ่งหน้าแนวนอน** ใช้สำหรับแทรกตัวแบ่งหน้าแนวนอนลงในแผ่นงาน Excel

**ข้อกำหนดเบื้องต้นและการตรวจสอบสิทธิ์**  
จำเป็นต้องมี JWT token ที่ถูกต้องสำหรับการเรียก API ทั้งหมดของ Aspose.Cells Cloud API รับ token ผ่านขั้นตอน OAuth 2.0 ตามที่อธิบายไว้ในคู่มือการตรวจสอบสิทธิ์ และรวม token ไว้ใน header คำขอเป็น `Authorization: Bearer <jwt token>` สมุดงานเป้าหมายต้องอยู่ในตำแหน่งที่จัดเก็บที่ API สามารถเข้าถึงได้ (ค่าเริ่มต้นคือ storage หรือ `storageName` ที่กำหนดเองที่คุณระบุ)

## API PutHorizontalPageBreak

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์ด้วย JWT token</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท    | ตำแหน่ง | คำอธิบาย                                                               |
| -------------- | ------- | -------- | ------------------------------------------------------------------------- |
| name           | string  | path     | ชื่อไฟล์ Excel                                                           |
| sheetName      | string  | path     | ชื่อแผ่นงานที่จะเพิ่มตัวแบ่งหน้า                                           |
| cellname       | string  | query    | อ้างอิงเซลล์ (เช่น **A1**) ที่ระบุจุดเริ่มต้นของตัวแบ่งหน้า                    |
| row            | integer | query    | ดัชนีแถว (เริ่มต้นที่ 0) สำหรับตัวแบ่งหน้า                                   |
| column         | integer | query    | ดัชนีคอลัมน์ (เริ่มต้นที่ 0) สำหรับตัวแบ่งหน้า                               |
| startColumn    | integer | query    | คอลัมน์เริ่มต้นของช่วงเมื่อแทรกตัวแบ่งหน้า                                  |
| endColumn      | integer | query    | คอลัมน์สิ้นสุดของช่วงเมื่อแทรกตัวแบ่งหน้า                                   |
| folder         | string  | query    | ตำแหน่งโฟลเดอร์ที่เก็บไฟล์ Excel                                           |
| storageName    | string  | query    | ชื่อของ storage บน Aspose Cloud                                             |

<a href="https://apireference.aspose.cloud/cells/#/PageBreaks/PutHorizontalPageBreak" target="_blank" rel="noopener noreferrer">สเปค OpenAPI</a> กำหนดอินเทอร์เฟซที่เข้าถึงได้แบบสาธารณะ ซึ่งช่วยให้คุณสามารถใช้งาน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
# ใช้ HTTPS เพื่อให้แน่ใจว่าการสื่อสารมีการเข้ารหัส
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks?row=18" \
  -X PUT \
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

{{< /tab >}}

{{< /tabs >}}

ตัวอย่างการตอบกลับข้อผิดพลาดเมื่อ JWT token ขาดหายหรือไม่ถูกต้อง:

```json
{
  "Code": 401,
  "Status": "Unauthorized",
  "Message": "JWT token ไม่ถูกต้องหรือขาดหาย"
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                          | ประยุกต์ใช้ตัวกรองสำเร็จ; การตอบกลับมีรายละเอียดของคำสั่ง |
| 400  | คำขอไม่ถูกต้อง (Bad Request)                 | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)                | JWT token ไม่ถูกต้องหรือขาดหาย |
| 413  | ข้อมูลส่งออกมีขนาดใหญ่เกินไป (Payload Too Large)           | ไฟล์ที่อัปโหลดเกินขีดจำกัดขนาด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error)       | เกิดข้อผิดพลาดที่ไม่คาดคิดในเซิร์ฟเวอร์ |

สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับการดำเนินการที่เกี่ยวข้อง ดูที่หน้า API สำหรับ **[รับตัวแบ่งหน้าแนวนอน](../get-horizontal-page-breaks/)** และ **[ลบตัวแบ่งหน้าแนวนอน](../delete-horizontal-page-break/)**

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่โครงการของคุณได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">ที่เก็บบน GitHub</a> เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutHorizontalPageBreak.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutHorizontalPageBreak.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutHorizontalPageBreak.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutHorizontalPageBreak.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutHorizontalPageBreak.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutHorizontalPageBreak.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutHorizontalPageBreak.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutHorizontalPageBreak.go" >}}
{{< /tab >}}

{{< /tabs >}}