---
title: "自动调整 Excel 工作簿中的行高"
second_title: "文档"
linktitle: "行"
type: docs
url: /zh/autofit-rows-on-an-excel-file/
aliases: [  /zh/auto-fit-rows-in-excel-workbooks/ , /zh/workbook/autofit/rows/ ]
keywords: "自动调整行高, Excel 工作簿, Aspose.Cells Cloud, REST API, 自动调整选项"
description: "了解如何使用 Aspose.Cells Cloud REST API 自动调整 Excel 工作簿中的行高。包含端点、参数、cURL 示例以及 C#、Java、Python 等多种语言的 SDK 代码片段。"
weight: 90
ArticleTitle: "自动调整 Excel 工作簿中的行高 – Aspose.Cells Cloud API"
---

**前提条件**  
调用 API 前，请从 Aspose 身份验证服务获取有效的 Bearer JWT 令牌，并确保目标工作簿已存储在受支持的存储位置（默认存储或您已配置的自定义存储）。

此 REST API 可帮助您对 Excel 工作簿执行**自动调整行高**操作，即在数据插入或修改后自动调整行高。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitrows
```

请求参数说明如下：

| 参数名称          | 类型              | 位置   | 描述                                                                 |
| ----------------- | ----------------- | ------ | -------------------------------------------------------------------- |
| name              | string            | path   | 工作簿文件名称。                                                     |
| autoFitterOptions | AutoFitterOptions | body   | 控制自动调整行为的选项。                                             |
| startRow          | integer           | query  | 需要自动调整的第一行索引。                                           |
| endRow            | integer           | query  | 需要自动调整的最后一行索引。                                         |
| firstColumn       | integer           | query  | 自动调整时考虑的第一列索引。                                         |
| lastColumn        | integer           | query  | 自动调整时考虑的最后一列索引。                                       |
| onlyAuto          | boolean           | query  | 若为 **true**，仅处理设置了 AutoFit 标志的行（默认值为 **false**）。 |
| folder            | string            | query  | 工作簿所在的文件夹路径。                                             |
| storageName       | string            | query  | 存储服务的名称。                                                     |

**AutoFitterOptions** 是一个对象，用于指定自动调整操作的行为方式（例如 `AutoFitMergedCells`、`IgnoreHidden`）。

**HTTP 状态码**

| 状态码 | 含义            | 描述                                             |
| ------ | --------------- | ------------------------------------------------ |
| 200    | OK（成功）      | 自动调整成功；响应包含操作详情。                 |
| 400    | Bad Request     | 缺少或无效参数（例如，不支持的文件类型）。       |
| 401    | Unauthorized    | JWT 令牌无效或缺失。                             |
| 413    | Payload Too Large | 上传文件超出大小限制。                         |
| 500    | Internal Server Error | 服务器内部意外错误。                         |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookRows) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 请求。

您可以使用 cURL 命令行工具调用 Aspose.Cells Web 服务。请将 `<jwt token>` 替换为您从 Aspose 身份验证服务获取的有效 Bearer JWT 令牌。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitrows" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*示例错误响应（例如，工作簿不存在）：*

```json
{
  "Code": 404,
  "Status": "Not Found",
  "Message": "指定的工作簿 'myWorkbook.xlsx' 不存在。"
}
```

{{< /tab >}}

{{< /tabs >}}

**注意事项**  
- 当 `AutoFitMergedCells` 设置为 **true** 时，合并单元格在自动调整过程中将被视为单一实体。  
- 若将 `IgnoreHidden` 设置为 **true**，将跳过隐藏的行与列，保留其当前尺寸。

## 云 SDK 家族

使用 SDK 是开发速度最快的方案。SDK 抽象了底层细节，让您能更专注于项目本身。如需查看 Aspose.Cells Cloud SDK 的完整列表，请访问 [GitHub 仓库](https://github.com/aspose-cells-cloud)。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookRows.go" >}}

{{< /tab >}}

{{< /tabs >}}