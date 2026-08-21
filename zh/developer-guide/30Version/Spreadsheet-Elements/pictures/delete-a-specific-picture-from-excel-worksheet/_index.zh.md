---
title: "从 Excel 工作表中删除图片 – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "删除"
type: docs
url: /pictures/delete/
aliases: [/delete-a-specific-picture-from-excel-worksheet/]
keywords: "Aspose.Cells, 云 API, 删除图片, Excel 工作表, REST"
description: "使用 Aspose.Cells Cloud REST API 从 Excel 工作表中删除图片。了解 DELETE 端点、所需参数、身份验证、错误代码及示例代码。"
weight: 50
ArticleTitle: "从 Excel 工作表中删除图片 – Aspose.Cells Cloud API"
---

此 REST API 可用于从 Excel 工作表中删除图片。

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### 请求参数

| 参数名称      | 类型    | 位置   | 必需 | 描述                                   |
| ------------- | ------- | ------ | ---- | -------------------------------------- |
| name          | string  | path   | 是   | 工作簿文件的名称。                     |
| sheetName     | string  | path   | 是   | 包含图片的工作表名称。                 |
| pictureIndex  | integer | path   | 是   | 待删除图片的从零开始的索引。           |
| folder        | string  | query  | 否   | 工作簿所在的文件夹。                   |
| storageName   | string  | query  | 否   | 存储服务的名称（可选）。               |

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 发起调用。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**示例响应头**

| 头部          | 值                            |
|---------------|-------------------------------|
| Content-Type  | application/json              |
| Content-Length| （长度不固定）                |
| Date          | （服务器时间）                |

{{< /tab >}}

{{< /tabs >}}

### 错误处理

| HTTP 状态码 | 含义                                               | 示例错误响应体                                                |
| ----------- | -------------------------------------------------- | ------------------------------------------------------------- |
| 200         | 图片删除成功。                                     | `{ "Code": 200, "Status": "OK" }`                             |
| 400         | 请求错误 – 参数无效。                              | `{ "Code": 400, "Message": "Invalid pictureIndex." }`         |
| 401         | 未授权 – 缺失或无效的令牌。                        | `{ "Code": 401, "Message": "Access token is missing or invalid." }` |
| 404         | 未找到 – 工作簿、工作表或图片不存在。              | `{ "Code": 404, "Message": "Resource not found." }`           |
| 500         | 服务器内部错误。                                   | `{ "Code": 500, "Message": "Unexpected server error." }`      |

## 云 SDK 开发套件家族

使用 SDK 是最快捷的开发方式。SDK 将处理底层细节，让您专注于项目本身。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同语言的 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}