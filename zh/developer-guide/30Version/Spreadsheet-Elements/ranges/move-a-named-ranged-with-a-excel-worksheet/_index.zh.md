---
title: "使用 Excel 工作表移动命名区域"
second_title: "文档"
linktitle: "移动"
type: docs
url: /zh/ranges/move/
aliases: [  /zh/move-a-named-range-with-an-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, 移动命名区域, Excel 工作表, REST API, 区域移动, SDK 示例"
description: "了解如何使用 Aspose.Cells Cloud REST API v3.0 在 Excel 工作表内移动命名区域，包括端点详情、身份验证、示例和 SDK 代码示例。"
weight: 20
ArticleTitle: "使用 Aspose.Cells Cloud API 在 Excel 工作表中移动命名区域"
---

在需要以编程方式重新组织数据时，移动命名区域是一项常见任务。本节介绍如何使用 Aspose.Cells Cloud REST API 将已定义区域重新定位到同一工作表上的新位置。

此 REST API 可将指定区域移动到 Excel 工作表上的目标区域。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/moveto
```

### 身份验证
该 API 需要通过 Aspose Cloud OAuth 流程获取的 **Bearer JWT 令牌**。请将令牌包含在 `Authorization` 请求头中：

```
Authorization: Bearer <jwt token>
```

该令牌必须具有 **Cells** 作用域。

### 前置条件
- 工作簿必须存储在 Aspose Cloud 存储中。  
- 如果文件不在根目录下，请提供存储名称 (`storageName`) 和文件夹路径 (`folder`)。  
- 使用支持 API 版本 **v3.0** 的最新 Aspose.Cells Cloud SDK。

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 名称             | 类型   | 位置 | 描述 |
|------------------|--------|------|------|
| **name**         | string | path | 工作簿文件名称 |
| **sheetName**    | string | path | 工作表名称 |
| **destRow**      | integer| query| 目标区域的起始行索引（从 0 开始） |
| **destColumn**   | integer| query| 目标区域的起始列索引（从 0 开始） |
| **range**        | object | body | 要移动的源区域的定义 |
| **folder**       | string | query| 工作簿所在文件夹路径 |
| **storageName**  | string | query| Aspose Cloud 存储名称 |

### 请求体

| 字段           | 类型   | 是否必需 | 描述 |
|----------------|--------|----------|------|
| **ColumnCount**| integer| 否 | 源区域中的列数 |
| **ColumnWidth**| integer| 否 | 每列的宽度（以磅为单位） |
| **FirstColumn**| integer| 否 | 源区域首列的零基索引 |
| **FirstRow**   | integer| 否 | 源区域首行的零基索引 |
| **Name**       | string | 否 | 区域名称（若为命名区域） |
| **RefersTo**   | string | 否 | 定义该区域的 A1 样式引用 |
| **RowCount**   | integer| 否 | 源区域中的行数 |
| **RowHeight**  | integer| 否 | 每行的高度（以磅为单位） |
| **Worksheet**  | string | 否 | 包含源区域的工作表名称 |

### 工作流程

1. **上传**工作簿到 Aspose Cloud 存储（如尚未存在）。  
2. **生成**通过 OAuth 端点获取 JWT 令牌。  
3. **构建**描述源区域的 JSON 负载。  
4. **调用**`moveto` 端点，传入所需路径、查询参数及 JSON 请求体。  
5. **验证**响应；成功调用将返回 `200 OK` 状态。

### 示例请求 / 响应

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/moveto?destRow=20&destColumn=20" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{ 
  "ColumnCount": 7,
  "ColumnWidth": 19,
  "FirstColumn": 0,
  "FirstRow": 9,
  "Name": "MyRange",
  "RefersTo": "A10:G10",
  "RowCount": 1,
  "RowHeight": 15,
  "Worksheet": "Sheet1"
}'
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

发生错误时，响应将包含一个可选的 `ErrorMessage` 字段，提供有关失败的详细信息。

**HTTP 状态码**

| 状态码 | 含义               | 描述 |
|--------|--------------------|------|
| 200    | OK（成功）         | 过滤器应用成功；响应包含操作详情。 |
| 400    | Bad Request（错误请求） | 参数缺失或无效（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。 |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。 |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。 |

**响应模式**

| 字段 | 类型 | 描述 |
|------|------|------|
| **Code** | integer | API 返回的类 HTTP 状态码（例如 200） |
| **Status** | string | 结果的文本描述（例如 "OK"） |
| **ErrorMessage** | string（可选） | 调用失败时的人类可读错误详情 |

## 云 SDK 家族

使用 SDK 是加快开发速度的最佳方式。SDK 处理底层细节，使您能专注于项目任务。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 以获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用 various SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMoveTo.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMoveTo.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMoveTo.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMoveTo.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMoveTo.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMoveTo.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMoveTo.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMoveTo.go" >}}

{{< /tab >}}

{{< /tabs >}}