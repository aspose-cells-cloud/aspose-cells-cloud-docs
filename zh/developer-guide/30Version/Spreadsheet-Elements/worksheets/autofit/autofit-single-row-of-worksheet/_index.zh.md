---
title: "在 Excel 工作表中自动调整行高"
second_title: "文档"
linktitle: "行"
type: docs
url: /zh/worksheets/autofit/row/
aliases: [  /zh/autofit-single-row-of-worksheet/ ]
description: "了解如何使用 Aspose.Cells Cloud REST API 对 Excel 工作表中的行进行自动调整。内容包括端点、参数、身份验证、错误处理、cURL 请求及 SDK 示例。"
keywords: "自动调整行高, Aspose.Cells Cloud, Excel API, REST, 工作表, SDK, 电子表格, 云 API"
weight: 30
ArticleTitle: "使用 Aspose.Cells Cloud API 在 Excel 工作表中自动调整行高"
---

此 REST API **自动调整 Excel 工作表中某一行的行高**。

## 安全与身份验证
Aspose.Cells Cloud API 采用安全机制，需要基于 [JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrow
```

### **请求参数**

| 参数名称          | 类型    | 位置   | 描述                                                                                                                                      |
| ----------------- | ------- | ------ | ----------------------------------------------------------------------------------------------------------------------------------------- |
| name              | string  | 路径   | Excel 文件的名称。                                                                                                                        |
| sheetName         | string  | 路径   | 工作表的名称。                                                                                                                            |
| rowIndex          | integer | 查询参数 | 待自动调整的行的从零开始的索引。                                                                                                          |
| firstColumn       | integer | 查询参数 | 操作中包含的首列索引。                                                                                                                    |
| lastColumn        | integer | 查询参数 | 操作中包含的末列索引。                                                                                                                    |
| autoFitterOptions | object  | 请求体 | 控制自动调整行为的对象（例如是否考虑合并单元格、是否换行等）。参见 [AutoFitterOptions](/cells/auto-fitter-options){:rel="noopener" title="控制自动调整行为"}。 |
| folder            | string  | 查询参数 | 文件所在的文件夹路径。                                                                                                                    |
| storageName       | string  | 查询参数 | 存储空间的名称。                                                                                                                          |

**示例 `autoFitterOptions` JSON 请求体**

```json
{
  "IsMergedCells": true,
  "IsWrapped": false,
  "AutoFitMergedCells": true,
  "AutoFitWrappedCells": false
}
```

### 实体定义

| 实体                | 描述                                                         |
| ------------------- | ------------------------------------------------------------ |
| `rowIndex`          | 目标行的从零开始的索引。                                     |
| `firstColumn`       | 自动调整操作的起始列。                                       |
| `lastColumn`        | 自动调整操作的结束列。                                       |
| `autoFitterOptions` | 可选设置，用于影响行的自动调整方式（如合并单元格、换行等）。 |

[OpenAPI 规范](/cells/#/Worksheets/PostAutofitWorksheetRow) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。下面的示例演示如何使用 cURL 调用该 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrow?rowIndex=2&firstColumn=1&lastColumn=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

| 字段   | 描述                                   |
| ------ | -------------------------------------- |
| Code   | `200` – 请求成功。                     |
| Status | `"OK"` – 行已成功完成自动调整。        |

{{< /tab >}}

{{< /tabs >}}

## 错误处理

API 返回标准 HTTP 状态码。此端点的常见错误响应如下：

| HTTP 状态码 | 示例负载                                                  | 含义                                                         |
| ----------- | --------------------------------------------------------- | ------------------------------------------------------------ |
| 400         | `{ "Code": 400, "Message": "Row index out of range." }`   | 提供的 `rowIndex` 超出工作表中行的范围。                     |
| 401         | `{ "Code": 401, "Message": "Invalid or expired token." }` | 身份验证失败 —— 请检查 JWT 令牌并确保请求使用 HTTPS 协议。   |
| 404         | `{ "Code": 404, "Message": "File not found." }`           | 找不到指定的 Excel 文件或工作表。                            |
| 500         | `{ "Code": 500, "Message": "Internal server error." }`    | 发生了意外的服务器端问题。                                   |

## 云 SDK 开发工具包家族

使用 SDK 是最快捷的开发方式。SDK 封装了底层细节，使您能专注于业务逻辑。请参阅 [GitHub 仓库](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"}，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示了如何使用不同语言的 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRow.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRow.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRow.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRow.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2c4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRow.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRow.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRow.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRow.go" >}}
{{< /tab >}}

{{< /tabs >}}

**另请参阅**：[自动调整列宽](/worksheets/autofit/column/)、[自动调整多行](/worksheets/autofit/rows/)、[AutoFitterOptions](/cells/auto-fitter-options)。