---
title: Aspose.Cells 云网 API - 在远程电子表格中搜索范围的断开链接
second_title: Documen
ArticleTitle: Search Broken Links of Range in Remote a Spreadshee
linktitle: 搜索远程范围损坏的链接
type: docs
url: /zh/search-broken-links-in-remote-range/
keywords: broken links, remote spreadsheet, Excel API, REST API, link checker, hyperlink validation, cloud storag
description: 高效搜索云存储中远程电子表格指定范围内的断开链接
weight: 100
kwords: Excel、Office 云、REST API、电子表格、PDF、CSV、Json、Markdown、断开链接、超链接验证、云存储
---
高效地搜索云存储中存储的远程电子表格指定范围内的断开链接。

## **搜索远程范围的断开链接 API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/broken-links
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路|要搜索的工作簿文件的名称。|
|工作表|细绳|小路|指定查找的工作表。|
|单元格区域|细绳|小路|指定查找的单元格区域。|
|文件夹|细绳|询问|存储工作簿的文件夹路径。|
|存储名称|细绳|询问|（可选）如果使用自定义云存储，则输入存储名称。如果省略，则使用默认存储。|
|地区|细绳|询问|电子表格区域设置。|
|密码|细绳|询问|打开电子表格文件的密码。|

### **回复**

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink",
        },
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### 错误代码

- **400 错误请求**：无效的 Apose.Cells Cloud API URI。
- **401 未授权**：访问令牌无效。或者客户端 ID 和密钥无效。
- **404 未找到**：电子表格文件无法访问。
- **500 服务器错误**：电子表格在获取计算数据时遇到异常。

## 我们应该在哪里使用“搜索电子表格 API 范围内的断开链接”？

当您需要在电子表格范围内搜索断开的链接时，您可以使用这个 API。

## 为什么要使用“搜索电子表格 API 范围内的断开链接”？

- 快速搜索电子表格范围内的断开链接。
- 通过现有的SDK即可快速完成开发。

## 如何使用 SDK 搜索电子表格 API 范围内的断开链接

### OpenAPI 规范

这[OpenAPI 规范](https://reference.aspose.cloud/cells/#/SearchControllor/SearchBrokenLinksInRemoteRange)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

### 使用 Aspose.Cells 云 SDK

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，让您能够以最少的代码轻松实现在电子表格范围内查找单元格的功能。
请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteRange.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteRange.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteRange.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteRange.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteRange.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteRange.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteRange.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteRange.go" >}}
{{< /tab >}}
{{< /tabs >}}
