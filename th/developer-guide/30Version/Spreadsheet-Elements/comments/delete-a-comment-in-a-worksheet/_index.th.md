---
---
title: "API ลบความคิดเห็นในแผ่นงาน – Aspose.Cells Cloud"
description: "ลบความคิดเห็นของเซลล์เฉพาะในแผ่นงาน Excel โดยใช้ REST API ของ Aspose.Cells Cloud (เวอร์ชัน 3.0) รวมถึงปลายทาง พารามิเตอร์ ตัวอย่างคำขอ/การตอบกลับ ตัวอย่างโค้ด SDK และการจัดการข้อผิดพลาด"
keywords: "Aspose.Cells, ลบความคิดเห็น, Excel API, REST, ความคิดเห็นในแผ่นงาน"
date: "2026-07-30"
lastModified: "2026-07-30"
---

# API ลบความคิดเห็นในแผ่นงาน – Aspose.Cells Cloud

> **อัปเดตหน้าล่าสุด:** 30 กรกฎาคม 2569  

## ภาพรวม
**ความคิดเห็น** คือข้อความหมายเหตุที่แนบมากับเซลล์เฉพาะในแผ่นงาน Excel  
การดำเนินการ **ลบความคิดเห็นในแผ่นงาน** จะลบความคิดเห็นออกจากเซลล์ที่ระบุ

![Aspose.Cells Cloud – ภาพประกอบการลบความคิดเห็นในแผ่นงาน](/cells/images/Aspose-image-for-open-graph.jpg "Aspose.Cells Cloud – API ลบความคิดเห็นในแผ่นงาน")

## การตรวจสอบสิทธิ์
ปลายทางทั้งหมดของ Aspose.Cells Cloud ต้องใช้การตรวจสอบสิทธิ์แบบใช้โทเค็น JWT  
ใส่โทเค็นในเฮดเดอร์ `Authorization`:

```
Authorization: Bearer <jwt token>
```

