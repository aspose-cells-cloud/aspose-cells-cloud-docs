---
title: "在 Excel 工作表中添加 OLE 对象"
second_title: "文档"
linktitle: "添加 OLE 对象"
type: docs
url: /oleobjects/add/
aliases: [/add-oleobject-to-excel-worksheet/]
keywords: "添加 OLE 对象, Excel, Aspose.Cells Cloud, REST API, SDK"
description: "使用 Aspose.Cells Cloud REST API 将 OLE 对象添加到 Excel 工作表中。该 API 可直接调用，也可通过 C#、Java、PHP、Ruby、Node.js、Python、Perl 和 Go 的 SDK 调用。"
ArticleTitle: "使用 Aspose.Cells Cloud API 将 OLE 对象添加到 Excel 工作表"
weight: 20
---

Aspose.Cells Cloud API 支持以编程方式操作 Excel 工作簿，包括将 OLE 对象（例如 Word 文档、PDF 文件或其他二进制文件）直接嵌入工作表中。

此 REST API 可将 **OLE 对象** 添加到 Excel 工作表中。

**前置条件** – 您必须拥有有效的 JWT 身份验证令牌，并且在调用端点之前，`oleFile` 或 `imageFile` 所引用的源文件应已上传至指定的存储位置。

## PutWorksheetOleObject API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称          | 类型     | 位置   | 描述                                       |
|-------------------|----------|--------|--------------------------------------------|
| name              | string   | path   | 工作簿文件名。                             |
| sheetName         | string   | path   | 工作表名称。                               |
| oleObject         | object   | body   | OLE 对象定义。                             |
| upperLeftRow      | integer  | query  | 左上角行索引（默认值为 0）。               |
| upperLeftColumn   | integer  | query  | 左上角列索引（默认值为 0）。               |
| height            | integer  | query  | OLE 对象高度（默认值为 0）。               |
| width             | integer  | query  | OLE 对象宽度（默认值为 0）。               |
| oleFile           | string   | query  | OLE 源文件名。                             |
| imageFile         | string   | query  | 预览图像文件名。                           |
| folder            | string   | query  | 包含工作簿的文件夹。                       |
| storageName       | string   | query  | 要使用的存储名称。                         |

**说明** – `upperLeftRow` 和 `upperLeftColumn` 使用从 0 开始的索引。`oleFile`（以及可选的 `imageFile`）必须已存在于目标存储中；否则请求将返回错误。

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/OleObjects/PutWorksheetOleObject) 定义了一个公开可用的编程接口，您可直接从 Web 浏览器执行 REST 交互。

您可以使用 **cURL** 命令行工具调用 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 添加 OLE 对象。**所有生产环境调用必须使用 HTTPS。**

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/oleobjects" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"ImageSourceFullName":"aspose-logo.png", "IsAutoSize":true, "SourceFullName":"Sample_Book2.xls", "UpperLeftRow":15, "Top":10, "UpperLeftColumn":5, "Left":10, "Width":400, "Height":400}'
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

![截图显示嵌入 Excel 工作表中的 OLE 对象](/cells/images/ole-object-example.png)

**可能的 HTTP 状态码**

| 状态码 | 描述                                         |
|--------|----------------------------------------------|
| 200    | OLE 对象添加成功。                           |
| 400    | 请求错误 — 缺少或无效的参数。                |
| 401    | 未授权 — 无效或缺失 JWT 令牌。               |
| 404    | 未找到 — 工作簿、工作表或源文件不存在。      |
| 500    | 服务器内部错误 — 意外失败。                  |

典型的成功响应返回以下 JSON 负载：

```json
{
  "Code": 200,
  "Status": "OK",
  "Data": {
    "OleObjectId": "12345",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Width": 400,
    "Height": 400,
    "SourceFullName": "Sample_Book2.xls",
    "ImageSourceFullName": "aspose-logo.png"
  }
}
```

## 云 SDK 家族

使用 SDK 可加快开发速度。SDK 抽象了底层细节，让您专注于业务逻辑。请参阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}