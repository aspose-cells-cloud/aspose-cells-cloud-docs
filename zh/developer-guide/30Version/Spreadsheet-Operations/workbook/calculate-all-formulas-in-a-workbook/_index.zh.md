---
title: "计算 Excel 工作簿中的所有公式"
second_title: "文档"
linktitle: "计算"
type: docs
url: /zh/calculate-all-formulas-on-an-excel-file/
aliases:
  [/calculate-all-formulas-in-a-workbook/, /workbook/calculate-all-formulas/]
keywords: "Aspose.Cells, 计算公式, Excel API, 云 SDK"
description: "通过 Aspose.Cells Cloud REST API 计算 Excel 工作簿中的每个公式。包含 cURL 示例、请求参数、响应模式、前置条件以及多种编程语言的 SDK 代码片段。"
weight: 140
ArticleTitle: "计算 Excel 工作簿中的所有公式"
---

此 REST API 可计算 Excel 工作簿中的**所有公式**。

**前置条件：** 调用此接口前，请确保您已准备以下内容：
- 有效的 JWT 身份验证令牌。（参见[身份验证指南](/authentication/)。）  
- 您的 Aspose.Cells Cloud 客户端 ID 和密钥。  
- 目标工作簿已上传至指定存储位置。（参见[存储配置](/storage/)。）

## PostWorkbookCalculateFormula API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/calculateformula
```

请求参数如下表所示：

| 参数名称        | 类型               | 位置   | 描述                                                                 |
| --------------- | ------------------ | ------ | -------------------------------------------------------------------- |
| **name**        | string             | path   | 工作簿文件的名称。                                                   |
| **options**     | CalculationOptions | body   | JSON 对象，指定计算设置（如 `CalcStackSize`、`IgnoreError`）。      |
| **ignoreError** | boolean            | query  | 当为 `true` 时，计算过程中出现的错误将被忽略。                       |
| **folder**      | string             | query  | 包含工作簿的文件夹路径。                                             |
| **storageName** | string             | query  | 工作簿所在存储服务的名称。                                           |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookCalculateFormula) 定义了一个公开可访问的编程接口，可让您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/calculateformula?ignoreError=true" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CalcStackSize": 1,
        "IgnoreError": true,
        "PrecisionStrategy": "string",
        "Recursive": true
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "WorkbookUrl": "https://api.aspose.cloud/v3.0/storage/file/Book1.xlsx",
  "ErrorMessage": null
}
```

{{< /tab >}}

{{< /tabs >}}

#### 响应详情

| 字段             | 类型   | 描述                                               |
| ---------------- | ------ | -------------------------------------------------- |
| **Code**         | int    | 类 HTTP 状态码（200 表示成功）。                  |
| **Status**       | string | 结果的简短文字描述（如 `OK`）。                    |
| **WorkbookUrl**  | string | 可下载更新后工作簿的直接 URL。                     |
| **ErrorMessage** | string | 请求失败时的详细错误信息；成功时为 `null`。        |

#### 下一步 / 常见错误

- **处理计算错误** – 设置 `ignoreError=false`，以便在公式无法求值时返回错误响应。
- **注意速率限制** – 检查 `X-RateLimit-Remaining` 响应头；若其值为 `0`，请在重试前暂停等待。
- **HTTP 状态码说明**：
  - `400` – 请求参数无效。
  - `401` – 身份验证失败（JWT 令牌无效或已过期）。
  - `404` – 未找到工作簿。
  - `500` – 服务端错误；若持续出现，请联系 Aspose 支持。

| 状态码 | 含义         | 返回条件                                               |
|--------|--------------|--------------------------------------------------------|
| 400    | 错误请求     | 请求参数无效或 JSON 格式错误。                         |
| 401    | 未授权       | 缺失、无效或过期的 JWT 令牌。                          |
| 404    | 未找到       | 指定的工作簿在存储中不存在。                           |
| 500    | 服务器内部错误 | 服务端意外失败；请联系 Aspose 支持。                   |

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，使您能专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("<clientId>", "<clientSecret>");
var request = new PostWorkbookCalculateFormulaRequest(
    name: "Book1.xlsx",
    folder: "",
    storageName: "",
    ignoreError: true,
    options: new CalculationOptions { CalcStackSize = 1, IgnoreError = true });

