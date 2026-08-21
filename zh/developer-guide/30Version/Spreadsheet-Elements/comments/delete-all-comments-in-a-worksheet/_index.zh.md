---
title: "删除工作表中的所有批注"
description: "使用 Aspose.Cells Cloud API 删除 Excel 文件中工作表的所有批注。了解 DELETE 接口、所需参数、身份验证、示例 cURL 请求、响应格式、错误代码及 SDK 示例。"
keywords: "Aspose, Cells, 删除批注, 工作表, API, REST, Excel, 云"
url: /zh/comments/clear/
aliases:
  - /delete-all-comments-in-a-worksheet/
weight: 50
---

# 删除工作表中的所有批注

**API 版本：** `v3.0`  
**资源：** `Worksheets` → `DeleteWorksheetComments`  

Aspose.Cells Cloud 提供了一个功能强大的 REST 接口，可删除指定工作表中的**所有**批注。该操作不可逆；一旦执行，批注将无法恢复。

---

## 前提条件

| 要求 | 说明 |
|------|------|
| **身份验证** | `Authorization` 请求头中需提供有效的 JWT 访问令牌（格式为 `Bearer <jwt token>`）。请通过 [OAuth2 身份验证流程](https://docs.aspose.cloud/cells/authentication/) 获取令牌。 |
| **存储空间** | 文件必须位于 Aspose.Cells Cloud 可访问的存储空间中（若省略 `storageName`，则默认使用主存储空间）。 |
| **权限** | 令牌必须具备读写目标文件的权限。 |
| **SDK（可选）** | 提供适用于 .NET、Java、PHP、Ruby、Node.js、Python、Perl 和 Go 的 SDK（详见 **SDK 示例** 部分）。 |

---

## HTTP 请求

### 接口地址

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments
```

### 路径参数

| 名称         | 类型   | 说明 |
|--------------|--------|------|
| `name`       | string | Excel 文件名（例如：`test.xlsx`）。 |
| `sheetName`  | string | 工作表名称（例如：`Sheet1`）。 |

### 查询参数

| 名称          | 类型   | 必填 | 说明 |
|---------------|--------|------|------|
| `folder`      | string | 否   | 包含文件的文件夹路径。 |
| `storageName` | string | 否   | 文件所在的存储空间名称。 |

### 请求头

| 请求头           | 值                                |
|------------------|-----------------------------------|
| `Authorization`  | `Bearer <jwt token>`              |
| `Accept`         | `application/json`                |
| `Content-Type`   | `application/json`                |

---

## 请求示例（cURL）

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments?folder=Documents&storageName=MyStorage" \
  -X DELETE \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*请将 `test.xlsx`、`Sheet1`、`Documents`、`MyStorage` 和 `<jwt token>` 替换为您实际使用的值。*

---

## 响应

### 成功响应（200）

```json
{
  "Code": 200,
  "Status": "OK"
}
```

响应体符合 `CellsCloudResponse` 模型定义。

### 错误响应

| HTTP 状态码 | 含义                         | 示例响应体 |
|-------------|------------------------------|-------------|
| **400**     | 请求错误 — 参数无效。         | `{ "Code": 400, "Message": "Invalid request." }` |
| **401**     | 未授权 — 缺失或无效的 JWT 令牌。 | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**     | 未找到 — 文件或工作表不存在。  | `{ "Code": 404, "Message": "Resource not found." }` |
| **500**     | 服务器内部错误。              | `{ "Code": 500, "Message": "Server error." }` |

---

## SDK 示例

以下代码片段展示了如何使用官方 Aspose.Cells Cloud SDK（版本 3.13.0）调用该接口。请将占位符（如 `<fileName>`、`<sheet>`、`<jwt token>` 等）替换为您的实际数据。

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new WorksheetsApi();
var name = "test.xlsx"; // string | 文件名。
var sheetName = "Sheet1"; // string | 工作表名。
var folder = "Documents"; // string | 文件夹路径（可选）
var storageName = "MyStorage"; // string | 存储空间名（可选）

try
{
    var response = apiInstance.DeleteWorksheetComments(name, sheetName, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("调用 WorksheetsApi.DeleteWorksheetComments 时发生异常: " + e.Message );
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
    echo '调用 WorksheetsApi->deleteWorksheetComments 时发生异常: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Ruby  

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::WorksheetsApi.new
name = 'test.xlsx'
sheet_name = 'Sheet1'
folder = 'Documents'          # 可选
storage_name = 'MyStorage'    # 可选

begin
  result = api_instance.delete_worksheet_comments(name, sheet_name, folder, storage_name)
  puts result.status
rescue AsposeCellsCloud::ApiError => e
  puts "调用 WorksheetsApi->delete_worksheet_comments 时发生异常: #{e}"
end
```

### Node.js（TypeScript）

```typescript
import { WorksheetsApi } from "@asposecloud/cells-sdk";

const api = new WorksheetsApi();
const name = "test.xlsx";
const sheetName = "Sheet1";
const folder = "Documents";
const storageName = "MyStorage";

api.deleteWorksheetComments(name, sheetName, folder, storageName)
    .then((response) => console.log(response.status))
    .catch((error) => console.error("错误:", error));
```

### Python  

```python
from asposecellscloud import WorksheetsApi

api_instance = WorksheetsApi()
name = "test.xlsx"
sheet_name = "Sheet1"
folder = "Documents"          # 可选
storage_name = "MyStorage"    # 可选

try:
    response = api_instance.delete_worksheet_comments(name, sheet_name, folder, storage_name)
    print(response.status)
except Exception as e:
    print("调用 WorksheetsApi->delete_worksheet_comments 时发生异常:", e)
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
    print "调用 WorksheetsApi->delete_worksheet_comments 时发生异常: $@\n";
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
        fmt.Printf("错误: %v\n", err)
        return
    }
    fmt.Println(resp.Status)
}
```

---

## 注意事项与限制

* 此操作将**删除指定工作表中的所有批注**，请谨慎使用 —— 操作不可撤销。
* 该请求**不接受请求体**；所有必需信息均通过 URL 和请求头传递。
* 若目标文件**受保护**或工作表为**只读**，API 将根据具体原因返回 `400` 或 `401` 错误。
* 该接口适用于存储在 **Aspose Cloud Storage** 中的文件，也支持通过 `storageName` 正确引用的 **Amazon S3**、**Azure Blob** 或 **Google Cloud Storage** 中的文件。

---

## 相关资源

* **OpenAPI 规范** – [DeleteWorksheetComments](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComments)
* **身份验证指南** – [Aspose.Cells Cloud 的 OAuth2](https://docs.aspose.cloud/cells/authentication/)
* **SDK 代码仓库** – <https://github.com/aspose-cells-cloud>
* **通用工作表 API 文档** – <https://docs.aspose.cloud/cells/worksheets/>

---

*最后更新时间：2026‑07‑30*