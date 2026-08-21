---
title: "คำนวณสูตรในแผ่นงาน Excel"
second_title: "เอกสาร"
linktype: "คำนวณ"
type: docs
url: /worksheets/calculate-formula/
aliases: [/calculate-formula-in-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, การคำนวณสูตร, REST API, SDKs, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift"
description: "คำนวณสูตรในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API รองรับ SDK หลายภาษา (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift) พร้อมตัวอย่างที่ใช้งานได้ทันที"
weight: 20
ArticleTitle: "คำนวณสูตรในแผ่นงาน Excel – เอกสารประกอบ Aspose.Cells Cloud"
---

REST API นี้ส่งค่า **ผลลัพธ์ที่คำนวณแล้วของสูตร** ในแผ่นงานกลับมา สามารถใช้ **ประเมินสูตร Excel** โดยตรงจากแอปพลิเคชันของคุณได้

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/formulaResult
```

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย                                           |
| ---------------- | -------- | -------- | -------------------------------------------------- |
| name             | string   | path     | ชื่อไฟล์ Excel                                     |
| sheetName        | string   | path     | ชื่อแผ่นงานที่มีสูตร                               |
| formula          | string   | query    | สูตรที่ต้องการประเมิน (เช่น `SUM(A5:A10)`)         |
| folder           | string   | query    | โฟลเดอร์ที่จัดเก็บเอกสารไว้                        |
| storageName      | string   | query    | ชื่อบริการจัดเก็บข้อมูล (ถ้ามี)                    |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetCalculateFormula) นิยามอินเทอร์เฟซการโปรแกรมที่เข้าถึงได้แบบสาธารณะ และอนุญาตให้คุณดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

### การยืนยันตัวตน

คำขอทั้งหมดต้องมี **Bearer JWT token** ที่ถูกต้องในส่วนหัว `Authorization`:

```
Authorization: Bearer <your_jwt_token>
```

คุณสามารถรับโทเค็นได้โดยทำตามขั้นตอน OAuth 2.0 ตามที่อธิบายไว้ในคู่มือการยืนยันตัวตนของ Aspose.Cells Cloud

### โค้ดสถานะของคำตอบที่เป็นไปได้

| โค้ด | คำอธิบาย                                               |
|-----|--------------------------------------------------------|
| 200 | คำขอสำเร็จ; ค่าสูตรจะถูกส่งกลับมา                     |
| 400 | คำขอไม่ถูกต้อง – พารามิเตอร์หายไปหรือไม่ถูกต้อง     |
| 401 | ไม่ได้รับอนุญาต – โทเค็น JWT ไม่ถูกต้องหรือหายไป     |
| 404 | ไม่พบ – ไฟล์หรือแผ่นงานที่ระบุไม่มีอยู่จริง          |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เงื่อนไขที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเรียกใช้บริการเว็บของ Aspose.Cells Cloud ได้อย่างง่ายดาย ตัวอย่างด้านล่างแสดงวิธีการร้องขอผลลัพธ์สูตรด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="คำตอบ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet2/formulaResult?formula=SUM(A5:A10)" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Value": {
    "Value": "0"
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการผสานรวม API SDK จะจัดการรายละเอียดระดับล่างให้คุณสามารถมุ่งเน้นที่ตรรกะทางธุรกิจของคุณ ดู [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "d1a2b3c4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a1b2c3d4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "b1c2d3e4f5g67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "c1d2e3f4g5h67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "d1e2f3g4h5i67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e1f2g3h4i5j67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f1g2h3i4j5k67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "g1h2i3j4k5l67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

**ดูเพิ่มเติม:**  
- [ดึงข้อมูลแผ่นงาน](https://docs.aspose.cloud/cells/worksheets/get-worksheet/)  
- [อัปเดตแผ่นงาน](https://docs.aspose.cloud/cells/worksheets/update-worksheet/)  
- [คำนวณสูตรทั้งหมด](https://docs.aspose.cloud/cells/worksheets/calculate-all-formulas/)  
---