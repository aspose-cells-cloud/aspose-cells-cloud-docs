---
---
title: "添加工作表注释"
description: "使用 Aspose.Cells Cloud REST API（PUT /v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}）向 Excel 工作表中的特定单元格添加注释。"
keywords: "Aspose.Cells, 云 API, 添加工作表注释, Excel, 电子表格, 单元格注释"
weight: 20
api_version: "v3.0"
---

# 添加工作表注释

使用 Aspose.Cells Cloud REST API 向 Excel 工作簿中工作表的特定单元格添加注释。

---

## 前提条件 / 身份验证

* 每个请求都需要一个 **Bearer JWT 令牌**。  
  *获取令牌*：通过 **/connect/token** 端点（参见[身份验证指南](/cells/authentication/)）。  
* 将令牌包含在 `Authorization` 请求头中：

```http
Authorization: Bearer <jwt token>
```

* 所有调用必须通过 **HTTPS** 进行，以保护令牌和数据安全。

---

## HTTP 请求

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### 路径参数

| 名称        | 类型   | 是否必需 | 描述 |
|-------------|--------|----------|-------------|
| `name`      | 字符串 | ✔️ | 工作簿文件名（例如：`test.xlsx`）。 |
| `sheetName` | 字符串 | ✔️ | 工作表名称（例如：`Sheet1`）。 |
| `cellName`  | 字符串 | ✔️ | 目标单元格地址（例如：`A1`）。 |

### 查询参数

| 名称          | 类型   | 是否必需 | 描述 |
|---------------|--------|----------|-------------|
| `folder`      | 字符串 | 可选     | 包含工作簿的文件夹路径。 |
| `storageName` | 字符串 | 可选     | 文件所在的存储服务名称。 |

### 请求体

请求体必须包含一个 **Comment（注释）** 对象，以 JSON 格式表示。

```json
{
  "CellName": "A1",
  "Author": "string",
  "HtmlNote": "string",
  "Note": "string",
  "AutoSize": true,
  "IsVisible": true,
  "Width": 10,
  "Height": 10,
  "TextHorizontalAlignment": "Left",
  "TextOrientationType": "NoRotation",
  "TextVerticalAlignment": "Top"
}
```

**Comment 对象字段说明**

| 字段                      | 类型     | 是否必需 | 描述 |
|---------------------------|----------|----------|-------------|
| `CellName`                | 字符串   | ✔️ | 单元格地址（必须与路径参数 `{cellName}` 的值一致）。 |
| `Author`                  | 字符串   | 可选     | 注释作者姓名。 |
| `HtmlNote`                | 字符串   | 可选     | HTML 格式的注释文本。 |
| `Note`                    | 字符串   | 可选     | 纯文本注释内容。 |
| `AutoSize`                | 布尔值   | 可选     | 是否自动调整注释框大小。 |
| `IsVisible`               | 布尔值   | 可选     | 默认是否显示注释。 |
| `Width` / `Height`        | 数值     | 可选     | 注释框尺寸（单位：点）。 |
| `TextHorizontalAlignment` | 字符串   | 可选     | 水平对齐方式（`Left`、`Center`、`Right`）。 |
| `TextOrientationType`     | 字符串   | 可选     | 文本方向（`NoRotation`、`Rotate90` 等）。 |
| `TextVerticalAlignment`   | 字符串   | 可选     | 垂直对齐方式（`Top`、`Center`、`Bottom`）。 |

---

## cURL 示例

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CellName": "A1",
        "Author": "test",
        "HtmlNote": "<font style=\"font-weight:bold;font-family:Tahoma;font-size:9pt;color:#000000;text-align:left;\">this is a comment</font>",
        "Note": "this is a comment",
        "AutoSize": true,
        "IsVisible": true,
        "Width": 10,
        "Height": 10,
        "TextHorizontalAlignment": "Left",
        "TextOrientationType": "NoRotation",
        "TextVerticalAlignment": "Top"
      }'
