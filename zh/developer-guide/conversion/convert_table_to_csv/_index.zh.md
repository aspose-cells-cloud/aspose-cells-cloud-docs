---
title: "将表格转换为 CSV"
ArticleTitle: "将表格转换为 CSV – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "将表格转换为 CSV"
type: docs
url: /cells/convert/table/csv
aliases: []
keywords: "将表格转换为 CSV, Aspose.Cells, 云 API"
description: "将本地磁盘上电子表格中的表格转换为 CSV 文件。"
weight: 1
---

## Aspose.Cells Cloud Web 服务的表格转换为 CSV 功能

此方法从本地文件系统读取电子表格文件，将其指定的表格转换为 CSV 文件，并返回转换结果。该方法完全在云服务器上运行，因此无需将文件中间上传至云存储。必须正确指定源文件路径和目标格式，并具备读取源文件的适当权限。若文件缺失、路径不可访问或转换失败，将抛出相应异常。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### 安全与身份验证

Aspose.Cells Cloud API 安全可靠，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称         | 类型   | 路径/查询字符串/HTTP 请求体 | 描述 |
|------------------|--------|-----------------------------|------|
| Spreadsheet      | 文件   | FormData                    | 上传电子表格文件。 |
| worksheet        | 字符串 | 查询字符串                  | 电子表格的工作表名称。 |
| tableName        | 字符串 | 查询字符串                  | 表格名称。 |
| outPath          | 字符串 | 查询字符串                  | （可选）工作簿所在文件夹路径，默认为 null。 |
| outStorageName   | 字符串 | 查询字符串                  | 输出文件存储名称。 |
| fontsLocation    | 字符串 | 查询字符串                  | 使用自定义字体。 |
| AutoRowsFit      | 布尔值 | 查询字符串                  | （可选）自动调整工作表中所有行高。 |
| AutoColumnsFit   | 布尔值 | 查询字符串                  | （可选）自动调整工作表中所有列宽。 |
| region           | 字符串 | 查询字符串                  | 电子表格区域/语言设置（例如 `zh-CN`、`fr-FR`）。影响数字格式、日期解析和区域特定行为。 |
| password         | 字符串 | 查询字符串                  | 打开电子表格文件所需的密码。 |

### 请求体参数

| 参数名称 | 类型 | 描述 |
| -------- | ---- | ---- |
| *无*     | *无* | *无需请求体；文件以 multipart/form-data 形式发送。* |

### 响应

```json
{
  "file": "生成的 CSV 文件的二进制流"
}
```

**响应状态码**

| 状态码 | 含义         | 描述 |
|--------|--------------|------|
| 200    | 成功         | 表格成功转换，并返回 CSV 文件。 |
| 400    | 请求错误     | 请求参数无效或 URL 格式不正确。 |
| 401    | 未授权       | 身份验证失败或未提供凭据。 |
| 404    | 未找到       | 源文件不可访问或不存在。 |
| 413    | 请求实体过大 | 上传的文件超过允许的大小限制。 |
| 500    | 内部服务器错误 | 转换过程中电子表格发生异常。 |

## 如何使用 SDK 调用表格转换为 CSV 功能

### 表格转换为 CSV 规范说明

[表格转换为 CSV API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToCsv) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器执行 REST 调用。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API：

{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}

{< tab tabNum="1" >}

```bash
# 使用 HTTPS 以建立安全连接
curl -v "https://api.aspose.cloud/v4.0/cells/convert/table/csv?worksheet={worksheet}&tableName={tableName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&AutoRowsFit={AutoRowsFit}&AutoColumnsFit={AutoColumnsFit}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "生成的 CSV 文件的二进制流"
}
```

{< /tab >}

{< /tabs >}

### 使用 Aspose Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 抽象了底层细节，使您能专注于项目任务。请查看 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Cloud Web 服务：
`[TBD]`
---