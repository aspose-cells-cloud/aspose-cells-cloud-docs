---
title: "Aspose.Cells Cloud API – 更新图表数值轴（POST /valueaxis）"
description: "使用 Aspose.Cells Cloud REST API 更新 Excel 工作表中图表的数值轴。包含端点、参数、请求体 schema、示例（cURL 和 SDK）、响应及错误处理。"
keywords:
  - Aspose.Cells Cloud
  - 更新图表数值轴
  - REST API
  - Excel 图表轴
  - POST valueaxis
  - cURL 示例
  - SDK
  - JSON 载荷
  - 图表轴设置
last_updated: 2026-07-30
---

# 更新图表数值轴（POST /valueaxis）

**摘要：**  
修改存储于 Aspose Cloud 中的 Excel 工作簿内特定图表的数值轴。您可在单次请求中设置边界、刻度单位、对数缩放及其他轴属性。

---

## 前提条件

1. **JWT 访问令牌** – 按照[身份验证指南](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)中的说明获取令牌。  
2. 目标**工作簿**必须已上传至 Aspose Cloud 存储空间（或默认存储）。  
3. 了解您希望修改的工作表名称及图表的**从零开始索引**（zero-based index）。

---

## 端点

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

*请将占位符替换为您的实际值。*

| 占位符 | 描述 |
|--------|------|
| `{name}` | Excel 文件名称（例如 `Book1.xlsx`）。 |
| `{sheetName}` | 包含图表的工作表名称（例如 `Sheet1`）。 |
| `{chartIndex}` | 图表的从零开始索引（例如 `0`）。 |

---

## 身份验证

该 API 使用 **JWT 令牌身份验证**。请在 `Authorization` 请求头中包含令牌：

```
Authorization: Bearer <jwt token>
```

---

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌身份验证</a>。

## 请求参数

| 名称            | 位置 | 类型   | 必填 | 描述 |
|-----------------|------|--------|------|------|
| **name**        | 路径 | 字符串 | 是   | 云端存储的 Excel 文件名。 |
| **sheetName**   | 路径 | 字符串 | 是   | 包含图表的工作表名称。 |
| **chartIndex**  | 路径 | 整数   | 是   | 待更新图表的从零开始索引。 |
| **axis**        | 请求体 | 对象   | 是   | 轴设置（详见 *请求体 Schema*）。 |
| **folder**      | 查询参数 | 字符串 | 否   | 文件所在云端文件夹路径。 |
| **storageName** | 查询参数 | 字符串 | 否   | 使用的存储服务名称。 |

---

## 请求体 Schema（`axis` 对象）

仅需提供您打算修改的属性。

| 属性           | 类型    | 必填 | 描述 |
|----------------|---------|------|------|
| `minimum`      | 数字    | 否   | 轴的下界。 |
| `maximum`      | 数字    | 否   | 轴的上界。 |
| `majorUnit`    | 数字    | 否   | 主刻度线之间的间隔。 |
| `minorUnit`    | 数字    | 否   | 次刻度线之间的间隔。 |
| `logBase`      | 数字    | 否   | 当 `isLogarithmic` 为 `true` 时所用的对数底数。 |
| `isLogarithmic`| 布尔值  | 否   | 轴是否采用对数刻度。 |
| `displayUnit`  | 字符串  | 否   | 轴上显示的单位标签（例如 `"Thousands"`）。 |
| `tickMark`     | 字符串  | 否   | 刻度线样式（`"inside"`、`"outside"` 等）。 |
| `crossAt`      | 数字    | 否   | 轴与垂直轴相交的位置。 |

### 请求体示例

```json
{
  "minimum": 0,
  "maximum": 200,
  "majorUnit": 20,
  "minorUnit": 5,
  "logBase": 10,
  "isLogarithmic": false,
  "displayUnit": "Units",
  "tickMark": "inside",
  "crossAt": 0
}
```

---

## 请求示例

### cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/<code class=\"placeholder\">{name}</code>/worksheets/<code class=\"placeholder\">{sheetName}</code>/charts/<code class=\"placeholder\">{chartIndex}</code>/valueaxis?folder=<code class=\"placeholder\">{folder}</code>&storageName=<code class=\"placeholder\">{storageName}</code>" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "minimum": 0,
        "maximum": 200,
        "majorUnit": 20,
        "minorUnit": 5,
        "logBase": 10,
        "isLogarithmic": false,
        "displayUnit": "Units",
        "tickMark": "inside",
        "crossAt": 0
      }'
```

### SDK 示例  

{{< tabs tabTotal="10" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var api = new ChartsApi("client_id", "client_secret");
var axis = new Axis()
{
    Minimum = 0,
    Maximum = 200,
    MajorUnit = 20,
    MinorUnit = 5,
    LogBase = 10,
    IsLogarithmic = false,
    DisplayUnit = "Units",
    TickMark = "inside",
    CrossAt = 0
};

var response = api.PostChartValueAxis("Book1.xlsx", "Sheet1", 0, axis);
Console.WriteLine($"Status: {response.Status}");
```
{{< /tab >}}

{{< tab tabNum="2" >}}
```java
import com.aspose.cells.cloud.api.ChartsApi;
import com.aspose.cells.cloud.model.Axis;

ChartsApi api = new ChartsApi("client_id", "client_secret");
Axis axis = new Axis()
        .minimum(0.0)
        .maximum(200.0)
        .majorUnit(20.0)
        .minorUnit(5.0)
        .logBase(10.0)
        .isLogarithmic(false)
        .displayUnit("Units")
        .tickMark("inside")
        .crossAt(0.0);

api.postChartValueAxis("Book1.xlsx", "Sheet1", 0, axis);
System.out.println("Value axis updated.");
```
{{< /tab >}}

{{< tab tabNum="3" >}}
```php
<?php
require 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\ChartsApi;
use Aspose\Cells\Cloud\Model\Axis;

$api = new ChartsApi('client_id', 'client_secret');
$axis = new Axis([
    'minimum' => 0,
    'maximum' => 200,
    'majorUnit' => 20,
    'minorUnit' => 5,
    'logBase' => 10,
    'isLogarithmic' => false,
    'displayUnit' => 'Units',
    'tickMark' => 'inside',
    'crossAt' => 0
]);

$api->postChartValueAxis('Book1.xlsx', 'Sheet1', 0, $axis);
echo "Value axis updated.\n";
?>
```
{{< /tab >}}

{{< tab tabNum="4" >}}
```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::ChartsApi.new('client_id', 'client_secret')
axis = AsposeCellsCloud::Axis.new(
  minimum: 0,
  maximum: 200,
  majorUnit: 20,
  minorUnit: 5,
  logBase: 10,
  isLogarithmic: false,
  displayUnit: 'Units',
  tickMark: 'inside',
  crossAt: 0
)

api.post_chart_value_axis('Book1.xlsx', 'Sheet1', 0, axis)
puts 'Value axis updated.'
```
{{< /tab >}}

{{< tab tabNum="5" >}}
```python
from asposecellscloud import ChartsApi, Axis

api = ChartsApi('client_id', 'client_secret')
axis = Axis(
    minimum=0,
    maximum=200,
    majorUnit=20,
    minorUnit=5,
    logBase=10,
    isLogarithmic=False,
    displayUnit='Units',
    tickMark='inside',
    crossAt=0
)

api.post_chart_value_axis('Book1.xlsx', 'Sheet1', 0, axis)
print('Value axis updated.')
```
{{< /tab >}}

{{< tab tabNum="6" >}}
```javascript
// Node.js 示例
const { ChartsApi, Axis } = require('asposecellscloud');

const api = new ChartsApi('client_id', 'client_secret');
const axis = new Axis({
    minimum: 0,
    maximum: 200,
    majorUnit: 20,
    minorUnit: 5,
    logBase: 10,
    isLogarithmic: false,
    displayUnit: 'Units',
    tickMark: 'inside',
    crossAt: 0
});

api.postChartValueAxis('Book1.xlsx', 'Sheet1', 0, axis)
   .then(response => console.log('Value axis updated.'))
   .catch(err => console.error(err));
```
{{< /tab >}}