```

---

## 响应架构

| 字段     | 类型     | 描述 |
|----------|----------|-------------|
| `Comment` | 对象     | 创建的注释对象（参见上方 **Comment 对象字段说明**，以及链接元数据）。 |
| `Code`    | 整数     | API 返回的 HTTP 状态码（例如：`200`）。 |
| `Status`  | 字符串   | 文本形式的状态消息（例如：`"OK"`）。 |

`Comment` 对象还包含一个 **link（链接）** 子对象：

| 子字段 | 类型   | 描述 |
|--------|----------|-------------|
| `Href` | 字符串   | 注释资源的自引用 URL。 |
| `Rel`  | 字符串   | 关系类型（`self`）。 |
| `Title`| 字符串   | 可选标题（可能为 `null`）。 |
| `Type` | 字符串   | 可选 MIME 类型（可能为 `null`）。 |

---

## 成功响应示例

```json
{
  "Comment": {
    "CellName": "A1",
    "Author": "test",
    "HtmlNote": "<Font Style=\"FONT-WEIGHT: bold;FONT-FAMILY: Tahoma;FONT-SIZE: 9pt;COLOR: #000000;TEXT-ALIGN: left;\">this is a comment</Font>",
    "Note": "this is a comment",
    "AutoSize": true,
    "IsVisible": true,
    "Width": 10,
    "Height": 10,
    "TextHorizontalAlignment": "Left",
    "TextOrientationType": "NoRotation",
    "TextVerticalAlignment": "Top",
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/comments/A1",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

---

## 错误响应

| HTTP 状态码 | 描述 | 示例 |
|-------------|-------------|---------|
| **400** | 请求错误 — 缺少或无效参数。 | `{ "Error": { "Code": "InvalidParameter", "Message": "The 'cellName' parameter is missing or malformed." }, "Code": 400, "Status": "Bad Request" }` |
| **401** | 未授权 — 缺少或无效的令牌。 | `{ "Error": { "Code": "InvalidToken", "Message": "Authentication failed." }, "Code": 401, "Status": "Unauthorized" }` |
| **404** | 未找到 — 工作簿、工作表或单元格不存在。 | `{ "Error": { "Code": "FileNotFound", "Message": "Workbook 'test.xlsx' not found." }, "Code": 404, "Status": "Not Found" }` |
| **500** | 服务器内部错误 — 服务器上发生意外情况。 | `{ "Error": { "Code": "ServerError", "Message": "An unexpected error occurred." }, "Code": 500, "Status": "Internal Server Error" }` |

---

## SDK 示例

以下 SDK 提供了该操作的现成封装。请将占位符值（`<YOUR_TOKEN>`、`<FILE_NAME>` 等）替换为实际数据。

{{< tabs tabTotal="8" tabID="sdk" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// 配置 API 客户端
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new WorksheetsApi(config);

// 准备注释对象
var comment = new Comment
{
    CellName = "A1",
    Author = "test",
    Note = "this is a comment",
    HtmlNote = "<font style=\"font-weight:bold;\">this is a comment</font>",
    AutoSize = true,
    IsVisible = true,
    Width = 10,
    Height = 10
};

try
{
    var response = apiInstance.PutWorksheetComment("test.xlsx", "Sheet1", "A1", comment, folder: null, storageName: null);
    Console.WriteLine(response);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling WorksheetsApi.PutWorksheetComment: " + e.Message );
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.*;
import com.aspose.cells.cloud.model.*;

ApiClient client = new ApiClient();
client.setAppSid("<your_client_id>");
client.setAppKey("<your_client_secret>");

WorksheetsApi worksheetsApi = new WorksheetsApi(client);

Comment comment = new Comment()
        .cellName("A1")
        .author("test")
        .note("this is a comment")
        .htmlNote("<font style=\"font-weight:bold;\">this is a comment</font>")
        .autoSize(true)
        .isVisible(true)
        .width(10)
        .height(10);

try {
    CommentResponse resp = worksheetsApi.putWorksheetComment("test.xlsx", "Sheet1", "A1", comment, null, null);
    System.out.println(resp);
} catch (ApiException e) {
    e.printStackTrace();
}
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppSid('<your_client_id>');
$config->setAppKey('<your_client_secret>');

$apiInstance = new Aspose\Cells\Api\WorksheetsApi(
    new GuzzleHttp\Client(),
    $config
);

$comment = new Aspose\Cells\Model\Comment([
    'CellName' => 'A1',
    'Author'   => 'test',
    'Note'     => 'this is a comment',
    'HtmlNote' => '<font style="font-weight:bold;">this is a comment</font>',
    'AutoSize' => true,
    'IsVisible'=> true,
    'Width'    => 10,
    'Height'   => 10
]);

try {
    $result = $apiInstance->putWorksheetComment('test.xlsx', 'Sheet1', 'A1', $comment);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorksheetsApi->putWorksheetComment: ', $e->getMessage(), PHP_EOL;
}
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.client_id = '<your_client_id>'
config.client_secret = '<your_client_secret>'

api_instance = AsposeCellsCloud::WorksheetsApi.new

comment = AsposeCellsCloud::Comment.new(
  cell_name: 'A1',
  author: 'test',
  note: 'this is a comment',
  html_note: '<font style="font-weight:bold;">this is a comment</font>',
  auto_size: true,
  is_visible: true,
  width: 10,
  height: 10
)

begin
  result = api_instance.put_worksheet_comment('test.xlsx', 'Sheet1', 'A1', comment)
  puts result
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling WorksheetsApi->put_worksheet_comment: #{e}"
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const { WorksheetsApi, Configuration, Comment } = require('asposecellscloud');

let config = new Configuration();
config.clientId = '<your_client_id>';
config.clientSecret = '<your_client_secret>';

let api = new WorksheetsApi(config);

let comment = new Comment({
  CellName: 'A1',
  Author: 'test',
  Note: 'this is a comment',
  HtmlNote: '<font style="font-weight:bold;">this is a comment</font>',
  AutoSize: true,
  IsVisible: true,
  Width: 10,
  Height: 10
});

api.putWorksheetComment('test.xlsx', 'Sheet1', 'A1', comment)
  .then(response => console.log(response))
  .catch(err => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
import asposecellscloud
from asposecellscloud.rest import ApiException
from asposecellscloud.models import Comment

config = asposecellscloud.Configuration()
config.client_id = '<your_client_id>'
config.client_secret = '<your_client_secret>'

api_instance = asposecellscloud.WorksheetsApi(asposecellscloud.ApiClient(config))

comment = Comment(
    CellName='A1',
    Author='test',
    Note='this is a comment',
    HtmlNote='<font style="font-weight:bold;">this is a comment</font>',
    AutoSize=True,
    IsVisible=True,
    Width=10,
    Height=10
)

try:
    api_response = api_instance.put_worksheet_comment('test.xlsx', 'Sheet1', 'A1', comment)
    print(api_response)
except ApiException as e:
    print("Exception when calling WorksheetsApi->put_worksheet_comment: %s\\n" % e)
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::Api::WorksheetsApi;
use AsposeCellsCloud::Object::Comment;

my $config = AsposeCellsCloud::Configuration->new(
    client_id     => '<your_client_id>',
    client_secret => '<your_client_secret>'
);
my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new();

my $comment = AsposeCellsCloud::Object::Comment->new(
    CellName => 'A1',
    Author   => 'test',
    Note     => 'this is a comment',
    HtmlNote => '<font style="font-weight:bold;">this is a comment</font>',
    AutoSize => 1,
    IsVisible=> 1,
    Width    => 10,
    Height   => 10
);

eval {
    my $result = $api_instance->put_worksheet_comment(
        name      => 'test.xlsx',
        sheet_name=> 'Sheet1',
        cell_name => 'A1',
        comment   => $comment
    );
    print $result;
};
if ($@) {
    warn "Exception when calling WorksheetsApi->put_worksheet_comment: $@";
}
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/model"
)

func main() {
    cfg := cellscloud.NewConfiguration()
    cfg.ClientId = "<your_client_id>"
    cfg.ClientSecret = "<your_client_secret>"

    apiInstance := api.NewWorksheetsApi(cfg)

    comment := model.Comment{
        CellName: "A1",
        Author:   "test",
        Note:     "this is a comment",
        HtmlNote: "<font style=\"font-weight:bold;\">this is a comment</font>",
        AutoSize: true,
        IsVisible: true,
        Width: 10,
        Height: 10,
    }

    resp, _, err := apiInstance.PutWorksheetComment("test.xlsx", "Sheet1", "A1", comment, nil, nil)
    if err != nil {
        fmt.Printf("Error: %v\\n", err)
    } else {
        fmt.Printf("Response: %+v\\n", resp)
    }
}
```

{{< /tab >}}

{{< /tabs >}}

---

## 参见

* **获取工作表注释** — `GET /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **更新工作表注释** — `POST /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **删除工作表注释** — `DELETE /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **清空所有注释** — `DELETE /cells/{name}/worksheets/{sheetName}/comments`  

---

## 附加说明

* 该端点路径中包含 **v3.0**。目前已有更新版本 (**v3.1**)，如需使用最新功能，请相应更新基础 URL。  
* 完整的 OpenAPI 定义请参见 [Aspose.Cells Cloud API 参考](/cells/#/Worksheets/PutWorksheetComment)。  
* 请根据 API 规范处理限流（HTTP 429）和重试机制。  

---
---