---
title: Aspose.Cells Cloud Web API - 将电子表格导出为格式文件
second_title: Documen
ArticleTitle: Export a Spreadsheet as a Format fil
linktitle: 将电子表格导出为 Forma
type: docs
url: /zh/export-spreadsheet-as-format/
keywords: Export spreadsheet, Aspose.Cells Cloud Web API, Convert spreadsheet, Spreadsheet formats, XLSX, PDF, CSV, JSON, Markdow
description: 高效地将存储在云存储中的电子表格转换为各种格式，如 XLSX、PDF 和 CSV
weight: 100
kwords: Excel, Office 云、REST、电子表格转换、PDF、CSV、JSON、Markdow
---
将云电子表格/Excel 导出为另一种格式的文件。

## **将电子表格导出为 API 格式**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTP 正文|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路| （必需）要检索的工作簿文件的名称。|
|格式|细绳|询问|（必需）所需的输出格式（例如，“Xlsx”、“Pdf”、“Csv”）。|
|文件夹|细绳|询问| （可选）存储工作簿的文件夹路径。默认值为 null。|
|存储名称|细绳|询问|（可选）如果使用自定义云存储，则输入存储名称。如果省略，则使用默认存储。|
|输出路径|细绳|询问| （可选）存储工作簿的文件夹路径。默认值为空。|
|输出存储名称|细绳|询问|输出文件存储名称。|
|字体位置|细绳|询问|使用自定义字体。|
|地区|细绳|询问|电子表格区域设置。|
|密码|细绳|询问|打开电子表格文件的密码。|

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

## 为什么要使用导出电子表格为格式 API？

- 您可以随时随地将云文件转换为不同的格式。
- 通过现有的SDK即可快速完成开发。

## 如何使用 SDK 将导出电子表格作为格式 API？

### 将电子表格导出为 API 格式规范

这[将电子表格导出为 API 格式规范](https://reference.aspose.cloud/cells/#/ConversionController/ExportSpreadsheetAsFormat)提供可公开访问的编程接口，以无缝执行 REST 交互。

### 使用 Aspose.Cells 云 SDK

使用 SDK 是最快的开发方式，因为它抽象了低级细节，允许您使用短代码将电子表格导出为格式文件。
请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例说明了如何与 Aspose.Cells Web 服务 via 各种 SDK 进行交互：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportSpreadsheetAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportSpreadsheetAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportSpreadsheetAsFormat.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportSpreadsheetAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportSpreadsheetAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportSpreadsheetAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportSpreadsheetAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportSpreadsheetAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}
