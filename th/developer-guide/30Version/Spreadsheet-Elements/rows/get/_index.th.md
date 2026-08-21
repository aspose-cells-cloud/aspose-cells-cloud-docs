---
---
title: "การดึงข้อมูลแถวเดียวจากแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud API"
description: "เรียนรู้วิธีดึงแถวที่ระบุจากแผ่นงาน Excel ที่จัดเก็บไว้ในที่เก็บข้อมูล Aspose Cloud โดยใช้ Aspose.Cells Cloud REST API รวมถึงไวยากรณ์คำขอ พารามิเตอร์ โครงสร้างการตอบกลับ ตัวอย่าง cURL และโค้ด SDK (C#, Java, Python)"
keywords: "Aspose.Cells Cloud, ดึงแถว, Excel API, spreadsheet REST, C# SDK, Java SDK, Python SDK"
date: 2026-07-30
api_version: "v3.0"
---

# ดึงข้อมูลแถวเดียวจากแผ่นงาน Excel

**จุดปลายทาง**: `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/rows/{rowIndex}`  

ดึงข้อมูลแถวจากแผ่นงานที่จัดเก็บไว้ในที่เก็บข้อมูล Aspose Cloud การดำเนินการนี้ต้องใช้โทเค็นการเข้าถึง OAuth 2.0 ที่ถูกต้องพร้อมขอบเขตสิทธิ์ **Read**

---

