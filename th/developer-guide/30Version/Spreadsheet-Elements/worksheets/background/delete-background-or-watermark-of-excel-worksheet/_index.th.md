---
title: "ลบพื้นหลังของแผ่นงานใน Excel"
second_title: "เอกสาร"
linktitle: "ลบ"
type: docs
url: /th/worksheets/background/delete/
aliases: [  /th/delete-background-or-watermark-of-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, ลบพื้นหลังของแผ่นงาน, Excel, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "ใช้ Aspose.Cells Cloud REST API เพื่อลบภาพพื้นหลังของแผ่นงาน Excel SDK มีให้ใช้งานสำหรับ C#, Java, PHP, Ruby, Node.js, Python, Perl และ Go"
weight: 210
ArticleTitle: "ลบพื้นหลังของแผ่นงานใน Excel โดยใช้ Aspose.Cells Cloud API"
---

API นี้จะลบภาพพื้นหลังของแผ่นงาน

**ข้อกำหนดเบื้องต้น:** คุณต้องมีสมุดงานที่จัดเก็บไว้ในพื้นที่จัดเก็บของ Aspose Cloud และมีโทเค็น JWT ที่ถูกต้องสำหรับการยืนยันตัวตน

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/background
```

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย                                          |
| ---------------- | -------- | -------- | ------------------------------------------------- |
| name             | string   | path     | ชื่อไฟล์ Excel                                     |
| sheetName        | string   | path     | ชื่อแผ่นงานที่ต้องการลบพื้นหลัง                   |
| folder           | string   | query    | โฟลเดอร์ในพื้นที่จัดเก็บที่ไฟล์ตั้งอยู่            |
| storageName      | string   | query    | ชื่อพื้นที่จัดเก็บ (ถ้าไม่ใช่พื้นที่จัดเก็บเริ่มต้น) |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetBackground) นิยามอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย การเรียกทั้งหมดจะต้องมีโทเค็น JWT ที่ถูกต้อง รับโทเค็นผ่านจุดสิ้นสุด OAuth2 token endpoint ตามที่อธิบายไว้ในคู่มือการยืนยันตัวตน

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/WorkSheetBackground_Sample_Test_Book.xls/worksheets/Sheet1/background" \
  -X DELETE \
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

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                   | คำอธิบาย                                               |
| ---- | --------------------------- | ------------------------------------------------------ |
| 200  | สำเร็จ (OK)                | ตัวกรองถูกใช้งานเรียบร้อยแล้ว; คำตอบกลับมีรายละเอียดของ операции |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                           |
| 413  | ข้อมูลส่งไปขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                         |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดในเซิร์ฟเวอร์                   |

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งกระบวนการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ และให้คุณโฟกัสไปที่งานของโปรเจกต์ของคุณ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}