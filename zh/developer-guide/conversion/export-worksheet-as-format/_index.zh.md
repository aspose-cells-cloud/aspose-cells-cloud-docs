---
title: Aspose.Cells 云网络 API - 将电子表格工作表导出为格式文件
second_title: Documen
ArticleTitle: Export a Spreadsheet Worksheet as a Format fil
linktitle: 导出工作表
type: docs
url: /zh/export-worksheet-as-format/
keywords: Export worksheet, Cloud storage conversion, File format transformation, API for spreadsheet
description: 高效地将云存储中的工作表转换为各种格式，例如 PDF、CSV 和图像
weight: 100
kwords: 导出工作表、云转换、PDF、图像格式、Excel、REST API、CSV、JSON、Markdown、处理 Excel 中的空白单元格
---
使用 Aspose.Cells Cloud Web API 将云电子表格/Excel 工作表导出为另一种格式的文件。

## **将工作表导出为格式 API**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路|（必需）要检索的工作簿文件的名称。|
|工作表|细绳|小路|（必需）要转换的特定工作表。|
|格式|细绳|询问|（必需）所需的输出格式（例如“png”、“pdf”、“svg”）。|
|文件夹|细绳|询问|（可选）存储工作簿的文件夹路径。默认值为 null。|
|存储名称|细绳|询问|（可选）自定义云存储的名称。如果省略，则使用默认存储。|
|输出路径|细绳|询问|（可选）输出文件夹路径。默认值为空。|
|输出存储名称|细绳|询问|（可选）输出文件存储名称。|
|字体位置|细绳|询问|（可选）如果需要，指定自定义字体。|
|地区|细绳|询问|电子表格区域设置。|
|密码|细绳|询问|访问电子表格文件的密码。|

### **回复**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream"
        }
    }
]
```

### 错误代码

- **400 错误请求**：无效的 Apose.Cells Cloud API URI。
- **401 未授权**：访问令牌无效。或者客户端 ID 和密钥无效。
- **404 未找到**：电子表格文件无法访问。
- **500 服务器错误**：电子表格在获取计算数据时遇到异常。

## 为什么要使用导出电子表格工作表作为格式 API？

- 您可以随时随地将云文件转换为不同的格式。
- 通过现有的SDK即可快速完成开发。

## 如何使用 SDK 将导出电子表格工作表作为格式 API？

### 将工作表导出为格式 API 规范

这[将工作表导出为格式 API 规范](https://reference.aspose.cloud/cells/#/ConversionController/ExportWorksheetAsFormat)提供一个可公开访问的编程接口，用于直接从 Web 浏览器执行 REST 交互。

### 使用 Aspose.Cells 云 SDK

使用 SDK 是最快的开发方式，因为它抽象了低级细节，允许您使用短代码将电子表格工作表导出为格式文件。
请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportWorksheetAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportWorksheetAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportWorksheetAsFormat.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportWorksheetAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportWorksheetAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportWorksheetAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportWorksheetAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportWorksheetAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}
