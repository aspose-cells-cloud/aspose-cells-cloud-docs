---
title: "ลบความคิดเห็นทั้งหมดในแผ่นงาน"
description: "ลบความคิดเห็นทั้งหมดออกจากแผ่นงานในไฟล์ Excel โดยใช้ API ของ Aspose.Cells Cloud ศึกษาเกี่ยวกับ endpoint การ DELETE พารามิเตอร์ที่จำเป็น การพิสูจน์ตัวตน ตัวอย่างคำสั่ง cURL รูปแบบการตอบกลับ รหัสข้อผิดพลาด และตัวอย่าง SDK"
keywords: "Aspose, Cells, ลบความคิดเห็น, แผ่นงาน, API, REST, Excel, คลาวด์"
url: /th/comments/clear/
aliases:
  - /delete-all-comments-in-a-worksheet/
weight: 50
---

# ลบความคิดเห็นทั้งหมดในแผ่นงาน

**เวอร์ชัน API:** `v3.0`  
**ทรัพยากร:** `Worksheets` → `DeleteWorksheetComments`  

Aspose.Cells Cloud มี endpoint REST ที่มีประสิทธิภาพสำหรับการลบ **ความคิดเห็นทั้งหมด** ออกจากแผ่นงานที่ระบุ การดำเนินการนี้เป็นการลบอย่างถาวร เมื่อดำเนินการแล้ว ความคิดเห็นจะไม่สามารถกู้คืนได้

---

## ข้อกำหนดเบื้องต้น

