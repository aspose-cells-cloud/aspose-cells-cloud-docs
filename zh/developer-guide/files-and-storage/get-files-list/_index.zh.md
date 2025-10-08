---
title: 获取文件列表 - Aspose.Cells AP
second_title: Developer Guide for Aspose.Cell
linktitle: 获取文件列表
type: docs
url: /zh/get-files-list/
keywords: Aspose.Cells API, Get Files List, REST API, Excel File Management, Cloud Storage, File Retrieval, Programming Interfac
description: 了解如何使用 Aspose.Cells API 从指定文件夹检索文件列表。本指南提供有关请求参数、响应结构的详细信息，以及各种编程语言的代码示例
weight: 100
kwords: Excel, Office 云, REST API, 电子表格, PDF, CSV, JSON, Markdown, 云文件管理, 获取文件列表
---
## **Excel API：获取文件列表**

```
GET http://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **功能描述**

这**获取文件列表**API 允许用户检索 Aspose.Cells 云存储中指定目录中包含的文件和文件夹的完整列表。此端点对于高效管理文件至关重要，并且支持各种文件格式。

### 请求参数**获取文件列表**API 是

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|小路|细绳|小路|从中检索文件列表的云存储文件夹的路径。|
|存储名称|细绳|询问|要访问的存储的名称。|

### **响应描述**

```json
{
  "Name": "FilesList",
  "Description": [
    "Files list"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": [
        "Files and folders contained by the specified StorageFile."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "StorageFile",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "StorageFile",
          "Name": "class:storagefile"
        },
        "Name": "container"
      }
    }
  ]
}
```

## OpenAPI 规范

这[OpenAPI 规范](https://reference.aspose.cloud/cells/#/FolderController/GetFilesList)定义一个可公开访问的编程接口，可直接从 Web 浏览器实现 REST 交互，从而方便集成和测试。

## Excel API SDK

使用 SDK 是加速开发流程的最佳方法。SDK 可以管理底层细节，让您专注于项目任务。如需查看 Aspose.Cells 云 SDK 的完整列表，请访问[GitHub 存储库](https://github.com/aspose-cells-cloud).

以下代码示例说明了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFilesList.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFilesList.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFilesList.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFilesList.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFilesList.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFilesList.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFilesList.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFilesList.go" >}}
{{< /tab >}}
{{< /tabs >}}
