---
title: "ลบรูปร่างทั้งหมดในแผ่นงาน Excel"
ArticleTitle: "ลบรูปร่างทั้งหมดในแผ่นงาน Excel – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktype: "ชัดเจน"
type: docs
url: /th/shapes/clear/
aliases: [  /th/delete-all-shapes-inside-the-worksheet/ ]
keywords: "Aspose.Cells Cloud, ลบรูปร่างทั้งหมด, แผ่นงาน Excel, REST API, SDK, cURL, .NET, Java, PHP, Ruby, Node.js, Python, Perl, Go, Android, Swift"
description: "ลบรูปร่างทั้งหมดจากแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API การดำเนินการนี้สามารถเข้าถึงได้ผ่าน cURL และ SDK ที่ครอบคลุมหลากหลายภาษา (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Android, Swift)"
weight: 40
---

API นี้จะลบชุดรูปร่างทั้งหมดออกจากแผ่นงาน Excel

**ข้อกำหนดเบื้องต้น:** จำเป็นต้องมี JWT access token ที่ถูกต้อง รับ token นี้ผ่านกระบวนการ OAuth2 ของ Aspose Cloud และใส่ไว้ใน header `Authorization` ดังตัวอย่างด้านล่าง

## API DeleteWorksheetShapes

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้การตรวจสอบสิทธิ์แบบ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer"> JWT token</a>

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย                                    |
| ---------------- | -------- | -------- | -------------------------------------------- |
| name             | string   | path     | ชื่อของเอกสาร Excel                         |
| sheetName        | string   | path     | ชื่อของแผ่นงาน                              |
| folder           | string   | query    | โฟลเดอร์ที่เก็บเอกสารไว้                   |
| storageName      | string   | query    | ชื่อที่จัดเก็บข้อมูลที่เอกสารนั้นอยู่       |

<a href="https://apireference.aspose.cloud/cells/#/Shapes/DeleteWorksheetShapes" rel="noopener noreferrer">OpenAPI Specification</a> กำหนด API แบบ-public ที่สามารถเข้าถึงได้ และช่วยให้คุณสามารถสื่อสารผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่าน command-line เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ผ่าน cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes" \
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

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว Cloud SDK

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ ให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ผ่าน SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetShapes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetShapes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetShapes.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetShapes.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetShapes.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetShapes.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetShapes.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetShapes.go" >}}

{{< /tab >}}

{{< /tabs >}}