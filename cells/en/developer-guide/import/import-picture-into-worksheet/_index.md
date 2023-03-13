---
title: "Import Picture into Excel Worksheet"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Import picture"
type: docs
url: /import/picture/
aliases: [/import-picture-into-excel-worksheet/,/import-picture-into-worksheet/,/import-data/picture/]
keywords: "Import picture into Excel files."
description: "Aspose.Cells Cloud REST API support importing picture into Excel files. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 19
---

This REST API `import picture data` into Excel work sheet.

The request is an HTTP request with multipart content (see [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). The first part of the multipart content contains the ImportPictureOption data and the second contains a data file.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```


The important parameters are described in the following table:


**ImportPictureOption**

| Parameter Name|Type|Description|
| :- | :- | :- |
| UpperLeftRow | int |  |
| UpperLeftColumn | int |  |
| LowerRightRow | int |  |
| LowerRightColumn | int |  |
| Filename | string | |
| Data | String |  |
| DestinationWorksheet | string | destination work sheet name. |
| IsInsert | string | true/false. |
| ImportDataType | string | IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture.|
| Source | FileSource | Indicates data file position when the BatchData parameter is null. |


**Example**


## Cloud SDK Family

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:


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

