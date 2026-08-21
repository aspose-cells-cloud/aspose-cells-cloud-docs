---
title: "ลบคุณสมบัติของเอกสารเฉพาะ"
second_title: "เอกสาร"
linktitle: "ลบ"
type: docs
url: /document-properties/delete/
aliases: [/remove-a-particular-document-property/]
keywords: "Aspose.Cells, ลบคุณสมบัติของเอกสาร, API ข้อมูลเมตา Excel, REST, SDK บนคลาวด์, ตัวอย่าง cURL"
description: "ลบคุณสมบัติของเอกสารเฉพาะออกจากสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API เวอร์ชัน 3.0 พร้อมตัวอย่าง cURL และ SDK สำหรับ C#, Java, Python และอื่นๆ"
weight: 50
---

REST API นี้ใช้ลบคุณสมบัติของเอกสารออกจากสมุดงาน

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | จำเป็น | คำอธิบาย                                  |
| ---------------- | ------ | -------- | ------ | ------------------------------------------- |
| name             | string | path     | ใช่    | ชื่อของสมุดงาน Excel                      |
| propertyName     | string | path     | ใช่    | ชื่อของคุณสมบัติของเอกสารที่ต้องการลบ    |
| folder           | string | query    | ไม่ใช่ | เส้นทางโฟลเดอร์ที่เก็บสมุดงานไว้         |
| storageName      | string | query    | ไม่ใช่ | ชื่อของบริการจัดเก็บข้อมูล                 |

[สเปค OpenAPI](https://apireference.aspose.cloud/cells/#/Properties/DeleteDocumentProperty) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้สาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์โดยใช้ cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
     -X DELETE \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
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

### การตอบกลับข้อผิดพลาด

| HTTP Status | คำอธิบาย                                                             | ตัวอย่าง JSON                                                  |
| ----------- | -------------------------------------------------------------------- | -------------------------------------------------------------- |
| 400         | คำขอไม่ถูกต้อง – ขาดพารามิเตอร์ที่จำเป็นหรือค่าไม่ถูกต้อง          | `{"Code":400,"Message":"Missing required parameter 'name'."}` |
| 401         | ไม่ได้รับอนุญาต – JWT token ไม่ถูกต้องหรือไม่มี                    | `{"Code":401,"Message":"Invalid access token."}`              |
| 404         | ไม่พบ – สมุดงานหรือคุณสมบัติที่ระบุไม่มีอยู่                       | `{"Code":404,"Message":"Document property not found."}`       |
| 500         | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เกิดเหตุการณ์ไม่คาดคิดบนเซิร์ฟเวอร์ | `{"Code":500,"Message":"An unexpected error has occurred."}`  |

## ครอบครัว Cloud SDK

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นไปที่งานของโครงการได้ กรุณาตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}