---
title: "更新图表第二值轴"
ArticleTitle: "更新图表第二值轴 – Aspose.Cells Cloud REST API"
type: docs
url: /zh/charts/second-value-axis/update/
weight: 160
keywords: "Aspose.Cells, 图表 API, 第二值轴, Excel, REST, 云 SDK"
description: "使用 Aspose.Cells Cloud REST API 更新 Excel 工作表中图表的第二值轴。包含请求示例、响应代码和前置条件。"
---

此 REST API 用于更新图表的第二值轴。

**前置条件：**  
- 有效的 JWT 访问令牌（参见[身份验证指南](https://docs.aspose.cloud/cells/authentication/)）。  
- 目标 Excel 文件必须存储于 Aspose Cloud 存储中（需提供 `folder`，以及可选的 `storageName`）。  
- 使用 API 版本 v3.0，请确保基础 URL 为 `https://api.aspose.cloud/v3.0`。

## PostChartSecondValueAxis API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **安全与身份验证**

Aspose.Cells Cloud API 具备安全性，需采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称      | 类型     | 位置   | 描述                                              |
| ------------- | -------- | ------ | ------------------------------------------------- |
| name          | string   | path   | Excel 文件名称。                                  |
| sheetName     | string   | path   | 包含图表的工作表名称。                            |
| chartIndex    | integer  | path   | 待修改图表的从零开始的索引。                      |
| axis          | object   | body   | 第二值轴的设置项。                                |
| folder        | string   | query  | 文件所在存储中的文件夹路径。                      |
| storageName   | string   | query  | 存储服务的名称。                                  |

**示例请求体（JSON）：**

```json
{
  "IsAutomaticMajorUnit": true,
  "Maximum": 100,
  "Minimum": 0,
  "MajorUnit": 10,
  "MinorUnit": 2,
  "Title": {
    "Text": "次坐标轴"
  }
}
```

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondValueAxis) 定义了一个公开可访问的编程接口，可让您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**HTTP 状态码**

| 状态码 | 含义             | 描述                                              |
| ------ | ---------------- | ------------------------------------------------- |
| 200    | OK（成功）       | 筛选条件应用成功；响应包含操作详情。              |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如不支持的文件类型）。         |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                             |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超出大小限制。                     |
| 500    | Internal Server Error（内部服务器错误） | 发生意外的服务器错误。                      |

**另请参阅：**  
- [获取图表第二值轴](https://docs.aspose.cloud/cells/charts/second-value-axis/get/)  
- [更新图表值轴](https://docs.aspose.cloud/cells/charts/value-axis/update/)

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，使您能够专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// C# 示例：更新第二值轴
var api = new CellsApi("clientId", "clientSecret");
var axis = new Axis { IsAutomaticMajorUnit = true, Maximum = 100 };
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Java 示例：更新第二值轴
CellsApi api = new CellsApi("clientId", "clientSecret");
Axis axis = new Axis();
axis.setIsAutomaticMajorUnit(true);
axis.setMaximum(100.0);
api.postChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// PHP 示例：更新第二值轴
$api = new CellsApi($clientId, $clientSecret);
$axis = new Axis();
$axis->setIsAutomaticMajorUnit(true);
$axis->setMaximum(100);
$api->postChartSecondValueAxis($name, $sheetName, $chartIndex, $axis);
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Ruby 示例：更新第二值轴
api = AsposeCellsCloud::ApiClient.new(client_id, client_secret)
axis = Axis.new(is_automatic_major_unit: true, maximum: 100)
api.post_chart_second_value_axis(name, sheet_name, chart_index, axis)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Python 示例：更新第二值轴
api = asposecellscloud.ApiClient(client_id, client_secret)
axis = Axis(is_automatic_major_unit=True, maximum=100)
api.post_chart_second_value_axis(name, sheet_name, chart_index, axis)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondValueAxis.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Android（Java）示例 —— 与上述 Java 代码片段相同
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
// Swift 示例：更新第二值轴
let api = CellsApi(clientId: "clientId", clientSecret: "clientSecret")
var axis = Axis()
axis.isAutomaticMajorUnit = true
axis.maximum = 100
api.postChartSecondValueAxis(name: name, sheetName: sheetName, chartIndex: chartIndex, axis: axis)
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Perl 示例：更新第二值轴
my $api = AsposeCellsCloud::ApiClient->new(client_id => $client_id, client_secret => $client_secret);
my $axis = AsposeCellsCloud::Object::Axis->new(isAutomaticMajorUnit => 1, maximum => 100);
$api->post_chart_second_value_axis(name => $name, sheet_name => $sheet_name, chart_index => $chart_index, axis => $axis);
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
// Go 示例：更新第二值轴
api := cells.NewApiClient("clientId", "clientSecret")
axis := cells.Axis{IsAutomaticMajorUnit: true, Maximum: 100}
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis)
```

{{< /tab >}}

{{< /tabs >}}