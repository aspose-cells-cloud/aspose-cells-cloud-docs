---
title: "批量转换 Excel 文件"
second_title: "文档"
type: docs
url: /batch/convert
keywords: "批量转换, Excel, Aspose.Cells Cloud, REST API, PDF, CSV, JSON, Markdown, 电子表格"
description: "了解如何使用 Aspose.Cells Cloud API 将多个 Excel 文件批量转换为 PDF、CSV、JSON 或 Markdown 等格式。本指南包含 REST 端点详情、请求参数、cURL 示例以及多种编程语言的 SDK 代码片段。"
weight: 100
---

此 REST API 支持对符合条件的文件进行**批量转换**。

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/convert
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称              | 类型   | 位置 | 描述                                           |
|----------------------|--------|------|------------------------------------------------|
| **batchConvertRequest** | 对象 | body | 包含转换设置的请求体。                         |

#### BatchConvertRequest 属性

| 名称              | 类型                | 描述                                           | 说明 |
|-------------------|---------------------|------------------------------------------------|------|
| **SourceFolder**  | 字符串              | 包含源 Excel 文件的文件夹路径。                | [可选] |
| **MatchCondition** | MatchConditionRequest | 用于选择需转换文件的匹配条件。                 | [可选] |
| **Format**        | 字符串              | 转换目标格式（例如：`pdf`、`csv`）。           | [可选] |
| **OutFolder**     | 字符串              | 转换后文件的保存目标文件夹。                   | [可选] |
| **SaveOptions**   | SaveOptions         | 控制文件保存方式的附加选项。                   | [可选] |

#### MatchConditionRequest 属性

| 名称                 | 类型       | 描述                                          | 说明 |
|----------------------|------------|-----------------------------------------------|------|
| **RegexPattern**     | 字符串     | 用于过滤文件名的正则表达式。                  | [可选] |
| **FullMatchConditions** | 字符串数组 | 用于精确匹配的文件名条件列表。               | [可选] |

### 请求体参数

| 参数名称 | 类型 | 描述                               |
| -------- | ---- | ---------------------------------- |
| data     | 文件 | 要创建的工作簿文件的二进制内容。   |

### **响应**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**HTTP 状态码**

| 状态码 | 含义                   | 返回时机                         |
|--------|------------------------|----------------------------------|
| 200 OK | 工作簿创建成功         | 正常流程                         |
| 201 Created | 工作簿已创建（替代响应） | API 返回已创建状态时         |
| 400 Bad Request | 参数无效 | 客户端错误                       |
| 401 Unauthorized | 缺失或无效的令牌 | 身份验证错误                   |
| 409 Conflict | 文件已存在且 `isWriteOver=false` | 与现有文件冲突 |

## 如何结合 SDK 使用 PostBatchConvert API

### PostBatchConvert API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/PostBatchConvert) 定义了一个公开可访问的编程接口，可让您直接通过网页浏览器发起 REST 调用。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/convert" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\",\"SaveOptions\":{\"SaveFormat\":\"pdf\",\"CalculateFormula\":true,\"EnableHTTPCompression\":true,\"OnePagePerSheet\":true,\"CreateDirectory\":false,\"Compliance\":\"None\"}}"
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

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Batch-Convet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Batch-Convet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-Batch-Convet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Batch-Convet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Batch-Convet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Batch-Convet.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Batch-Convet.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d763dc80b0aff6275403dc1d82ad59a5" "Examples-Batch-Convet.go" >}}

{{< /tab >}}

{{< /tabs >}}