---
title: "将列表对象转换为区域——Aspose.Cells Cloud API"
ArticleTitle: "使用 Aspose.Cells Cloud API 将列表对象转换为区域"
second_title: "文档"
linktitle: "转换"
type: docs
url: /zh/list-objects/to-range/
aliases:
  - /convert-list-object-or-table-to-range/
  - /tables/to-range/
keywords: "Aspose Cells API，将列表对象转换为区域，Excel REST API"
description: "了解如何使用 Aspose.Cells Cloud REST API 将 Excel ListObject（表格）转换为区域。内容包括请求语法、参数、示例 cURL、响应模式、身份验证详情、错误代码以及 SDK 示例。"
weight: 30
---

此 REST API 可将 Excel 工作表中的 **ListObject（表格）** 转换为 **区域（Range）**。

**前置条件：**  
调用端点前，请确保：
- 工作簿已上传至您的 Aspose Cloud 存储空间；
- 工作表中包含目标 ListObject；
- 使用受支持的文件格式（例如 .xlsx、.xlsm）。

## REST API

**身份验证**  
调用此操作时，必须在 `Authorization` 请求头中包含有效的 JWT 令牌。您可通过向 OAuth 2.0 令牌端点发送 POST 请求（附带您的客户端 ID 和客户端密钥）来获取该令牌。该令牌必须包含 `Cells.ReadWrite` 作用域，并在令牌服务返回的有效期内有效。

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/ConvertToRange
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称            | 类型    | 位置   | 是否必填 | 默认值 | 描述                                           |
| ------------------- | ------- | ------ | -------- | ------ | ---------------------------------------------- |
| **name**            | string  | 路径   | 是       | –      | Excel 文件的名称。                             |
| **sheetName**       | string  | 路径   | 是       | –      | 包含 ListObject 的工作表名称。                 |
| **listObjectIndex** | integer | 路径   | 是       | –      | 待转换 ListObject（表格）的从零开始索引。      |
| **folder**          | string  | 查询   | 否       | –      | 文件所在文件夹的路径。                         |
| **storageName**     | string  | 查询   | 否       | –      | 存储服务的名称。                               |

> **注意：** 此操作仅适用于现代 Excel 格式，如 **.xlsx** 和 **.xlsm**。ListObject 不得受保护。有关 ListObjects 的更多信息，请参阅 [ListObjects 概述](/list-objects/)；有关区域操作的详细说明，请参阅 [区域文档](/ranges/)。

### cURL 示例（请求）

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0/ConvertToRange" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>"
```

{{< /tab >}}

#### 响应模式

API 返回 **200 OK** 响应，包含新创建区域的详细信息。

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

| 字段            | 类型    | 描述                                       |
| --------------- | ------- | ------------------------------------------ |
| **Code**        | integer | 类 HTTP 状态码（200 表示成功）。           |
| **Status**      | string  | 文本形式的状态消息。                       |
| **RangeName**   | string  | 分配给所创建区域的名称。                   |
| **Address**     | string  | 区域的完整地址，含工作表名称。             |
| **FirstRow**    | integer | 区域中首行的从零开始索引。                 |
| **FirstColumn** | integer | 区域中首列的从零开始索引。                 |
| **RowCount**    | integer | 区域中的行数。                             |
| **ColumnCount** | integer | 区域中的列数。                             |

**HTTP 状态码**

| 状态码 | 含义            | 描述                                           |
|--------|-----------------|------------------------------------------------|
| 200    | OK（成功）      | 筛选器应用成功；响应包含操作详情。             |
| 400    | Bad Request（请求错误） | 缺失或无效参数（例如不支持的文件类型）。     |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                         |
| 413    | Payload Too Large（载荷过大） | 上传文件超出大小限制。                     |
| 500    | Internal Server Error（内部服务器错误） | 服务器意外错误。                         |

**错误响应模式（示例）：**

```json
{
  "Code": 400,
  "Message": "Invalid listObjectIndex. Index must be between 0 and 5."
}
```

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 开发工具包

使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，使您能专注于项目核心任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectConvertToRange.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectConvertToRange.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectConvertToRange.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectConvertToRange.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectConvertToRange.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectConvertToRange.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectConvertToRange.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectConvertToRange.go" >}}

{{< /tab >}}

{{< /tabs >}}