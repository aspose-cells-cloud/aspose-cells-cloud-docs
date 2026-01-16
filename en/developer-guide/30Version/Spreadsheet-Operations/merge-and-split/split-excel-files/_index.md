---
title: "Split an Excel workbook to multi-files"
second_title: "Document"
linktitle: "Split an Excel file"
type: docs
url: /split-multi-excel-files/
aliases: [ /split/multi-files/]
keywords: "Excel, Aspose.Cells Cloud, REST API, split workbook, multi-file, JPEG, PNG, PDF, CSV, JSON"
description: "The Aspose.Cells Cloud REST API enables splitting an Excel workbook into multiple files in various formats. This documentation provides request parameters, a cURL example, and SDK code samples for languages such as C#, Java, PHP, Ruby, Node.js, Python, Perl, and Go."
weight: 130
---

This REST API splits an Excel `workbook` into multiple files in different formats.

**Query Parameter**

| Parameter Name      | Type    | Description                                          |
|---------------------|---------|------------------------------------------------------|
| format              | string  | Desired output format for the split files.           |
| from                | integer | Starting worksheet index.                            |
| to                  | integer | Ending worksheet index.                              |
| horizontalResolution| integer | Image horizontal resolution.                         |
| verticalResolution  | integer | Image vertical resolution.                           |
| outFolder           | string  | Output folder for the split files.                   |
| splitNameRule       | string  | Naming rule applied to split files.                  |
| folder              | string  | Folder containing the original workbook.             |
| storageName         | string  | Name of the storage to use.                          |

## REST API

| **API**                | **Type** | **Description**          | **Swagger Link** |
|------------------------|----------|--------------------------|------------------|
| /cells/{name}/split    | POST     | Split an Excel workbook  | [PostWorkbookSplit](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookSplit) |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookSplit) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/split?format=jpeg&from=1&to=1&horizontalResolution=0&verticalResolution=0" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
{
  "Result": {
    "Documents": [
      {
        "Id": 1,
        "link": {
          "Href": "413e3375-c163-4d5c-8b84-8f95f63902f6.png",
          "Rel": null,
          "Title": null,
          "Type": null
        }
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}