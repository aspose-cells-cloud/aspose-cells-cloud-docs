---
title: "เข้ารหัสสมุดงาน Excel ด้วย Aspose.Cells Cloud API – ตัวอย่าง cURL และ SDK แบบด่วน"
second_title: "เอกสาร"
linktitle: "เข้ารหัสไฟล์ Excel"
type: docs
url: /th/excel-file-encrypt/
aliases: [  /th/encrypt-excel-workbooks/ , /th/workbook/encrypt/ ]
keywords: "Aspose Cells เข้ารหัสสมุดงาน, API เข้ารหัส Excel, REST API, cURL, .NET, Java, Python, PHP, Ruby, Node.js, Go, Perl"
description: "เรียนรู้วิธีการเข้ารหัสสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API (เวอร์ชัน 3.0) มีตัวอย่างคำสั่ง cURL โค้ดตัวอย่าง SDK (C#, Java, Python, …), พารามิเตอร์ที่จำเป็น และการจัดการข้อผิดพลาด"
weight: 20
ArticleTitle: "เข้ารหัสสมุดงาน Excel ด้วย Aspose.Cells Cloud API – ตัวอย่าง cURL และ SDK"
---

REST API นี้จะเข้ารหัส **สมุดงาน** Excel

**ข้อกำหนดเบื้องต้น:** คุณต้องมีโทเค็น JWT ที่ถูกต้อง และอัปโหลดสมุดงานไปยังตำแหน่งที่จัดเก็บไว้แล้วก่อนเรียกใช้เอนพอยต์นี้

## API PostEncryptDocument

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบใช้โทเค็น JWT</a>

### **พารามิเตอร์ Query**

| ชื่อพารามิเตอร์ | ประเภท   | จำเป็น | คำอธิบาย                                      |
| -------------- | ------ | -------- | ------------------------------------- |
| folder         | string | ✗        | เส้นทางโฟลเดอร์ของสมุดงานต้นฉบับ                 |
| storageName    | string | ✗        | ชื่อของพื้นที่จัดเก็บที่ต้องการใช้งาน              |

### **พารามิเตอร์ Request Body**

| ชื่อพารามิเตอร์ | ประเภท                      | จำเป็น | คำอธิบาย                              |
| -------------- | ------------------------- | -------- | ------------------------------------- |
| encryption     | WorkbookEncryptionRequest | ✓        | การตั้งค่าการเข้ารหัสสำหรับสมุดงาน           |

#### **WorkbookEncryptionRequest**

| ชื่อพารามิเตอร์ | ประเภท    | จำเป็น | คำอธิบาย                                                                              |
| -------------- | ------- | -------- | ---------------------------------------------------------------------------------- |
| EncryptionType | string  | ✓        | อัลกอริทึมการเข้ารหัส ดูค่าที่รองรับและคำอธิบายในตารางด้านล่าง                              |
| KeyLength      | integer | ✗        | ความยาวของคีย์การเข้ารหัสเป็นหน่วยบิต (จะถูกละเว้นสำหรับ `XOR` และ `Compatible`) |
| Password       | string  | ✓        | รหัสผ่านที่ใช้ในการเข้ารหัส                                                           |

#### **ค่าของ EncryptionType**

| ค่า                               | คำอธิบาย                                         |
| --------------------------------- | --------------------------------------------- |
| `XOR`                             | อัลกอริทึม XOR แบบง่าย (แบบเก่า มีความปลอดภัยต่ำ)     |
| `Compatible`                      | การเข้ารหัสที่เข้ากันได้กับ Excel 97‑2003 (40‑บิต) |
| `EnhancedCryptographicProviderV1` | AES‑128 พร้อมแฮช SHA‑1                           |
| `StrongCryptographicProvider`     | AES‑256 พร้อมแฮช SHA‑512 (ปลอดภัยที่สุด)             |

### Response

```json
{
  "Status":"OK",
  "Code":200
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | กรองข้อมูลสำเร็จ; response มีรายละเอียดของปฏิบัติการ |
| 400  | Bad Request                 | พารามิเตอร์หายไปหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | Unauthorized                | โทเค็น JWT ไม่ถูกต้องหรือหายไป |
| 413  | Payload Too Large           | ไฟล์ที่อัปโหลดเกินขีดจำกัดขนาด |
| 500  | Internal Server Error       | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์ |
## วิธีใช้ API PostEncryptDocument ร่วมกับ SDK

### ข้อมูลจำเพาะ API PostEncryptDocument

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostEncryptDocument" rel="noopener noreferrer">ข้อมูลจำเพาะ OpenAPI</a> กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้สาธารณะ และช่วยให้คุณดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# เข้ารหัสสมุดงาน "test.xlsx" โดยใช้อัลกอริทึม XOR (คีย์ 128‑บิต) และรหัสผ่าน "mateen"
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 128, "Password": "mateen"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**คำตอบข้อผิดพลาดที่เป็นไปได้**

| สถานะ HTTP | โค้ด                | ข้อความ                                         |
| ----------- | ------------------- | ----------------------------------------------- |
| 400         | BadRequest          | พารามิเตอร์หายไปหรือไม่ถูกต้อง                  |
| 401         | Unauthorized        | โทเค็นการยืนยันตัวตนหายไปหรือไม่ถูกต้อง      |
| 403         | Forbidden           | ไม่มีสิทธิ์เพียงพอในการเข้าถึงพื้นที่จัดเก็บ |
| 500         | InternalServerError | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์                        |

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งกระบวนการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโปรเจกต์ของคุณ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostEncryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostEncryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostEncryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostEncryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostEncryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostEncryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostEncryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostEncryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}