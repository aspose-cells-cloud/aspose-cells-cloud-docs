---
title: "Import Picture into Excel Worksheet"
second_title: "Document"
linktitle: "Import picture"
type: docs
url: /import-picture-into-excel-worksheet/
aliases:
  - /import-picture-into-worksheet/
  - /import-data/picture/
  - /import/picture/
keywords: "Import picture, Excel, Aspose.Cells Cloud, REST API, SDK"
description: "Use Aspose.Cells Cloud REST API to import pictures into Excel worksheets. The API is available through multiple SDKs (Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift)."
weight: 19
---

This REST API **imports picture data** into an Excel worksheet.

The request is an HTTP request with multipart content (see [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). The first part of the multipart content contains the `ImportPictureOption` data and the second part contains the picture file.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

The important parameters are described in the following table:

**ImportPictureOption**

| Parameter Name      | Type       | Description |
|---------------------|------------|-------------|
| UpperLeftRow        | int        | Row index of the upper‑left corner where the picture will be placed. |
| UpperLeftColumn     | int        | Column index of the upper‑left corner where the picture will be placed. |
| LowerRightRow       | int        | Row index of the lower‑right corner that defines the picture’s bounds. |
| LowerRightColumn    | int        | Column index of the lower‑right corner that defines the picture’s bounds. |
| Filename            | string     | Name of the picture file. |
| Data                | string     | Base64‑encoded binary data of the picture. |
| DestinationWorksheet| string     | Name of the worksheet where the picture will be inserted. |
| IsInsert            | string     | `true` to insert the picture; `false` to replace existing content. |
| ImportDataType      | string     | Type of data being imported (e.g., `Picture`, `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`). |
| Source              | FileSource | Indicates the data file’s location when the `BatchData` parameter is null. |

**Example**

## Cloud SDK Family

Using an SDK is the best way to accelerate development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js"  tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

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