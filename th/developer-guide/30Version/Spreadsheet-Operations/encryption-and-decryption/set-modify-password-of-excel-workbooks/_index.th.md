---
title: "การแก้ไขการป้องกันด้วยรหัสผ่านของสมุดงาน Excel"
second_title: "เอกสาร"
linktype: "แก้ไขรหัสผ่านของไฟล์ Excel"
type: docs
url: /th/workbook/password/modify/
aliases:
  - /set-modify-password-of-excel-workbooks/
  - /workbook/modify-password/
keywords: "รหัสผ่าน Excel, Aspose.Cells Cloud, การป้องกันการเขียน, REST API, แก้ไขรหัสผ่านสมุดงาน"
description: "เปลี่ยนรหัสผ่านการป้องกันการเขียนของสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API (v3.0) รวมตัวอย่าง cURL และ SDK"
weight: 100
ArticleTitle: "การแก้ไขการป้องกันด้วยรหัสผ่านของสมุดงาน Excel – Aspose.Cells Cloud"
---

REST API นี้ **เปลี่ยนรหัสผ่านการป้องกันการเขียน** ของสมุดงาน Excel ที่มีอยู่

การอัปเดตรหัสผ่านการป้องกันการเขียนด้วยโปรแกรมช่วยให้คุณเปลี่ยนหรือแทนที่รหัสผ่านได้โดยไม่จำเป็นต้องดาวน์โหลดไฟล์ ซึ่งมีประโยชน์มากเมื่อจัดการสมุดงานที่ได้รับการป้องกันที่เก็บไว้ในพื้นที่จัดเก็บของ Aspose.Cells Cloud


## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/writeProtection
```

### ความปลอดภัยและการยืนยันตัวตน

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ [การยืนยันตัวตนด้วยโทเค็น JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)


### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                      |
| ---------------- | -------- | ------- | --------------------------------------------- |
| **name**         | string   | path    | ชื่อของสมุดงาน Excel (จำเป็น)                  |
| **password**     | string   | body (JSON) | รหัสผ่านการป้องกันการเขียนใหม่ที่ต้องการตั้งค่า (จำเป็น) |
| **folder**       | string   | query   | โฟลเดอร์ที่สมุดงานถูกจัดเก็บ (ไม่บังคับ)        |
| **storageName**  | string   | query   | ชื่อของบริการจัดเก็บข้อมูล (ไม่บังคับ)          |

### การตอบกลับ

```json
{
  "Status":"OK",
  "Code":200
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | คำอธิบาย                                      |
|-----|-----------------------------|---------------------------------------------|
| 200 | OK                          | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400 | Bad Request                 | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401 | Unauthorized                | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย               |
| 413 | Payload Too Large           | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด              |
| 500 | Internal Server Error       | ข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด           |

## วิธีใช้ PutDocumentProtectFromChanges API ด้วย SDK

### ข้อมูลเฉพาะของ PutDocumentProtectFromChanges API

[ข้อมูลเฉพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutDocumentProtectFromChanges) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบเปิดเผย ซึ่งช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย คำสั่ง cURL ด้านล่างแสดงวิธีเรียกใช้ Cloud API

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/writeProtection?folder=Samples&storageName=Default" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{ "Password": "aspose" }'
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

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นที่ตรรกะทางธุรกิจของคุณได้ โปรดตรวจสอบ [ kho คลังบน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutDocumentProtectFromChanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutDocumentProtectFromChanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutDocumentProtectFromChanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutDocumentProtectFromChanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutDocumentProtectFromChanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutDocumentProtectFromChanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutDocumentProtectFromChanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutDocumentProtectFromChanges.go" >}}

{{< /tab >}}

{{< /tabs >}}