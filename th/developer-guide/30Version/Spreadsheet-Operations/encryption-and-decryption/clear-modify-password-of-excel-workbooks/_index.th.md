---
title: "การลบการป้องกันการเขียน (รหัสผ่าน) จากสมุดงาน Excel"
second_title: "เอกสาร"
linktype: "ล้างรหัสผ่านไฟล์ Excel"
type: docs
url: /clear-excel-files-password/
aliases:
  [
    "/clear-modify-password-of-excel-workbooks/",
    "/workbook/clear-modify-password/",
    "/workbook/password/clear/",
  ]
keywords: "Aspose.Cells, Excel, การลบรหัสผ่าน, การป้องกันการเขียน, REST API, ตัวอย่าง SDK"
description: "เรียนรู้วิธีการลบการป้องกันการเขียน (รหัสผ่าน) จากสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API ซึ่งรวมถึงตัวอย่าง cURL ขั้นตอนการตรวจสอบสิทธิ์ และตัวอย่างโค้ด SDK"
weight: 110
ArticleTitle: "การลบการป้องกันการเขียน (รหัสผ่าน) จากสมุดงาน Excel"
---

REST API นี้จะลบ **การป้องกันการเขียน (รหัสผ่าน)** จากสมุดงาน Excel ทำให้คุณสามารถ **ลบการป้องกันรหัสผ่านของ Excel** ได้อย่างเป็นโปรแกรม

**ข้อกำหนดเบื้องต้น:** รับ JWT token ที่ถูกต้อง ตรวจสอบให้แน่ใจว่าสมุดงานถูกเก็บไว้ในตำแหน่งที่จัดเก็บที่รองรับ และใช้เวอร์ชัน API v3.0

สำหรับการเพิ่มการป้องกัน โปรดดูคู่มือ [การป้องกัน Excel](/cells/protect/)

## API DeleteDocumentUnprotectFromChanges

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/writeProtection
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์แบบ JWT token</a>

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย                                     |
| ---------------- | ------ | -------- | --------------------------------------------- |
| `name`           | string | path     | ชื่อของสมุดงาน Excel                         |
| `folder`         | string | query    | โฟลเดอร์ที่เก็บสมุดงาน (ไม่บังคับ)           |
| `storageName`    | string | query    | ชื่อของบริการจัดเก็บข้อมูล (ไม่บังคับ)        |

### การตอบกลับ

```json
{
  "Status":"OK",
  "Code":200
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                      | คำอธิบาย                                             |
| ---- | ------------------------------ | ----------------------------------------------------- |
| 200  | OK                             | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | Bad Request                    | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | Unauthorized                   | JWT token ไม่ถูกต้องหรือขาดหาย                        |
| 413  | Payload Too Large              | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                    |
| 500  | Internal Server Error          | เกิดข้อผิดพลาดภายในเซิร์ฟเวอร์อย่างไม่คาดคิด         |

## วิธีใช้ API DeleteDocumentUnprotectFromChanges ร่วมกับ SDK

### ข้อมูลเฉพาะของ API DeleteDocumentUnprotectFromChanges

[ข้อมูลเฉพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDocumentUnprotectFromChanges) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้สาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่ง command-line เพื่อเข้าถึงบริการ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API REST โดยใช้ cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xlsx/writeProtection" \
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


### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานโปรเจกต์ของคุณได้ โปรดตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ที่สมบูรณ์

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentUnprotectFromChanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentUnprotectFromChanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentUnprotectFromChanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentUnprotectFromChanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentUnprotectFromChanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentUnprotectFromChanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentUnprotectFromChanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentUnprotectFromChanges.go" >}}

{{< /tab >}}

{{< /tabs >}}