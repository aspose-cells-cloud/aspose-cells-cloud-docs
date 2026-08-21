---
title: "在 Excel 工作表中自动调整多行行高"
second_title: "文档"
linktitle: "行"
type: docs
url: /worksheets/autofit/rows/
aliases: [/autofit-multiple-rows-of-worksheet/]
keywords: "自动调整行高, Excel, Aspose.Cells Cloud, REST API, 工作表, 电子表格"
description: "了解如何使用 Aspose.Cells Cloud REST API 自动调整 Excel 工作表中的多行行高。内容包括请求语法、参数说明、cURL 示例、SDK 代码片段及错误处理。"
weight: 40
ArticleTitle: "在 Excel 工作表中自动调整多行行高 – Aspose.Cells Cloud API 文档"
---

此 REST API 可自动调整 Excel 工作表中行的行高。

## 安全与身份验证
Aspose.Cells Cloud API 安全可靠，需采用 [基于 JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrows
```

### **请求参数**

| 参数名称              | 类型    | 位置   | 描述                                                                                                                                   | 必填  |
| --------------------- | ------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------- | ----- |
| **name**              | string  | 路径   | Excel 文件的名称。                                                                                                                     | ✔     |
| **sheetName**         | string  | 路径   | 工作表的名称。                                                                                                                         | ✔     |
| **autoFitterOptions** | object  | 请求体 | 控制行自动调整方式的选项（例如：忽略隐藏行）。请参阅下方字段简要说明。                                                                  | ✖     |
| **startRow**          | integer | 查询参数 | 首个需自动调整的行（基于 1 的索引）。                                                                                                  | ✔     |
| **endRow**            | integer | 查询参数 | 最后一个需自动调整的行（包含）。                                                                                                       | ✔     |
| **onlyAuto**          | boolean | 查询参数 | 当为 `true` 时，API 仅调整由 Excel 自动计算行高的行；当为 `false` 时，执行完整自动调整。                                               | ✖     |
| **folder**            | string  | 查询参数 | 包含文档的文件夹。                                                                                                                     | ✖     |
| **storageName**       | string  | 查询参数 | 存储服务的名称。                                                                                                                       | ✖     |

**autoFitterOptions** 字段（全部可选）：

- `AutoFitMergedCells` _(boolean)_ – 若为 `true`，计算行高时会考虑合并单元格。
- `IgnoreHidden` _(boolean)_ – 若为 `true`，自动调整过程中将忽略隐藏行。
- `OnlyAuto` _(boolean)_ – 与查询参数 `onlyAuto` 功能相同；若设置该字段，将覆盖查询参数值。

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetRows) 定义了一个公开可访问的编程接口，您可直接通过网页浏览器发起 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrows?startRow=1&endRow=7" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": false}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

典型错误响应包括：

- **400 Bad Request（错误请求）** – 参数值无效或 JSON 请求体格式错误。
- **401 Unauthorized（未授权）** – 缺失或无效的 JWT 令牌。
- **404 Not Found（未找到）** – 指定的文件或工作表不存在。
- **500 Internal Server Error（内部服务器错误）** – 发生意外服务器错误。

**HTTP 状态码**

| 状态码 | 含义                 | 描述                                   |
|--------|----------------------|----------------------------------------|
| 200    | OK（成功）           | 成功应用筛选；响应包含操作详情。       |
| 400    | Bad Request（错误请求） | 参数缺失或无效（例如：不支持的文件类型）。 |
| 401    | Unauthorized（未授权）  | JWT 令牌无效或缺失。                   |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。                 |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                   |

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 家族
使用 SDK 是最快捷的开发方式。SDK 将处理底层细节，让您专注于项目本身。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}