---
title: "从 Excel 工作表中获取合并单元格 — Aspose.Cells Cloud API"
type: docs
url: /zh/get-mergedcell-from-a-worksheet/
weight: 60
keywords: "Aspose.Cells Cloud, 合并单元格, Excel 工作表, REST API, Aspose.Cells SDK, Excel 合并单元格"
description: "了解如何使用 Aspose.Cells Cloud API（v3.0）从 Excel 工作表中检索合并单元格范围。包含身份验证步骤、完整的 cURL 请求示例、响应模式、错误处理以及 C#、Java、Python 等多种语言的 SDK 示例。"
---

此 REST API 返回 Excel 工作表中**合并单元格**的信息。

> **注意** —— API 对象名称为 **MergedCell**（单数形式）。在文本描述中，我们指的是“合并单元格”这一概念（复数）。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/mergedCells
```

## 安全性与身份验证

Aspose.Cells Cloud API 采用安全机制，需使用 [基于 JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

### 请求参数

| 参数名称       | 类型   | 位置   | 描述                           |
|----------------|--------|--------|--------------------------------|
| **name**       | string | path   | Excel 文件名。                 |
| **sheetName**  | string | path   | 工作表名称。                   |
| **folder**     | string | query  | 包含文档的文件夹。             |
| **storageName**| string | query  | 要使用的存储空间名称。         |

## **响应**

返回 `MergedCellsResponse` 对象。

```json
{
  "Status":"OK",
  "Code":200,
  "MergedCells":{
    "Count": 0,
    "MergedCellList":[
      {
        "Link":{
          "Href":"",
          "Rel":"",
          "Type":"",
          "Title":""
        }
      }
    ]
  }
}
```

**HTTP 状态码**

| 状态码 | 含义               | 描述                                       |
|--------|--------------------|--------------------------------------------|
| 200    | OK（成功）         | 合并单元格查询成功；响应包含操作详情。     |
| 400    | Bad Request（错误请求） | 参数缺失或无效（例如：不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                       |
| 413    | Payload Too Large（请求体过大） | 上传文件大小超出限制。                 |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                 |

## 如何结合 SDK 使用 GetWorksheetMergedCells API

### GetWorksheetMergedCells API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetMergedCells) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 调用。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例演示如何通过 cURL 调用 Cloud API：

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/mergedCells" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MergedCells": {
    "Count": 1,
    "MergedCells": [
      {
      "link": {
            "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/cells/mergedcells/0",
            "Rel": "self"
          }
      }
    ]    
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### 使用 Aspose.Cells Cloud SDK

使用 SDK 是对接 API 的最快开发方式。SDK 自动处理底层细节，使您能专注于业务逻辑。完整的 Aspose.Cells Cloud SDK 列表请参见 [GitHub 仓库](https://github.com/aspose-cells-cloud)。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetMergedCells.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetMergedCells.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetMergedCells.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetMergedCells.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetMergedCells.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetMergedCells.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetMergedCells.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetMergedCells.go" >}}

{{< /tab >}}

{{< /tabs >}}