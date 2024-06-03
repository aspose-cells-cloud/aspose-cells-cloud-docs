---
title: 将图片导入 Excel 工作表
second_title: Aspose.Cells Cloud Documen
linktitle: 导入图片
type: docs
url: /zh/import/picture/
aliases: [/import-picture-into-excel-worksheet/,/import-picture-into-worksheet/,/import-data/picture/]
keywords: Import picture into Excel files
description: Aspose.Cells Cloud REST API 支持将图片导入 Excel 文件。SDK 支持多种开发语言。包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 19
kwords: Excel, Office 云, REST API, 电子表格, PDF, CSV, Json, Markdwon, 将图片导入 Excel 工作表
---
此 REST 将 API `import picture data` 放入 Excel 工作表。

该请求是具有多部分内容的 HTTP 请求（请参阅[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)或者[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)）。多部分内容的第一部分包含 ImportPictureOption 数据，第二部分包含数据文件。

## 重置 API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```


其中重要参数说明如下表：


**导入图片选项**

|参数名称|类型|描述|
|:- |:- |:- |
|左上行|整数||
|左上列|整数||
|右下行|整数||
|右下栏|整数||
|文件名|细绳||
|数据|细绳||
|目的地工作表|细绳|目标工作表名称。|
|是否插入|细绳|真假。|
|导入数据类型|细绳|整数数组/双精度数组/字符串数组/二维整数数组/二维双精度数组/二维字符串数组/批数据/CSV数据/图片。|
|来源|文件源|当 BatchData 参数为空时，指示数据文件位置。|


**例子**


## Cloud SDK 系列

使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)获得 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：


{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}


{{< /tab >}}

{{< tab tabNum="3" >}}



{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}

{{< tab tabNum="9" >}}


{{< /tab >}}

{{< /tabs >}}

