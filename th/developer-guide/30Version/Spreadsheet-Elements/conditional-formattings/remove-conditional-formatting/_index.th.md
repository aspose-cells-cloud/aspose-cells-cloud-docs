---
title: "การลบรูปแบบที่มีเงื่อนไข – เอกสารอ้างอิง API ของ Aspose.Cells Cloud"
type: docs
url: /th/conditional-formattings/delete/
aliases:
  - /remove-conditional-formatting/
keywords: "Aspose.Cells, รูปแบบที่มีเงื่อนไข, การลบ, API, Excel, คลาวด์"
description: "ลบกฎรูปแบบที่มีเงื่อนไขออกจากชีตงานโดยใช้ Aspose.Cells Cloud REST API ประกอบด้วยพารามิเตอร์ การยืนยันตัวตน ตัวอย่างคำขอ/การตอบกลับ และตัวอย่างโค้ด SDK"
weight: 60
---

# การลบรูปแบบที่มีเงื่อนไข

## ข้อมูลพื้นฐาน
รูปแบบที่มีเงื่อนไขช่วยให้คุณสามารถใช้รูปแบบเชิงภาพกับเซลล์ที่ตรงตามเกณฑ์เฉพาะ (เช่น เน้นค่าที่มากกว่าเกณฑ์) ในสถานการณ์อัตโนมัติ คุณอาจจำเป็นต้องลบกฎที่มีอยู่ก่อนหน้านี้ จุดสิ้นสุดนี้จะลบกฎรูปแบบที่มีเงื่อนไขออกจากชีตงานในสมุดงาน Excel ที่จัดเก็บไว้ในพื้นที่จัดเก็บของ Aspose Cloud

## ข้อกำหนดเบื้องต้น
- บัญชี **Aspose Cloud** ที่เปิดใช้งานผลิตภัณฑ์ **Cells**  
- **โทเค็น JWT** ที่สร้างขึ้นผ่านการไหลของข้อมูลรับรองไคลเอนต์ OAuth 2.0  
- สมุดงาน (`{name}`) จะต้องมีอยู่แล้วใน **โฟลเดอร์** และ **พื้นที่จัดเก็บ** ที่ระบุ (หากมี)  
- ใช้เวอร์ชัน API **v3.0** (ค่าเริ่มต้น) ใน URL ที่แสดงด้านล่าง

## การยืนยันตัวตน
จุดสิ้นสุดทั้งหมดของ Aspose.Cells Cloud ต้องใช้การยืนยันตัวตนแบบใช้โทเค็น JWT

```http
Authorization: Bearer <access_token>
```

### รับโทเค็นการเข้าถึง (cURL)

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
  -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>&scope=Cells"
