---
title: Aspose.Cells 云网络 API - 将一个电子表格合并到另一个电子表格中。
second_title: Aspose.Cells Cloud"
ArticleTitle: Merge one spreadsheet into anothe
linktitle: 合并远程电子表格
type: docs
url: /zh/merge-remote-spreadsheet/
keywords: Merge spreadsheets, cloud storage, Aspose.Cells Cloud Web API, spreadsheet merging, XLSX, CSV, PD
description: 将存储在云存储中的电子表格文件合并到另一个电子表格中，您可以指定数据输出的格式和位置。
weight: 100
kwords: Excel, Office 云, REST API, 电子表格, PDF, CSV, JSON, Markdown, 合并空白单元格, 云处理
---
将存储在云存储中的电子表格文件合并到另一个电子表格中，您可以指定数据输出的格式和位置。

## **合并远程电子表格 API**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路|要合并的工作簿文件的名称。|
|合并电子表格|细绳|询问|要合并的电子表格文件列表。|
|文件夹|细绳|询问|存储工作簿的文件夹路径。|
|输出格式|细绳|询问|输出文件格式（例如，XLSX、PDF）。|
|合并到一张表中|布尔值|询问|是否将所有数据合并到单个工作表中。|
|存储名称|细绳|询问|（可选）如果使用自定义云存储，则输入存储名称。如果省略，则默认为默认存储。|
|输出路径|细绳|询问|（可选）合并工作簿的文件夹路径。默认为 null。|
|输出存储名称|细绳|询问|输出文件的存储名称。|
|字体位置|细绳|询问|自定义字体位置。|
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

## 我们应该在哪里使用合并远程电子表格 API？

- 当您需要在云存储中将多个数据文件合并在一起时。


## 为什么要使用合并远程电子表格 API？

- 云存储文件无需下载，直接在云端合并即可。
- 通过现有的SDK即可快速完成开发。

## 如何使用 SDK 合并远程电子表格 API

### 合并远程电子表格 API 规范

这[合并远程电子表格 API 规范](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeRemoteSpreadsheet)提供可公开访问的编程接口，用于直接从 Web 浏览器执行 REST 交互。

## Excel API SDK

### 使用 Aspose.Cells 云 SDK

使用 SDK 是最快的开发方式，因为它抽象了低级细节，允许您使用短代码将一个电子表格合并到另一个电子表格中。
请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。
以下代码示例演示了如何使用各种 SDK 与 Aspose.Cells Web 服务进行交互：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeRemoteSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeRemoteSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeRemoteSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeRemoteSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeRemoteSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeRemoteSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeRemoteSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeRemoteSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
