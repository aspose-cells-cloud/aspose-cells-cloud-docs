---
title: "批量拆分"
second: "文档"
type: docs
url: /zh/batch/split
keywords: "批量拆分, Aspose.Cells Cloud, REST API, Excel, PDF, CSV, JSON, 电子表格, 云 SDK"
description: "Aspose.Cells Cloud 批量拆分 API 的文档，支持将电子表格文件拆分为 PDF、CSV 或 JSON 等多种格式。包含请求详情、示例 cURL 命令以及各编程语言的 SDK 使用方法。"
weight: 100
---

此 REST API 可对符合条件的文件执行**批量拆分**操作。

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/split
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称           | 类型               | 路径/查询/字符串/HTTP Body | 描述                           |
|--------------------|--------------------|----------------------------|--------------------------------|
| BatchSplitRequest | BatchSplitRequest  | body                       | 包含拆分选项的请求体负载。     |

### **BatchSplitRequest** 属性

| 名称             | 类型                | 描述                                 | 备注       |
|------------------|---------------------|--------------------------------------|------------|
| SourceFolder     | string              | 包含源文件的文件夹。                 | [可选]     |
| SourceStorage    | string              | 源文件所在存储空间的名称。           | [可选]     |
| MatchCondition   | MatchConditionRequest | 用于筛选需拆分文件的匹配条件。       | [可选]     |
| Format           | string              | 期望的输出格式（例如 pdf、csv）。    | [可选]     |
| FromIndex        | integer             | 拆分起始页码索引。                   | [可选]     |
| ToIndex          | integer             | 拆分结束页码索引。                   | [可选]     |
| OutFolder        | string              | 拆分后文件的输出文件夹。             | [可选]     |
| SaveOptions      | SaveOptions         | 保存输出时的附加选项。               | [可选]     |

### **MatchConditionRequest** 属性

| 名称               | 类型       | 描述                     | 备注       |
|--------------------|------------|--------------------------|------------|
| RegexPattern       | string     | 用于匹配文件名的正则表达式。 | [可选]     |
| FullMatchConditions | string[]  | 精确匹配条件列表。        | [可选]     |

### 请求体参数

| 参数名称 | 类型 | 描述                           |
|----------|------|--------------------------------|
| data     | file | 要创建的工作簿文件的二进制内容。 |

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

| 状态码 | 含义                         | 返回时机                             |
|--------|------------------------------|--------------------------------------|
| 200 OK | 工作簿成功创建               | 正常流程                             |
| 201 Created | 工作簿已创建（替代响应） | API 返回已创建状态时                |
| 400 Bad Request | 参数无效             | 客户端错误                           |
| 401 Unauthorized | 缺少或无效的令牌     | 身份验证错误                         |
| 409 Conflict | 文件已存在且 `isWriteOver=false` | 与已有文件发生冲突              |

## 如何使用 SDK 调用 PostBatchSplit API

### PostBatchSplit API 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/Batch/PostBatchSplit) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/split" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\"}"
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

使用 SDK 是加速开发的最优方式。SDK 负责处理底层细节，让您专注于拆分任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}
---