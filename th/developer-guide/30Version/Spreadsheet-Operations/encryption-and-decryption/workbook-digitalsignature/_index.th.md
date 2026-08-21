---
title: "เพิ่มลายเซ็นดิจิทัลลงในสมุดงาน Excel"
ArticleTitle: "เพิ่มลายเซ็นดิจิทัลลงในสมุดงาน Excel – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktitle: "ลายเซ็นดิจิทัล"
type: docs
url: /th/excel-digital-signature/
aliases:
  - /protect/digital-signature/
  - /workbook/digital-signature/
keywords: "Aspose.Cells Cloud, ลายเซ็นดิจิทัล, สมุดงาน Excel, REST API, .pfx, JWT, signature API"
description: "เรียนรู้วิธีเพิ่มลายเซ็นดิจิทัลลงในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API (เวอร์ชัน 4.0) รวมถึง endpoint, พารามิเตอร์, การรับรองความถูกต้อง, โครงสร้างการตอบกลับ, การจัดการข้อผิดพลาด และตัวอย่าง SDK สำหรับหลายภาษา"
weight: 35
---


**ข้อกำหนดเบื้องต้น:**  
ก่อนเรียก endpoint นี้ โปรดตรวจสอบให้แน่ใจว่าคุณมี:

- โทเค็น JWT ที่ใช้งานได้ซึ่งได้มาจากการรับรองความถูกต้องของ Aspose Cloud  
- สมุดงานเป้าหมายที่อัปโหลดไว้ในพื้นที่จัดเก็บของ Aspose Cloud ของคุณแล้ว  
- ไฟล์ลายเซ็นดิจิทัลในรูปแบบ `.pfx` หรือ `.p12` และรหัสผ่านของไฟล์ดังกล่าว

REST API นี้จะเพิ่ม **ลายเซ็นดิจิทัล** ลงในสมุดงาน Excel

## API PostDigitalSignature

```http
POST https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature
```

### **ความปลอดภัยและการรับรองความถูกต้อง**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การรับรองความถูกต้องแบบใช้โทเค็น JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์         | ชนิดข้อมูล | ตำแหน่ง               | คำอธิบาย                                                |
| ------------------------ | --------- | ---------------------- | ------------------------------------------------------- |
| **name**                 | string    | `<code>path</code>`    | ชื่อของสมุดงาน                                         |
| **digitalsignaturefile** | string    | `<code>query</code>`   | เส้นทางไปยังไฟล์ลายเซ็นดิจิทัล (`.pfx` หรือ `.p12`)    |
| **password**             | string    | `<code>query</code>`   | รหัสผ่านของสมุดงาน หากสมุดงานนั้นได้รับการป้องกันไว้   |
| **folder**               | string    | `<code>query</code>`   | โฟลเดอร์ที่สมุดงานถูกจัดเก็บไว้                        |
| **storageName**          | string    | `<code>query</code>`   | ชื่อของบริการจัดเก็บข้อมูลที่จะใช้งาน                  |

*หมายเหตุ: หากชื่อไฟล์มีอักขระพิเศษ ให้เข้ารหัส URL ก่อนนำใส่ในสตริงคำขอ (query string)*

### การจัดการข้อผิดพลาด

| สถานะ HTTP | ความหมาย                                               |
| ----------- | ------------------------------------------------------ |
| 200         | ลงลายเซ็นสำเร็จ                                       |
| 400         | คำขอผิดพลาด – พารามิเตอร์หายไปหรือไม่ถูกต้อง        |
| 401         | ไม่ได้รับอนุญาต – โทเค็น OAuth ไม่ถูกต้องหรือหมดอายุ |
| 403         | ถูกปฏิเสธ – สิทธิ์ไม่เพียงพอหรือถูกปฏิเสธการเข้าถึง   |
| 500         | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – ความล้มเหลวที่ไม่คาดคิด  |

### การตอบกลับข้อผิดพลาดตามสถานะ HTTPS

| สถานะ HTTP | โค้ด                | คำอธิบาย                                                  |
| ----------- | ------------------- | --------------------------------------------------------- |
| 400         | BadRequest          | พารามิเตอร์หายไปหรือไม่ถูกต้อง                          |
| 401         | Unauthorized        | โทเค็นการเข้าถึงไม่ถูกต้องหรือหายไป                     |
| 404         | NotFound            | ไม่พบสมุดงานที่ระบุในโฟลเดอร์หรือพื้นที่จัดเก็บที่กำหนด |
| 500         | InternalServerError | ข้อผิดพลาดภายในเซิร์ฟเวอร์ที่ไม่คาดคิด                  |


## วิธีใช้ API PostDigitalSignature ร่วมกับ SDK

### ข้อมูลจำเพาะ API PostDigitalSignature

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Protection/PostDigitalSignature) นิยามอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้แบบเปิดเผย และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเรียกใช้บริการเว็บของ Aspose.Cells ตัวอย่างต่อไปนี้แสดงคำขอไปยัง API:

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature?digitalsignaturefile=signature.pfx&password=YourPassword" \
  -X POST \
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

**โครงสร้างการตอบกลับ**  
API จะส่งกลับวัตถุ JSON ที่มีฟิลด์ดังต่อไปนี้:

| ฟิลด์        | ชนิดข้อมูล | คำอธิบาย                                             |
| ------------ | --------- | ---------------------------------------------------- |
| `Code`       | int       | โค้ดสถานะแบบ HTTP เพื่อบ่งชี้ผลลัพธ์                 |
| `Status`     | string    | ข้อความสั้นที่บรรยายผลลัพธ์ (เช่น `OK`)              |
| `SignatureId`| string    | ตัวระบุของลายเซ็นดิจิทัลที่ลง (ไม่บังคับ)             |
| `Message`    | string    | ข้อมูลเพิ่มเติมหรือรายละเอียดข้อผิดพลาด (ไม่บังคับ) |

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK จะช่วยให้การบูรณาการง่ายขึ้นและลดโค้ดส่วนที่ซ้ำซ้อน โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostDigitalSignature.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostDigitalSignature.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostDigitalSignature.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostDigitalSignature.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82a2de2e4189bc27ae92abf73c36b4df0" "Example_PostDigitalSignature.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostDigitalSignature.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostDigitalSignature.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostDigitalSignature.go" >}}

{{< /tab >}}

{{< /tabs >}}