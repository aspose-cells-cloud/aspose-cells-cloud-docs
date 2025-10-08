---
title: Aspose.Cells Cloud Web API - 替换远程电子表格中的内容
second_title: Documen
ArticleTitle: Replace Content in Remote a Spreadshee
linktitle: 替换远程电子表格内容
type: docs
url: /zh/replace-content-in-remote-spreadsheet/
keywords: Replace content, remote spreadsheet, Excel API, REST API, cloud storage, text replacemen
description: 使用 Excel API 高效替换远程电子表格中的文本
weight: 100
kwords: Excel、Office 云、REST API、电子表格、PDF、CSV、JSON、Markdown、替换 Excel 中的内容、基于云的文本替换、修改远程电子表格中的文本
---
有效地替换远程电子表格文件中的指定文本。

## **替换远程电子表格中的内容 API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/replace/content
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路|要修改的工作簿文件的名称。|
|搜索文本|细绳|询问|要在电子表格中搜索的文本。|
|替换文本|细绳|询问|用于替换所发现内容的文本。|
|文件夹|细绳|询问|存储工作簿的文件夹路径。|
|存储名称|细绳|询问|（可选）如果使用自定义云存储，则输入存储名称。如果省略，则使用默认存储。|
|地区|细绳|询问|电子表格区域设置。|
|密码|细绳|询问|打开电子表格文件的密码。|

### **回复**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
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

## 我们应该在哪里使用远程电子表格 API 中的替换内容？

当您需要替换远程电子表格中的内容时，您可以使用这个API。

## 为什么要使用远程电子表格 API 中的替换内容？

- 快速替换远程电子表格中的内容。
- 通过现有的SDK即可快速完成开发。

## 如何使用 SDK 替换远程电子表格 API 中的内容

### OpenAPI 规范

这[OpenAPI 规范](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteSpreadsheet)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

### 使用 Aspose.Cells 云 SDK

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，让您能够以最少的代码轻松实现电子表格单元格内容的替换。
请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：
