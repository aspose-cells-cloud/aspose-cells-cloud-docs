---
title: "ถอดรหัสสมุดงาน Excel"
second_title: "เอกสาร"
linktype: "ถอดรหัสไฟล์ Excel"
type: docs
url: /excel-file-decrypt/
aliases: [/decrypt-excel-workbooks/, /workbook/decrypt/]
keywords: "Aspose.Cells, การถอดรหัส Excel, REST API, SDK บนคลาวด์"
description: "เรียนรู้วิธีถอดรหัสสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API ซึ่งประกอบด้วยพารามิเตอร์ที่จำเป็น ตัวอย่าง cURL ตัวอย่างโค้ด SDK และรายละเอียดการจัดการข้อผิดพลาด"
ArticleTitle: "วิธีถอดรหัสสมุดงาน Excel โดยใช้ Aspose.Cells Cloud API"
weight: 50
---

**ข้อกำหนดเบื้องต้น**

- โทเค็น JWT ที่ใช้งานได้
- สมุดงานต้องถูกอัปโหลดลงในพื้นที่จัดเก็บของ Aspose Cloud และต้องระบุเส้นทางในพารามิเตอร์คิวรี `folder`

## API DeleteDecryptWorkbook

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้การตรวจสอบสิทธิ์แบบใช้โทเค็น JWT ซึ่งอธิบายรายละเอียดเพิ่มเติมได้ที่ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์คำขอ REST API</a>

### พารามิเตอร์คิวรี

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย |
| -------------- | ------ | ----------------------------------------------- |
| folder         | string | เส้นทางโฟลเดอร์ของสมุดงานต้นฉบับ |
| storageName    | string | ชื่อพื้นที่จัดเก็บที่สมุดงานนั้นอยู่ |

### พารามิเตอร์เนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ประเภท                      | คำอธิบาย |
| -------------- | ------------------------- | -------------------------------------------- |
| encryption     | WorkbookEncryptionRequest | การตั้งค่าการเข้ารหัสที่จำเป็นสำหรับการถอดรหัส |

### WorkbookEncryptionRequest

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย |
| -------------- | ------- | ------------------------------------------------------------------------------------------------------------- |
| EncryptionType | string  | อัลกอริทึมการเข้ารหัส (`XOR`, `Compatible`, `EnhancedCryptographicProviderV1`, `StrongCryptographicProvider`) |
| KeyLength      | integer | ความยาวของคีย์การเข้ารหัสเป็นบิต |
| Password       | string  | รหัสผ่านที่ใช้ในการถอดรหัส |

### การตอบกลับ

```json
{
  "Status":"OK",
  "Code":200
}
```

**ตัวอย่างการตอบกลับข้อผิดพลาด**

```json
{
  "Code": "400",
  "Message": "พารามิเตอร์คำขอไม่ถูกต้อง"
}
```

```json
{
  "Code": "401",
  "Message": "การตรวจสอบสิทธิ์ล้มเหลว โทเค็น JWT ไม่ถูกต้องหรือไม่มี"
}
```

```json
{
  "Code": "413",
  "Message": "ข้อมูลที่ส่งมามีขนาดใหญ่เกินไป ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่อนุญาต"
}
```

```json
{
  "Code": "500",
  "Message": "ข้อผิดพลาดภายในเซิร์ฟเวอร์ โปรดลองอีกครั้งภายหลัง"
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                 | กรองข้อมูลสำเร็จ; การตอบกลับมีรายละเอียดของ оперATION |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็น JWT ไม่ถูกต้องหรือไม่มี |
| 413  | ข้อมูลที่ส่งมามีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดภายในเซิร์ฟเวอร์ |

## วิธีใช้ API DeleteDecryptWorkbook ด้วย SDK

### ข้อกำหนด API DeleteDecryptWorkbook

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDecryptWorkbook) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถเรียกใช้การโต้ตอบ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้ **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 1280, "Password": "aspose"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [repository บน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDecryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDecryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDecryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDecryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDecryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDecryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDecryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDecryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}