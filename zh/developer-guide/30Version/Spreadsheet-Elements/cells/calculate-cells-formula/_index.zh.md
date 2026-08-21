---
title: "计算单元格公式 – Aspose.Cells Cloud API"
type: docs
url: /zh/calculate-cells-formula/
weight: 90
keywords: "Aspose.Cells Cloud, 计算单元格公式, Excel API, REST API, SDK"
description: "通过 Aspose.Cells Cloud REST API（v3.0）计算 Excel 单元格公式。包含端点、参数、cURL 示例及 SDK 代码片段。"
ArticleTitle: "计算单元格公式 – Aspose.Cells Cloud API 文档"
---

## REST API

此 REST API 用于计算 Excel 工作簿中的**单元格公式**。

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/calculate
```

## 安全与身份验证

Aspose.Cells Cloud API 采用安全机制，需使用 [基于 JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

### 请求参数

| 参数名称       | 类型   | 参数位置（路径/查询/请求体） | 描述                                                   |
| -------------- | ------ | ---------------------------- | ------------------------------------------------------ |
| name           | string | path                         | Excel 文件名称（例如：`Book1.xlsx`）。                |
| sheetName      | string | path                         | 包含目标单元格的工作表名称。                           |
| cellName       | string | path                         | 待计算单元格的地址（例如：`A1`）。                     |
| options        | object | body                         | 包含计算选项的 JSON 对象（详见 **Options 对象** 表格）。 |
| folder         | string | query                        | 文件在存储中的文件夹路径。                             |
| storageName    | string | query                        | Aspose Cloud 存储空间的名称。                          |

#### Options 对象

| 字段            | 类型    | 描述                                                               | 默认值  |
| --------------- | ------- | ------------------------------------------------------------------ | ------- |
| CalcStackSize   | string  | 最大计算堆栈大小。                                                 | `"1"`   |
| IgnoreError     | boolean | 若为 `true`，忽略计算错误，并将单元格值设为 `#N/A`。              | `false` |
| Recursive       | boolean | 启用对依赖单元格的递归计算。                                       | `false` |
| Precision       | string  | 数值结果的小数位数。                                               | `"15"`  |
| UseThreading    | boolean | 启用多线程计算。                                                   | `false` |

### **响应**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 状态码**

| 状态码 | 含义            | 描述                                       |
|--------|-----------------|--------------------------------------------|
| 200    | OK（成功）      | 筛选器应用成功；响应包含操作详情。         |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如：不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                      |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。                 |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                   |

## 如何结合 SDK 使用 PostCellCalculate API

### PostCellCalculate API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Cells/PostCellCalculate) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例演示了如何通过 cURL 调用 Cloud API。**首先需通过 `/connect/token` 端点完成身份验证以获取 JWT 令牌**，然后将 `<jwt token>` 替换为实际的令牌值。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/calculate" \
  -d '{"CalcStackSize":"1"}' \
  -X POST \
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

使用 SDK 是加速开发的最佳方式。SDK 抽象了底层细节，使您能够专注于项目任务本身。请查阅 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a> 以获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCellCalculate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCellCalculate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCellCalculate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCellCalculate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCellCalculate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCellCalculate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCellCalculate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCellCalculate.go" >}}

{{< /tab >}}

{{< /tabs >}}