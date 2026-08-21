---
title: "วิธีการดึงเนื้อหาช่วงข้อมูลจากแผ่นงาน Excel"
second_title: "เอกสาร"
linktype: "ดู"
type: docs
url: /th/ranges/get/
keywords: "Aspose.Cells, Excel, API, ดึง, range, สเปรดชีต, REST"
description: "เรียนรู้วิธีดึงเนื้อหาช่วงข้อมูลจากแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API พร้อมตัวอย่างไคลเอนต์ซอร์สโค้ดและไวยากรณ์คำขอ"
weight: 20
ArticleTitle: "วิธีดึงเนื้อหาช่วงข้อมูลจากแผ่นงาน Excel – Aspose.Cells Cloud API"
---

## การทำงานกับการดึงเนื้อหาช่วงข้อมูลจากแผ่นงาน Excel

- [วิธีดึงข้อมูลเซลล์ตามช่วงที่ตั้งชื่อไว้](/cells/ranges/get/values/)
- [วิธีดึงช่วงที่ตั้งชื่อไว้จากสมุดงาน Excel](/cells/ranges/get/name/)

**ข้อกำหนดเบื้องต้น**

- โทเคนการเข้าถึง Aspose Cloud ที่ถูกต้อง (หรือ `client_id`/`client_secret` สำหรับ OAuth)
- ไฟล์ Excel ต้องถูกอัปโหลดไว้ในโฟลเดอร์ที่ตั้งค่าไว้ใน storage
- SDK ของ Aspose.Cells Cloud เวอร์ชัน 3.0 หรือใหม่กว่า

การดำเนินการ **Get Range** จะส่งคืนเนื้อหาของช่วงที่ระบุในแผ่นงาน  
เป็นคำขอแบบ `GET` ที่เรียบง่าย โดยส่งคืนข้อมูลช่วงในรูปแบบ JSON (หรือรูปแบบอื่นตามที่ร้องขอ)

**ภาพรวมคำขอ**

| องค์ประกอบ | ค่า |
|-----------|-----|
| **HTTP Method** | `GET` |
| **จุดปลายทาง (Endpoint)** | `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}` |
| **พารามิเตอร์ในเส้นทาง (Path Parameters)** | `fileName` – ชื่อไฟล์ Excel (รวมส่วนขยายไฟล์ด้วย) <br> `sheetName` – ชื่อแผ่นงาน <br> `rangeName` – ชื่อช่วง (เช่น `A1:B10`) |
| **พารามิเตอร์ใน Query String** (ไม่บังคับ) | `folder` – โฟลเดอร์ของ storage <br> `storage` – ชื่อ storage <br> `outFormat` – รูปแบบของ response (เช่น `json`, `xml`) |
| **ส่วนหัว (Headers)** | `Authorization: Bearer <access_token>` <br> `Accept: application/json` |

**ตัวอย่าง cURL**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges/A1:B10?folder=Samples&storage=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/json"
```

**ตัวอย่าง C#**

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

var apiInstance = new CellsApi("client_id", "client_secret");
var request = new GetRangeRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    rangeName: "A1:B10",
    folder: "Samples",
    storage: "MyStorage"
);
var response = apiInstance.GetRange(request);
Console.WriteLine(response);
```

**ตัวอย่าง Java**

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.requests.GetRangeRequest;

CellsApi api = new CellsApi("client_id", "client_secret");
GetRangeRequest request = new GetRangeRequest(
        "Book1.xlsx",
        "Sheet1",
        "A1:B10",
        "Samples",
        "MyStorage",
        null,
        null);
var response = api.getRange(request);
System.out.println(response);
```

**ตัวอย่าง Python**

```python
from asposecellscloud import CellsApi, GetRangeRequest

api = CellsApi(client_id="client_id", client_secret="client_secret")
request = GetRangeRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    range_name="A1:B10",
    folder="Samples",
    storage="MyStorage"
)
response = api.get_range(request)
print(response)
```

**โครงสร้างข้อมูล Response (JSON)**

```json
{
  "Code": 200,
  "Status": "OK",
  "Range": {
    "ColumnCount": 2,
    "RowCount": 1,
    "FirstRow": 0,
    "FirstColumn": 0,
    "Values": [
      ["Value1", "Value2"]
    ]
  }
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | คำอธิบาย                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                          | ใช้ตัวกรองเรียบร้อยแล้ว; response ประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request)                 | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)                | JWT token ไม่ถูกต้องหรือขาดหาย |
| 413  | ข้อมูลที่ส่งมามีขนาดใหญ่เกินไป (Payload Too Large)           | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error)       | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

- `200 OK` – ดึงช่วงข้อมูลเรียบร้อยแล้ว  
- `400 Bad Request` – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง  
- `401 Unauthorized` – โทเคนการเข้าถึงไม่ถูกต้องหรือขาดหาย  
- `404 Not Found` – ไม่พบไฟล์ แผ่นงาน หรือช่วงข้อมูลที่ระบุ  
- `500 Internal Server Error` – เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์

**ตัวอย่าง Response ข้อผิดพลาด**

```json
// 400 Bad Request
{
  "Code": 400,
  "Message": "พารามิเตอร์ของคำขอนั้นไม่ถูกต้องหรือขาดหาย"
}
```

```json
// 401 Unauthorized
{
  "Code": 401,
  "Message": "โทเคนการเข้าถึงไม่ถูกต้องหรือขาดหาย"
}
```

```json
// 404 Not Found
{
  "Code": 404,
  "Message": "ไม่พบไฟล์ แผ่นงาน หรือช่วงข้อมูลที่ระบุ"
}
```

**ดูเพิ่มเติม**

- [วิธีดึงข้อมูลเซลล์ตามช่วงที่ตั้งชื่อไว้](/cells/ranges/get/values/)  
- [วิธีดึงช่วงที่ตั้งชื่อไว้จากสมุดงาน Excel](/cells/ranges/get/name/)  
- [อัปเดตเนื้อหาของช่วง](/cells/ranges/update/)  
- [ลบช่วงข้อมูล](/cells/ranges/delete/)  
---