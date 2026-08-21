---
title: "取消透视表"
ArticleTitle: "取消透视表 – Aspose.Cells Cloud API"
second_title: "文档"
linktype: "取消透视表"
type: docs
url: /cells/unpivot/table
aliases: []
keywords: "Aspose.Cells, 取消透视, 转换"
description: "交换电子表格中的行和列。"
weight: 1
---

## Aspose.Cells Cloud Web 服务的取消透视表功能

交换电子表格中的行和列。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/table
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称         | 类型    | 路径/查询字符串/HTTP 正文 | 描述                                                                                                     |
|------------------|---------|---------------------------|----------------------------------------------------------------------------------------------------------|
| Spreadsheet      | 文件    | FormData                  | 上传电子表格文件。                                                                                       |
| worksheet        | 字符串  | 查询参数                  | 工作表名称。                                                                                             |
| index            | 整数    | 查询参数                  | 指定的数据范围。                                                                                         |
| skipEmptyValue   | 布尔值  | 查询参数                  | 是否跳过空值（默认值：true）。                                                                          |
| outPath          | 字符串  | 查询参数                  | （可选）工作簿保存的文件夹路径，默认为 null。                                                          |
| outStorageName   | 字符串  | 查询参数                  | 输出文件的存储名称。                                                                                    |
| region           | 字符串  | 查询参数                  | 电子表格区域/语言设置（例如 `zh-CN`、`fr-FR`），影响数字格式、日期解析及区域性特定行为。                |
| password         | 字符串  | 查询参数                  | 打开电子表格文件所需的密码。                                                                            |

### 请求体参数

| 参数名称 | 类型 | 描述 |
| -------- | ---- | ---- |
| N/A      | N/A  | 无请求体参数。 |

### **响应**

```json
{
  "File": "取消透视后电子表格的二进制流"
}
```

**响应状态码**

| 状态码 | 含义           | 描述                                 |
|--------|----------------|--------------------------------------|
| 200    | OK（成功）     | 返回取消透视后的电子表格文件。       |
| 400    | Bad Request    | 请求参数无效。                       |
| 401    | Unauthorized   | 身份验证失败，或 JWT 令牌缺失/无效。 |
| 413    | Payload Too Large | 上传文件超出允许的大小限制。      |
| 500    | Internal Server Error | 服务器内部意外错误。           |

## 如何使用 SDK 实现取消透视表功能

### 取消透视表规范

[取消透视表 API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4# /Transform/UnpivotTable) 定义了一个公开可访问的编程接口，可让您直接在 Web 浏览器中执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例演示如何通过 cURL 调用 Cloud API。

{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}

{< tab tabNum="1" >}

```bash
# 使用 HTTPS 以确保安全连接
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/table?worksheet={worksheet}&index={index}&skipEmptyValue={skipEmptyValue}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}" \
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
  "File": "取消透视后电子表格的二进制流"
}
```

{< /tab >}

{< /tabs >}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最快方式。SDK 封装了底层细节，让您专注于项目任务。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 代码仓库</a>，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Cloud Web 服务：
 `[待定]`
---