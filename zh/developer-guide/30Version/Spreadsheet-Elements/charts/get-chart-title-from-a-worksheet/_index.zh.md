---
title: "从工作表中获取图表标题"
type: docs
url: /charts/title/get/
aliases: [/get-chart-title-from-a-worksheet/]
weight: 120
keywords:
  - "Aspose.Cells Cloud"
  - "Chart Title"
  - "Excel"
  - "REST API"
  - "Get Chart Title"
  - "cURL"
  - "SDK"
  - "Excel chart automation"
  - "GET chart title"
description: "了解如何使用 Aspose.Cells Cloud REST API 从 Excel 工作表中检索图表标题。包含端点、参数、身份验证、示例 cURL 和 SDK 代码。"
ArticleTitle: "从工作表中获取图表标题"
---

此 REST API 可检索存储在 Excel 工作簿工作表中的图表标题。

**前提条件**：调用此端点前，您必须持有有效的 Aspose.Cells Cloud OAuth2/JWT 访问令牌，且该令牌需具备 `Cells.Read` 权限范围。工作簿必须已上传至指定的存储位置。

## GetWorksheetChartTitle API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### 安全与身份验证

Aspose.Cells Cloud API 安全可靠，采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称      | 类型     | 位置   | 描述                           |
| ------------- | -------- | ------ | ------------------------------ |
| name          | string   | path   | 工作簿文件名称。               |
| sheetName     | string   | path   | 包含图表的工作表名称。         |
| chartIndex    | integer  | path   | 图表的从零开始的索引。         |
| folder        | string   | query  | 工作簿所在的文件夹路径。       |
| storageName   | string   | query  | 存储服务的名称。               |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChartTitle) 定义了一个公开可用的编程接口，可让您直接通过 Web 浏览器执行 REST 交互。

您可使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/charts/0/title" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Title": {
    "Text": "第一季度销售额",
    "Font": {
      "Name": "Arial",
      "Size": 12,
      "IsBold": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**响应字段**

| 字段                | 描述                               |
| ------------------- | ---------------------------------- |
| `Title.Text`        | 用作图表标题的实际文本。           |
| `Title.Font.Name`   | 标题所用字体族（例如 _Arial_）。   |
| `Title.Font.Size`   | 字体大小（单位：磅）。             |
| `Title.Font.IsBold` | 指示标题文本是否为粗体。           |

**响应状态码**

| 状态码 | 描述                             |
| ------ | -------------------------------- |
| 200 OK | 图表标题已成功检索。             |
| 401 Unauthorized | 身份验证失败，或令牌缺失/无效。  |
| 404 Not Found | 指定的工作簿、工作表或图表不存在。 |
| 500 Internal Server Error | 发生了意外的服务器错误。         |

**注意事项**：图表索引为从零开始；请确保图表存在。若工作簿尚未上传，请先通过相应 API 上传。

**在脚本中提取标题的方法（使用 `jq`）**

```bash
# 假设 JSON 响应已保存至 response.json
title=$(jq -r '.Title.Text' response.json)
echo "图表标题：$title"
```

## 云 SDK 开发工具包（SDK Family）

使用 SDK 是加快开发速度的最佳方式。SDK 会处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// C# 示例：使用 Aspose.Cells Cloud SDK
var config = new Configuration
{
    AccessToken = "<jwt token>",
    BasePath = "https://api.aspose.cloud"
};
var api = new ChartsApi(config);
var response = api.GetWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, folder: "", storageName: "");
Console.WriteLine(response.Title.Text);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Java 示例：使用 Aspose.Cells Cloud SDK
Configuration config = new Configuration();
config.setAccessToken("<jwt token>");
config.setBasePath("https://api.aspose.cloud");
ChartsApi api = new ChartsApi(config);
ChartTitleResponse response = api.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "");
System.out.println(response.getTitle().getText());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
// PHP 示例：使用 Aspose.Cells Cloud SDK
$config = new Aspose\Cells\Configuration();
$config->setAccessToken('<jwt token>');
$config->setHost('https://api.aspose.cloud');
$apiInstance = new Aspose\Cells\Api\ChartsApi($config);
$response = $apiInstance->getWorksheetChartTitle('Book1.xlsx', 'Sheet1', 0, '', '');
echo $response->getTitle()->getText();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Ruby 示例：使用 Aspose.Cells Cloud SDK
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '<jwt token>'
config.host = 'https://api.aspose.cloud'

api_instance = AsposeCellsCloud::ChartsApi.new
result = api_instance.get_worksheet_chart_title('Book1.xlsx', 'Sheet1', 0, '', '')
puts result.title.text
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Python 示例：使用 Aspose.Cells Cloud SDK
from asposecellscloud import ChartsApi, Configuration

config = Configuration()
config.access_token = "<jwt token>"
config.host = "https://api.aspose.cloud"

api_instance = ChartsApi(config)
response = api_instance.get_worksheet_chart_title("Book1.xlsx", "Sheet1", 0, "", "")
print(response.title.text)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Node.js 示例：使用 Aspose.Cells Cloud SDK
const { ChartsApi, Configuration } = require('asposecellscloud');

let config = new Configuration();
config.accessToken = "<jwt token>";
config.basePath = "https://api.aspose.cloud";

let apiInstance = new ChartsApi(config);
apiInstance.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "", (error, data) => {
    if (error) console.error(error);
    else console.log(data.title.text);
});
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Android（Java）示例：使用 Aspose.Cells Cloud SDK
Configuration config = new Configuration();
config.setAccessToken("<jwt token>");
config.setBasePath("https://api.aspose.cloud");
ChartsApi api = new ChartsApi(config);
ChartTitleResponse response = api.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "");
Log.d("ChartTitle", response.getTitle().getText());
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
// Swift 示例：使用 Aspose.Cells Cloud SDK
import AsposeCellsCloud

let config = Configuration()
config.accessToken = "<jwt token>"
config.host = "https://api.aspose.cloud"

let api = ChartsApi(configuration: config)
api.getWorksheetChartTitle(name: "Book1.xlsx", sheetName: "Sheet1", chartIndex: 0, folder: "", storageName: "") { result, error in
    if let title = result?.title?.text {
        print("图表标题：\(title)")
    }
}
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Perl 示例：使用 Aspose.Cells Cloud SDK
use AsposeCellsCloud::ChartsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new();
$config->{access_token} = '<jwt token>';
$config->{host} = 'https://api.aspose.cloud';

my $api_instance = AsposeCellsCloud::ChartsApi->new($config);
my $result = $api_instance->get_worksheet_chart_title('Book1.xlsx', 'Sheet1', 0, '', '');
print $result->{title}{text}, "\n";
```

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e1b22ed45ca780faa3231c3a8c60ddd4" >}}

{{< /tab >}}

{{< /tabs >}}

您还可参考各 SDK 的独立文档，了解更高级的场景，例如更新或删除图表标题。

**另请参阅**： [更新图表标题](/charts/title/put/)、 [删除图表标题](/charts/title/delete/)。