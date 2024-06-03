---
title: 导出 Excel 工作表的一页
second_title: Aspose.Cells Cloud Documen
linktitle: 帕格
type: docs
url: /zh/worksheets/page-to-different-formats/
aliases: [/get-worksheet-for-page-index/]
keywords: Get page to different format content from an Excel worksheet
description: Aspose.Cells Cloud REST API 支持从 Excel 工作表获取不同格式内容的页面。SDK 支持多种开发语言。其中包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 240
kwords: Excel、Office 云、REST API、电子表格、PDF、CSV、Json、Markdwon、导出 Excel 工作表的一页
---
[获取/单元格/{名称}/工作表/{工作表名称}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet)API 可让您将工作表的指定页面转换为各种格式的文件。支持的格式：[XLS](https://docs.fileformat.com/spreadsheet/xls/), [扩展](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [硅通孔 (TSV)](https://docs.fileformat.com/spreadsheet/tsv/), [超音速巡航导弹](https://docs.fileformat.com/spreadsheet/xlsm/), [消耗臭氧层物质](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [奥特斯](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [差分输入](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/),[动态图片](https://docs.fileformat.com/image/gif/), [BMP](https://docs.fileformat.com/image/bmp/), [沃姆福](https://docs.fileformat.com/image/wmf/),[TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [数字](https://docs.fileformat.com/spreadsheet/numbers/), [福尔马林](https://docs.fileformat.com/spreadsheet/fods/).


## 休息 API

这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorkshee)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。
 
您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例显示如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&pageIndex=1&folder=DotnetFiles" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

Converted Image 

```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK 系列
 
使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)获得 Aspose.Cells Cloud SDKs 的完整列表。
 
以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="7" tabID="4" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Android" tabName5="Ruby" tabName6="PHP" tabName7="Node.js" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "c26975dacdc050fccd6d003b487b39d9" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a555abf44e31590c6ae3260c1bcd3066" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "3c7008ae0d54a40cd0c92a1273bfd7d5" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "bd5c03f09104b9d59941d6583117dce2" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "64a33901d4f45c9edf31ab83e816981e" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "daa94750c751cb595de0b8a357c051ed" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "a4bb7786b0d6bc98d8b51da49a687cf5" >}}

{{< /tab >}}

{{< /tabs >}}
