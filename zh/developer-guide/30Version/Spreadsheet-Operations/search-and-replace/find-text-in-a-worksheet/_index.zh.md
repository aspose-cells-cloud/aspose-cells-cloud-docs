---
title: "在 Excel 工作表中查找文本"
second_title: "文档"
linktitle: "在工作表中查找"
type: docs
url: /zh/worksheets/find-text/
aliases: [  /zh/find-text-in-a-worksheet/ ]
weight: 40
keywords: "Excel, Aspose.Cells Cloud, REST API, 查找文本, 工作表, 电子表格, 搜索"
description: "使用 Aspose.Cells Cloud REST API 在 Excel 工作表中查找文本。该 API 支持多种 SDK 和编程语言。"
---

此 REST API 用于在 Excel 工作表中搜索文本。

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/findText
```


### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。


### 请求参数

| 参数名称     | 类型   | 位置   | 描述           |
| ------------ | ------ | ------ | -------------- |
| name         | string | path   | 文档名称。     |
| sheetName    | string | path   | 工作表名称。   |
| text         | string | query  | 待搜索的文本。 |
| folder       | string | query  | 文档所在文件夹。|
| storageName  | string | query  | 存储名称。     |

### **响应**

```json
{
  "Status":"OK",
  "Code":200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

**HTTP 状态码**

| 状态码 | 含义               | 描述                                             |
|--------|--------------------|--------------------------------------------------|
| 200    | OK（成功）         | 成功应用筛选；响应包含操作详情。                 |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如，不支持的文件类型）。       |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                             |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超出大小限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                             |

## 如何使用 PostWorksheetTextSearch API（结合 SDK）

### PostWorksheetTextSearch API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetTextSearch) 定义了一个公开可访问的编程接口，可让您直接通过网页浏览器执行 REST 交互。

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/findText?text=a" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是开发速度最快的方式。SDK 封装了底层细节，使您可以专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetTextSearch.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetTextSearch.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetTextSearch.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetTextSearch.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetTextSearch.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetTextSearch.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetTextSearch.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetTextSearch.go" >}}

{{< /tab >}}

{{< /tabs >}}