var response = api.PostWorkbookCalculateFormula(request);
Console.WriteLine($"Status: {response.Status}");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

CellsApi api = new CellsApi("<clientId>", "<clientSecret>");
PostWorkbookCalculateFormulaRequest request = new PostWorkbookCalculateFormulaRequest()
        .name("Book1.xlsx")
        .ignoreError(true)
        .options(new CalculationOptions().calcStackSize(1).ignoreError(true));

WorkbookResponse result = api.postWorkbookCalculateFormula(request);
System.out.println("Status: " + result.getStatus());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\CellsApi;
use Aspose\Cells\Cloud\Model\CalculationOptions;
use Aspose\Cells\Cloud\Model\PostWorkbookCalculateFormulaRequest;

$api = new CellsApi("<clientId>", "<clientSecret>");
$options = new CalculationOptions([
    "CalcStackSize" => 1,
    "IgnoreError"   => true
]);

$request = new PostWorkbookCalculateFormulaRequest([
    "name"    => "Book1.xlsx",
    "ignoreError" => true,
    "options" => $options
]);

$response = $api->postWorkbookCalculateFormula($request);
echo "Status: " . $response->getStatus();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new("<clientId>", "<clientSecret>")
options = AsposeCellsCloud::CalculationOptions.new(
  calc_stack_size: 1,
  ignore_error: true
)

request = AsposeCellsCloud::PostWorkbookCalculateFormulaRequest.new(
  name: 'Book1.xlsx',
  ignore_error: true,
  options: options
)

response = api.post_workbook_calculate_formula(request)
puts "Status: #{response.status}"
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const {
  CellsApi,
  PostWorkbookCalculateFormulaRequest,
  CalculationOptions,
} = require("asposecellscloud");

const api = new CellsApi("<clientId>", "<clientSecret>");
const options = new CalculationOptions({ CalcStackSize: 1, IgnoreError: true });

const request = new PostWorkbookCalculateFormulaRequest({
  name: "Book1.xlsx",
  ignoreError: true,
  options: options,
});

api.postWorkbookCalculateFormula(request).then((response) => {
  console.log(`Status: ${response.status}`);
});
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
from asposecellscloud import CellsApi, PostWorkbookCalculateFormulaRequest, CalculationOptions

api = CellsApi("<clientId>", "<clientSecret>")
options = CalculationOptions(calc_stack_size=1, ignore_error=True)

request = PostWorkbookCalculateFormulaRequest(
    name="Book1.xlsx",
    ignore_error=True,
    options=options
)

response = api.post_workbook_calculate_formula(request)
print(f"Status: {response.status}")
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::CellsApi;
use AsposeCellsCloud::Object::PostWorkbookCalculateFormulaRequest;
use AsposeCellsCloud::Object::CalculationOptions;

my $api = AsposeCellsCloud::CellsApi->new(
    client_id     => '<clientId>',
    client_secret => '<clientSecret>'
);

my $options = AsposeCellsCloud::Object::CalculationOptions->new(
    CalcStackSize => 1,
    IgnoreError   => JSON::true
);

my $request = AsposeCellsCloud::Object::PostWorkbookCalculateFormulaRequest->new(
    name        => 'Book1.xlsx',
    ignoreError => JSON::true,
    options     => $options
);

my $response = $api->post_workbook_calculate_formula(request => $request);
print "Status: " . $response->{Status} . "\n";
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3/api"
    "github.com/asposecellscloud/asposecellscloud-go/v3/model"
)

func main() {
    cfg := api.NewConfiguration()
    cfg.AddDefaultHeader("client-id", "<clientId>")
    cfg.AddDefaultHeader("client-secret", "<clientSecret>")
    client := api.NewAPIClient(cfg)

    opts := model.CalculationOptions{
        CalcStackSize: 1,
        IgnoreError:   true,
    }

    req := model.PostWorkbookCalculateFormulaRequest{
        Name:        "Book1.xlsx",
        IgnoreError: true,
        Options:     &opts,
    }

    resp, _, err := client.CellsApi.PostWorkbookCalculateFormula(req)
    if err != nil {
        panic(err)
    }
    fmt.Printf("Status: %s\n", resp.Status)
}
```

{{< /tab >}}

{{< /tabs >}}