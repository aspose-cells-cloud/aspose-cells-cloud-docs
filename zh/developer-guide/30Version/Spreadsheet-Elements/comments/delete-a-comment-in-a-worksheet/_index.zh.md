---
---
title: "删除工作表批注 API – Aspose.Cells Cloud"
description: "使用 Aspose.Cells Cloud REST API (v3.0) 删除 Excel 工作表中特定单元格的批注。包含端点、参数、请求/响应示例、SDK 代码片段及错误处理。"
keywords: "Aspose.Cells, 删除批注, Excel API, REST, 工作表批注"
date: "2026-07-30"
lastModified: "2026-07-30"
---

# 删除工作表批注 API – Aspose.Cells Cloud

> **最后更新日期：** 2026 年 7 月 30 日  

## 概述
**批注** 是附加到 Excel 工作表中特定单元格的文本注释。  
**删除工作表批注** 操作将从指定单元格中移除批注。

![Aspose.Cells Cloud – 删除工作表批注示意图](/cells/images/Aspose-image-for-open-graph.jpg "Aspose.Cells Cloud – 删除工作表批注 API")

## 身份验证
所有 Aspose.Cells Cloud 端点均需使用 **基于 JWT 令牌的身份验证**。  
请在 `Authorization` 请求头中包含令牌：

```
Authorization: Bearer <jwt token>
```

有关获取 JWT 令牌的详细信息，请参阅 [身份验证指南](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## 前提条件
- 有效的 JWT 访问令牌。  
- 目标工作簿 (`{name}`) 必须存在于指定的存储位置。  
- 可选：为所选编程语言安装了相应的 Aspose.Cells Cloud SDK。

## HTTP 请求

### 端点
```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### 路径参数
| 参数名      | 类型   | 是否必需 | 描述 |
|-------------|--------|----------|------|
| `name`      | string | ✅ | Excel 工作簿的名称（例如 `test.xlsx`）。 |
| `sheetName` | string | ✅ | 包含批注的工作表名称。 |
| `cellName`  | string | ✅ | 将删除批注的单元格地址（例如 `A1`）。 |

### 查询参数
| 参数名        | 类型   | 是否必需 | 描述 |
|---------------|--------|----------|------|
| `folder`      | string | ❌ | 工作簿所在的文件夹路径。若省略，则使用根文件夹。 |
| `storageName` | string | ❌ | 存储服务的名称（例如 `MyCloud`）。若省略，则使用默认存储。 |

## 请求示例

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

## 响应

### 成功（200）

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP 状态码**

| 状态码 | 含义           | 描述                                     |
|--------|----------------|------------------------------------------|
| 200    | OK（成功）     | 批注删除成功；响应包含操作详情。         |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                     |
| 413    | Payload Too Large（负载过大） | 上传的文件超出大小限制。             |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。             |

### 错误响应

| HTTP 状态码 | 描述 | 示例 |
|-------------|------|------|
| 400 | 错误请求 – 缺少或格式错误的参数。 | `{ "Code": 400, "Message": "Invalid parameters." }` |
| 401 | 未授权 – 无效或缺失的令牌。 | `{ "Code": 401, "Message": "Authentication required." }` |
| 404 | 未找到 – 文件、工作表或批注不存在。 | `{ "Code": 404, "Message": "Resource not found." }` |
| 500 | 内部服务器错误 – 服务器上发生意外情况。 | `{ "Code": 500, "Message": "Server error." }` |

## SDK 示例
以下为最常用编程语言的可直接运行代码片段。请将 `<jwt token>`、`test.xlsx`、`Sheet1` 和 `A1` 替换为您的实际值。

### C#
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using Aspose.Cells.Cloud.SDK.Client;

// 配置 API 客户端
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

## 相关操作
- [添加工作表批注](/comments/add/)  
- [更新工作表批注](/comments/update/)  

## 速率限制
Aspose.Cells Cloud 默认对每个账户实施 **每分钟 100 次请求的速率限制**。超过限制将返回 HTTP 429 Too Many Requests（请求过多）。请实现指数退避机制，或遵循 `Retry-After` 响应头字段，以避免被限流。

## 参见
- **OpenAPI 规范：** <https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComment>  
- **身份验证指南：** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **SDK 仓库：** <https://github.com/aspose-cells-cloud>  

---
---