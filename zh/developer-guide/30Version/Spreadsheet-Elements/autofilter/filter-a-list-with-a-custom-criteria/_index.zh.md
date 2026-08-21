---
title: "在 Excel 工作表中添加自定义筛选条件"
second_title: "文档"
linktitle: "添加自定义筛选"
type: docs
url: /zh/autofilter/add-custom-filter/
aliases: [  /zh/filter-a-list-with-a-custom-criteria/ , /zh/autofilter/add-a-custom-filter/ ]
keywords: "Excel, 自定义筛选, Aspose.Cells Cloud, REST API, 自动筛选, 工作表, 自定义条件"
description: "了解如何使用 Aspose.Cells Cloud REST API 为 Excel 工作表添加自定义筛选条件。内容包括请求详情、cURL 示例以及多种编程语言的 SDK 代码片段。"
weight: 65
ArticleTitle: "在 Excel 工作表中添加自定义条件 – Aspose.Cells Cloud API"
---

此 REST API 使用**自定义条件**筛选列表。

## PutWorksheetCustomFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/custom
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要使用<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数：

| 参数名称       | 类型    | 位置     | 描述                                                                 |
|----------------|---------|----------|----------------------------------------------------------------------|
| name           | string  | path     | Excel 文件名称。                                                     |
| sheetName      | string  | path     | 包含待筛选数据的工作表名称。                                         |
| range          | string  | query    | 应用筛选的单元格区域（例如 `A1:B1`）。                              |
| fieldIndex     | integer | query    | 应用筛选的列的从零开始的索引。                                       |
| operatorType1  | string  | query    | 第一个比较运算符（例如 `LessOrEqual`、`Equal`）。                   |
| criteria1      | string  | query    | 第一个筛选值或表达式。                                               |
| isAnd          | boolean | query    | 若为 `true`，则使用 **AND** 连接两个条件；否则使用 **OR**。         |
| operatorType2  | string  | query    | 第二个比较运算符（可选）。                                           |
| criteria2      | string  | query    | 第二个筛选值或表达式（可选）。                                       |
| matchBlanks    | boolean | query    | 若为 `true`，则在筛选结果中包含空白单元格。                         |
| refresh        | boolean | query    | 若为 `true`，则在应用筛选后强制刷新工作表。                         |
| folder         | string  | query    | 存储中文件所在的文件夹路径。                                         |
| storageName    | string  | query    | 存储服务的名称。                                                     |

### **响应**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                     |
|--------|------------------|------------------------------------------|
| 200    | OK（成功）       | 筛选成功应用；响应包含操作详情。         |
| 400    | Bad Request（错误请求） | 参数缺失或无效（例如，不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                     |
| 413    | Payload Too Large（请求实体过大） | 上传文件超过大小限制。                  |
| 500    | Internal Server Error（内部服务器错误） | 发生意外的服务器错误。                 |

## 如何使用 SDK 调用 PutWorksheetCustomFilter API

### PutWorksheetCustomFilter API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetCustomFilter) 定义了一个公开可用的编程接口，可让您直接通过网页浏览器发起 REST 交互。

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells 网络服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/custom?range=A1:B1&fieldIndex=0&operatorType1=LessOrEqual&criteria1=1" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是最快捷的开发方式。SDK 会处理底层细节，让您专注于项目逻辑。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells 网络服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetCustomFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetCustomFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetCustomFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetCustomFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetCustomFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetCustomFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetCustomFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetCustomFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

有关其他自动筛选操作（例如添加标准筛选或日期筛选），请参阅自动筛选章节中的相关文档页面。