| ข้อกำหนด | รายละเอียด |
|----------|-----------|
| **การพิสูจน์ตัวตน** | จำเป็นต้องมี JWT access token ที่ถูกต้องใน header `Authorization` (`Bearer <jwt token>`) รับ token ได้จาก [ขั้นตอนการพิสูจน์ตัวตน OAuth2](https://docs.aspose.cloud/cells/authentication/) |
| **พื้นที่จัดเก็บข้อมูล (Storage)** | ไฟล์ต้องอยู่ในพื้นที่จัดเก็บข้อมูลที่ Aspose.Cells Cloud เข้าถึงได้ (จะใช้ default storage หากไม่ระบุ `storageName`) |
| **สิทธิ์การเข้าถึง** | Token ต้องมีสิทธิ์ในการอ่านและเขียนไฟล์เป้าหมาย |
| **SDK (ไม่บังคับ)** | มี SDK ให้ใช้งานสำหรับ .NET, Java, PHP, Ruby, Node.js, Python, Perl และ Go (ดูหัวข้อ **ตัวอย่าง SDK**) |

---

## คำขอ HTTP

### Endpoint

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments
```

### Path Parameters

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย |
|------------------|--------|----------|
| `name`    | string | ชื่อไฟล์ Excel (เช่น `test.xlsx`) |
| `sheetName` | string | ชื่อแผ่นงาน (เช่น `Sheet1`) |

### Query Parameters

| ชื่อพารามิเตอร์ | ประเภท | จำเป็น | คำอธิบาย |
|------------------|--------|--------|----------|
| `folder`    | string | ไม่บังคับ | เส้นทางไปยังโฟลเดอร์ที่เก็บไฟล์ |
| `storageName` | string | ไม่บังคับ | ชื่อของพื้นที่จัดเก็บข้อมูลที่ไฟล์นั้นๆ อยู่ |

### Request Headers

| Header                | Value                              |
|-----------------------|------------------------------------|
| `Authorization`       | `Bearer <jwt token>`               |
| `Accept`              | `application/json`                |
| `Content-Type`        | `application/json`                |

---

## ตัวอย่างคำสั่ง Request (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments?folder=Documents&storageName=MyStorage" \
  -X DELETE \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*แทนค่า `test.xlsx`, `Sheet1`, `Documents`, `MyStorage` และ `<jwt token>` ด้วยค่าจริงของคุณ*

---

## การตอบกลับ

### สำเร็จ (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

เนื้อหาส่วน response body อยู่ในรูปแบบของโมเดล `CellsCloudResponse`

### การตอบกลับกรณีข้อผิดพลาด

| HTTP Code | ความหมาย | ตัวอย่าง Body |
|-----------|----------|---------------|
| **400**   | คำขอไม่ถูกต้อง – พารามิเตอร์ไม่ถูกต้อง | `{ "Code": 400, "Message": "Invalid request." }` |
| **401**   | ไม่ได้รับอนุญาต – ไม่มี JWT token หรือ token ไม่ถูกต้อง | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**   | ไม่พบ – ไฟล์หรือแผ่นงานไม่มีอยู่จริง | `{ "Code": 404, "Message": "Resource not found." }` |
| **500**   | ข้อผิดพลาดภายในเซิร์ฟเวอร์ | `{ "Code": 500, "Message": "Server error." }` |

---

## ตัวอย่าง SDK

โค้ดตัวอย่างต่อไปนี้แสดงวิธีการเรียก endpoint โดยใช้ SDK ทางการของ Aspose.Cells Cloud (เวอร์ชัน 3.13.0) แทนค่า placeholder (`<fileName>`, `<sheet>`, `<jwt token>` เป็นต้น) ด้วยข้อมูลจริงของคุณ

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new WorksheetsApi();
var name = "test.xlsx"; // string | ชื่อไฟล์
var sheetName = "Sheet1"; // string | ชื่อแผ่นงาน
var folder = "Documents"; // string | เส้นทางโฟลเดอร์ (ไม่บังคับ)
var storageName = "MyStorage"; // string | ชื่อพื้นที่จัดเก็บข้อมูล (ไม่บังคับ)

try
{
    var response = apiInstance.DeleteWorksheetComments(name, sheetName, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling WorksheetsApi.DeleteWorksheetComments: " + e.Message );
}
```

### Java  

```java
import com.aspose.cells.cloud.sdk.api.WorksheetsApi;
import com.aspose.cells.cloud.sdk.model.*;

public class DeleteWorksheetComments {
    public static void main(String[] args) {
        WorksheetsApi api = new WorksheetsApi();
        String name = "test.xlsx";
        String sheetName = "Sheet1";
        String folder = "Documents";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse resp = api.deleteWorksheetComments(name, sheetName, folder, storageName);
            System.out.println(resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### PHP  

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

use Aspose\Cells\Cloud\Api\WorksheetsApi;

$apiInstance = new WorksheetsApi();
$name = "test.xlsx";
$sheetName = "Sheet1";
$folder = "Documents";
$storageName = "MyStorage";

try {
    $result = $apiInstance->deleteWorksheetComments($name, $sheetName, $folder, $storageName);
    echo $result->getStatus();
} catch (Exception $e) {
    echo 'Exception when calling WorksheetsApi->deleteWorksheetComments: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Ruby  

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::WorksheetsApi.new
name = 'test.xlsx'
sheet_name = 'Sheet1'
folder = 'Documents'          # ไม่บังคับ
storage_name = 'MyStorage'    # ไม่บังคับ

begin
  result = api_instance.delete_worksheet_comments(name, sheet_name, folder, storage_name)
  puts result.status
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling WorksheetsApi->delete_worksheet_comments: #{e}"
end
```

### Node.js (TypeScript)  

```typescript
import { WorksheetsApi } from "@asposecloud/cells-sdk";

const api = new WorksheetsApi();
const name = "test.xlsx";
const sheetName = "Sheet1";
const folder = "Documents";
const storageName = "MyStorage";

api.deleteWorksheetComments(name, sheetName, folder, storageName)
    .then((response) => console.log(response.status))
    .catch((error) => console.error("Error:", error));
```

### Python  

```python
from asposecellscloud import WorksheetsApi

api_instance = WorksheetsApi()
name = "test.xlsx"
sheet_name = "Sheet1"
folder = "Documents"          # ไม่บังคับ
storage_name = "MyStorage"    # ไม่บังคับ

try:
    response = api_instance.delete_worksheet_comments(name, sheet_name, folder, storage_name)
    print(response.status)
except Exception as e:
    print("Exception when calling WorksheetsApi->delete_worksheet_comments:", e)
```

### Perl  

```perl
use AsposeCellsCloud::Api::WorksheetsApi;

my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new();

my $name = 'test.xlsx';
my $sheet_name = 'Sheet1';
my $folder = 'Documents';
my $storage_name = 'MyStorage';

eval {
    my $result = $api_instance->delete_worksheet_comments(
        name => $name,
        sheet_name => $sheet_name,
        folder => $folder,
        storage_name => $storage_name
    );
    print $result->{status}, "\n";
};
if ($@) {
    print "Exception when calling WorksheetsApi->delete_worksheet_comments: $@\n";
}
```

### Go  

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    cfg := sdk.NewConfiguration()
    cfg.AddDefaultHeader("Authorization", "Bearer <jwt token>")
    api := sdk.NewWorksheetsApi(cfg)

    name := "test.xlsx"
    sheetName := "Sheet1"
    folder := "Documents"
    storageName := "MyStorage"

    resp, _, err := api.DeleteWorksheetComments(name, sheetName, folder, storageName)
    if err != nil {
        fmt.Printf("Error: %v\n", err)
        return
    }
    fmt.Println(resp.Status)
}
```

---

## หมายเหตุและข้อจำกัด

* การดำเนินการนี้จะ **ลบความคิดเห็นทั้งหมด** ในแผ่นงานที่ระบุ โปรดใช้ด้วยความระมัดระวังเนื่องจากไม่มีคำสั่งย้อนกลับ
* คำขอ **ไม่รับ request body** ข้อมูลที่จำเป็นทั้งหมดจะถูกส่งผ่าน URL และ headers เท่านั้น
* หากไฟล์เป้าหมายถูก **ป้องกันไว้** หรือแผ่นงานอยู่ในโหมด **อ่านอย่างเดียว (read-only)** API จะคืนค่าข้อผิดพลาด `400` หรือ `401` ขึ้นอยู่กับสาเหตุหลัก
* Endpoint นี้ใช้ได้กับไฟล์ที่จัดเก็บไว้ใน **Aspose Cloud Storage** รวมถึง **Amazon S3**, **Azure Blob** หรือ **Google Cloud Storage** เมื่ออ้างอิงด้วย `storageName` อย่างถูกต้อง

---

## แหล่งข้อมูลที่เกี่ยวข้อง

* **OpenAPI Specification** – [DeleteWorksheetComments](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComments)
* **คำแนะนำการพิสูจน์ตัวตน** – [OAuth2 สำหรับ Aspose.Cells Cloud](https://docs.aspose.cloud/cells/authentication/)
* **ที่เก็บ SDK** – <https://github.com/aspose-cells-cloud>
* **API ทั่วไปเกี่ยวกับ Worksheets** – <https://docs.aspose.cloud/cells/worksheets/>

---

*อัปเดตล่าสุด: 30 กรกฎาคม 2569*
---