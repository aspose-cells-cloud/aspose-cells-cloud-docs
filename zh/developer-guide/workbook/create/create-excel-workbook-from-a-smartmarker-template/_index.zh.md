---
title: 如何使用智能标记模板创建 Excel 工作簿
second_title: Aspose.Cells Cloud Documen
linktitle: 智能市场
type: docs
url: /zh/workbook/create/smartmarker/
aliases: [/create-excel-workbook-from-a-smartmarker-template/,/workbook/smartmarker/]
keywords: How to create an Excel workbook with a smart marker template
description: Aspose.Cells Cloud REST API 如何使用智能标记模板创建 Excel 工作簿。 SDK支持多种开发语言。它们包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 40
---
这个REST API表示用`smart marker`创建`workbook`。

**查询参数**

|参数名称|类型|描述|
|:- |:- |:- |
|xml文件|细绳||
|出路|细绳||
|文件夹|细绳|原始工作簿文件夹。|
|存储名称|细绳|存储名称。|

**请求正文参数**

|参数名称|类型|描述|
|:- |:- |:- |
|xml文件|文件||


## 休息 API

|**API**|**类型**|**描述**|**招摇链接**|
|:- |:- |:- |:- |
|/cells/{名称}/smartmarker|邮政|从 SmartMarker 模板文件创建一个新的 Excel 工作簿|[PostWorkbookGetSmartMarkerResult](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookGetSmartMarkerResult)|


这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookGetSmartMarkerResult)定义了一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

您可以使用**cURL**用于轻松访问 Aspose.Cells Web 服务的命令行工具。以下示例显示如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/newworkbook_14.xlsx/smartmarker?xmlFile=Sample_SmartMarker_Data.xml" -H "accept: multipart/form-data" -H "x-aspose-client: Containerize.Swagger"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

HttpResponseMessage with the processing result in content.

}

```

{{< /tab >}}

{{< /tabs >}}


## 云 SDK 系列

使用 SDK 是加速开发的最佳方式。 SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 仓库](https://github.com/aspose-cells-cloud)有关 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用各种 SDK 调用 Aspose.Cells Web 服务：


{{< tabs tabTotal="11" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" tabName11="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorkbookPostWorkbookGetSmartMarkerResult.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-workbook-CreateWorkbookFromSmartMarkerTemplate-create-from-smart-marker.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PutWorkbookCreate-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-create_new_workbook-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "CreateExcelWorkbookFromSmartMarkerTemplate.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Workbook-CreateWorkbookFromSmartMakerTemplate-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-workbook-CreateWorkbookFromSmartMarkerTemplate-create-from-smart-marker.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Workbook-CreateWorkbookFromSmartMakerTemplate-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "42b369351a3909d9f38916d9f6e10d9a" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}

{{< gist "aspose-cells-cloud-gists" "f83596a0e742321c1a0296332804d047" >}}

{{< /tab >}}

{{< /tabs >}}
