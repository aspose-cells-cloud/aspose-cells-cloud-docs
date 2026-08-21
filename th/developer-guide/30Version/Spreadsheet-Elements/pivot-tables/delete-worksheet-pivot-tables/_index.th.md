---
title: "ลบพิวต์ทัเบิลทั้งหมดในเวิร์กชีต Excel"
description: "ลบพิวต์ทัเบิลทั้งหมดออกจากเวิร์กชีตที่ระบุโดยใช้ Aspose.Cells Cloud REST API"
keywords: "Aspose.Cells, พิวต์ทัเบิล, ลบ, REST API, Excel"
date: 2026-07-30
api_version: "v3.0"
---

# ลบพิวต์ทัเบิลทั้งหมดในเวิร์กชีต Excel

## ภาพรวม
การดำเนินการนี้จะลบ **พิวต์ทัเบิลทั้งหมด** ออกจากเวิร์กชีตที่ระบุในไฟล์ Excel ซึ่งมีประโยชน์เมื่อคุณต้องการรีเซ็ตการวิเคราะห์ของเวิร์กชีตหรือล้างพิวต์ทัเบิลที่ไม่ได้ใช้งานออกทั้งหมดในคำขอเดียว

## สิ่งที่ต้องมีก่อนใช้งาน
ก่อนเรียก API โปรดตรวจสอบให้แน่ใจว่าคุณได้ดำเนินขั้นตอนต่อไปนี้เรียบร้อยแล้ว:

1. **บัญชี Aspose Cloud** – สมัครใช้งานบัญชี Aspose Cloud หากคุณยังไม่มีบัญชี  
2. **โทเค็น JWT** – สร้าง JSON Web Token (JWT) สำหรับการยืนยันตัวตน ดูรายละเอียดได้ที่[คู่มือการยืนยันตัวตน](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
3. **การตั้งค่าที่จัดเก็บข้อมูล** – อัปโหลดไฟล์ Excel เป้าหมายไปยังที่จัดเก็บข้อมูลของ Aspose Cloud หรือที่จัดเก็บข้อมูลภายนอกที่เชื่อมต่ออยู่ บันทึก **โฟลเดอร์** และ **ชื่อที่จัดเก็บข้อมูล** (ถ้ามี) ที่ไฟล์นั้นอยู่

## การยืนยันตัวตน
API ของ Aspose.Cells Cloud ต้องใช้ **การยืนยันตัวตนด้วยโทเค็น JWT** ใส่โทเค็นนี้ในส่วนหัว `Authorization` ของการร้องขอแต่ละรายการ:

```
Authorization: Bearer <jwt token>
```

## คำร้องขอ HTTP

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### พารามิเตอร์เส้นทาง (Path Parameters)
| ชื่อ | ชนิดข้อมูล | จำเป็น | คำอธิบาย |
|------|--------|----------|-------------|
| `name` | ข้อความ (string) | จำเป็น | ชื่อไฟล์ Excel (เช่น `Sample.xlsx`) |
| `sheetName` | ข้อความ (string) | จำเป็น | ชื่อเวิร์กชีตที่จะลบพิวต์ทัเบิลทั้งหมดออก (เช่น `Sheet1`) |

### พารามิเตอร์คิวรี (Query Parameters)
| ชื่อ | ชนิดข้อมูล | จำเป็น | คำอธิบาย |
|------|--------|----------|-------------|
| `folder` | ข้อความ (string) | ไม่จำเป็น | โฟลเดอร์ที่เก็บไฟล์ไว้ |
| `storageName` | ข้อความ (string) | ไม่จำเป็น | ชื่อที่จัดเก็บข้อมูลที่ต้องการใช้งาน (หากไฟล์ไม่อยู่ในที่จัดเก็บข้อมูลเริ่มต้น) |

## ตัวอย่างคำร้องขอ (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables?folder=SampleFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

## การตอบกลับที่สำเร็จ
บริการจะส่งกลับวัตถุ `CellsCloudResponse` มาตรฐานซึ่งแสดงสถานะของการดำเนินการ

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## การจัดการข้อผิดพลาด

| สถานะ HTTP | ความหมาย | ตัวอย่าง payload |
|-------------|---------|-----------------|
| **400** | คำร้องขอไม่ถูกต้อง – พารามิเตอร์ที่จำเป็นขาดหายหรือไม่ถูกต้อง | `{ "Code": 400, "Message": "Missing required parameter 'name'." }` |
| **401** | ไม่ได้รับอนุญาต – โทเค็น JWT ไม่ถูกต้องหรือหมดอายุ | `{ "Code": 401, "Message": "Invalid authentication token." }` |
| **404** | ไม่พบ – ไฟล์หรือเวิร์กชีตไม่มีอยู่จริง | `{ "Code": 404, "Message": "Worksheet not found." }` |
| **500** | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน – ข้อผิดพลาดที่ไม่คาดคิด | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## ตัวอย่าง SDK

โค้ดตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้งานการดำเนินการนี้ผ่าน SDK ต่างๆ ของ Aspose.Cells Cloud

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Initialise the API client
var apiInstance = new CellsApi("<client-id>", "<client-secret>");

// Configure request parameters
string name = "Sample_Pivot_Table_Example.xls";
string sheetName = "Sheet2";
string folder = "SampleFolder";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteWorksheetPivotTables(name, sheetName, folder, storageName);
    Console.WriteLine($"Response code: {response.Code}, status: {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.DeleteWorksheetPivotTables: " + e.Message);
}
```

### Java

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

public class DeletePivotTables {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("<client-id>", "<client-secret>");
        String name = "Sample_Pivot_Table_Example.xls";
        String sheetName = "Sheet2";
        String folder = "SampleFolder";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse result = api.deleteWorksheetPivotTables(name, sheetName, folder, storageName);
            System.out.println("Code: " + result.getCode() + ", Status: " + result.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python

```python
import asposecellscloud_sdk
from asposecellscloud_sdk import CellsApi, ApiException

