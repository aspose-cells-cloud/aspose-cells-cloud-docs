---
title: "将 Excel 转换为 TIFF"
second_title: "文档"
linketitle: "Excel 转 TIFF"
type: docs
url: /zh/convert-excel-file-to-tiff-file/
aliases: [/zh/convert-excel-file-to-tiff-in-cloud/, /zh/convert/excel-to-tiff/]
keywords: "Aspose.Cells Cloud、Excel 转 TIFF 转换、REST API、cURL、SDK、.NET、Java、Python、图像导出"
description: "了解如何使用 Aspose.Cells Cloud API 将 Excel 工作簿转换为高质量 TIFF 图像。包含详细的 cURL 命令、SDK 示例（C#、Java、Python 等）、身份验证步骤及错误处理说明。"
weight: 90
---

Aspose.Cells Cloud 的 **Convert**（转换）、**SaveAs**（另存为）和 **Export**（导出）接口可将 Excel 工作簿转换为 TIFF 图像。  
您可以直接使用 **cURL** 调用这些接口，或通过支持的 SDK 进行调用。

## REST API

| **API**                | **方法** | **用途**                                                                                     | **Swagger 链接**                                                                            |
| ---------------------- | -------- | -------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `/cells/convert`       | PUT      | 将请求体中提供的工作簿转换为指定格式（TIFF）。                                               | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |
| `/cells/{name}`        | GET      | 将指定名称的工作簿导出为其他格式（TIFF），并将结果以响应体形式返回。                         | [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)               |
| `/cells/{name}/saveAs` | POST     | 将工作簿保存为指定格式（TIFF），并将结果存储至云端存储空间。                                 | [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)   |

这些接口为公开访问接口，可直接从网页浏览器或任意 HTTP 客户端发起调用。

### cURL 示例

{{< tabs tabTotal="3" tabID="11" tabName11="convert" tabName12="saveas" tabName13="export">}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/convert?format=tiff" \
     -X PUT \
     -d '{"File":{"Name":"book1.xlsx","Data":"<base64‑content>"},"SaveFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx/saveas?newfilename=book1.tiff" \
     -X POST \
     -d '{"SaveFormat":"tiff","ImageFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="13" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=tiff" \
     -X GET \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< /tabs >}}

> **注意：**
>
> - **Convert** 接口的请求体必须包含文件（或已存储文件的引用）及所需的 `SaveFormat`。
> - **Export** 接口无需请求体；格式通过查询字符串指定（`format=tiff`）。

## 错误处理

| **状态码** | **含义**       | **常见原因**                     |
| ---------- | -------------- | -------------------------------- |
| 200        | 成功           | 返回 TIFF 图像（二进制流）。     |
| 400        | 请求错误       | 缺失或格式错误的参数。           |
| 401        | 未授权         | JWT 令牌无效或缺失。             |
| 404        | 未找到         | 指定的工作簿不存在。             |
| 500        | 服务器内部错误 | 服务器端出现意外情况。           |

发生错误时，API 将返回包含 `Code`（代码）、`Message`（消息），以及可选的 `Description`（描述）字段的 JSON 负载。

## 云 SDK 家族

使用 SDK 是最快捷的开发方式。SDK 将处理底层细节，使您能专注于项目本身。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbookToTiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbookToTiff.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbookToTiff.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbookToTiff.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbookToTiff.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbookToTiff.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbookToTiff.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbookToTiff.go" >}}

{{< /tab >}}

{{< /tabs >}}