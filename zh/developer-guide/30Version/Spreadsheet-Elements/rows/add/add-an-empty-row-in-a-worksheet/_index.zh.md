---
title: "在 Excel 工作表中添加空行"
ArticleTitle: "使用 Aspose.Cells Cloud API 在 Excel 工作表中添加空行"
second_title: "文档"
linktitle: "行"
type: docs
url: /zh/rows/add/row/
aliases: [  /zh/add-an-empty-row-in-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, 添加空行, 工作表, REST API, 插入行, 云电子表格"
description: "使用 Aspose.Cells Cloud REST API 向 Excel 工作表插入空行。支持多种 SDK（C#、Java、Python、Go、PHP、Ruby、Node.js、Perl、Android、Swift），便于快速开发。"
weight: 20
---

此 REST API 可向 Excel 工作表添加新行，将空行插入到指定的从零开始的索引位置。

**前提条件：**  
- 必须在 `Authorization` 请求头中包含有效的 Aspose Cloud 访问令牌（Bearer JWT）。  
- 目标工作簿必须已上传至您的 Aspose Cloud 存储空间，且 `folder` 与 `storageName` 参数应指向其所在位置。

**注意事项：**  
- `rowIndex` 为从零开始的索引；在索引 0 处插入将在工作表顶部添加一行。  
- Excel 工作表最多支持 1,048,576 行；若尝试超出此限制进行插入，将导致错误。

## PutInsertWorksheetRow API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **安全性与身份验证**

Aspose.Cells Cloud API 安全可靠，需采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **请求参数**

| 参数名称     | 类型    | 位置   | 描述                                             |
|------------|-------|------|------------------------------------------------|
| name       | string| path | 工作簿文件名。                                     |
| sheetName  | string| path | 工作表名称。                                       |
| rowIndex   | integer| path| 新行将被插入的从零开始的索引位置。                     |
| folder     | string| query| 包含工作簿的存储空间路径。                           |
| storageName| string| query| 要使用的 Aspose Cloud 存储空间名称。                 |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetRow) 定义了一个公开可访问的编程接口，允许您直接从网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/10" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **注意：** 所有 Aspose.Cells Cloud 接口均需使用 HTTPS 协议；生产环境调用请务必使用安全的 `https://` 方案。

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

**HTTP 状态码**

| 状态码 | 含义             | 描述                                             |
|------|------------------|------------------------------------------------|
| 200  | OK（成功）         | 筛选器应用成功；响应包含操作详情。                      |
| 400  | Bad Request（错误请求） | 缺少或无效参数（例如不支持的文件类型）。                |
| 401  | Unauthorized（未授权）  | 无效或缺失 JWT 令牌。                              |
| 413  | Payload Too Large（请求实体过大） | 上传文件超过大小限制。                            |
| 500  | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                             |

*错误响应示例（例如，当行索引超出工作表限制时）：*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "行索引超出范围。允许的最大行数为：1048576。"
}
```

## 云 SDK 家族

使用 SDK 是加快开发速度的最佳方式。SDK 封装了底层细节，使您能专注于项目任务本身。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}