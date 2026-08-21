---
---
title: "การใช้งานคุณสมบัติ Autofit ในแผ่นงาน Excel"
second_title: "เอกสาร"
linktype: "Autofit"
type: docs
url: /worksheets/autofit/
aliases: [/autofit-rows-and-columns-of-worksheet/]
keywords: "autofit, คอลัมน์, แถว, Aspose.Cells, Cloud, Excel, API, ปรับขนาด"
description: "เรียนรู้วิธีการปรับขนาดแถวและคอลัมน์อัตโนมัติในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API พร้อมตัวอย่างโค้ดสำหรับ cURL, .NET, Java และ Python"
weight: 20
ArticleTitle: "การใช้งานคุณสมบัติ Autofit ในแผ่นงาน Excel – Aspose.Cells Cloud API"
---

## การใช้งานคุณสมบัติ autofit ในแผ่นงาน Excel

- [วิธีการ autoFit คอลัมน์ในแผ่นงาน Excel](/cells/worksheets/autofit/column/)
- [วิธีการ autoFit คอลัมน์หลายคอลัมน์ในแผ่นงาน Excel](/cells/worksheets/autofit/columns/)
- [วิธีการ autoFit แถวในแผ่นงาน Excel](/cells/worksheets/autofit/row/)
- [วิธีการ autoFit หลายแถวในแผ่นงาน Excel](/cells/worksheets/autofit/rows/)

**ข้อกำหนดเบื้องต้น**  
ก่อนใช้งานการดำเนินการ autoFit คุณต้องมี:

1. บัญชี Aspose.Cells Cloud พร้อม **Client Id** และ **Client Secret** ที่ถูกต้อง  
2. สมุดงานที่อัปโหลดไว้ในพื้นที่จัดเก็บของ Aspose Cloud (หรือเข้าถึงได้ผ่าน URL สาธารณะ)  
3. ชื่อแผ่นงานที่คุณต้องการแก้ไข

**อ้างอิง API**

| การดำเนินการ | HTTP Method | Endpoint | พารามิเตอร์ที่จำเป็น | เนื้อหาคำขอ | ตัวอย่างการตอบกลับ | รหัสสถานะ |
|-----------|-------------|----------|--------------------|--------------|----------------|--------------|
| autoFit **คอลัมน์** | POST | `/cells/worksheets/{sheetName}/autofit/column` | `sheetName` (path) <br> `columnIndex` (query) | *ไม่มี* | `{ "code": 200, "status": "OK", "message": "Column autofitted." }` | 200, 400, 401, 404, 500 |
| autoFit **คอลัมน์หลายคอลัมน์** | POST | `/cells/worksheets/{sheetName}/autofit/columns` | `sheetName` (path) <br> `startColumn`, `endColumn` (query) | *ไม่มี* | `{ "code": 200, "status": "OK", "message": "Columns autofitted." }` | 200, 400, 401, 404, 500 |
| autoFit **แถว** | POST | `/cells/worksheets/{sheetName}/autofit/row` | `sheetName` (path) <br> `rowIndex` (query) | *ไม่มี* | `{ "code": 200, "status": "OK", "message": "Row autofitted." }` | 200, 400, 401, 404, 500 |
| autoFit **หลายแถว** | POST | `/cells/worksheets/{sheetName}/autofit/rows` | `sheetName` (path) <br> `startRow`, `endRow` (query) | *ไม่มี* | `{ "code": 200, "status": "OK", "message": "Rows autofitted." }` | 200, 400, 401, 404, 500 |

**ตัวอย่างโค้ด**

*cURL*

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/worksheets/MySheet/autofit/columns?startColumn=0&endColumn=5" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json"
```

*.NET (C#)*

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// ตรวจสอบสิทธิ์
var apiInstance = new CellsApi("{client_id}", "{client_secret}");

// เรียกใช้งาน autoFit คอลัมน์
var response = apiInstance.PostWorksheetAutofitColumns(
    name: "Workbook.xlsx",
    sheetName: "Sheet1",
    startColumn: 0,
    endColumn: 5,
    folder: "",
    storageName: ""
);
Console.WriteLine(response.Status);
```

*Java*

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.*;

CellsApi api = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");

// autoFit หลายแถว
PostWorksheetAutofitRowsResponse resp = api.postWorksheetAutofitRows(
    "Workbook.xlsx",
    "Sheet1",
    0,   // startRow
    10,  // endRow
    "",  // folder
    ""   // storageName
);
System.out.println(resp.getStatus());
```

*Python*

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "YOUR_CLIENT_ID"
config.client_secret = "YOUR_CLIENT_SECRET"
api_client = ApiClient(configuration=config)
api = CellsApi(api_client)

# autoFit คอลัมน์เดียว
response = api.post_worksheet_autofit_column(
    name="Workbook.xlsx",
    sheet_name="Sheet1",
    column_index=2,
    folder="",
    storage_name=""
)
print(response.status)
```

ตัวอย่างโค้ดเหล่านี้แสดงวิธีการ:

1. ตรวจสอบสิทธิ์กับ Aspose.Cells Cloud โดยใช้ **Client Id** และ **Client Secret** ของคุณ  
2. เรียกใช้ endpoint สำหรับ autoFit ที่เหมาะสม สำหรับคอลัมน์หรือแถว  
3. ประมวลผลการตอบกลับ ซึ่งยืนยันว่าการดำเนินการเสร็จสมบูรณ์

**ขั้นตอนถัดไป**

หลังจากเรียกใช้งาน autoFit เสร็จสมบูรณ์ คุณสามารถดาวน์โหลดสมุดงานที่อัปเดตแล้ว:

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Workbook.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -o UpdatedWorkbook.xlsx
```

คุณสามารถปรับค่าพารามิเตอร์ `startColumn`, `endColumn`, `startRow` และ `endRow` ตามช่วงที่ต้องการได้ตามใจชอบ
---