---
title: "从 Excel 工作表中获取文本项"
second_title: "文档"
linktitle: "在工作表中获取文本项"
type: docs
url: /worksheets/get-text-items/
aliases: [/get-text-items-from-a-worksheet/]
weight: 20
keywords: "Aspose.Cells, 云 API, Excel, 工作表, 文本项, REST"
description: "使用 Aspose.Cells Cloud REST API 从 Excel 文件的特定工作表中检索所有文本项。包含 cURL 示例、SDK 代码、身份验证步骤及响应模式。"
ArticleTitle: "从 Excel 工作表中获取文本项"
---

## REST API

此 REST API 用于读取 Excel 文件中工作表的文本项。

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{worksheet}/textItems
```

### 安全与身份验证
Aspose.Cells Cloud API 采用安全机制，需使用 [基于 JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

### 请求参数


| 参数名称     | 类型   | 位置   | 必填 | 描述                                |
|------------|------|------|----|-----------------------------------|
| name       | string | path | 是  | 工作簿文件名。                         |
| sheetName  | string | path | 是  | 工作表名称。                           |
| folder     | string | query| 否  | 包含该工作簿的文件夹路径。                  |
| storageName| string | query| 否  | Aspose Cloud 存储空间名称。               |

### **响应**

```json
{
  "Status":"OK",
  "Code":200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

**HTTP 状态码**

| 状态码 | 含义               | 描述                                         |
|-------|------------------|--------------------------------------------|
| 200   | OK（成功）         | 成功应用筛选；响应包含操作详情。                   |
| 400   | Bad Request（错误请求） | 缺少或参数无效（例如：不支持的文件类型）。             |
| 401   | Unauthorized（未授权）   | JWT 令牌无效或缺失。                            |
| 413   | Payload Too Large（载荷过大） | 上传的文件超过大小限制。                         |
| 500   | Internal Server Error（内部服务器错误） | 意外的服务器错误。                        |

## 如何结合 SDK 使用 GetWorksheetTextItems API

### GetWorksheetTextItems API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetTextItems){:target="_blank" rel="noopener noreferrer"} 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/sheet1/textItems" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

SDK 可简化集成过程，通过处理底层细节，使您专注于项目任务本身。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"} 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetTextItems.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetTextItems.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetTextItems.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetTextItems.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetTextItems.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetTextItems.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetTextItems.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetTextItems.go" >}}

{{< /tab >}}

{{< /tabs >}}

---