{{< tab tabNum="7" >}}
```java
// Android (Java) 示例
ChartsApi api = new ChartsApi("client_id", "client_secret");
Axis axis = new Axis()
        .minimum(0.0)
        .maximum(200.0)
        .majorUnit(20.0)
        .minorUnit(5.0)
        .logBase(10.0)
        .isLogarithmic(false)
        .displayUnit("Units")
        .tickMark("inside")
        .crossAt(0.0);

api.postChartValueAxis("Book1.xlsx", "Sheet1", 0, axis);
```
{{< /tab >}}

{{< tab tabNum="8" >}}
```swift
import AsposeCellsCloud

let api = ChartsApi(clientId: "client_id", clientSecret: "client_secret")
var axis = Axis()
axis.minimum = 0
axis.maximum = 200
axis.majorUnit = 20
axis.minorUnit = 5
axis.logBase = 10
axis.isLogarithmic = false
axis.displayUnit = "Units"
axis.tickMark = "inside"
axis.crossAt = 0

api.postChartValueAxis(name: "Book1.xlsx", sheetName: "Sheet1", chartIndex: 0, axis: axis) { result, error in
    if let error = error {
        print("Error: \\(error)")
    } else {
        print("Value axis updated.")
    }
}
```
{{< /tab >}}

{{< tab tabNum="9" >}}
```perl
use Aspose::Cells::Cloud::Api::ChartsApi;
use Aspose::Cells::Cloud::Model::Axis;

my $api  = ChartsApi->new('client_id', 'client_secret');
my $axis = Axis->new(
    minimum        => 0,
    maximum        => 200,
    majorUnit      => 20,
    minorUnit      => 5,
    logBase        => 10,
    isLogarithmic  => JSON::false,
    displayUnit    => 'Units',
    tickMark       => 'inside',
    crossAt        => 0
);

$api->postChartValueAxis('Book1.xlsx', 'Sheet1', 0, $axis);
print "Value axis updated.\n";
```
{{< /tab >}}

{{< tab tabNum="10" >}}
```go
package main

import (
    "context"
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v2/api"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v2/model"
)

func main() {
    cfg := api.NewConfiguration()
    cfg.AddDefaultHeader("client_id", "client_id")
    cfg.AddDefaultHeader("client_secret", "client_secret")
    client := api.NewAPIClient(cfg)

    axis := model.Axis{
        Minimum:       0,
        Maximum:       200,
        MajorUnit:     20,
        MinorUnit:     5,
        LogBase:       10,
        IsLogarithmic: false,
        DisplayUnit:   "Units",
        TickMark:      "inside",
        CrossAt:       0,
    }

    _, err := client.ChartsApi.PostChartValueAxis(context.Background(), "Book1.xlsx", "Sheet1", 0, axis)
    if err != nil {
        fmt.Println("Error:", err)
    } else {
        fmt.Println("Value axis updated.")
    }
}
```
{{< /tab >}}

{{< /tabs >}}

---

## 响应

### 成功（200）

```json
{
  "Code": 200,
  "Status": "OK"
}
```

响应类型为 `CellsCloudResponse`。

**HTTP 状态码**

| 状态码 | 含义           | 描述 |
|--------|----------------|------|
| 200    | OK（成功）     | 筛选条件已成功应用；响应包含操作详情。 |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。 |
| 413    | Payload Too Large（载荷过大） | 上传文件超出大小限制。 |
| 500    | Internal Server Error（内部服务器错误） | 意外服务器错误。 |
---

## 其他资源

- **OpenAPI 规范** – [查看 / 下载 JSON-YAML](https://apireference.aspose.cloud/cells/#/Charts/PostChartValueAxis)  
- **SDK 仓库** – <https://github.com/aspose-cells-cloud>  
- **身份验证指南** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>

---

*如有任何疑问或反馈，请联系 Aspose.Cells Cloud 支持团队。*
---