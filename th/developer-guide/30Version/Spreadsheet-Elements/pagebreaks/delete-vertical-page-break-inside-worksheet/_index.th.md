---
title: ลบตัวแบ่งหน้าแนวตั้ง – Aspose.Cells Cloud REST API
description: ลบตัวแบ่งหน้าแนวตั้งออกจากWorksheets ในไฟล์ Excel โดยใช้ Aspose.Cells Cloud REST API (v3.0) รวมถึงไวยากรณ์คำขอ พารามิเตอร์ ตัวอย่าง โค้ดการตอบกลับ และตัวอย่างโค้ด SDK
keywords: ลบตัวแบ่งหน้าแนวตั้ง, Aspose.Cells Cloud, REST API
slug: delete-vertical-page-break
api_version: v3.0
---

# ลบตัวแบ่งหน้าแนวตั้ง

ลบตัวแบ่งหน้าแนวตั้งออกจากWorksheets ในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API

---

## สิ่งที่ต้องมีก่อนใช้งาน

* ต้องระบุ **โทเค็นการตรวจสอบสิทธิ์ JWT** ในส่วนหัว `Authorization`  
* สมุดงาน (`{name}`) ต้องถูกจัดเก็บไว้ใน **โฟลเดอร์** หรือ **พื้นที่จัดเก็บ** ที่ระบุ และสามารถเข้าถึงได้โดยไคลเอนต์ API

---

## คำขอ HTTP

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks/{index}
```

| พารามิเตอร์ | ประเภท | ตำแหน่ง | จำเป็น | คำอธิบาย |
|-------------|--------|----------|--------|-----------|
| **name**      | สตริง | เส้นทาง | ใช่ | ชื่อของไฟล์ Excel |
| **sheetName** | สตริง | เส้นทาง | ใช่ | ชื่อของWorksheets ที่มีตัวแบ่งหน้า |
| **index**     | จำนวนเต็ม| เส้นทาง | ใช่ | ดัชนีแบบเริ่มต้นที่ 0 ของตัวแบ่งหน้าแนวตั้งที่ต้องการลบ |
| **folder**    | สตริง | คิวรี | ไม่บังคับ | เส้นทางของโฟลเดอร์ที่เก็บไฟล์ไว้ |
| **storageName**| สตริง| คิวรี | ไม่บังคับ | ชื่อของบริการพื้นที่จัดเก็บ |

---

## ตัวอย่างคำขอ

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/verticalpagebreaks/0?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

---

## การตอบกลับเมื่อสำเร็จ

| โค้ด | คำอธิบาย |
|------|-----------|
| **200** | ตัวแบ่งหน้าแนวตั้งถูกลบเรียบร้อยแล้ว |

**ตัวอย่างข้อมูลตอบกลับ**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

## การตอบกลับเมื่อเกิดข้อผิดพลาด

| โค้ด HTTP | คำอธิบาย |
|-----------|-----------|
| **401** | ไม่ได้รับอนุญาต – โทเค็นขาดหายหรือไม่ถูกต้อง |
| **404** | ไม่พบ – ไฟล์, Worksheets หรือดัชนีของตัวแบ่งหน้าที่ระบุไม่มีอยู่จริง |
| **400** | คำขอไม่ถูกต้อง – ไวยากรณ์ของคำขอหรือพารามิเตอร์ไม่ถูกต้อง |
| **500** | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เกิดสิ่งผิดปกติที่ไม่คาดคิดขึ้น |

**ตัวอย่างข้อมูลตอบกลับข้อผิดพลาด**

*401 – ไม่ได้รับอนุญาต*

```json
{
  "Code": 401,
  "Message": "โทเค็นการตรวจสอบสิทธิ์ไม่ถูกต้อง"
}
```

*404 – ไม่พบ*

```json
{
  "Code": 404,
  "Message": "ไม่พบไฟล์, Worksheets หรือดัชนีของตัวแบ่งหน้าที่ระบุ"
}
```

*400 – คำขอไม่ถูกต้อง*

```json
{
  "Code": 400,
  "Message": "พารามิเตอร์ของคำขอไม่ถูกต้องหรือมีรูปแบบไม่ถูกต้อง"
}
```

*500 – ข้อผิดพลาดภายในเซิร์ฟเวอร์*

```json
{
  "Code": 500,
  "Message": "เกิดข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด"
}
```

---

## ตัวอย่างโค้ด SDK

ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้การดำเนินการ **DeleteVerticalPageBreak** โดยใช้ SDK ต่างๆ ของ Aspose.Cells Cloud

<details><summary>**C#**</summary>

```csharp
// Install-Package Aspose.Cells-Cloud
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("client_id", "client_secret");
string name = "Book1.xlsx";
string sheetName = "Sheet1";
int index = 0;
string folder = "Docs";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName);
    Console.WriteLine($"Status: {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.DeleteVerticalPageBreak: " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class DeleteVerticalPageBreak {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String folder = "Docs";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse resp = api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName);
            System.out.println("Status: " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"
api_client = ApiClient(configuration=config)
api = CellsApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
index = 0
folder = "Docs"
storage_name = "MyStorage"

try:
    response = api.delete_vertical_page_break(name, sheet_name, index, folder, storage_name)
    print("Status:", response.status)
except Exception as e:
    print("Error:", e)
```

</details>

<details><summary>**Node.js**</summary>

```javascript
const { CellsApi, ApiClient, Configuration } = require('asposecellscloud');

const config = new Configuration();
config.clientId = "client_id";
config.clientSecret = "client_secret";

const api = new CellsApi(new ApiClient(config));

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const folder = "Docs";
const storageName = "MyStorage";

api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName)
  .then(response => console.log('Status:', response.status))
  .catch(error => console.error('Error:', error));
```

</details>

<details><summary>**Go**</summary>

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration()
    config.ClientId = "client_id"
    config.ClientSecret = "client_secret"

    api := asposecellscloud.NewAPIClient(config).CellsApi
    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    folder := "Docs"
    storageName := "MyStorage"

    resp, _, err := api.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println("Status:", resp.Status)
}
```

</details>

*(ตัวอย่างโค้ด SDK สำหรับ PHP, Ruby, Perl และภาษาอื่นๆ มีรูปแบบเดียวกัน และสามารถดูได้ในที่เก็บ GitHub อย่างเป็นทางการ)*

---

## แหล่งข้อมูลที่เกี่ยวข้อง

* **ข้อมูลจำเพาะ OpenAPI** – [DeleteVerticalPageBreak](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteVerticalPageBreak)  
* **Aspose.Cells Cloud SDKs** – <https://github.com/aspose-cells-cloud>  
* **คู่มือการตรวจสอบสิทธิ์** – <https://docs.aspose.cloud/cells/authentication/>  

---

*เอกสารอัปเดตครั้งล่าสุด: 2026-07-30*