## สารบัญ
1. [ข้อกำหนดเบื้องต้น](#prerequisites)  
2. [คำขอ HTTP](#http-request)  
3. [พารามิเตอร์](#parameters)  
   - [พารามิเตอร์เส้นทาง](#path-parameters)  
   - [พารามิเตอร์คิวรี](#query-parameters)  
4. [ตัวอย่าง cURL](#curl-example)  
5. [การตอบกลับ](#response)  
   - [โครงสร้างการตอบกลับที่สำเร็จ](#success-schema)  
   - [โค้ดสถานะ](#status-codes)  
6. [ตัวอย่างโค้ด SDK](#sdk-code-samples)  
   - [C#](#c)  
   - [Java](#java)  
   - [Python](#python)  
7. [การดำเนินการที่เกี่ยวข้อง](#related-operations)  
8. [หมายเหตุและข้อจำกัด](#notes--limits)  

---

## ข้อกำหนดเบื้องต้น
- **บัญชี Aspose Cloud** ที่มีการสมัครสมาชิกที่ยังมีผล  
- **โทเค็นการเข้าถึง OAuth 2.0** ที่มีขอบเขตสิทธิ์ **Read**  
- สมุดงานเป้าหมายต้องมีอยู่แล้วในที่เก็บข้อมูล Aspose Cloud  

---

## คำขอ HTTP
```http
GET /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}?folder={folder}&storageName={storageName} HTTP/1.1
Host: api.aspose.cloud
Authorization: Bearer {access_token}
Accept: application/json
```

*URL หลัก*: `https://api.aspose.cloud/v3.0`

---

## พารามิเตอร์

### พารามิเตอร์เส้นทาง
| ชื่อ      | ชนิดข้อมูล | จำเป็น | คำอธิบาย                         |
|-----------|------------|--------|-------------------------------------|
| `name`    | สตริง | ✅       | ชื่อไฟล์สมุดงาน (เช่น `MyWorkbook.xlsx`) |
| `sheetName`| สตริง | ✅     | ชื่อแผ่นงาน (เช่น `Sheet1`) |
| `rowIndex`| จำนวนเต็ม| ✅       | ดัชนีของแถวที่ต้องการดึง (เริ่มต้นที่ 0) |

### พารามิเตอร์คิวรี *(ไม่บังคับ)*
| ชื่อ        | ชนิดข้อมูล | จำเป็น | คำอธิบาย |
|-------------|------------|--------|-------------|
| `folder`    | สตริง | ❌       | เส้นทางไปยังโฟลเดอร์ในที่เก็บข้อมูลบนคลาวด์ที่อยู่ภายในสมุดงาน |
| `storageName`| สตริง| ❌       | ชื่อของบริการที่เก็บข้อมูล (ถ้าใช้ที่เก็บข้อมูลแบบกำหนดเอง) |

---

## ตัวอย่าง cURL
```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/rows/5?folder=Docs&storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## การตอบกลับ

### โครงสร้างการตอบกลับที่สำเร็จ (`200 OK`)
```json
{
  "Code": 200,
  "Status": "OK",
  "Row": {
    "Index": 5,
    "Height": 15.0,
    "Style": { /* วัตถุรูปแบบ */ },
    "Cells": [
      { "ColumnIndex": 0, "Value": "A6", "DataType": "String" },
      { "ColumnIndex": 1, "Value": 123, "DataType": "Number" }
      /* ...เซลล์เพิ่มเติม... */
    ]
  }
}
```

### โค้ดสถานะ
| โค้ด | ความหมาย |
|------|---------|
| **200** | ดึงข้อมูลแถวสำเร็จ |
| **401** | ไม่ได้รับอนุญาต – ไม่มีหรือโทเค็นการเข้าถึงไม่ถูกต้อง |
| **404** | ไม่พบสมุดงาน แผ่นงาน หรือแถว |
| **500** | ข้อผิดพลาดภายในเซิร์ฟเวอร์ |

### ตัวอย่างข้อผิดพลาด (`401 Unauthorized`)
```json
{
  "Code": 401,
  "Message": "โทเค็นการเข้าถึงไม่พบหรือไม่ถูกต้อง"
}
```

---

## ตัวอย่างโค้ด SDK

### C#  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var clientId = "YOUR_CLIENT_ID";
var clientSecret = "YOUR_CLIENT_SECRET";

var api = new CellsApi(clientId, clientSecret);
var response = api.CellsRows_GetWorksheetRow(
    name: "MyWorkbook.xlsx",
    sheetName: "Sheet1",
    rowIndex: 5,
    folder: "Docs",
    storageName: null   // ไม่บังคับ
);

Console.WriteLine($"ดึงข้อมูลแถว {response.Row.Index} สำเร็จ มีเซลล์ {response.Row.Cells.Count} เซลล์");
```

### Java  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.RowResponse;

CellsApi api = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");
RowResponse response = api.cellsRowsGetWorksheetRow(
    "MyWorkbook.xlsx",
    "Sheet1",
    5,
    "Docs",
    null   // storageName – ไม่บังคับ
);

System.out.println("ดัชนีแถว: " + response.getRow().getIndex());
System.out.println("จำนวนเซลล์: " + response.getRow().getCells().size());
```

### Python  
```python
from asposecellscloud import CellsApi, ApiException
from asposecellscloud.models import RowResponse

client_id = "YOUR_CLIENT_ID"
client_secret = "YOUR_CLIENT_SECRET"

api = CellsApi(client_id, client_secret)

try:
    response = api.cells_rows_get_worksheet_row(
        name="MyWorkbook.xlsx",
        sheet_name="Sheet1",
        row_index=5,
        folder="Docs",
        storage_name=None
    )
    print(f"ดึงข้อมูลแถว {response.row.index} สำเร็จ มีเซลล์ {len(response.row.cells)} เซลล์")
except ApiException as e:
    print("ข้อผิดพลาดเมื่อเรียกใช้ CellsApi->cells_rows_get_worksheet_row:", e)
```

---

## การดำเนินการที่เกี่ยวข้อง
| การดำเนินการ | คำอธิบาย |
|--------------|----------|
| **เพิ่มแถว** | `POST /cells/{name}/worksheets/{sheetName}/rows` – เพิ่มแถวใหม่ลงในแผ่นงาน |
| **ลบแถว** | `DELETE /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}` – ลบแถวที่มีอยู่ออก |
| **ดึงข้อมูลหลายแถว** | `GET /cells/{name}/worksheets/{sheetName}/rows` – ดึงข้อมูลชุดของแถว |
| **ภาพรวมการดำเนินการเกี่ยวกับแถว** | `/cells/rows/` – เอกสารทั่วไปสำหรับจุดปลายทางที่เกี่ยวข้องกับแถว |

---

## หมายเหตุและข้อจำกัด
- **ขีดจำกัดอัตรา**: สูงสุด 100 คำขอต่อนาทีต่อบัญชี  
- **รูปแบบที่รองรับ**: XLS, XLSX, CSV, ODS  
- ดัชนีของแถวเริ่มต้นที่ **0** (แถวแรกคือ `0`)  
- ตรวจสอบให้แน่ใจว่าสมุดงานถูกอัปโหลดไปยัง `folder` ที่ระบุก่อนเรียกใช้จุดปลายทางนี้  

---
---