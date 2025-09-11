---
title: "Aspose.Cells Cloud Web API - Build a new Spreadsheet with a spreadsheet template."
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Build a new Spreadsheet with a spreadsheet template - Timeline WorkPlan Table, Sales Data Comparison, etc."
linktitle: "Create Spreadsheet"
type: docs
url: /create-spreadsheet/
keywords: "Spreadsheet Creation, Excel API, REST API, Office Cloud, Template Support, Productivity Enhancement"
description: "The Excel API allows users to create a new spreadsheet with a specified name, supporting optional templates for predefined content or formatting, enhancing user productivity."
weight: 100
kwords: "Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Match all blank cells in an Excel worksheet, Spreadsheet Creation, Template Support, Productivity Enhancement"
---

Create a new spreadsheet, which can be either a blank spreadsheet or a usable spreadsheet created based on the specified template.

## **Create Spreadsheet API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/create
```

### **Request Parameters:**

| Parameter Name   | Type   | Path/Query String/HTTP Body | Description |
| ---------------- | ------ | ----------------------------- | ----------- |
| format           | String | Query                         | Specifies the name of the new spreadsheet. This name will be used to identify the spreadsheet in the system. |
| template         | String | Query                         | Optional. If provided, the new spreadsheet will be created based on the specified template. This can be useful for applying predefined layouts and styles. |
| outPath          | String | Query                         | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName   | String | Query                         | Output file Storage Name. |
| region           | String | Query                         | The spreadsheet region setting. |
| password         | String | Query                         | The password for opening the spreadsheet file. |

### **Response**

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

### Error Codes

- **400 Bad Request**: Invalid Apose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Create Spreadsheet API?

When you need to new a spreadsheet, you can use this API.

## Why should you use the Create Spreadsheet API?

- Not only can you create a blank spreadsheet, but you can also create a specific spreadsheet based on a template.
- Development can be quickly completed through the existing SDK.

## How to Use the Create Spreadsheet API with SDKs

### Create Spreadsheet API Specification

The [Create Spreadsheet API Specification](https://reference.aspose.cloud/cells/#/ManagementController/CreateSpreadsheet) defines a publicly accessible programming interface and enables REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to build the spreadsheet with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}