```

**การตอบกลับ**

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

ใช้ `access_token` ที่ได้รับในส่วนหัว `Authorization` สำหรับทุกคำขอ

## คำขอ HTTP

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### พารามิเตอร์เส้นทาง

| ชื่อ      | ชนิดข้อมูล | จำเป็น | คำอธิบาย |
|-----------|--------|----------|-------------|
| `name`    | ข้อความ | ใช่      | ชื่อไฟล์สมุดงาน (เช่น `Book1.xlsx`) |
| `sheetName` | ข้อความ | ใช่   | ชีตงานที่มีรูปแบบที่มีเงื่อนไข |
| `index`   | จำนวนเต็ม| ใช่      | ดัชนีแบบเริ่มต้นที่ 0 ของกฎรูปแบบที่มีเงื่อนไขที่ต้องการลบ |

### พารามิเตอร์คิวรี

| ชื่อ        | ชนิดข้อมูล | จำเป็น | คำอธิบาย |
|-------------|--------|----------|-------------|
| `folder`    | ข้อความ | ไม่จำเป็น | โฟลเดอร์คลาวด์ที่สมุดงานอยู่ |
| `storageName`| ข้อความ| ไม่จำเป็น| ชื่อบริการพื้นที่จัดเก็บของ Aspose Cloud |

## ตัวอย่างคำขอ (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0?folder=MyFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### การตอบกลับที่ประสบความสำเร็จ

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | คำอธิบาย                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                          | ใช้ตัวกรองสำเร็จ; การตอบกลับประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request)                 | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)                | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | ข้อมูลส่งออกมีขนาดใหญ่เกินไป (Payload Too Large)           | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error)       | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์ |
## การตอบกลับข้อผิดพลาด

| รหัส HTTP | เหตุผล | ตัวอย่างเนื้อหา |
|-----------|--------|--------------|
| **400**   | คำขอไม่ถูกต้อง – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401**   | ไม่ได้รับอนุญาต – โทเค็น JWT ขาดหายหรือไม่ถูกต้อง | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | ไม่พบ – สมุดงานหรือชีตงานไม่มีอยู่ | `{ "Code":"404", "Message":"File not found." }` |
| **500**   | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน – การล้มเหลวของเซิร์ฟเวอร์ที่ไม่คาดคิด | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

## ตัวอย่าง SDK
ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้การดำเนินการ **Delete Conditional Formatting** โดยใช้ SDK ทางการของ Aspose.Cells Cloud

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK;
using Aspose.Cells.Cloud.SDK.Requests;

// กำหนดค่าไคลเอนต์ API
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new ConditionalFormattingsApi(config);

// ลบรูปแบบที่มีเงื่อนไข
var request = new DeleteWorksheetConditionalFormattingRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
);
apiInstance.DeleteWorksheetConditionalFormatting(request);
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.*;
import com.aspose.cells.cloud.sdk.model.*;
import com.aspose.cells.cloud.sdk.requests.*;

ApiClient client = new ApiClient();
client.setAppKey("<your_client_id>");
client.setAppSid("<your_client_secret>");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(client);

DeleteWorksheetConditionalFormattingRequest request = new DeleteWorksheetConditionalFormattingRequest(
        "Book1.xlsx",
        "Sheet1",
        0,
        "MyFolder",
        null);

api.deleteWorksheetConditionalFormatting(request);
```

### Node.js

```javascript
const { ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest } = require('asposecellscloud');

const config = {
    clientId: "<your_client_id>",
    clientSecret: "<your_client_secret>"
};

const apiInstance = new ConditionalFormattingsApi(config);

const request = new DeleteWorksheetConditionalFormattingRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
});

apiInstance.deleteWorksheetConditionalFormatting(request)
    .then(() => console.log('Conditional formatting deleted.'))
    .catch(err => console.error(err));
```

### Python

```python
from asposecellscloud import ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest, ApiClient

api_client = ApiClient(client_id="<your_client_id>", client_secret="<your_client_secret>")
api = ConditionalFormattingsApi(api_client)

request = DeleteWorksheetConditionalFormattingRequest(
    name="Book1.xlsx",
    sheetName="Sheet1",
    index=0,
    folder="MyFolder",
    storageName=None
)

api.delete_worksheet_conditional_formatting(request)
print("Conditional formatting removed.")
```

*(ตัวอย่าง SDK เพิ่มเติมสำหรับ Ruby, Go, Perl และ Swift มีอยู่ใน [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud).)*

## ดูเพิ่มเติม
- **คู่มือการยืนยันตัวตน** – [การยืนยันตัวตนแบบใช้โทเค็น JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **สเปค OpenAPI** – โครงสร้างรายละเอียดสำหรับจุดสิ้นสุดนี้ (เปิดในแท็บใหม่)  
  `<a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormatting" target="_blank" rel="noopener noreferrer">สเปค OpenAPI</a>`  
- **ภาพรวมของรูปแบบที่มีเงื่อนไข** – เรียนรู้วิธีการสร้าง แก้ไข และแสดงรายการกฎรูปแบบ  
- **SDK ของ Aspose.Cells Cloud** – รายการภาษาที่รองรับทั้งหมดบน [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud)  

---  

*หน้านี้ใช้แม่แบบเอกสารอ้างอิง API มาตรฐานของ Aspose.Cells Cloud มีส่วนข้อกำหนดเบื้องต้น และปฏิบัติตามแนวทางที่ดีที่สุดสำหรับการเข้าถึงและ SEO*