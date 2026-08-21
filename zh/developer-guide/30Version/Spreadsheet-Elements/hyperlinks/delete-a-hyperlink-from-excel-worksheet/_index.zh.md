---
title: "删除工作表超链接"
type: docs
url: /zh/hyperlinks/delete/
description: "使用 Aspose.Cells Cloud API 按索引删除工作表超链接。了解所需参数、身份验证方法，并查看 C#、Java、Python 等语言的代码示例。"
keywords: "Aspose.Cells, 云, 删除超链接, Excel API, REST, 工作表超链接"
ArticleTitle: "删除工作表超链接 – Aspose.Cells Cloud API 文档"
weight: 40
---

此 REST API 可根据索引删除 Excel 工作表中的工作表超链接。

## 安全与身份验证
Aspose.Cells Cloud API 采用安全机制，需要基于 [JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

### REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

### 请求参数

| 参数名称         | 类型    | 位置 | 是否必需 | 描述                                             |
| ---------------- | ------- | ---- | -------- | ------------------------------------------------ |
| **name**         | string  | 路径 | ✅       | Excel 文档名称。                                 |
| **sheetName**    | string  | 路径 | ✅       | 工作表名称。                                     |
| **hyperlinkIndex** | integer | 路径 | ✅       | 待删除超链接的从零开始的索引。                   |
| **folder**       | string  | 查询 | ❌       | 包含文档的文件夹（默认为根目录）。               |
| **storageName**  | string  | 查询 | ❌       | 存储服务名称（省略时使用默认存储）。             |

#### 响应状态码

| 状态码                        | 描述                                           | 示例响应体                                         |
| ----------------------------- | ---------------------------------------------- | -------------------------------------------------- |
| **200 OK**                    | 超链接删除成功。                               | `{"Code":200,"Status":"OK"}`                       |
| **400 Bad Request**           | 缺少或无效参数。                               | `{"Code":400,"Message":"Invalid hyperlinkIndex."}` |
| **401 Unauthorized**          | 身份验证令牌缺失或无效。                       | `{"Code":401,"Message":"Invalid access token."}`   |
| **404 Not Found**             | 文件、工作表或超链接索引不存在。               | `{"Code":404,"Message":"Resource not found."}`     |
| **500 Internal Server Error** | 服务器内部意外错误。                           | `{"Code":500,"Message":"Internal server error."}`  |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Hypelinks/DeleteWorksheetHyperlink) 定义了一个公开可访问的编程接口，可让您直接在 Web 浏览器中执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用该 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

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

## 云 SDK 家族

使用 SDK 是开发速度最快的方式。SDK 处理底层细节，让您专注于项目本身。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务。为保证可靠性，代码片段已内联嵌入；原始 Gist 链接供参考。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// ExampleDeleteWorksheetHyperlink.cs
// 来源：https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d
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
// 来源：https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f
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
// 来源：https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152
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
// 来源：https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new('<client_id>', '<client_secret>')
result = api.delete_worksheet_hyperlink('test1.xlsx', 'Sheet1', 0)
puts result.status
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
// Example_DeleteWorksheetHyperlink.ts (Node.js)
// 来源：https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0
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
// Example_DeleteWorksheetHyperlink.py
// 来源：https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1
from asposecellscloud import CellsApi, Configuration

config = Configuration(app_sid='<client_id>', app_key='<client_secret>')
api = CellsApi(config)

api.delete_worksheet_hyperlink('test1.xlsx', 'Sheet1', 0)
print('Hyperlink deleted')
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
// Example_DeleteWorksheetHyperlink.pl
// 来源：https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca
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
// 来源：https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185
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