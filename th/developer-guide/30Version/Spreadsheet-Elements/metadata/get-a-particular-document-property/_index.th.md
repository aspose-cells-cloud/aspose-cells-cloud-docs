---
title: "รับคุณสมบัติของเอกสารเฉพาะ"
second_title: "เอกสาร"
linktitle: "รับ"
type: docs
url: /document-properties/get/
aliases: [/get-a-particular-document-property/]
keywords: "Aspose.Cells, Cloud API, รับคุณสมบัติของเอกสาร, metadata ของ Excel, REST GET, ตัวอย่าง SDK"
description: "ดึงคุณสมบัติของเอกสารที่มีชื่อ (เช่น Author, Title) จากไฟล์ Excel โดยใช้ Aspose.Cells Cloud REST API รวมถึงตัวอย่าง cURL, ตัวอย่างโค้ด SDK และโครงสร้างการตอบกลับ"
weight: 20
---

API นี้ REST จะอ่านคุณสมบัติของเอกสารตามชื่อ

## API บนเว็บ (REST API)

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย                                   |
| ---------------- | ------ | -------- | ------------------------------------------ |
| name             | string | path     | ชื่อของไฟล์ Excel                          |
| propertyName     | string | path     | ชื่อของคุณสมบัติของเอกสารที่ต้องการรับค่า |
| folder           | string | query    | โฟลเดอร์ที่เก็บไฟล์ (ไม่บังคับ)           |
| storageName      | string | query    | ชื่อของพื้นที่จัดเก็บ (ไม่บังคับ)         |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Properties/GetDocumentProperty) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถเรียกใช้การโต้ตอบ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้ **เครื่องมือ cURL ผ่านบรรทัดคำสั่ง** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "DocumentProperty": {
    "Name": "Author",
    "Value": "",
    "BuiltIn": "True",
    "link": {
      "Href": "/test.xlsx/documentproperties/Author",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### รายละเอียดการตอบกลับ

วัตถุ JSON ที่ API ส่งกลับมามีฟิลด์ต่อไปนี้:

| ฟิลด์                           | ประเภท  | คำอธิบาย                                                 |
| ------------------------------- | ------- | --------------------------------------------------------- |
| **DocumentProperty.Name**       | string  | ชื่อของคุณสมบัติ (เช่น `Author`)                         |
| **DocumentProperty.Value**      | string  | ค่าของคุณสมบัติ อาจว่างเปล่าหากยังไม่ได้ตั้งค่า           |
| **DocumentProperty.BuiltIn**    | boolean | แสดงสถานะว่าคุณสมบัตินี้เป็นคุณสมบัติในตัวของ Excel หรือไม่ |
| **DocumentProperty.link.Href**  | string  | URL สัมพัทธ์ไปยังทรัพยากรของคุณสมบัติ                    |
| **DocumentProperty.link.Rel**   | string  | ประเภทความสัมพันธ์ มักจะเป็น `self`                      |
| **DocumentProperty.link.Title** | string  | ชื่อที่อ่านเข้าใจได้ (อาจเป็น `null`)                    |
| **DocumentProperty.link.Type**  | string  | ชนิด MIME ของทรัพยากรที่เชื่อมโยง (อาจเป็น `null`)        |
| **Code**                        | integer | รหัสสถานะ HTTP ที่บริการส่งกลับมา                        |
| **Status**                      | string  | คำอธิบายสถานะในรูปแบบข้อความ (เช่น `OK`)                |

### การตอบกลับข้อผิดพลาด

| สถานะ HTTP | รหัส                   | คำอธิบาย                                      |
| ----------- | ---------------------- | --------------------------------------------- |
| 400         | `InvalidParameter`     | พารามิเตอร์คำขอลหนึ่งตัวขึ้นไปไม่ถูกต้อง     |
| 401         | `AuthenticationFailed` | ไม่มีหรือโทเค็น JWT ไม่ถูกต้อง                |
| 404         | `PropertyNotFound`     | คุณสมบัติของเอกสารที่ระบุไม่มีอยู่จริง       |
| 500         | `InternalError`        | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์     |

รูปแบบเนื้อหาของข้อผิดพลาดทั่วไปมีลักษณะดังนี้:

```json
{
  "Code": 404,
  "Status": "Property not found"
}
```

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งกระบวนการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานของโครงการได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}

### คำศัพท์

| คำศัพท์               | นิยาม                                                                 |
| --------------------- | --------------------------------------------------------------------- |
| **Document Property** | ข้อมูลเมตาที่เกี่ยวข้องกับสมุดงาน Excel (เช่น Author, Title, Created) |
| **Metadata**          | คำทั่วไปสำหรับข้อมูลที่อธิบายข้อมูลอื่นๆ ในบริบทนี้หมายถึงคุณสมบัติของเอกสาร |
| **Custom Property**   | คุณสมบัติที่ผู้ใช้กำหนดเอง ซึ่งไม่อยู่ในชุดคุณสมบัติในตัวของระบบ     |

### คำถามที่พบบ่อย

**Q:** _ฉันจะรับคุณสมบัติ Author ของไฟล์ Excel ที่จัดเก็บไว้ใน Aspose Cloud ได้อย่างไร?_  
**A:** ส่งคำขอ GET ไปยัง `https://api.aspose.cloud/v3.0/cells/{fileName}/documentproperties/author` โดยใช้โทเค็น Bearer ที่ถูกต้อง ซึ่งจะได้รับ JSON ในการตอบกลับที่มี `DocumentProperty.Name = "Author"` และ `Value` ของมัน

**Q:** _ข้อผิดพลาดอะไรจะเกิดขึ้นหากคุณสมบัติที่ร้องขอไม่มีอยู่จริง?_  
**A:** API จะส่งกลับ HTTP 404 พร้อมเนื้อหา JSON ที่มี `Code: 404` และ `Status: "Property not found"`

**Q:** _ฉันจำเป็นต้องระบุ `storageName` เมื่อไฟล์อยู่ในพื้นที่จัดเก็บเริ่มต้นหรือไม่?_  
**A:** ไม่จำเป็น พารามิเตอร์คิวรี `storageName` เป็นตัวเลือก คุณสามารถละเว้นเพื่อใช้พื้นที่จัดเก็บเริ่มต้นที่กำหนดไว้สำหรับบัญชีของคุณ