---
title: 导出字符
second_title: Aspose.Cells Cloud Documen
linktitle: 字符
type: docs
url: /zh/export/excel-chart-to-different-formats/
keywords: Export Excel chart to kinds of format files
description: Aspose.Cells Cloud REST API 支持将Excel图表导出为各种格式文件。 SDK支持多种开发语言。它们包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 20
---
您可以导出格式：[PNG](https://docs.fileformat.com/Image/png/), [动图](https://docs.fileformat.com/image/gif/), [JPEG](https://docs.fileformat.com/image/jpeg/),  [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [WMF](https://docs.fileformat.com/image/Wmf/), [PDF](https://docs.fileformat.com/pdf/).

- **休息 API**

|**API**|**类型**|**描述**|**招摇链接**|
|:- |:- |:- |:- |
|/细胞/出口|邮政|将请求内容中的 Excel 对象导出为某种格式|[导出后](https://apireference.aspose.cloud/cells/#/LiteCells/PostExport)|


这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/LiteCells/PostExport)定义了一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

您可以使用**cURL**用于轻松访问 Aspose.Cells Web 服务的命令行工具。以下示例显示如何使用 cURL 调用 Cloud API。


- **要求**
```bash

curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=chart&format=tiff" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger" -d {"File":{}}
```

- **回复**

```bash
{
    "Files": [{
        "Filename": "Book1_xlsx_Sheet4_Charts_0.tif",
        "FileSize": 10040,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "Book1_xlsx_Sheet4_Charts_1.tif",
        "FileSize": 12978,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "Book1_xlsx_Sheet4_Charts_2.tif",
        "FileSize": 7002,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "Book1_xlsx_Sheet4_Charts_3.tif",
        "FileSize": 11532,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "Book1_xlsx_Sheet6_Charts_0.tif",
        "FileSize": 8270,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "myDocument_xlsx_Sheet3_Charts_0.tif",
        "FileSize": 42570,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "myDocument_xlsx_Sheet3_Charts_1.tif",
        "FileSize": 12102,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "myDocument_xlsx_Sheet3_Charts_2.tif",
        "FileSize": 8290,
        "FileContent": "-----Base64String--------"
    }]
}
```

- **云 SDK 系列**

使用 SDK 是加速开发的最佳方式。 SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 仓库](https://github.com/aspose-cells-cloud)有关 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用各种 SDK 调用 Aspose.Cells Web 服务：


{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Export-chart-tiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}


{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LiteCells-Export-chart-tiff.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}

{{< /tabs >}}
