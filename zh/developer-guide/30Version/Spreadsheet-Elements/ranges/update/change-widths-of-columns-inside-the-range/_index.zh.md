---
title: "修改范围内列的宽度"
ArticleTitle: "修改范围内列的宽度 – Aspose.Cells Cloud API"
second_title: "文档"
linktype: "文档"
type: docs
url: /zh/ranges/update/column-width/
aliases: [  /zh/change-widths-of-columns-inside-the-range/ ]
keywords: "Aspose.Cells, 列宽, REST API, Excel, SDK, 范围, 云服务"
description: "了解如何使用 Aspose.Cells Cloud REST API 或 SDK（C#、Java、Python 等）修改范围内列的宽度。包含 cURL 示例、请求/响应详情及认证步骤。"
weight: 74
---

此 REST API 用于设置指定范围内的列宽。

## 安全与认证
Aspose.Cells Cloud API 采用安全机制，需使用 [基于 JWT Token 的认证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth
```

**前置条件** – 调用该端点前，您必须完成以下步骤：

1. 创建 Aspose Cloud 账户，获取 *客户端 ID* 和 *客户端密钥*。  
2. 通过调用 OAuth 端点（`/connect/token`）获取 JWT Token，Token 将在 `access_token` 字段中返回。  
3. 将目标工作簿上传至您的 Aspose Cloud 存储空间（或确保其已存在于指定文件夹中）。  

请求参数如下：

| 参数名称     | 类型   | 位置   | 描述                     |
|--------------|--------|--------|--------------------------|
| name         | string | path   | 工作簿文件名             |
| sheetName    | string | path   | 工作表名称               |
| value        | number | query  | 所需的列宽数值           |
| range        | object | body   | 定义目标单元格范围的 Range 对象 |
| folder       | string | query  | 工作簿所在文件夹路径     |
| storageName  | string | query  | 存储服务名称             |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeColumnWidth) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例演示如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

<h3 id="request">请求</h3>

```bash
# 调用工作簿 *test.xlsx*、工作表 *Sheet1* 的列宽端点，
# 将选定列的宽度设置为 20 磅。
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/columnWidth?value=20" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "ColumnCount": 7,
        "ColumnWidth": 19,
        "FirstColumn": 0,
        "FirstRow": 9,
        "Name": "string",
        "RefersTo": "string",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

<h3 id="response">响应</h3>

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*可能的错误响应*

| HTTP 状态码 | 描述                         |
|-------------|------------------------------|
| 400         | 请求错误 – JSON 或参数无效   |
| 401         | 未授权 – 缺少或无效的 Token  |
| 404         | 未找到 – 工作簿或工作表不存在 |

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 家族
使用 SDK 是加快开发速度的最佳方式。SDK 会处理底层细节，使您能专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeColumnWidth.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeColumnWidth.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeColumnWidth.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeColumnWidth.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeColumnWidth.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeColumnWidth.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeColumnWidth.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeColumnWidth.go" >}}

{{< /tab >}}

{{< /tabs >}}

## 常见问题

**问：** *调用哪个端点可设置 Excel 工作簿中某范围的列宽？*  
**答：** `POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth`，其中 `{name}` 为工作簿文件名，`{sheetName}` 为目标工作表名称。

**问：** *使用列宽 API 时如何进行身份验证？*  
**答：** 在请求头中添加 `Authorization: Bearer <jwt token>`。通过 Aspose Cloud OAuth 流程（`/connect/token`），使用您的客户端 ID 和客户端密钥获取 JWT Token。

**问：** *若要将 A–C 列的宽度改为 25 磅，应发送怎样的 JSON 请求体？*  
**答：**

```json
{
  "FirstColumn": 0,
  "ColumnCount": 3,
  "FirstRow": 0,
  "RowCount": 1
}
```

同时在请求 URL 中添加查询参数 `value=25`。