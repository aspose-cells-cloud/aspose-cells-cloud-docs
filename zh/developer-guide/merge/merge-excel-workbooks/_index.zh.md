---
title: 将 Excel 工作簿合并到其他 Excel 文件中
second_title: Aspose.Cells Cloud Documen
linktitle: 工作台
type: docs
url: /zh/workbook/merge/
aliases: [/merge-excel-workbooks/]
keywords: Merge an Excel Workbooks into other Excel file
description: Aspose.Cells Cloud REST API 支持将 Excel 文件合并到其他 Excel 文件中。 SDK支持多种开发语言。它们包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 50
---
此 REST API 表示将 Excel `workbook` 合并到其他 Excel 工作簿中。

**查询参数**

|参数名称|类型|描述|
|:- |:- |:- |
|文件夹|细绳|原始工作簿文件夹。|
|存储名称|细绳|存储名称。|

## 休息 API

|**API**|**类型**|**描述**|**招摇链接**|
|:- |:- |:- |:- |
|/单元格/{名称}/合并|邮政|合并Excel工作簿|[工作簿合并后](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbooksMerge)|

这[开放API规范](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbooksMerge)定义了一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

您可以使用**cURL**命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示如何使用 cURL 呼叫云端 API。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/merge?mergeWith=test2.xlsx" -H "accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Workbook": {

    "FileName": "test.xlsx",

    "Links": [

      {

        "Href": "/test.xlsx",

        "Rel": "self",

        "Title": null,

        "Type": null

      },

      {

        "Href": "/test.xlsx",

        "Rel": "alternate",

        "Title": "Download As CSV",

        "Type": "text/csv"

      },

      {

        "Href": "/test.xlsx",

        "Rel": "alternate",

        "Title": "Download As HTML",

        "Type": "text/html"

      },

      {

        "Href": "/test.xlsx",

        "Rel": "alternate",

        "Title": "Download As ODS",

        "Type": "application/vnd.oasis.opendocument.spreadsheet"

      },

      {

        "Href": "/test.xlsx",

        "Rel": "alternate",

        "Title": "Download As PDF",

        "Type": "application/pdf"

      },

      {

        "Href": "/test.xlsx",

        "Rel": "alternate",

        "Title": "Download As Table Delimited Text Format",

        "Type": "text/plain"

      },

      {

        "Href": "/test.xlsx",

        "Rel": "alternate",

        "Title": "Download As TIFF",

        "Type": "image/tiff"

      },

      {

        "Href": "/test.xlsx",

        "Rel": "alternate",

        "Title": "Download As Microsoft Excel 2003",

        "Type": "application/vnd.ms-excel"

      },

      {

        "Href": "/test.xlsx",

        "Rel": "alternate",

        "Title": "Download As Microsoft Excel 2007",

        "Type": "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"

      },

      {

        "Href": "/test.xlsx",

        "Rel": "alternate",

        "Title": "Download As XPS",

        "Type": "application/vnd.ms-xpsdocument"

      }

    ],

    "Worksheets": {

      "link": {

        "Href": "/worksheets",

        "Rel": "self",

        "Title": null,

        "Type": null

      }

    },

    "DefaultStyle": {

      "link": {

        "Href": "/defaultstyle",

        "Rel": "self",

        "Title": null,

        "Type": null

      }

    },

    "DocumentProperties": {

      "link": {

        "Href": "/documentproperties",

        "Rel": "self",

        "Title": null,

        "Type": null

      }

    },

    "Names": {

      "link": {

        "Href": "/names",

        "Rel": "self",

        "Title": null,

        "Type": null

      }

    },

    "Settings": {

      "link": {

        "Href": "/settings",

        "Rel": "self",

        "Title": null,

        "Type": null

      }

    },

    "IsWriteProtected": "False",

    "IsProtected": "False",

    "IsEncryption": "false",

    "Password": null

  },

  "Code": 200,

  "Status": "OK"

}


Response headers


```

{{< /tab >}}

{{< /tabs >}}

## 云SDK系列

使用 SDK 是加快开发速度的最佳方式。 SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)有关 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="11" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" tabName11="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorkbookPostWorkbooksMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-workbook-MergeWorkbooks-merge-excel-workbooks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostWorkbooksMerge-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-merge_workbooks-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "MergeExcelWorkbooks.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Workbook-MergeWorkbooks-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-workbook-MergeWorkbooks-merge-excel-workbooks.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Workbook-MergeWorkbooks-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "c1a1b01c65fb7af8a56a09412fb3a6cf" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}

{{< gist "aspose-cells-cloud-gists" "d010d44b4ecd78fbc05fef9ec61146f9" >}}

{{< /tab >}}

{{< /tabs >}}
