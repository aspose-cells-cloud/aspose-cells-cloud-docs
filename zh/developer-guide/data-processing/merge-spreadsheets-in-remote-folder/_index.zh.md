---
title: Aspose.Cells Cloud Web API - 将匹配的电子表格文件合并到远程文件夹中的文件中
second_title: Documen
ArticleTitle: Merge matching spreadsheet files into a file in a remote Folder
linktitle: 合并远程文件夹中的电子表格
type: docs
url: /zh/merge-spreadsheets-in-remote-folder/
keywords: Merge spreadsheets, cloud storage, Excel API, remote processing, spreadsheet formats, REST AP
description: 将云存储中存储的电子表格文件合并为一个文件，文件格式支持30种格式输出，如PDF，Csv，Json等常见格式
weight: 100
kwords: Excel、Office 云、REST API、电子表格、PDF、CSV、JSON、Markdown、合并电子表格、云处理、远程文件处理
---
将匹配的电子表格文件合并到远程文件夹中的文件中，输出文件格式支持 30 多种格式，例如 PDF、Csv、Json 和其他常见格式。


## **合并远程文件夹中的电子表格 API**

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|文件夹|细绳|询问|存储合并文件的文件夹。|
|文件匹配表达式|细绳|询问|用于匹配合并文件的表达式。|
|输出格式|细绳|询问|所需的输出文件格式。|
|合并到一张表中|布尔值|询问|指示是否将所有数据合并到单个工作表中。|
|存储名称|细绳|询问| （可选）自定义云存储的名称；如果省略，则默认为默认存储。|
|输出路径|细绳|询问| （可选）存储工作簿的文件夹路径；默认为空。|
|输出存储名称|细绳|询问|输出文件的存储名称。|
|字体位置|细绳|询问|指定自定义字体。|
|地区|细绳|询问|设置电子表格区域。|
|密码|细绳|询问|打开电子表格文件的密码。|

## **回复**

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

### 错误代码

- **400 错误请求**：无效的 Apose.Cells Cloud API URI。
- **401 未授权**：访问令牌无效。或者客户端 ID 和密钥无效。
- **404 未找到**：电子表格文件无法访问。
- **500 服务器错误**：电子表格在获取计算数据时遇到异常。

## 我们应该在哪里使用远程文件夹 API 中的合并电子表格？

当您需要将多个数据文件合并在一起时，您可以使用这个API。

## 为什么要使用远程文件夹 API 中的合并电子表格？

- 云存储文件无需下载，直接在云端合并即可。
- 批量合并多个电子表格文件，支持匹配表达式。
- 通过现有的SDK即可快速完成开发。

## 如何使用 SDK 中的远程文件夹 API 中的合并电子表格

### 合并远程文件夹中的电子表格 API 规格

这[合并远程文件夹中的电子表格 API 规格](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder)提供一个可公开访问的编程接口，允许直接从 Web 浏览器进行 REST 交互。

### 使用 Aspose.Cells 云 SDK

使用 SDK 是最快的开发方式，因为它抽象了低级细节，允许您使用短代码将匹配的电子表格文件合并到远程文件夹中的文件中。
请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例说明了如何使用各种 SDK 与 Aspose.Cells Web 服务进行交互：
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheetsInRemoteFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheetsInRemoteFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheetsInRemoteFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheetsInRemoteFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheetsInRemoteFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheetsInRemoteFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheetsInRemoteFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheetsInRemoteFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}
