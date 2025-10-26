---
title: Aspose.Cells Cloud Web API - 将电子表格拆分为多个文件，每个工作表一个文件
second_title: Documen
ArticleTitle: Split a spreadsheet into multiple files, one for each worksheet
linktitle: 在 Clou 中拆分远程电子表格
type: docs
url: /zh/split-remote-spreadsheet/
keywords: spreadsheet splitting, cloud spreadsheet API, split Excel file, multi-format outpu
description: 将存储在云存储中的电子表格拆分为多种输出格式，无需下载
weight: 100
kwords: Excel、Office 云、REST、电子表格、PDF、CSV、JSON、Markdown、拆分远程电子表格
---
将存储在云中的电子表格拆分为具有 30 种输出文件格式的单独文件。

## **拆分远程电子表格 API**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/split/spreadsheet
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTP 正文|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路|要拆分的工作簿文件的名称。|
|文件夹|细绳|询问|存储工作簿的文件夹路径。|
|从|整数|询问|开始工作表索引。|
|到|整数|询问|结束工作表索引。|
|输出格式|细绳|询问|所需的输出格式（例如，“Xlsx”，“Pdf”，“Csv”）。|
|存储名称|细绳|询问|（可选）如果使用自定义云存储，则输入存储名称。如果省略，则使用默认存储。|
|输出路径|细绳|询问| （可选）存储工作簿的文件夹路径。默认值为 null。|
|输出存储名称|细绳|询问|输出文件存储名称。|
|字体位置|细绳|询问|使用自定义字体。|
|地区|细绳|询问|电子表格区域设置。|
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

## 我们应该在哪里使用拆分远程电子表格 API？

当您需要将多个数据文件合并在一起时，您可以使用这个API。

## 为什么要使用 Split Remote Spreadsheet API？

- 云存储文件无需下载，直接在云端分割即可。
- 通过现有的SDK即可快速完成开发。

## 如何使用带有 SDK 的 Split Remote Spreadsheet API

### 拆分远程电子表格 API 规格

这[拆分远程电子表格 API 规格](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitRemoteSpreadsheet)定义一个可公开访问的编程接口并直接从 Web 浏览器实现 REST 交互。

### 使用 Aspose.Cells 云 SDK

使用 SDK 是最快的开发方式，因为它抽象了低级细节，允许您使用短代码将存储在云中的电子表格拆分为单独的文件。
请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。
以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitFileInRemote.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitFileInRemote.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitFileInRemote.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitFileInRemote.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitFileInRemote.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitFileInRemote.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitFileInRemote.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitFileInRemote.go" >}}
{{< /tab >}}
{{< /tabs >}}