# Configure API client
configuration = asposecellscloud_sdk.Configuration()
configuration.api_key['client_id'] = '<client-id>'
configuration.api_key['client_secret'] = '<client-secret>'

api_instance = CellsApi(asposecellscloud_sdk.ApiClient(configuration))

name = 'Sample_Pivot_Table_Example.xls'
sheet_name = 'Sheet2'
folder = 'SampleFolder'
storage_name = 'MyStorage'

try:
    response = api_instance.delete_worksheet_pivot_tables(name, sheet_name, folder, storage_name)
    print(f'Code: {response.code}, Status: {response.status}')
except ApiException as e:
    print("Exception when calling CellsApi->delete_worksheet_pivot_tables: %s\n" % e)
```

### Node.js

```javascript
const { CellsApi, Configuration } = require('asposecellscloud-sdk');

const config = new Configuration({
    clientId: '<client-id>',
    clientSecret: '<client-secret>'
});
const apiInstance = new CellsApi(config);

const name = 'Sample_Pivot_Table_Example.xls';
const sheetName = 'Sheet2';
const folder = 'SampleFolder';
const storageName = 'MyStorage';

apiInstance.deleteWorksheetPivotTables(name, sheetName, folder, storageName)
    .then(result => {
        console.log(`Code: ${result.code}, Status: ${result.status}`);
    })
    .catch(err => {
        console.error('Error:', err);
    });
```

*SDK อื่นๆ (Go, PHP, Ruby, Swift, Perl, Android) มีให้ใช้งานใน[ kho ซอฟต์แวร์ SDK ของ Aspose.Cells Cloud](https://github.com/aspose-cells-cloud)*

## ดูเพิ่มเติม
- [ลบพิวต์ทัเบิลที่ระบุ](https://docs.aspose.cloud/cells/pivot-tables/delete-specific/)
- [รับพิวต์ทัเบิลทั้งหมดในเวิร์กชีต](https://docs.aspose.cloud/cells/pivot-tables/get-all/)
- [ภาพรวมการยืนยันตัวตน](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)
- [สเปค OpenAPI สำหรับ DeleteWorksheetPivotTables](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTables)

---

*เอกสารอัปเดตล่าสุดเมื่อ 2026-07-30 เนื้อหาทั้งหมดถูกเข้ารหัสด้วย UTF-8*