---
title: "创建空 Excel 工作簿"
second_title: "文档"
linktitle: "空工作簿"
type: docs
url: /create-an-empty-excel-file/
aliases:
  [
    /create-an-empty-excel-workbook/,
    /workbook/new/,
    /workbook/create/empty-workbook/,
  ]
keywords: "Aspose.Cells, 云服务, Excel, 空工作簿, REST API, SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API 创建空 Excel 工作簿。包含 cURL 和 SDK 示例。"
weight: 20
ArticleTitle: "使用 Aspose.Cells Cloud API 创建空 Excel 工作簿"
---

此 REST API 用于创建一个**空工作簿**。

## PutWorkbookCreate API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证方式</a>。

### 查询参数

| 参数名         | 类型    | 描述                                           |
| -------------- | ------- | ---------------------------------------------- |
| templateFile   | string  | 用作基础的模板工作簿路径（可选）。             |
| dataFile       | string  | 用于填充工作簿的数据文件路径（可选）。         |
| isWriteOver    | boolean | `true` 表示覆盖已存在的文件；`false` 则否则。 |
| folder         | string  | 创建后工作簿的目标文件夹（可选）。             |
| storageName    | string  | 要使用的存储服务名称。                         |

### 请求体参数

| 参数名 | 类型 | 描述                         |
| ------ | ---- | ---------------------------- |
| data   | file | 要创建的工作簿文件的二进制内容。 |

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

| 状态码 | 含义                     | 返回时机                           |
|------|--------------------------|------------------------------------|
| 200 OK | 工作簿创建成功           | 正常流程                           |
| 201 Created | 工作簿已创建（备用响应） | API 返回已创建状态时             |
| 400 Bad Request | 参数无效 | 客户端错误                         |
| 401 Unauthorized | 缺失或无效令牌 | 身份验证错误                     |
| 409 Conflict | 文件已存在且 `isWriteOver=false` | 与已有文件冲突                   |

## 如何结合 SDK 使用 PutWorkbookCreate API

### PutWorkbookCreate API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate) 定义了一个公开可访问的编程接口，使您能直接通过 Web 浏览器发起 REST 请求交互。

您可使用 **cURL** 命令行工具访问 Aspose.Cells Web 服务。请在请求头中包含 `Authorization` 字段，并附带有效的 OAuth2/JWT 访问令牌。对于空工作簿，请求体为可选项；若您需要上传文件，请添加 `--data-binary @empty.xlsx`，如下所示。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
# 创建名为 newworkbook.xlsx 的空工作簿
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?isWriteOver=false" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     --data-binary @empty.xlsx   # 若需创建真正空的工作簿，请省略本行
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```
{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 抽象了底层细节，让您专注于项目任务本身。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何通过多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreateEmpty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreateEmpty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreateEmpty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreateEmpty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreateEmpty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreateEmpty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreateEmpty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreateEmpty.go" >}}

{{< /tab >}}

{{< /tabs >}}