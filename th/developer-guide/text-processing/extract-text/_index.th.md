---
title: "Aspose.Cells Cloud Web API – ดึงข้อความ"
second_title: "Aspose.Cells Cloud – โค้ดสั้นออนไลน์"
linktitle: "ดึงข้อความ"
type: docs
url: /th/extract-text/
keywords: "Aspose.Cells Cloud, ดึงข้อความ, Excel API, การดึงข้อความจากเซลล์, REST API"
description: "ดึงสตริงย่อย ตัวเลข หรืออักขระจากเซลล์ในไฟล์ Excel โดยใช้ Aspose.Cells Cloud API รองรับการดึงข้อความก่อน/หลังข้อความที่ระบุ การดึงตามตำแหน่ง และการส่งออกโดยตรงไปยังช่วงใหม่"
weight: 100
ArticleTitle: "เอกสาร Aspose.Cells Cloud Extract Text API"
---

ดึงสตริงย่อย อักขระ หรือตัวเลขจากเซลล์ในสมุดงานไปยังเซลล์อื่น โดยไม่ต้องใช้สูตรที่ซับซ้อน เช่น FIND, MIN, LEFT หรือ RIGHT

## **ExtractText API**

```http
PUT https://api.aspose.cloud/v4.0/cells/content/extract/text
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์แบบ JWT token</a>

```bash
-H "Authorization: Bearer {access_token}"
```

### พารามิเตอร์คำขอของ **extractText** API มีดังนี้

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
|------------------|-----------|----------|------------|
| Spreadsheet | ไฟล์ | FormData | อัปโหลดไฟล์สมุดงาน |
| extractTextType | String | Query | ค่า Enum ระบุโหมดการดึงข้อมูล ค่าที่อนุญาต: `Before`, `After`, `BeforePosition`, `AfterPosition` |
| beforeText | String | Query | ข้อความที่ต้องปรากฏ **ก่อน** สตริงย่อยที่ต้องการดึง ใช้เมื่อ `extractTextType=Before` |
| afterText | String | Query | ข้อความที่ต้องปรากฏ **หลัง** สตริงย่อยที่ต้องการดึง ใช้เมื่อ `extractTextType=After` |
| beforePosition | Integer | Query | จำนวนอักขระที่จะดึงจากด้านซ้ายของเซลล์ ใช้เมื่อ `extractTextType=BeforePosition` |
| afterPosition | Integer | Query | จำนวนอักขระที่จะดึงจากด้านขวาของเซลล์ ใช้เมื่อ `extractTextType=AfterPosition` |
| outPositionRange | String | Query | ช่วงปลายทาง (เช่น `Sheet1!A1`) ที่ข้อความที่ดึงจะถูกเขียนลง |
| worksheet | String | Query | ชื่อแผ่นงานที่มีเซลล์ต้นทาง |
| range | String | Query | เซลล์หรือช่วงต้นทาง (เช่น `A1`) |
| outPath | String | Query _(ไม่บังคับ)_ | เส้นทางโฟลเดอร์ในพื้นที่จัดเก็บที่สมุดงานผลลัพธ์จะถูกบันทึก หากไม่ระบุ ผลลัพธ์จะส่งกลับในเนื้อหา response |
| outStorageName | String | Query | ชื่อพื้นที่จัดเก็บที่จะใช้สำหรับไฟล์ผลลัพธ์ |
| region | String | Query | การตั้งค่าภูมิภาคของสมุดงาน (เช่น `US`, `EU`) |
| password | String | Query | รหัสผ่านสำหรับเปิดสมุดงานที่ได้รับการป้องกัน |

**ตัวอย่างคำสั่ง cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/extract/text?extractTextType=Before&beforeText=Total&outPositionRange=Sheet1!B1&worksheet=Sheet1&range=A1" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Sample.xlsx"
```

### **Response**

เมื่อคำขอสำเร็จ API จะส่งกลับ JSON payload ที่ประกอบด้วยข้อความที่ดึงได้และที่อยู่ของเซลล์ที่ถูกเขียนลง:

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

หากมีการระบุพารามิเตอร์ `outPath` response จะมีเพียงข้อความสถานะเท่านั้น และสมุดงานจะถูกเขียนไปยังตำแหน่งที่ระบุ

**ตัวอย่าง response เมื่อไม่ระบุ `outPath`**

```json
{
  "Code": 200,
  "Status":"OK"
}
```

### รหัสข้อผิดพลาด

- **200 OK** – การดึงข้อมูลเสร็จสมบูรณ์  
- **202 Accepted** – คำขอได้รับการยอมรับเพื่อดำเนินการแบบไม่ đồng步 (asynchronous)  
- **400 Bad Request** – URI ของ Aspose.Cells Cloud API ไม่ถูกต้องหรือพารามิเตอร์ที่จำเป็นขาดหายไป  
- **401 Unauthorized** – access token, client ID หรือ client secret ไม่ถูกต้อง  
- **404 Not Found** – ไม่สามารถเข้าถึงไฟล์สมุดงานที่ระบุ  
- **500 Server Error** – เกิดข้อผิดพลาดที่ไม่คาดคิดขณะประมวลผลสมุดงาน

## OpenAPI Specification

[OpenAPI Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/ExtractText) นิยามอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้สาธารณะ และช่วยให้คุณดำเนินการ REST interactions โดยตรงจากเว็บเบราว์เซอร์

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งพัฒนา SDK จะจัดการรายละเอียดเบื้องต้น ช่วยให้คุณสามารถใช้ฟังก์ชัน **ดึงข้อความ** สำหรับเซลล์ได้ด้วยโค้ดเพียงเล็กน้อย โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{<tab tabNum="1" >}}

```csharp
// ตัวอย่าง C# – ดึงข้อความ (โค้ดถูกลดทอนเพื่อลดความยาว)
```

{{</tab>}}

{{<tab tabNum="2" >}}

```java
// ตัวอย่าง Java – ดึงข้อความ (โค้ดถูกลดทอนเพื่อลดความยาว)
```

{{</tab>}}

{{<tab tabNum="3" >}}

```php
// ตัวอย่าง PHP – ดึงข้อความ (โค้ดถูกลดทอนเพื่อลดความยาว)
```

{{</tab>}}

{{<tab tabNum="4" >}}

```ruby
# ตัวอย่าง Ruby – ดึงข้อความ (โค้ดถูกลดทอนเพื่อลดความยาว)
```

{{</tab>}}

{{<tab tabNum="5" >}}

```javascript
// ตัวอย่าง Node.js – ดึงข้อความ (โค้ดถูกลดทอนเพื่อลดความยาว)
```

{{</tab>}}

{{<tab tabNum="6" >}}

```python
# ตัวอย่าง Python – ดึงข้อความ (โค้ดถูกลดทอนเพื่อลดความยาว)
```

{{</tab>}}

{{<tab tabNum="7" >}}

```perl
# ตัวอย่าง Perl – ดึงข้อความ (โค้ดถูกลดทอนเพื่อลดความยาว)
```

{{</tab>}}

{{<tab tabNum="8" >}}

```go
// ตัวอย่าง Go – ดึงข้อความ (โค้ดถูกลดทอนเพื่อลดความยาว)
```

{{</tab>}}

{{< /tabs >}}