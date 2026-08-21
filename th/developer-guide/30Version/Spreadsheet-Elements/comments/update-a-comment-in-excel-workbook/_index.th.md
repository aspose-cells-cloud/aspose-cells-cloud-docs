---
title: "อัปเดตความคิดเห็นในเซลล์ของเวิร์กชีต"
type: docs
url: /comments/update/
aliases: [/update-a-comment-in-excel-workbook/]
keywords: "Aspose.Cells Cloud, REST API, Excel, เวิร์กชีต, ความคิดเห็นในเซลล์, อัปเดตความคิดเห็นในเวิร์กชีต, ออบเจกต์ความคิดเห็น"
description: "ใช้ Aspose.Cells Cloud REST API เพื่ออัปเดตความคิดเห็นในเซลล์ของเวิร์กชีตในสมุดงาน Excel รวมถึงรายละเอียดคำขอ โค้ดการตอบกลับ และตัวอย่าง SDK"
weight: 30
ArticleTitle: "อัปเดตความคิดเห็นในเซลล์ของเวิร์กชีต – API ของ Aspose.Cells Cloud"
---

REST API นี้ใช้สำหรับอัปเดตความคิดเห็นในเซลล์ของเวิร์กชีต โดยใช้จุดสิ้นสุดนี้เพื่อ **อัปเดตความคิดเห็นในเวิร์กชีต** ภายในไฟล์ Excel  

**ข้อกำหนดเบื้องต้น:**  
- ต้องแนบโทเค็น OAuth/JWT ที่ถูกต้องไว้ในเฮดเดอร์ `Authorization`  
- สมุดงานต้องถูกจัดเก็บไว้ในตำแหน่งที่จัดเก็บบนคลาวด์ที่รองรับ (ระบุ `folder` และอาจระบุ `storageName` ด้วย)  

## API PostWorksheetComment

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **ความปลอดภัยและการพิสูจน์ตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การพิสูจน์ตัวตนแบบใช้โทเค็น JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย                                                                 |
| ---------------- | -------- | -------- | ------------------------------------------------------------------------ |
| name             | string   | path     | ชื่อของเอกสาร Excel                                                      |
| sheetName        | string   | path     | ชื่อของเวิร์กชีตที่มีเซลล์นั้น                                           |
| cellName         | string   | path     | ที่อยู่ของเซลล์ (เช่น **A1**)                                            |
| comment          | object   | body     | ออบเจกต์ **Comment** ที่กำหนดความคิดเห็นที่จะเพิ่มหรืออัปเดต             |
| folder           | string   | query    | โฟลเดอร์ที่เอกสารถูกจัดเก็บ                                             |
| storageName      | string   | query    | ชื่อของบริการที่จัดเก็บข้อมูล                                           |

<a href="https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetComment" rel="noopener noreferrer">สเปค OpenAPI</a> นิยามอินเทอร์เฟซการโปรแกรมที่สามารถเข้าถึงได้แบบเปิดเผย และอนุญาตให้คุณดำเนินการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ผ่าน cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/a1" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CellName": "a1",
        "Author": "test",
        "HtmlNote": "string",
        "Note": "this is a comment",
        "AutoSize": true,
        "IsVisible": true,
        "Width": 10,
        "Height": 10
      }'
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

รหัสสถานะการตอบกลับที่เป็นไปได้:

| รหัส | คำอธิบาย                                                                 |
|------|--------------------------------------------------------------------------|
| 200  | อัปเดตความคิดเห็นเรียบร้อยแล้ว                                          |
| 400  | คำขอไม่ถูกต้อง – ขาดหรือพารามิเตอร์ไม่ถูกต้อง                           |
| 401  | ไม่ได้รับอนุญาต – การพิสูจน์ตัวตนล้มเหลว                                |
| 404  | ไม่พบ – สมุดงาน เวิร์กชีต หรือความคิดเห็นไม่มีอยู่                      |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์                                               |

**หมายเหตุ / เคล็ดลับ:**  
- ความยาวสูงสุดของความคิดเห็นคือ 1024 ตัวอักษร  
- รองรับตัวอักษร UTF‑8; หลีกเลี่ยงตัวอักษรควบคุม  

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนาด้วย Aspose.Cells Cloud SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่โครงการของคุณได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บ GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetComment.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetComment.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetComment.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetComment.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetComment.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetComment.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetComment.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetComment.go" >}}

{{< /tab >}}

{{< /tabs >}}

การดำเนินการที่เกี่ยวข้อง:  
- [รับความคิดเห็นในเวิร์กชีต](/comments/get/)  
- [เพิ่มความคิดเห็นในเวิร์กชีต](/comments/add/)  
- [ลบความคิดเห็นในเวิร์กชีต](/comments/delete/)