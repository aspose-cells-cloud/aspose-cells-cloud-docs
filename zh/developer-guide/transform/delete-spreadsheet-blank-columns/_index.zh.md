---
title: Aspose.Cells Cloud Web API - 删除电子表格中的空白列
second_title: Documen
ArticleTitle: Delete Blank Columns in a Spreadshee
linktitle: 删除空白列
type: docs
url: /zh/delete-spreadsheet-blank-columns/
keywords: Aspose.Cells Cloud Web API, Delete Blank Columns, Spreadsheet Cleanup, REST, Excel, Office Clou
description: 有效地从 Excel 电子表格中删除所有空白列，改善数据管理和可用性
weight: 100
kwords: Excel、Office 云、电子表格、PDF、CSV、JSON、Markdown、删除空白列、Excel 工作表清理
---
从 Excel 电子表格中删除所有不包含任何数据或其他对象的空白列。

## **删除电子表格空白列 AP**

```http
PUT http://api.aspose.cloud/v4.0/cells/delete/blank-columns
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTP 正文|描述|
|:- |:- |:- |:- |
|电子表格|文件|表单数据|上传电子表格文件。|
|输出路径|细绳|询问|（可选）存储工作簿的文件夹路径。默认值为 null。|
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

## 我们应该在哪里使用删除电子表格空白列 API？

当你需要转换数据时，你可以使用这个API。

## 为什么要使用删除电子表格空白列 API？

- 从 Excel 电子表格中快速删除所有不包含任何数据或其他对象的空白列。
- 通过现有的SDK即可快速完成开发。

## 如何使用 SDK 删除电子表格空白列 API

### 删除电子表格空白列 API 规范

这[删除电子表格空白列 API 规范](https://reference.aspose.cloud/cells/#/TransformController/DeleteSpreadsheetBlankColumns)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

### 使用 Aspose.Cells 云 SDK

使用 SDK 是最快的开发方式，因为它抽象了低级细节，允许您使用短代码删除电子表格的空白列。
请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteSpreadsheetBlankColumns.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteSpreadsheetBlankColumns.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteSpreadsheetBlankColumns.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteSpreadsheetBlankColumns.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteSpreadsheetBlankColumns.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteSpreadsheetBlankColumns.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteSpreadsheetBlankColumns.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteSpreadsheetBlankColumns.go" >}}
{{< /tab >}}
{{< /tabs >}}
