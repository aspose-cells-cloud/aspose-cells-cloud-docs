---
title: Aspose.Cells Cloud Web API - 将电子表格数据转换为 PDF 文件
second_title: Documen
ArticleTitle: Convert a Spreadsheet Table data to a Pdf file
linktitle: 将表格转换为 PD
type: docs
url: /zh/convert-table-to-pdf/
keywords: Table to PDF conversion, Excel to PDF, REST API, Spreadsheet conversion, Aspose.Cells Cloud Web AP
description: 使用我们高效的 API 将本地驱动器上的电子表格转换为 PDF 文件
weight: 100
kwords: Excel、Office 云、REST API、电子表格、PDF、CSV、JSON、Markdown、Excel 表格转换、云 PDF 服务
---
将本地电子表格/Excel 表格数据转换为 pdf 文件。

## **将表格转换为 PDF API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|电子表格|文件|表单数据|上传要转换的电子表格文件。|
|工作表|细绳|询问|电子表格/Excel的工作表名称|
|表名|细绳|询问|要转换的表的名称。|
|输出路径|细绳|询问|（可选）转换后的 PDF 的存储文件夹路径。默认值为空。|
|输出存储名称|细绳|询问|指定输出文件存储的名称。|
|字体位置|细绳|询问|对 PDF 使用自定义字体。|
|地区|细绳|询问|定义电子表格区域设置。|
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

## 为什么要使用将表格转换为 PDF API？

- 无需云存储，减少云资源负担。
- 通过现有的SDK即可快速完成开发。

## 如何使用 SDK 将表格转换为 PDF API？

### 将表格转换为 PDF API 规格

这[将表格转换为 PDF API 规格](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToPdf)提供可公开访问的编程接口，用于直接从 Web 浏览器执行 REST 交互。

### 使用 Aspose.Cells 云 SDK

使用 SDK 是最快的开发方式，因为它抽象了低级细节，允许您使用短代码将电子表格数据转换为 pdf 文件。
请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例说明了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToPdf.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToPdf.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToPdf.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToPdf.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToPdf.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToPdf.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToPdf.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToPdf.go" >}}
{{< /tab >}}
{{< /tabs >}}
