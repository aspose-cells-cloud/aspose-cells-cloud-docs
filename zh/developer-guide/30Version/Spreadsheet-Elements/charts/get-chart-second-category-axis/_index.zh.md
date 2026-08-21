---
title: "获取图表第二分类轴"
type: docs
url: /zh/charts/second-category-axis/get/
weight: 60
keywords: "获取图表第二分类轴, Aspose.Cells Cloud API, Excel 图表坐标轴, REST API, 第二分类轴, Aspose.Cells"
description: "通过 Aspose.Cells Cloud REST API 获取 Excel 工作表中图表的第二分类轴。包含请求格式、参数、示例 cURL 命令、响应模式、状态码及使用说明。"
ArticleTitle: "获取图表第二分类轴 – Aspose.Cells Cloud API"
---

此 REST API 用于获取图表的**第二分类轴**。

## GetChartSecondCategoryAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称       | 类型    | 参数位置（路径/查询） | 描述                                               |
| -------------- | ------- | --------------------- | -------------------------------------------------- |
| name           | string  | path                  | 存储于云端的 Excel 文件名称。                      |
| sheetName      | string  | path                  | 包含图表的工作表名称。                             |
| chartIndex     | integer | path                  | 请求其坐标轴的图表的从零开始的索引。               |
| folder         | string  | query                 | 存储中文件所在的文件夹路径。                       |
| storageName    | string  | query                 | 要使用的 Aspose Cloud 存储名称（可选）。           |

### **响应**

