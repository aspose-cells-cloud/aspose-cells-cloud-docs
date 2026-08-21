---
title: "รับข้อมูลเมตาดาต้าจากไฟล์ Excel"
second_title: "เอกสาร"
linktitle: "รับข้อมูลโดยไม่ต้องใช้พื้นที่จัดเก็บข้อมูล"
type: docs
url: /metadata/get/
keywords: "Aspose.Cells, Excel, metadata, REST API, cloud SDK"
description: "ดึงข้อมูลเมตาดาต้าแบบติดตั้งมาหรือแบบกำหนดเองจากสมุดงาน Excel โดยใช้ REST API ของ Aspose.Cells Cloud ประกอบด้วยรูปแบบคำร้องขอ พารามิเตอร์ ตัวอย่างโค้ด SDK และการจัดการข้อผิดพลาด"
weight: 23
ArticleTitle: "รับข้อมูลเมตาดาต้าจากไฟล์ Excel - Aspose.Cells Cloud API"
---

REST API นี้ใช้ดึง **ข้อมูลเมตาดาต้า** จากไฟล์ Excel หนึ่งไฟล์หรือหลายไฟล์  
คำร้องขอต้องระบุส่วนหัว `Authorization: Bearer <access_token>` ซึ่งได้รับจากโหมดการรับรองความถูกต้อง OAuth 2.0 ด้วย client-credentials flow

**ข้อกำหนดเบื้องต้น**: คุณต้องมี access token ที่ถูกต้องก่อนเรียก endpoint นี้ โดยรับมาจาก endpoint ออก token OAuth 2.0 ของ Aspose Cloud ตัวอย่างคำร้องขอ curl เพื่อรับ token:

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>"
```

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/metadata/get
```

### พารามิเตอร์ Query

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย                                                                 |
| ---------------- | ---------- | ------------------------------------------------------------------------ |
| type             | string     | `ALL` / `BuiltIn` / `Custom` – ระบุกลุ่มข้อมูลเมตาดาต้าที่ต้องการส่งคืน |

### พารามิเตอร์ Request Body

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย                                                               |
| ---------------- | ---------- | ---------------------------------------------------------------------- |
| ไฟล์ Excel       | data file  | ไฟล์ Excel ที่ส่งมาเป็นส่วนแรกของคำร้องขอแบบ multipart               |

### การตอบกลับ

```json
[
  {
    "Name": "Author",
    "Value": "John Doe",
    "BuiltIn": true,
    "IsReadOnly": false
  },
  {
    "Name": "CustomProp1",
    "Value": "Custom Value",
    "BuiltIn": false,
    "IsReadOnly": false
  }
]
```

| โค้ด | ความหมาย                 | เกิดขึ้นเมื่อ                                  |
|------|---------------------------|-----------------------------------------------|
| 200  | สำเร็จ                   | ส่งคืนข้อมูลเมตาดาต้าแล้ว                     |
| 400  | คำร้องขอไม่ถูกต้อง       | ขาดไฟล์หรือ query ไม่ถูกต้อง                 |
| 401  | ไม่ได้รับอนุญาต           | token ไม่ถูกต้องหรือขาดหายไป                 |
| 404  | ไม่พบ                     | ไม่พบไฟล์ที่ระบุ                              |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ | เซิร์ฟเวอร์ล้มเหลวโดยไม่คาดคิด               |

API นี้จะส่งกลับค่าสถานะ HTTP มาตรฐานเหล่านี้ พร้อมกับ JSON object ของข้อผิดพลาดเมื่อจำเป็น

### ครอบครัว SDK สำหรับ Cloud

การใช้ SDK จะเร่งความเร็วการพัฒนาได้ เนื่องจากจัดการรายละเอียดระดับต่ำให้ ดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud ได้ที่ [repository บน GitHub](https://github.com/aspose-cells-cloud)

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกบริการเว็บ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}