สำหรับรายละเอียดเกี่ยวกับการรับโทเค็น JWT โปรดดู [คู่มือการตรวจสอบสิทธิ์](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## ข้อกำหนดเบื้องต้น
- โทเค็นการเข้าถึง JWT ที่ถูกต้อง  
- สมุดงานเป้าหมาย (`{name}`) ต้องมีอยู่ในตำแหน่งที่จัดเก็บที่ระบุ  
- ทางเลือก: หนึ่งใน SDK ของ Aspose.Cells Cloud ที่ติดตั้งไว้สำหรับภาษาที่คุณเลือก

## คำขอ HTTP

### ปลายทาง
```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### พารามิเตอร์ในเส้นทาง
| พารามิเตอร์ | ประเภท | จำเป็น | คำอธิบาย |
|-------------|--------|--------|----------|
| `name`      | string | ✅ | ชื่อของสมุดงาน Excel (เช่น `test.xlsx`) |
| `sheetName` | string | ✅ | ชื่อของแผ่นงานที่มีความคิดเห็น |
| `cellName`  | string | ✅ | ที่อยู่ของเซลล์ที่จะลบความคิดเห็น (เช่น `A1`) |

### พารามิเตอร์ใน query string
| พารามิเตอร์   | ประเภท | จำเป็น | คำอธิบาย |
|---------------|--------|--------|----------|
| `folder`      | string | ❌ | เส้นทางของโฟลเดอร์ที่เก็บสมุดงาน หากไม่ระบุ จะใช้โฟลเดอร์ราก |
| `storageName` | string | ❌ | ชื่อของบริการจัดเก็บ (เช่น `MyCloud`) หากไม่ระบุ จะใช้พื้นที่จัดเก็บเริ่มต้น |

## ตัวอย่างคำขอ

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

## การตอบกลับ

### สำเร็จ (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                      | คำอธิบาย |
|------|-------------------------------|----------|
| 200  | สำเร็จ (OK)                  | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | ข้อมูลในคำขอมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

### การตอบกลับเมื่อเกิดข้อผิดพลาด

| โค้ด HTTP | คำอธิบาย | ตัวอย่าง |
|-----------|----------|---------|
| 400 | คำขอไม่ถูกต้อง – พารามิเตอร์ขาดหายหรือผิดรูปแบบ | `{ "Code": 400, "Message": "Invalid parameters." }` |
| 401 | ไม่ได้รับอนุญาต – โทเค็นไม่ถูกต้องหรือขาดหาย | `{ "Code": 401, "Message": "Authentication required." }` |
| 404 | ไม่พบ – ไฟล์ แผ่นงาน หรือความคิดเห็นไม่มีอยู่ | `{ "Code": 404, "Message": "Resource not found." }` |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เงื่อนไขที่ไม่คาดคิดบนเซิร์ฟเวอร์ | `{ "Code": 500, "Message": "Server error." }` |

## ตัวอย่าง SDK
ด้านล่างนี้คือโค้ดตัวอย่างที่พร้อมใช้งานสำหรับภาษาที่นิยมที่สุด แทนที่ `<jwt token>`, `test.xlsx`, `Sheet1` และ `A1` ด้วยค่าของคุณเอง

### C#
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using Aspose.Cells.Cloud.SDK.Client;

// ตั้งค่าไคลเอ็นต์ของ API
var config = new Configuration
{
    AccessToken = "<jwt token>",
    BasePath = "https://api.aspose.cloud"
};

var apiInstance = new WorksheetsApi(config);
try
{
    var result = apiInstance.DeleteWorksheetComment(
        name: "test.xlsx",
        sheetName: "Sheet1",
        cellName: "A1",
        folder: "Docs",
        storageName: "MyStorage"
    );
    Console.WriteLine("Comment deleted. Status: " + result.Status);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling WorksheetsApi.DeleteWorksheetComment: " + e.Message);
}
```

### Java
```java
import com.aspose.cloud.cells.api.WorksheetsApi;
import com.aspose.cloud.cells.client.ApiException;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class DeleteWorksheetCommentExample {
    public static void main(String[] args) {
        WorksheetsApi api = new WorksheetsApi();
        api.getApiClient().setAccessToken("<jwt token>");
        try {
            CellsCloudResponse response = api.deleteWorksheetComment(
                "test.xlsx",
                "Sheet1",
                "A1",
                "Docs",
                "MyStorage"
            );
            System.out.println("Deleted comment, status: " + response.getStatus());
        } catch (ApiException e) {
            System.err.println("Exception when calling WorksheetsApi#deleteWorksheetComment");
            e.printStackTrace();
        }
    }
}
```

### PHP
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAccessToken('<jwt token>');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new Aspose\Cells\Api\WorksheetsApi(
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->deleteWorksheetComment(
        'test.xlsx',
        'Sheet1',
        'A1',
        'Docs',
        'MyStorage'
    );
    echo "Comment deleted. Status: " . $result->getStatus();
} catch (Exception $e) {
    echo 'Exception when calling WorksheetsApi->deleteWorksheetComment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Ruby
```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '<jwt token>'
config.host = 'https://api.aspose.cloud'

api_instance = AsposeCellsCloud::WorksheetsApi.new
begin
  result = api_instance.delete_worksheet_comment('test.xlsx', 'Sheet1', 'A1', 'Docs', 'MyStorage')
  puts "Comment deleted – status: #{result.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling WorksheetsApi->delete_worksheet_comment: #{e}"
end
```

### Node.js (TypeScript)
```typescript
import { WorksheetsApi, Configuration } from "@asposecloud/cells-cloud";

const config = new Configuration({
    accessToken: "<jwt token>",
    basePath: "https://api.aspose.cloud"
});

const api = new WorksheetsApi(config);

api.deleteWorksheetComment("test.xlsx", "Sheet1", "A1", "Docs", "MyStorage")
    .then((response) => {
        console.log("Comment deleted. Status:", response.status);
    })
    .catch((error) => {
        console.error("Error deleting comment:", error);
    });
```

### Python
```python
from asposecellscloud.apis import WorksheetsApi
from asposecellscloud import Configuration, ApiClient

config = Configuration()
config.access_token = "<jwt token>"
config.host = "https://api.aspose.cloud"

api_client = ApiClient(configuration=config)
api = WorksheetsApi(api_client)

try:
    response = api.delete_worksheet_comment(
        name="test.xlsx",
        sheet_name="Sheet1",
        cell_name="A1",
        folder="Docs",
        storage_name="MyStorage"
    )
    print("Comment deleted. Status:", response.status)
except Exception as e:
    print("Exception when calling WorksheetsApi->delete_worksheet_comment:", e)
```

### Perl
```perl
use AsposeCellsCloud::Api::WorksheetsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    access_token => '<jwt token>',
    host => 'https://api.aspose.cloud'
);
my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new($config);

eval {
    my $result = $api_instance->delete_worksheet_comment(
        name        => 'test.xlsx',
        sheet_name  => 'Sheet1',
        cell_name   => 'A1',
        folder      => 'Docs',
        storage_name=> 'MyStorage'
    );
    print "Comment deleted. Status: " . $result->{status} . "\n";
};
if ($@) {
    warn "Exception when calling WorksheetsApi->delete_worksheet_comment: $@\n";
}
```

### Go
```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/api"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/config"
)

func main() {
    cfg := config.NewConfiguration()
    cfg.AccessToken = "<jwt token>"
    cfg.Host = "https://api.aspose.cloud"

    apiInstance := api.NewWorksheetsApi(cfg)

    result, _, err := apiInstance.DeleteWorksheetComment(
        "test.xlsx",   // name
        "Sheet1",      // sheetName
        "A1",          // cellName
        "Docs",        // folder (optional)
        "MyStorage",   // storageName (optional)
    )
    if err != nil {
        fmt.Printf("Error when calling DeleteWorksheetComment: %v\n", err)
        return
    }
    fmt.Printf("Comment deleted. Status: %s\n", result.Status)
}
```

## การดำเนินการที่เกี่ยวข้อง
- [เพิ่มความคิดเห็นในแผ่นงาน](/comments/add/)  
- [อัปเดตความคิดเห็นในแผ่นงาน](/comments/update/)  

## การจำกัดอัตรา
Aspose.Cells Cloud บังคับใช้ **ขีดจำกัดอัตราเริ่มต้นที่ 100 คำขอต่อนาทีต่อบัญชี** หากเกินขีดจำกัดนี้ จะได้รับ HTTP 429 Too Many Requests ให้ใช้การหน่วงเวลารูปแบบ exponential back‑off หรือปฏิบัติตามเฮดเดอร์ `Retry-After` เพื่อหลีกเลี่ยงการถูกจำกัดอัตรา

## ดูเพิ่มเติม
- **สเปค OpenAPI:** <https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComment>  
- **คู่มือการตรวจสอบสิทธิ์:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **ที่เก็บ SDK:** <https://github.com/aspose-cells-cloud>  

---
---