```json
{
  "Code": 200,
  "Status": "OK",
  "Axis": {
    "Name": "第二分类轴",
    "IsVisible": true,
    "AxisLine": { "Style": "Solid", "Weight": 1 },
    "TickMarks": "Inside",
    "Label": {
      "Font": { "Size": 10, "Color": "#000000" },
      "Format": "General"
    }
  }
}
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                           |
|--------|------------------|------------------------------------------------|
| 200    | OK（成功）       | 操作成功执行；响应包含操作详情。               |
| 400    | Bad Request（错误请求） | 缺少或无效的参数（例如，不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | 无效或缺失 JWT 令牌。                         |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。                    |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                    |

## 如何结合 SDK 使用 GetChartSecondCategoryAxis API

### GetChartSecondCategoryAxis API 规范

**GetChartSecondCategoryAxis** 操作在 [OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Charts/GetChartSecondCategoryAxis) 中定义，支持从 Web 浏览器或任意 HTTP 客户端直接发起 REST 请求。

您可以使用 `cURL` 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 `cURL` 调用该 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis?folder={folder}&storageName={storageName}" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Axis": {
    "Name": "第二分类轴",
    "IsVisible": true,
    "AxisLine": { "Style": "Solid", "Weight": 1 },
    "TickMarks": "Inside",
    "Label": {
      "Font": { "Size": 10, "Color": "#000000" },
      "Format": "General"
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是将该 API 快速集成到项目中的最佳方式。SDK 封装了身份验证、请求构建和响应解析等底层细节，使您能专注于业务逻辑。Aspose.Cells Cloud SDK 的完整列表请参见 [GitHub 仓库](https://github.com/aspose-cells-cloud)。

以下代码示例展示了如何使用不同 SDK 调用**获取图表第二分类轴**操作：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// 配置 API 客户端
var config = new Configuration
{
    ClientId = "<your-client-id>",
    ClientSecret = "<your-client-secret>"
};
var apiInstance = new ChartsApi(config);

// 构建请求
var request = new GetChartSecondCategoryAxisRequest(
    name: "Sample.xlsx",
    sheetName: "Sheet1",
    chartIndex: 0,
    folder: "Documents",
    storageName: null
);

// 执行请求
var response = apiInstance.GetChartSecondCategoryAxis(request);
Console.WriteLine($"Axis Name: {response.Axis.Name}");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.ChartsApi;
import com.aspose.cells.cloud.model.*;
import com.aspose.cells.cloud.model.requests.*;

public class GetSecondCategoryAxis {
    public static void main(String[] args) {
        // 配置 API 客户端
        Configuration config = new Configuration();
        config.setClientId("<your-client-id>");
        config.setClientSecret("<your-client-secret>");

        ChartsApi api = new ChartsApi(config);

        // 构建请求
        GetChartSecondCategoryAxisRequest request = new GetChartSecondCategoryAxisRequest(
                "Sample.xlsx", "Sheet1", 0, "Documents", null);

        // 执行请求
        AxisResponse response = api.getChartSecondCategoryAxis(request);
        System.out.println("Axis Name: " + response.getAxis().getName());
    }
}
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
use Aspose\Cells\Cloud\Sdk\Api\ChartsApi;
use Aspose\Cells\Cloud\Sdk\Configuration;
use Aspose\Cells\Cloud\Sdk\Model\Requests\GetChartSecondCategoryAxisRequest;

// 配置客户端
$config = new Configuration();
$config->setClientId('<your-client-id>');
$config->setClientSecret('<your-client-secret>');

$apiInstance = new ChartsApi($config);

$request = new GetChartSecondCategoryAxisRequest(
    'Sample.xlsx',       // name
    'Sheet1',            // sheetName
    0,                   // chartIndex
    'Documents',         // folder
    null                 // storageName
);

try {
    $result = $apiInstance->getChartSecondCategoryAxis($request);
    echo "Axis Name: " . $result->getAxis()->getName();
} catch (Exception $e) {
    echo 'Exception when calling ChartsApi->getChartSecondCategoryAxis: ', $e->getMessage(), PHP_EOL;
}
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

# 配置 SDK
config = AsposeCellsCloud::Configuration.new
config.client_id = '<your-client-id>'
config.client_secret = '<your-client-secret>'

api_instance = AsposeCellsCloud::ChartsApi.new

begin
  result = api_instance.get_chart_second_category_axis(
    name: 'Sample.xlsx',
    sheet_name: 'Sheet1',
    chart_index: 0,
    folder: 'Documents'
  )
  puts "Axis Name: #{result.axis.name}"
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling ChartsApi->get_chart_second_category_axis: #{e}"
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
import asposecellscloud
from asposecellscloud.rest import ApiException
from asposecellscloud.apis.charts_api import ChartsApi
from asposecellscloud.models import GetChartSecondCategoryAxisRequest

# 配置 API 客户端
config = asposecellscloud.Configuration()
config.client_id = '<your-client-id>'
config.client_secret = '<your-client-secret>'

api_instance = ChartsApi(asposecellscloud.ApiClient(config))

request = GetChartSecondCategoryAxisRequest(
    name='Sample.xlsx',
    sheet_name='Sheet1',
    chart_index=0,
    folder='Documents'
)

try:
    response = api_instance.get_chart_second_category_axis(request)
    print('Axis Name:', response.axis.name)
except ApiException as e:
    print('Exception when calling ChartsApi->get_chart_second_category_axis:', e)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Node.js 示例：使用 Aspose.Cells Cloud SDK
const { ChartsApi, Configuration } = require('asposecellscloud');

const config = new Configuration({
    clientId: '<your-client-id>',
    clientSecret: '<your-client-secret>'
});
const api = new ChartsApi(config);

(async () => {
    try {
        const response = await api.getChartSecondCategoryAxis({
            name: 'Sample.xlsx',
            sheetName: 'Sheet1',
            chartIndex: 0,
            folder: 'Documents'
        });
        console.log('Axis Name:', response.axis.name);
    } catch (error) {
        console.error('Error:', error);
    }
})();
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Android (Java) 示例：使用 Aspose.Cells Cloud SDK for Android
import com.aspose.cells.cloud.sdk.api.ChartsApi;
import com.aspose.cells.cloud.sdk.model.*;
import com.aspose.cells.cloud.sdk.model.requests.*;

public class GetSecondCategoryAxisAndroid {
    public void execute() {
        Configuration config = new Configuration();
        config.setClientId("<your-client-id>");
        config.setClientSecret("<your-client-secret>");

        ChartsApi api = new ChartsApi(config);
        GetChartSecondCategoryAxisRequest request = new GetChartSecondCategoryAxisRequest(
                "Sample.xlsx", "Sheet1", 0, "Documents", null);

        try {
            AxisResponse response = api.getChartSecondCategoryAxis(request);
            System.out.println("Axis Name: " + response.getAxis().getName());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
import AsposeCellsCloud

let config = Configuration(clientId: "<your-client-id>", clientSecret: "<your-client-secret>")
let api = ChartsApi(configuration: config)

let request = GetChartSecondCategoryAxisRequest(
    name: "Sample.xlsx",
    sheetName: "Sheet1",
    chartIndex: 0,
    folder: "Documents",
    storageName: nil
)

api.getChartSecondCategoryAxis(request: request) { result, error in
    if let axis = result?.axis {
        print("Axis Name: \(axis.name ?? "")")
    } else if let err = error {
        print("Error: \(err)")
    }
}
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
use Aspose::Cells::Cloud::Sdk::Api::ChartsApi;
use Aspose::Cells::Cloud::Sdk::Configuration;

my $config = Aspose::Cells::Cloud::Sdk::Configuration->new(
    client_id     => '<your-client-id>',
    client_secret => '<your-client-secret>'
);
my $api = Aspose::Cells::Cloud::Sdk::Api::ChartsApi->new($config);

my $response = $api->get_chart_second_category_axis(
    name        => 'Sample.xlsx',
    sheet_name  => 'Sheet1',
    chart_index => 0,
    folder      => 'Documents'
);
print "Axis Name: " . $response->axis->name . "\n";
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
)

func main() {
    cfg := asposecellscloud.NewConfiguration()
    cfg.ClientId = "<your-client-id>"
    cfg.ClientSecret = "<your-client-secret>"

    apiInstance := api.NewChartsApi(cfg)

    request := asposecellscloud.GetChartSecondCategoryAxisRequest{
        Name:      "Sample.xlsx",
        SheetName: "Sheet1",
        ChartIndex: 0,
        Folder:    "Documents",
        StorageName: nil,
    }

    result, _, err := apiInstance.GetChartSecondCategoryAxis(request)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println("Axis Name:", result.Axis.Name)
}
```

{{< /tab >}}

{{< /tabs >}}