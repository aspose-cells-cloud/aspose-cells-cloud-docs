---
title: 设置 Rang 的样式
second_title: Aspose.Cells Cloud Documen
linktitle: 设置样式
type: docs
url: /zh/ranges/update/style/
aliases: [/set-the-style-of-the-range/]
keywords: Set range style on an Excel workshee
description: Aspose.Cells Cloud REST API 支持在 Excel 工作表上设置范围样式。 SDK支持多种开发语言。它们包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 70
---
## **介绍**
此示例允许您设置范围的样式，在您的应用程序中使用 Aspose.Cells Cloud API。您可以将我们的 REST API 与任何语言一起使用：.NET、Java、PHP、Ruby、Rails、Python、jQuery 等等。
## **API 资料**

|**API**|**类型**|**描述**|**资源链接**|
|:- |:- |:- |:- |
|/cells/{name}/worksheets/{sheetName}/ranges/style|邮政|设置命名范围的单元格样式|[PostWorksheetCellsRangeStyle](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeStyle)|
### **cURL 示例**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/style" -H "accept: application/json" -H "Content-Type: application/json" -d "{ \"Range\": { \"ColumnCount\": 2, \"ColumnWidth\": 0, \"FirstColumn\": 1, \"FirstRow\": 1, \"Name\": \"string\", \"RefersTo\": \"string\", \"RowCount\": 2, \"RowHeight\": 0, \"Worksheet\": \"Sheet1\" }, \"Style\": { \"Font\": { \"DoubleSize\": 1, \"IsBold\": true, \"IsItalic\": true, \"IsStrikeout\": true, \"IsSubscript\": true, \"IsSuperscript\": true } }}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Code": 200,

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}
## **SDK源码**
可以从以下页面下载 Aspose.Cells Cloud SDK：[可用的 SDK](/cells/zh/available-sdks/)
### **开发工具包范例**
{{< tabs tabTotal="4" tabID="4" tabName1="PHP" tabName2="Ruby" tabName3="Objective C" tabName4="Go" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}



{{< /tab >}}

{{< tab tabNum="3" >}}



{{< /tab >}}

{{< tab tabNum="4" >}}



{{< gist "aspose-cells-cloud-gists" "81d7e60eaf43ae7192df00993997afde" >}}

{{< /tab >}}

{{< /tabs >}}
