---
title: 从 Aspose.Cells AP 下载文件
second_title: Developer Guide for Aspose.Cells AP
linktitle: 下载文件 AP
type: docs
url: /zh/download-file/
keywords: Aspose.Cells API, Download File, REST API, Excel File, Office Cloud, Spreadsheet Download, File Management, File Retrieval, CSV, PDF, JSON, Markdow
description: 了解如何使用 Aspose.Cells API 更高效地下载文件（包括 Excel、PDF、CSV 等）
weight: 100
kwords: Excel, Office 云、REST API、电子表格、PDF、CSV、JSON、Markdown、下载 Excel 文件、检索空白 Cells
---
## **Excel API：下载文件**

```
GET http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **功能描述**

这**下载文件**API 允许您检索存储在 Aspose 云存储中的文件。此功能对于管理和访问各种文件格式（包括 Excel 电子表格、PDF 和 CSV）至关重要。

### 请求参数**下载文件**API 是

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|小路|细绳|小路|您要下载的文件的路径。|
|存储名称|细绳|询问|将从中检索文件的存储的名称。|
|版本号|细绳|询问|要下载的文件的版本标识符（如果适用）。|

### **响应描述**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

## OpenAPI 规范

这[OpenAPI 规范](https://reference.aspose.cloud/cells/#/FileController/DownloadFile)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

## Excel API SDK

使用 SDK 是加速开发的最佳方式。SDK 可以处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DownloadFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DownloadFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DownloadFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DownloadFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DownloadFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DownloadFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DownloadFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DownloadFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
