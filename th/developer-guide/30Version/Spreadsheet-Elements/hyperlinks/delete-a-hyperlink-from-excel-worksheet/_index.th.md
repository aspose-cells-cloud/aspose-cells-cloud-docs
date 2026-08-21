---
title: "ลบลิงก์ในแผ่นงาน"
type: docs
url: /hyperlinks/delete/
description: "ลบลิงก์ในแผ่นงานโดยใช้ดัชนีผ่าน Aspose.Cells Cloud API เรียนรู้พารามิเตอร์ที่จำเป็น การตรวจสอบสิทธิ์ และดูตัวอย่างโค้ดสำหรับ C#, Java, Python และอื่นๆ"
keywords: "Aspose.Cells, Cloud, ลบลิงก์, Excel API, REST, ลิงก์ในแผ่นงาน"
ArticleTitle: "ลบลิงก์ในแผ่นงาน – เอกสารประกอบ Aspose.Cells Cloud API"
weight: 40
---

REST API นี้ใช้ลบลิงก์ในแผ่นงานโดยใช้ดัชนีของลิงก์บนแผ่นงาน Excel

## ความปลอดภัยและการตรวจสอบสิทธิ์
Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้การตรวจสอบสิทธิ์แบบ [โทเค็น JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

### REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์   | ประเภท   | ตำแหน่ง | จำเป็น | คำอธิบาย                                                                 |
| ------------------ | ------- | -------- | ------ | ------------------------------------------------------------------------ |
| **name**           | string  | path     | ✅     | ชื่อของเอกสาร Excel                                                      |
| **sheetName**      | string  | path     | ✅     | ชื่อของแผ่นงาน                                                          |
| **hyperlinkIndex** | integer | path     | ✅     | ดัชนีของลิงก์ที่จะลบ (เริ่มต้นที่ 0)                                    |
| **folder**         | string  | query    | ❌     | โฟลเดอร์ที่เก็บเอกสาร (ค่าเริ่มต้น: รูท)                                 |
| **storageName**    | string  | query    | ❌     | ชื่อของบริการจัดเก็บข้อมูล (จะใช้บริการจัดเก็บค่าเริ่มต้นหากไม่ระบุ) |

#### คำตอบ (Responses)

| รหัสสถานะ                     | คำอธิบาย                                                 | ตัวอย่างเนื้อหา                                    |
| ----------------------------- | -------------------------------------------------------- | -------------------------------------------------- |
| **200 OK**                    | ลบลิงก์เรียบร้อยแล้ว                                   | `{"Code":200,"Status":"OK"}`                       |
| **400 Bad Request**           | พารามิเตอร์ไม่ครบหรือไม่ถูกต้อง                        | `{"Code":400,"Message":"Invalid hyperlinkIndex."}` |
| **401 Unauthorized**          | โทเค็นการตรวจสอบสิทธิ์ไม่ครบหรือไม่ถูกต้อง             | `{"Code":401,"Message":"Invalid access token."}`   |
| **404 Not Found**             | ไฟล์ แผ่นงาน หรือดัชนีลิงก์ไม่มีอยู่                     | `{"Code":404,"Message":"Resource not found."}`     |
| **500 Internal Server Error** | ข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด                     | `{"Code":500,"Message":"Internal server error."}`  |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Hypelinks/DeleteWorksheetHyperlink) นิยามอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถปฏิบัติการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL เพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างด้านล่างแสดงวิธีการเรียก API ผ่าน cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="คำตอบ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test1.xlsx/worksheets/Sheet1/hyperlinks/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK สำหรับ Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจาก SDK จะจัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นไปที่โปรเจกต์ของคุณได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกเว็บเซอร์วิสของ Aspose.Cells ผ่าน SDK ต่างๆ  snippet ของโค้ดมีไว้ให้โดยตรงเพื่อความน่าเชื่อถือ และมีลิงก์ไปยัง Gist ต้นฉบับให้ตรวจสอบเพิ่มเติม

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// ExampleDeleteWorksheetHyperlink.cs
// แหล่งที่มา: https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("<client_id>", "<client_secret>");
var response = apiInstance.DeleteWorksheetHyperlink(
    name: "test1.xlsx",
    sheetName: "Sheet1",
    hyperlinkIndex: 0,
    folder: null,
    storageName: null);
Console.WriteLine(response.Status);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Example_DeleteWorksheetHyperlink.java
// แหล่งที่มา: https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

CellsApi api = new CellsApi("<client_id>", "<client_secret>");
ApiResponse<Void> response = api.deleteWorksheetHyperlink(
    "test1.xlsx",
    "Sheet1",
    0,
    null,
    null);
System.out.println("Status: " + response.getStatusCode());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// Example_DeleteWorksheetHyperlink.php
// แหล่งที่มา: https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152
require_once('vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppSid('<client_id>');
$config->setAppKey('<client_secret>');

$apiInstance = new Aspose\Cells\Api\CellsApi($config);
$response = $apiInstance->deleteWorksheetHyperlink(
    "test1.xlsx",
    "Sheet1",
    0,
    null,
    null);
echo $response->getStatusCode();
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Example_DeleteWorksheetHyperlink.rb
// แหล่งที่มา: https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new('<client_id>', '<client_secret>')
result = api.delete_worksheet_hyperlink('test1.xlsx', 'Sheet1', 0)
puts result.status
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
// Example_DeleteWorksheetHyperlink.ts (Node.js)
// แหล่งที่มา: https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0
const AsposeCellsCloud = require("asposecellscloud");
const api = new AsposeCellsCloud.CellsApi("<client_id>", "<client_secret>");

api
  .deleteWorksheetHyperlink("test1.xlsx", "Sheet1", 0, null, null)
  .then(() => console.log("Hyperlink deleted"))
  .catch((err) => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
# Example_DeleteWorksheetHyperlink.py
// แหล่งที่มา: https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1
from asposecellscloud import CellsApi, Configuration

config = Configuration(app_sid='<client_id>', app_key='<client_secret>')
api = CellsApi(config)

api.delete_worksheet_hyperlink('test1.xlsx', 'Sheet1', 0)
print('Hyperlink deleted')
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
# Example_DeleteWorksheetHyperlink.pl
// แหล่งที่มา: https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca
use AsposeCellsCloud::CellsApi;

my $api_instance = AsposeCellsCloud::CellsApi->new('<client_id>', '<client_secret>');
my $result = $api_instance->delete_worksheet_hyperlink(
    name => 'test1.xlsx',
    sheet_name => 'Sheet1',
    hyperlink_index => 0);
print "Status: $result->{status}\n";
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
// Example_DeleteWorksheetHyperlink.go
// แหล่งที่มา: https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration("<client_id>", "<client_secret>")
    api := asposecellscloud.NewAPIClient(config).CellsApi
    _, err := api.DeleteWorksheetHyperlink("test1.xlsx", "Sheet1", 0, nil, nil)
    if err != nil {
        fmt.Println(err)
    } else {
        fmt.Println("Hyperlink deleted")
    }
}
```

{{< /tab >}}

{{< /tabs >}}