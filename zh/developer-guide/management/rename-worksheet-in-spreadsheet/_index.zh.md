---
title: Aspose.Cells Cloud Web API - 在电子表格中重命名工作表
second_title: Documen
ArticleTitle: Rename worksheet in Spreadshee
linktitle: 在电子表格中重命名工作表
type: docs
url: /zh/rename-worksheet-in-spreadsheet/
keywords: Excel API, Rename Worksheet, Workbook Management, REST API, Spreadsheet Organizatio
description: Web API 端点允许用户重命名工作簿中的指定工作表，从而增强组织性和可读性
weight: 100
kwords: Excel API、重命名工作表、工作簿管理、REST API、电子表格、PDF、CSV、JSON、Markdown、匹配 Excel 工作表中的所有空白单元格
---
重命名电子表格中的工作表名称。

## **在电子表格中重命名工作表名称 API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|电子表格|文件|表单数据|上传电子表格文件。|
|源名称|细绳|询问|要重命名的工作表的当前名称。|
|目标名称|细绳|询问|工作表的新名称。|
|输出路径|细绳|询问|（可选）存储工作簿的文件夹路径。默认为 null。|
|输出存储名称|细绳|询问|输出文件存储名称。|
|地区|细绳|询问|电子表格区域设置。|
|密码|细绳|询问|打开电子表格文件的密码。|

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

## 我们应该在哪里使用电子表格 API 中的重命名工作表？

当您需要在电子表格中重命名工作表时，可以使用此 API。

## 为什么要使用电子表格 API 中的重命名工作表？

- 从电子表格快速重命名工作表。
- 通过现有的SDK即可快速完成开发。

## 如何使用 SDKs 在电子表格 API 中使用重命名工作表

### OpenAPI 规范

这[OpenAPI 规范](https://reference.aspose.cloud/cells/#/ManagementController/RenameWorksheetInSpreadsheet)详细介绍了一个可公开访问的编程接口，允许直接从 Web 浏览器进行 REST 交互。

### 使用 Aspose.Cells 云 SDK

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，让您能够以最少的代码轻松实现电子表格中单元格工作表名称的重命名。
请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例说明了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RenameWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RenameWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RenameWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RenameWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RenameWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RenameWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RenameWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RenameWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
