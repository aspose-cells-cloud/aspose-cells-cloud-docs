---
title: Aspose.Cells Cloud Web API - 将电子表格图表导出为格式文件
second_title: Documen
ArticleTitle: Export a Spreadsheet Chart as a Format fil
linktitle: 将图表导出为 Forma
type: docs
url: /zh/export-chart-as-format/
keywords: Export Chart, Aspose.Cells Cloud Web API, Spreadsheet Conversion, PDF Export, Image Export, REST, Excel, CSV, JSO
description: 高效地将存储在云中的电子表格中的图表转换为指定格式，如 PDF 或直接转换为图像，无需下载
weight: 100
kwords: 导出图表、REST、电子表格转换、PDF、CSV、JSON、Markdown、Excel、图像格式
---
使用 Aspose.Cells Cloud Web API 将云电子表格/Excel 图表导出为另一种格式的文件。

## **将图表导出为格式 API**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路| （必需）要检索的工作簿文件的名称。|
|工作表|细绳|小路|工作表名称|
|图表索引|整数|小路|图表索引|
|格式|细绳|询问|（必需）所需的输出格式（例如“png”、“pdf”、“svg”）。|
|文件夹|细绳|询问| （可选）存储工作簿的文件夹路径；默认为空。|
|存储名称|细绳|询问|（可选）如果使用自定义云存储，则输入存储的名称；如果省略，则使用默认存储。|
|输出路径|细绳|询问| （可选）存储工作簿的文件夹路径；默认为空。|
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

## 为什么要使用“导出电子表格图表为格式 API”？

- 您可以随时随地将云文件转换为不同的格式。
- 通过现有的SDK即可快速完成开发。

## 如何使用 SDK 将电子表格图表导出为格式 API？

### 导出图表为 API 格式规范

这[导出图表为 API 格式规范](https://reference.aspose.cloud/cells/#/ConversionController/ExportChartAsFormat)定义一个可公开访问的编程接口，允许您直接从 Web 浏览器执行 REST 交互。

### 使用 Aspose.Cells 云 SDK

使用 SDK 是最快的开发方式，因为它抽象了低级细节，允许您使用短代码将电子表格图表数据导出为格式文件。
请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。
以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportChartAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportChartAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportChartAsFormat.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportChartAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportChartAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportChartAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportChartAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportChartAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}
