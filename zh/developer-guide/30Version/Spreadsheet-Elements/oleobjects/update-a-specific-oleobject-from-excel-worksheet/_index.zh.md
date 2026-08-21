---
title: "更新 Excel 工作表中的 OLE 对象"
second_title: "文档"
linktitle: "更新"
type: docs
url: /zh/oleobjects/update/
aliases: [/update-a-specific-oleobject-from-excel-worksheet/]
keywords: "更新 OLE 对象, Excel, Aspose.Cells Cloud, REST API, SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API 更新 Excel 工作表中的 OLE 对象（如图像、图表等）。包含 cURL、SDK 示例、认证步骤及错误处理说明。"
weight: 30
author: "Aspose Cloud 文档团队"
lastmod: "2024-03-01"
ArticleTitle: "更新 Excel 工作表中的 OLE 对象 – Aspose.Cells Cloud API 指南"
---

此 REST API 用于更新 Excel 工作表中的 **OLE 对象**。

### **安全与认证**

Aspose.Cells Cloud API 采用安全机制，需进行 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的认证</a>。

## PostUpdateWorksheetOleObject API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

请求参数如下：

| 参数名           | 类型     | 位置   | 描述                                    |
| ---------------- | -------- | ------ | --------------------------------------- |
| name             | string   | 路径   | 工作簿名称。                            |
| sheetName        | string   | 路径   | 工作表名称。                            |
| oleObjectIndex   | integer  | 路径   | OLE 对象在工作表中的索引（从 0 开始）。 |
| ole              | object   | 请求体 | 待更新的 OLE 对象的 JSON 表示。         |
| folder           | string   | 查询   | 包含该工作簿的文件夹路径。              |
| storageName      | string   | 查询   | 存储服务的名称。                        |

### 请求体字段

| 字段名              | 类型    | 是否必需 | 描述                                       |
| ------------------- | ------- | -------- | ------------------------------------------ |
| ImageSourceFullName | string  | 可选     | 用于 OLE 对象的图像文件路径。              |
| IsAutoSize          | boolean | 可选     | 是否自动调整 OLE 对象大小。                |
| SourceFullName      | string  | 必需     | OLE 对象的源文件（如图像或图表）路径。     |
| UpperLeftRow        | integer | 必需     | 左上角单元格的行索引（从 0 开始）。        |
| UpperLeftColumn     | integer | 必需     | 左上角单元格的列索引（从 0 开始）。        |
| Left                | integer | 可选     | 距离左上角的水平偏移量（单位：磅）。       |
| Top                 | integer | 可选     | 距离左上角的垂直偏移量（单位：磅）。       |
| Width               | integer | 必需     | OLE 对象的宽度（单位：磅）。               |
| Height              | integer | 必需     | OLE 对象的高度（单位：磅）。               |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/OleObjects/PostUpdateWorksheetOleObject) 定义了一个公开可用的编程接口，允许您直接从 Web 浏览器发起 REST 调用。

您可使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
  -X POST \
  -d '{"ImageSourceFullName":"aspose-logo.png","IsAutoSize":true,"SourceFullName":"Sample_Book2.xls","UpperLeftRow":15,"Top":10,"UpperLeftColumn":5,"Left":10,"Width":400,"Height":400}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "OLEObject": {
    "Index": 0,
    "ImageSourceFullName": "aspose-logo.png",
    "IsAutoSize": true,
    "SourceFullName": "Sample_Book2.xls",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Left": 10,
    "Top": 10,
    "Width": 400,
    "Height": 400
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## 错误响应

| HTTP 状态码 | Code | 消息                                     |
| ----------- | ---- | ---------------------------------------- |
| 400         | 4000 | 错误请求 — 缺少或无效的参数。            |
| 401         | 4010 | 未授权 — 无效或缺失的 JWT 令牌。         |
| 404         | 4040 | 未找到 — 工作簿、工作表或 OLE 对象不存在。|
| 500         | 5000 | 服务器内部错误 — 服务端发生意外故障。    |

API 还会在响应体中返回自定义的 **Code** 字段，与 HTTP 状态码对应（如：200 → 2000，400 → 4000 等）。

## 何时使用此 API？

当您需要修改已有的 OLE 对象（如嵌入的图像、图表或文档）而无需重新上传整个工作表时，请使用此接口。典型场景包括：更新图像源、调整对象大小或在工作簿生成后修改其位置。相关操作请参阅 [添加 OLE 对象](/zh/oleobjects/add/) 和 [删除 OLE 对象](/zh/oleobjects/delete/)。

## 云 SDK 开发套件

使用 SDK 是最快捷的开发方式。SDK 封装了底层细节，让您专注于业务逻辑。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud) 获取 Aspose.Cells Cloud SDK 的完整列表。

以下是一个使用 Aspose.Cells Cloud SDK 更新 OLE 对象的 C# 示例：

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var config = new Configuration
{
    AppSid = "<your-app-sid>",
    AppKey = "<your-app-key>"
};
var oleApi = new OleObjectsApi(config);
var request = new OleObjectUpdateRequest
{
    ImageSourceFullName = "aspose-logo.png",
    IsAutoSize = true,
    SourceFullName = "Sample_Book2.xls",
    UpperLeftRow = 15,
    UpperLeftColumn = 5,
    Left = 10,
    Top = 10,
    Width = 400,
    Height = 400
};

var response = oleApi.UpdateWorksheetOleObject("SampleBook.xlsx", "Sheet1", 0, request, folder: "myFolder");
Console.WriteLine($"Status: {response.Status}");
```

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUpdateWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUpdateWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUpdateWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUpdateWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUpdateWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUpdateWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUpdateWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUpdateWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}