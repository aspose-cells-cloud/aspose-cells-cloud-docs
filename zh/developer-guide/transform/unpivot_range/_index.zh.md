---
title: "UnpivotRange"
ArticleTitle: "UnpivotRange – Aspose.Cells Cloud"
second_title: "文档"
linktype: "docs"
url: /zh/cells/unpivot/range
aliases: []
keywords: "Aspose.Cells, UnpivotRange, API"
description: "交换电子表格中的行与列。"
weight: 10
---

## Aspose.Cells Cloud Web 服务的 UnpivotRange 功能

交换电子表格中的行与列。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/range
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称         | 类型   | 路径/查询字符串/HTTP 请求体 | 描述                                                                                                                                              |
|------------------|--------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | 文件   | FormData                    | 上传电子表格文件。                                                                                                                                |
| worksheet        | 字符串 | 查询字符串                  | 工作表名称。                                                                                                                                      |
| cellArea         | 字符串 | 查询字符串                  | 指定的数据范围。                                                                                                                                  |
| skipEmptyValue   | 布尔值 | 查询字符串                  | 若为 true，则跳过空值。默认值：true。                                                                                                             |
| outPath          | 字符串 | 查询字符串                  | （可选）工作簿所在文件夹路径。默认为 null。                                                                                                       |
| outStorageName   | 字符串 | 查询字符串                  | 输出文件存储名称。                                                                                                                                |
| region           | 字符串 | 查询字符串                  | 电子表格区域/语言设置（例如 `en-US`、`fr-FR`）。影响数字格式化、日期解析及区域特定行为。                                                          |
| password         | 字符串 | 查询字符串                  | 打开电子表格文件所需的密码。                                                                                                                      |

### 请求体参数

| 参数名称 | 类型 | 描述 |
|----------|------|------|
| —        | —    | —    |

### **响应**

```json
{
  "File": "二进制流"
}
```

**响应状态码**

| 状态码 | 含义            | 描述                                   |
|--------|-----------------|----------------------------------------|
| 200    | 成功 (OK)       | 返回去透视后的电子表格文件。             |
| 400    | 请求错误 (Bad Request) | 请求参数无效。                         |
| 401    | 未授权 (Unauthorized) | 身份验证失败。                         |
| 413    | 请求实体过大 (Payload Too Large) | 上传文件超出大小限制。             |
| 500    | 内部服务器错误 (Internal Server Error) | 服务器遇到意外情况。             |

## 如何使用 SDK 调用 UnpivotRange 功能

### UnpivotRange 规范

[UnpivotRange API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{UnpivotRange}) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Cloud Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}

{< tab tabNum="1" >}

```bash
# 使用 HTTPS 以确保连接安全
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/range?worksheet=Sheet1&cellArea=A1:C10&skipEmptyValue=true&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=yourPassword" -X PUT -H "Content-Type: multipart/form-data" -H "Accept: application/octet-stream" -H "Authorization: Bearer <jwt token>" -F 'Spreadsheet=@sample.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "FileUrl": "https://example.com/output/unpivoted.xlsx"
}
```

{< /tab >}

{< /tabs >}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 封装了底层细节，让您专注于项目任务。请查看 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用 various SDK 调用 Aspose.Cells Cloud Web 服务：
 `[TBD]`
---