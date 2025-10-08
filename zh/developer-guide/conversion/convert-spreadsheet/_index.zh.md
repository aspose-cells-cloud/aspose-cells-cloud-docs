---
title: Aspose.Cells Cloud Web API - 将电子表格转换为其他格式的文件
second_title: Documen
ArticleTitle: Convert a Spreadsheet to another format file
linktitle: 转换电子表格
type: docs
url: /zh/convert-spreadsheet/
keywords: spreadsheet conversion, convert spreadsheet, cloud conversion, REST API, XLSX, PDF, CSV, JSON, Markdown, convert local file
description: 使用 Excel API 轻松将电子表格从本地驱动器转换为各种指定格式
weight: 100
kwords: Excel、Office 云、REST API、电子表格转换、PDF、CSV、JSON、Markdown、匹配 Excel 工作表中的所有空白单元格
---
使用 Aspose.Cells Cloud Web API 将本地电子表格/Excel 文件转换为其他格式的文件。

|**输出格式**|**描述**|
|:- |:- |
|[XLS](https://docs.fileformat.com/spreadsheet/xls/)|Excel 95/5.0 - 2003 工作簿。|
|[XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)|Office 开放 XML SpreadsheetML 文件格式。|
|[XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)|Excel 二进制工作簿。|
|[XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)|Excel 启用宏的工作簿。|
|[XLT](https://docs.fileformat.com/spreadsheet/xlt/)|Excel 97 - Excel 2003 模板。|
|[西林通](https://docs.fileformat.com/spreadsheet/xltx/)|Excel 模板。|
|[XLTM](https://docs.fileformat.com/spreadsheet/xltm/)|Excel 启用宏的模板。|
|[XLAM](https://docs.fileformat.com/spreadsheet/xlam/)|Excel 启用宏的插件文件，用于向 Excel 添加新功能。|
|[CSV](https://docs.fileformat.com/spreadsheet/csv/)|CSV（逗号分隔值）文件。|
|[TSV](https://docs.fileformat.com/spreadsheet/tsv/)|TSV（制表符分隔值）文件。|
|[TXT](https://docs.fileformat.com/word-processing/txt/)|分隔的纯文本文件。|
|[HTML](https://docs.fileformat.com/web/html/)|HTML格式。|
|[移动HTML](https://docs.fileformat.com/web/mhtml/)|MHTML 文件。|
|[消耗臭氧层物质](https://docs.fileformat.com/spreadsheet/ods/)|ODS（开放文档电子表格）。|
|电子表格ML|Excel 2003 XML 文件。|
|[数字](https://docs.fileformat.com/spreadsheet/numbers/)|该文档由苹果公司的“Numbers”应用程序创建，该应用程序是苹果公司 iWork office 套件的一部分，该套件是一组在 Mac OS X 和 iOS 操作系统上运行的应用程序。|
|[JSON](https://docs.fileformat.com/web/json/)|JavaScript 对象表示法|
|[DIF](https://docs.fileformat.com/spreadsheet/dif/)|数据交换格式。|
|[数据库文件](https://docs.fileformat.com/database/dbf/)|扩展名为 .dbf 的文件是名为 dBASE 的数据库管理系统应用程序使用的数据库文件。|
|[PDF](https://docs.fileformat.com/pdf/)|Adobe 便携式文档格式。|
|[XPS](https://docs.fileformat.com/page-description-language/xps/)|XML 论文规范格式。|
|[SVG](https://docs.fileformat.com/page-description-language/svg/)|可缩放矢量图形格式。|
|[TIFF](https://docs.fileformat.com/image/tiff/)|标记图像文件格式|
|[PNG](https://docs.fileformat.com/image/png/)|便携式网络图形格式|
|[BMP](https://docs.fileformat.com/image/bmp/)|位图图像格式|
|[EMF](https://docs.fileformat.com/image/emf/)|增强型图元文件格式|
|[JPEG](https://docs.fileformat.com/image/jpeg/)|JPEG是一种使用有损压缩方法保存的图像格式。|
|[GIF](https://docs.fileformat.com/image/gif/)|图形交换格式|
|[降价](https://docs.fileformat.com/word-processing/md/)|代表一个 markdown 文档。|
|[西南交通大学](https://docs.fileformat.com/spreadsheet/sxc/)|OpenOffice 和 StarOffice 使用的基于 XML 的格式|
|[食物中毒](https://docs.fileformat.com/spreadsheet/fods/)|这是一种以平面 XML 形式存储的开放文档格式。|
|[DOCX](https://docs.fileformat.com/word-processing/docx/)|Microsoft Word 文档的一种著名格式，是 XML 和二进制文件的组合。|
|[PPTX](https://docs.fileformat.com/presentation/pptx/)|PPTX 格式基于 Microsoft PowerPoint 开放 XML 演示文稿文件格式。|
|[SQL脚本](https://docs.fileformat.com/database/sql/)|结构化查询语言。|
|[XHTML](https://docs.fileformat.com/web/xhtml/)|XHTML 是一种基于文本的文件格式，带有 XML 标记，使用 HTML 4.0 的重新表述。|
|[电子书](https://docs.fileformat.com/ebook/epub/)|扩展名为 .epub 的文件是一种电子书文件格式，为出版商和消费者提供标准的数字出版格式。|
|[XML](https://docs.fileformat.com/web/xml/)|XML 代表可扩展标记语言，与 HTML 类似，但在使用标签定义对象方面有所不同。|
|[奥茨](https://docs.fileformat.com/spreadsheet/ots/)|打开文档模板表（OTS）文件。|
|[AZW3](https://docs.fileformat.com/ebook/azw3/)|AZW 是亚马逊为其 Kindle 设备开发的数字电子书文件格式。AZW3，也称为 Kindle 格式 8 (KF8)。|

## **转换电子表格 API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/spreadsheet
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|电子表格|文件|表单数据|上传要转换的电子表格文件。|
|格式|细绳|询问|（必需）所需的输出格式（例如“Xlsx”、“Pdf”、“Csv”）。|
|输出路径|细绳|询问|（可选）转换后的工作簿的存储文件夹路径。默认值为空。|
|输出存储名称|细绳|询问|指定输出文件存储名称。|
|字体位置|细绳|询问|对电子表格使用自定义字体。|
|地区|细绳|询问|指定电子表格区域设置。|
|密码|细绳|询问|如果电子表格文件受到保护，则输入打开该文件的密码。|

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

## 为什么要使用转换电子表格 API？

- 无需云存储，减少云资源负担。
- 通过现有的SDK即可快速完成开发。

## 如何使用带有 SDK 的转换电子表格 API？

### 转换电子表格 API 规格

这[转换电子表格 API 规格](https://reference.aspose.cloud/cells/#/ConversionController/ConvertSpreadsheet)定义一个可公开访问的编程接口，允许您直接从 Web 浏览器执行 REST 交互。

### 使用 Aspose.Cells 云 SDK

使用 SDK 是最快的开发方式，因为它抽象了低级细节，允许您使用短代码将电子表格文件转换为另一种格式的文件。
请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorkbook.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorkbook.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorkbook.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorkbook.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorkbook.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorkbook.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorkbook.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorkbook.go" >}}
{{< /tab >}}
{{< /tabs >}}
