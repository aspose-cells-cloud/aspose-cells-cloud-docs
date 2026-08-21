---
title: "取消隐藏 Excel 工作表中的行"
second_title: "文档"
linktitle: "取消隐藏"
type: docs
url: /zh/rows/unhide/
aliases: [  /zh/unhide-rows-in-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud、Excel、取消隐藏行、REST API、电子表格、.NET、Java、Python、Node.js、Ruby、Go、PHP、Perl、Swift、Aspose.Cells Cloud REST API"
description: "使用 Aspose.Cells Cloud REST API 取消隐藏 Excel 工作表中的行。该 API 可通过多种 SDK 访问，包括 .NET、Java、Python、Node.js、Ruby、Go、PHP、Perl 和 Swift。"
weight: 50
ArticleTitle: "使用 Aspose.Cells Cloud API 取消隐藏 Excel 工作表中的行"
---

此 REST API 用于取消隐藏 Excel 工作表中的行。

**前提条件：** 在调用此接口之前，请从 Aspose Cloud 认证服务获取有效的 JWT 访问令牌，并确保目标工作簿已上传至受支持的存储空间。

## PostUnhideWorksheetRows API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/unhide
```

### **安全与认证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的认证方式</a>。

### **请求参数**

| 参数名        | 类型     | 位置   | 描述                                      |
| ------------- | -------- | ------ | ----------------------------------------- |
| name          | string   | path   | 工作簿名称。                              |
| sheetName     | string   | path   | 工作表名称。                              |
| startrow      | integer  | query  | 要取消隐藏的首行索引（从 0 开始计数）。   |
| totalRows     | integer  | query  | 要取消隐藏的行数。                        |
| height        | number   | query  | 行高（默认值为 15.0）。                   |
| folder        | string   | query  | 文档所在文件夹。                          |
| storageName   | string   | query  | 存储空间名称。                            |

<a href="https://apireference.aspose.cloud/cells/#/Cells/PostUnhideWorksheetRows" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可用的编程接口，可让您直接通过网页浏览器发起 REST 交互。

**认证说明**  
所有请求必须通过从 Aspose Cloud 认证服务获取的 JWT 访问令牌进行认证。请将令牌置于 `Authorization: Bearer <jwt token>` 请求头中。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/unhide?startrow=1&totalRows=1&height=15" \
 -X POST \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt token>"
# 注意：此接口的 POST 请求体为空
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

**HTTP 状态码说明**

| 状态码 | 含义             | 描述                                           |
| ------ | ---------------- | ---------------------------------------------- |
| 200    | OK（成功）       | 筛选操作成功；响应中包含操作详情。             |
| 400    | Bad Request（错误请求） | 缺失或无效的参数（例如不支持的文件类型）。     |
| 401    | Unauthorized（未授权）  | JWT 令牌无效或缺失。                           |
| 413    | Payload Too Large（请求体过大） | 上传文件超出大小限制。                        |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                         |

如需进一步排查问题，请参阅 [错误处理指南](/error-handling/)。

## 云 SDK 开发套件

使用 SDK 是加速开发进程的最佳方式。SDK 封装了底层细节，让您能够专注于项目核心任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}