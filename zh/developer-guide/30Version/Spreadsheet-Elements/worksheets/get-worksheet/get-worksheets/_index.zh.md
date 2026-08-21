---
title: "获取所有工作表"
second_title: "文档"
linktitle: "全部"
type: docs
url: /zh/worksheets/get-all/
aliases: [  /zh/get-worksheet-count/ ]
keywords: "Aspose.Cells, 云 API, 获取工作表, Excel, REST, SDK"
description: "通过 Aspose.Cells Cloud REST API（v3.0）检索 Excel 工作簿中的工作表列表。包含 cURL 示例、SDK 代码片段及响应格式说明。"
weight: 10
---

此 REST API 返回工作簿中包含的工作表信息。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **请求参数**

| 参数名称       | 类型   | 位置   | 描述                         |
| -------------- | ------ | ------ | ---------------------------- |
| name           | string | path   | Excel 文档的名称。           |
| folder         | string | query  | 包含该文档的文件夹。         |
| storageName    | string | query  | 要使用的存储空间的名称。     |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheets) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器发起 REST 请求。

您可以使用 cURL 命令行工具访问 Aspose.Cells Cloud 服务。以下示例展示了获取工作表列表的 GET 请求：

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": {
    "WorksheetList": [
      {
        "link": {
          "Href": "/Sheet1",
          "Rel": "self"
        }
      },
      {
        "link": {
          "Href": "/Sheet2",
          "Rel": "self"
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## 错误处理

此端点返回的典型 HTTP 状态码如下：

| 状态码 | 含义         | 描述                         |
| ------ | ------------ | ---------------------------- |
| 400  | 请求错误     | 缺少必需参数（如 `name`）。  |
| 401  | 未授权       | JWT 令牌无效或缺失。         |
| 404  | 未找到       | 指定的工作簿不存在。         |
| 500  | 服务器内部错误 | 服务器出现意外状况。         |

错误响应以 JSON 格式返回，例如：

```json
{
  "Code": "401",
  "Message": "Invalid access token."
}
```

## 云 SDK 家族

使用 SDK 是加快开发速度的最佳方式。SDK 将处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}