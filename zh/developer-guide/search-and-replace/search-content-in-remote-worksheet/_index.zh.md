---
title: Aspose.Cells 云网络 API - 在远程电子表格中搜索工作表内容
second_title: Documen
ArticleTitle: Search Worksheet Content in Remote Spreadshee
linktitle: 搜索远程工作表内容
type: docs
url: /zh/search-content-in-remote-worksheet/
keywords: Excel API, Search Remote Worksheet, Cloud Spreadsheet, REST API, Search Text, Aspose.Cells, Document Search, Spreadsheet AP
description: 高效地搜索存储在云中的远程电子表格的工作表中的文本
weight: 100
kwords: Excel、Office 云、REST API、电子表格、PDF、CSV、JSON、Markdown、匹配 Excel 工作表中的所有空白单元格、远程工作表搜索
---
在云存储中存储的远程电子表格的工作表中搜索指定的文本。

## **接口详细信息**

## **在远程工作表中搜索内容**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/content
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路|要搜索的工作簿文件的名称。|
|工作表|细绳|小路|工作表的名称。|
|搜索文本|细绳|询问|要搜索的文本。|
|忽略大小写|布尔值|询问|指示搜索时是否忽略大小写。|
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

## 我们应该在电子表格 API 的工作表中的哪里使用搜索内容？

当您需要在电子表格的工作表中搜索内容时，您可以使用这个API。

## 为什么要使用电子表格 API 工作表中的搜索内容？

- 使用此 API 轻松搜索远程电子表格工作表中的内容。
- 通过现有的SDK即可快速完成开发。

## 如何使用 SDK 在电子表格 API 的工作表中搜索断开的链接

### OpenAPI 规范

这[OpenAPI 规范](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteWorksheet)定义一个可公开访问的编程接口并直接从 Web 浏览器实现 REST 交互。

### 使用 Aspose.Cells 云 SDK

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，让您能够以最少的代码轻松实现电子表格工作表单元格的搜索内容。
请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：
