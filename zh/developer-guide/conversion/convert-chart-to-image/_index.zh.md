---
title: Aspose.Cells Cloud Web API - 将电子表格图表转换为图像
second_title: Documen
ArticleTitle: Convert a Spreadsheet Chart to an Imag
linktitle: 将图表转换为图像
type: docs
url: /zh/convert-chart-to-image/
keywords: convert chart to image, png, svg, tiff, jpg, bmp, convert a Spreadsheet chart to png,convert an Excel chart to svg, convert an Excel chart to jpg, convert a Spreadsheet chart to bmp, convert an Excel chart to tif
description: 使用 Aspose.Cells Cloud Web API 将图表从本地电子表格/Excel 文件转换为图像文件
weight: 100
kwords: 将 Excel 图表转换为图像、png、svg、tiff、jpg、bmp、电子表格
---
将图表从本地电子表格/Excel文件转换为图像格式文件。支持**图像格式：** [PNG](https://docs.fileformat.com/image/png/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/)

## **将图表转换为图像 API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/chart/image
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|电子表格|文件|表单数据|上传包含图表的电子表格文件。|
|工作表|细绳|询问|如果适用，请指定工作表名称。|
|图表索引|整数|询问|要转换的图表的索引。|
|格式|细绳|询问|（必需）所需的图像类型（例如，svg、png、jpg）。|
|输出路径|细绳|询问|（可选）存储工作簿的文件夹路径；默认为空。|
|输出存储名称|细绳|询问|输出文件的存储名称。|
|字体位置|细绳|询问|如果需要，指定自定义字体。|
|地区|细绳|询问|设置电子表格区域。|
|密码|细绳|询问|打开电子表格文件的密码。|

## **回复**

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

## 您应该在哪里使用“将图表转换为图像 API”？

- 将电子表格中的图表导出为图像。

## 为什么要使用“将图表转换为图像 API”？

- 无需云存储，减少云资源负担。
- 通过现有的SDK即可快速完成开发。

## 如何使用 SDK 将图表转换为图像 API？

### 将图表转换为图像 API 规格

这[将图表转换为图像 API 规格](https://reference.aspose.cloud/cells/#/ConversionController/ConvertChartToImage)定义一个可公开访问的编程接口，并使您能够直接从 Web 浏览器执行 REST 交互。

### 使用 Aspose.Cells 云 SDK

使用 SDK 是最快的开发方式，因为它抽象了低级细节，允许您使用短代码将图表转换为图像。
请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToImage.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToImage.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToImage.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToImage.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToImage.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToImage.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToImage.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToImage.go" >}}
{{< /tab >}}
{{< /tabs >}}
