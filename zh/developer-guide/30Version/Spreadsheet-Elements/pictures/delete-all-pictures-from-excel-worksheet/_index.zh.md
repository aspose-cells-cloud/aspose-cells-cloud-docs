---
title: "删除 Excel 工作表中的所有图片"
second_title: "文档"
linktitle: "清除"
type: docs
url: /zh/pictures/clear/
aliases: [  /zh/delete-all-pictures-from-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, 删除所有图片, 工作表, REST API, 清除图片"
description: "了解如何使用 Aspose.Cells Cloud REST API 通过 cURL 和 SDK 示例删除 Excel 工作表中的所有图片。"
weight: 60
ArticleTitle: "如何使用 Aspose.Cells Cloud 删除 Excel 工作表中的所有图片"
---

此 REST API 将删除工作表中的**所有**图片。

**前置条件**  
- 拥有有效的 OAuth 2.0 访问令牌的 Aspose.Cells Cloud 活跃账户。  
- 需要 API 版本 3.0 或更高版本；早期版本已弃用。  
- 目标 Excel 文件必须存储在受支持的存储位置（默认或自定义）。

**版本兼容性**  
该端点遵循 Cells Cloud 3.0 API 规范。请确保您的客户端库和请求 URL 指向 `api.aspose.cloud/v3.0`。

## DeleteWorksheetPictures API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### **请求参数**

| 参数名称      | 类型   | 位置   | 描述                               |
| ------------- | ------ | ------ | ---------------------------------- |
| name          | string | Path   | Excel 文件的名称。                 |
| sheetName     | string | Path   | 包含图片的工作表名称。             |
| folder        | string | Query  | 文件所在的文件夹。                 |
| storageName   | string | Query  | 存储服务的名称。                   |

### 错误响应

| HTTP 状态码 | 描述                                       |
| ----------- | ------------------------------------------ |
| 401         | 未授权 – 缺少或无效的令牌。               |
| 404         | 未找到 – 指定的文件、工作表或分页索引不存在。 |
| 400         | 错误请求 – 请求语法错误或参数无效。        |
| 500         | 服务器内部错误 – 遇到意外情况。            |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Pictures/DeleteWorksheetPictures) 定义了一个公开可访问的编程接口，可让您直接通过 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用该 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/pictures" \
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

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 开发工具包

使用 SDK 是最快捷的开发方式。SDK 会处理底层细节，让您专注于业务逻辑。请参阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用 various SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPictures.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPictures.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPictures.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPictures.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPictures.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPictures.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPictures.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPictures.go" >}}

{{< /tab >}}

{{< /tabs >}}

**备注**：DELETE 操作不支持分页，且受 Aspose.Cells Cloud API 默认速率限制（每分钟 100 个请求）约束。请相应调整客户端逻辑。

**参见**：  
- [/pictures/delete/](../delete/) – 删除工作表中的某张特定图片。  
- [/pictures/add/](../add/) – 向工作表添加图片。  
---