---
title: "设置 Excel 工作表缩放比例 – Aspose.Cells Cloud API v3.0"
second_title: "文档"
linktitle: "缩放"
type: docs
url: /zh/worksheets/zoom/
aliases: [  /zh/set-zoom-in-excel-worksheet/ ]
keywords: "Aspose.Cells, Excel 缩放, 工作表缩放, REST API, 云 SDK, Excel 自动化"
description: "了解如何使用 Aspose.Cells Cloud API v3.0 设置工作表缩放比例（10%–400%）。包含 cURL 和 SDK 示例及错误处理方法。"
weight: 20
ArticleTitle: "设置 Excel 工作表缩放比例 – Aspose.Cells Cloud API v3.0"
---

此 REST API 用于设置 Excel 工作表的缩放比例。**需要身份验证**；请在每个请求的 `Authorization` 标头中包含有效的 Bearer JWT 令牌。

## 安全与身份验证
Aspose.Cells Cloud API 采用安全机制，需使用 [基于 JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/zoom
```

### **请求参数**

| 参数        | 类型     | 位置   | 描述                                                         |
| ----------- | -------- | ------ | ------------------------------------------------------------ |
| name        | string   | 路径   | Excel 文件（工作簿）名称。                                   |
| sheetName   | string   | 路径   | 待修改的工作表名称。                                         |
| value       | integer  | 查询   | 缩放百分比（允许范围为 **10–400**，例如 `40` 表示 40%）。    |
| folder      | string   | 查询   | 文件所在文件夹路径。                                         |
| storageName | string   | 查询   | 存储服务名称。                                               |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetZoom) 定义了一个公开可访问的编程接口，您可直接通过网页浏览器进行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例演示如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/zoom?value=40" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
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

**错误响应信息**  
可能的 HTTP 状态码包括：

- `400 Bad Request`（错误请求）——缺少或无效参数。
- `401 Unauthorized`（未授权）——缺少或无效 JWT 令牌。
- `404 Not Found`（未找到）——指定的文件或工作表不存在。
- `500 Internal Server Error`（内部服务器错误）——服务器端出现意外错误。

每个错误响应均返回一个 JSON 主体，其中包含 `Code` 状态码和描述性 `Message` 消息。

## 云 SDK 开发工具包系列

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}

{{< /tab >}}

{{< /tabs >}}