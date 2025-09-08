---
title: "Aspose.Cells Cloud Web API - Replace Range Content in Remote Spreadsheet"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Replace Range Content in Remote a Spreadsheet"
linktitle: "Replace Remote Range Content"
type: docs
url: /replace-content-in-remote-range/
keywords: "API, Excel API, Replace Content, Remote Spreadsheet, Cloud Storage, Text Replacement, REST API"
description: "Efficiently replace text within specified ranges of remote spreadsheets using Aspose.Cells Cloud API."
weight: 100
kwords: "Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Match all blank cells in an Excel worksheet, remote text replacement, cloud storage integration"
---


Efficiently replace specified text within a range of a remote spreadsheet file.

## **Replace Content in Remote Range API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
| :- | :- | :- |:- |
| name | String | Path | The name of the workbook file to be modified. |
| searchText | String | Query | The text to search for within the spreadsheet. |
| replaceText | String | Query | The text to replace the searched text with. |
| worksheet | String | Path | The name of the worksheet where the replacement will occur. |
| cellArea | String | Path | The specific cell area for the replacement. |
| folder | String | Query | The folder path where the workbook is stored. |
| storageName | String | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| region | String | Query | The spreadsheet region setting. |
| password | String | Query | The password for opening the spreadsheet file. |

### **Response**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### Error Codes

- **400 Bad Request**: Invalid Apose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Replace content of Range in Remote Spreadsheet API?

When you need to replace content of Range in remote spreadsheet, you can use this API.

## Why should you use the Replace content of Range in Remote Spreadsheet API?

- Quickly replace content of Range in remote spreadsheets.
- Development can be quickly completed through the existing SDK.

## How to Use the Replace content of Range in Remote Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteRange) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement replace content in spreadsheets for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ReplaceTextInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ReplaceTextInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ReplaceTextInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ReplaceTextInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ReplaceTextInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ReplaceTextInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ReplaceTextInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ReplaceTextInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}
